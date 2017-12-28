# Eπεξεργασία δεδομένων raster GIS με R

Η παρουσίαση αφορά επεξεργασία δορυφορικών δεδομένων με R.
Συγκεκριμένα περιλαμβάνει τον υπολογισμό του δείκτη [*Vegetation Adjusted NTL Urban
Index (VANUI)*](http://urban.yale.edu/publications/2013/101016jrse201210022) που βασίζεται στον υπολογισμό του δείκτη βλάστησης [*NDVI*](https://en.wikipedia.org/wiki/Normalized_Difference_Vegetation_Index) και εικόνες με
νυκτερινά φώτα. Το παράδειγμα που θα παρουσιαστεί αφορά υπολογισμό του VANUI για
την Αθήνα χρησιμοποιώντας δεδομένα MODIS<sup>[1](#modis)</sup> για τον NDVI και δεδομένα [*DMSP/OLS*](https://ngdc.noaa.gov/eog/dmsp.html)<sup>[2](#dmsp)</sup> για νυχτερινά φώτα.


# Σύνοψη

Το τρέχον αποθετήριο αποτελεί το υλικό για την παρουσίαση του εργαστηρίου (workshop) *"Eπεξεργασία δεδομένων raster GIS με R"* στο συνέδριο [FOSSCOMM2017](https://www.fosscomm.hua.gr/).
Οι τρέχουσες οδηγίες καθοδηγούν τον ενδιαφερόμενο να μεταφορτώσει τα αρχεία του εργαστηρίου στο τοπικό του σύστημα.
Επιπλέον ενημερώνει τον χρήστη για το λογισμικό που απαιτείται να εγκαταστήσει για την επιτυχή παρακολούθησή του.


# Προαπαιτούμενα

Για την επιτυχή παρακολούθηση του εργαστηρίου και την εκτέλεσή του συνοδευτικού κώδικα απαιτείται η εγκατάσταση των παρακάτω λογισμικών (τρέχουσες εκδόσεις):

* το πακέτο στατιστικής [R](https://www.r-project.org/)
* τo περιβάλλον εργασία της R, [rstudio](https://www.rstudio.com/)
* το σύστημα διαχείρισης εκδόσεων [git](https://git-scm.com/) (προαιρετικά)

Επιπλέον απαιτούνται οι κάτωθι βιβλιοθήκες της R:

* [MODIS](https://cran.r-project.org/web/packages/MODIS/)
* [raster](https://cran.r-project.org/web/packages/raster/)

Η εγκατάσταση τους γίνεται με τις ακόλουθες εντολές σε ένα [R session](https://cran.r-project.org/doc/manuals/r-release/R-intro.html#Invoking-R):

```
install.packages("raster")
install.packages("MODIS")
```

**Σημαντικό:** Για την ομαλή διεξαγωγή του εργαστηρίου προτείνεται η προεγκατάσταση των ανωτέρω λογισμικών.


# Λήψη του υλικού του εργαστηρίου

Η λήψη του υλικού μπορεί να γίνει με την κλωνοποίηση του τρέχοντος αποθετηρίου χρησιμοποιώντας την εντολή:

```
git clone https://github.com/kokkytos/rasterRfosscomm2017.git
```

Eναλλακτικά το αποθετήριο είναι διαθέσιμο και σε [συμπιεσμένη μορφή](https://github.com/kokkytos/rasterRfosscomm2017/archive/master.zip).

# Εκτέλεση των εντολών

Οι εντολές για την εκτέλεση των διαδιακασιών επεξεργασίας δεδομένων και υπολογισμού δεικτών βρίσκονται στο αρχείο [*notebook.Rmd*](notebook.Rmd) υπό την μορφή *«λόγιου προγραμματισμoυ»* (*literate programming*).
Το αρχείο  [*notebook.Rmd*](notebook.Rmd) είναι αναγνώσιμο από το λογισμικό [rstudio](https://www.rstudio.com/). 

# Δεδομένα δορυφορικών εικόνων

Τα συνοδευτικά δεδομένα δορυφορικών εικόνων περιέχονται στον κατάλογο *data* (στους καταλόγους *ndvi* και *ols*)


# Συγγραφείς

* [Λιάκος Λεωνίδας](https://gr.linkedin.com/in/leonidasliakos)

* [Σταθάκης Δημήτρης](https://gr.linkedin.com/in/dstath)

# Ερωτήσεις/Παρατηρήσεις

Τυχόν ερωτήσεις ή παρατηρήσεις θα υποβάλλονται στην [σχετική ενότητα του αποθετηρίου](https://github.com/kokkytos/rasterRfosscomm2017/issues).

# Άδεια

Το τρέχον έργο παρέχεται υπό την άδεια [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).

# Πηγές δορυφορικών εικόνων

<a name="dmsp">1</a>. Image and Data processing by NOAA's National Geophysical Data Center. DMSP data collected by the US Air Force Weather Agency.

<a name="modis">2</a>. K. Didan. (2015). MOD13Q1 MODIS/Terra Vegetation Indices 16-Day L3 Global 250m SIN Grid V006. NASA EOSDIS Land Processes DAAC. https://doi.org/10.5067/modis/mod13q1.006
