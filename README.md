CQRS nədir və nə üçün istifadə olunur:
CQRS Command Query Responsibilty Segregation mənasını verir, yəni məlumat mənbəyinə yazma və məlumat mənbəyindən oxuma əməliyyatlarını ayıran nümunə kimi müəyyən edilə bilər. “Commmand” dediyimiz termin verilənlər bazasının üzərinə yazma əməliyyatları, “Query” isə verilənlər bazasından oxu əməliyyatlarıdır.
Bəs niyə biz CQRS tətbiq etməliyik? Mikroservis strukturlarının tətbiqlərdə yayılması ilə CQRS tətbiqinin daha tez-tez istifadə olunmağa başladığını fərq etmiş ola bilərsiniz. Bunun səbəbi Query və Command əməliyyatlarının ayrılması kodu daha oxunaqlı edir.

Niyə CQRS və MediaTR Kitabxanasından istifadə edirik
MediaTR və CQRS istifadə etməməyin bəzi üstünlükləri var.
Loosely Coupling: MediaTR kitabxanasından CQRS ilə istifadə bizə praktikada Loosely coupled arxitektura ilə işləməyə imkan verir. Asılılıqları aradan qaldıraraq, komandalara tək cavab prinsipi ilə bir-birindən müstəqil inkişaf edib yerləşdirməyə, uğursuzluq vəziyyətlərində və miqyasda daha müstəqil və daha sürətli cavab almağa imkan verir.

//Migrations
Hər layihədə olduğu kimi Code First yanaşması ilə qurduğumuz layihəmizdə də yenilənməsi lazım olan məqamlar qaçılmaz olacaq. Code First nümunəsinin tətbiq olunduğu layihədə verilənlər bazasına birbaşa müdaxilənin çox əlverişsiz olduğunu bilirik.
Təbii ki, SQL Serverdən fiziki verilənlər bazasını silib yenidən quraşdıraraq indiyə qədər etdiyimiz bütün əməliyyatları müşahidə etmişik. Burada Miqrasiya strukturları sayəsində yeniliklərimizi Visual Studio vasitəsilə fiziki verilənlər bazasına tez əks etdirə biləcəyik. Gördüyünüz kimi kod hissəsində etdiyimiz dəyişiklikləri verilənlər bazasına əks etdirmək üçün Miqrasiya çağırırıq.
