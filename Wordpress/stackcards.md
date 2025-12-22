# StackCards

![StackCards Demo](images/Lib-StackCards.giff)

// Sayfa_id wordpress için

body.page-id-29598 .site-content,
body.page-id-29598 .content-area,
body.page-id-29598 .wd-page-content {
    background-color: #2596be !important;
}

.all-cards {
display: flex;
flex-direction: column; /* Arrange cards vertically in the column */
}

.card1 {
position: -webkit-sticky; /* For Safari */
position: sticky;
top: 50px; /* Offset from the top */
}

.card2 {
position: -webkit-sticky; /* For Safari */
position: sticky;
top: 100px; /* Offset from the top */
}

.card3 {

position: -webkit-sticky; /* For Safari */
position: sticky;
top: 150px; /* Offset from the top */
}

.card4 {
position: -webkit-sticky; /* For Safari */
position: sticky;
top: 200px; /* Offset from the top */
}
//Burada önemli noktalar şunlar :
adım-1:wordpreste bir container aç ve şunu yap  gelişmiş > css sınıfları > all-cards yaz
adım-2:containerın içine kaç tane card istiyorsan o kadar container aç 
adım-3: gelişmiş > css sınıfları > card1 yaz Z-Endeksi 1 yap
adım-4: gelişmiş > css sınıfları > card2 yaz Z-Endeksi 2 yap
adım-5: gelişmiş > css sınıfları > card3 yaz Z-Endeksi 3 yap
adım-6: gelişmiş > css sınıfları > card4 yaz Z-Endeksi 4 yap   bunlar cardların üstüste gelme katmanını ayarlar 
adım-7: cardalara resim eklemek içim biçem göresel seç de