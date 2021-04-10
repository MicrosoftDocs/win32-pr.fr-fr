---
description: Cette rubrique fournit des informations sur les considérations relatives à la sécurité des fonctionnalités de prise en charge internationale.
ms.assetid: 4034f479-ad29-4c6f-82c6-977f420c4d4d
title: 'Considérations relatives à la sécurité : fonctionnalités internationales'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb9f8b849e9fb1a07f01031832449b9c9027ae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210797"
---
# <a name="security-considerations-international-features"></a>Considérations relatives à la sécurité : fonctionnalités internationales

Cette rubrique fournit des informations sur les considérations relatives à la sécurité des fonctionnalités de prise en charge internationale. Vous pouvez l’utiliser comme point de départ, puis consulter la documentation de la technologie internationale qui vous intéresse pour les considérations relatives à la sécurité spécifique à la technologie.

Cette rubrique contient les sections suivantes.

-   [Considérations relatives à la sécurité pour les fonctions de conversion de caractères](#security-considerations-for-character-conversion-functions)
-   [Considérations relatives à la sécurité pour les fonctions de comparaison](#security-considerations-for-comparison-functions)
-   [Considérations relatives à la sécurité pour les jeux de caractères dans les noms de fichiers](#security-considerations-for-character-sets-in-file-names)
-   [Considérations relatives à la sécurité pour les noms de domaine internationaux](#security-considerations-for-internationalized-domain-names)
-   [Considérations sur la sécurité pour les fonctions ANSI](#security-considerations-for-ansi-functions)
-   [Considérations relatives à la sécurité pour la normalisation Unicode](#security-considerations-for-unicode-normalization)

## <a name="security-considerations-for-character-conversion-functions"></a>Considérations relatives à la sécurité pour les fonctions de conversion de caractères

[**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) et [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) sont les fonctions Unicode et de jeu de caractères les plus couramment utilisées pour convertir des caractères entre ANSI et Unicode. Ces fonctions sont susceptibles de provoquer des risques de sécurité, car elles comptent différemment les éléments des mémoires tampons d’entrée et de sortie. Par exemple, [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) prend une mémoire tampon d’entrée comptée en octets et place les caractères convertis dans une mémoire tampon dimensionnée en caractères Unicode. Lorsque votre application utilise cette fonction, elle doit dimensionner les mémoires tampons correctement pour éviter un dépassement de mémoire tampon.

[**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) a pour valeur par défaut le mappage le mieux adapté pour les pages de codes, par exemple 1252. Toutefois, ce type de mappage autorise plusieurs représentations de la même chaîne, laissant potentiellement votre application vulnérable aux attaques. Par exemple, la lettre majuscule latine A avec un tréma (« Ä ») peut être mappée à la lettre majuscule latine A (« A »); un caractère Unicode dans une langue asiatique peut être mappé à une barre oblique (« / »). L’utilisation de l’indicateur de caractères de l' \_ option WC n’est pas la \_ meilleure \_ \_ . il est préférable d’un point de vue de la sécurité.

Certaines pages de codes, par exemple, les pages de codes 5022x (ISO-2022-x), sont par nature non sécurisées, car elles autorisent plusieurs représentations de la même chaîne. Le code écrit correctement effectue des vérifications de sécurité au format Unicode, mais ces types de pages de codes étendent la susceptibilité aux attaques de vos applications et doivent être évitées si possible.

## <a name="security-considerations-for-comparison-functions"></a>Considérations relatives à la sécurité pour les fonctions de comparaison

Les comparaisons de chaînes peuvent présenter des problèmes de sécurité. Étant donné que toutes les fonctions de comparaison sont légèrement différentes, une fonction peut signaler que deux chaînes sont égales, tandis qu’une autre fonction peut les considérer comme étant distinctes. Voici plusieurs fonctions que vos applications peuvent utiliser pour comparer des chaînes :

-   [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia). Compare deux chaînes de caractères en fonction des règles des paramètres régionaux, sans respect de la casse. La fonction compare les chaînes en vérifiant les premiers caractères les unes par rapport aux autres, et ainsi de suite, jusqu’à ce qu’il trouve une inégalité ou qu’il atteigne les terminaisons des chaînes.
-   [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa). Compare des chaînes à l’aide de techniques similaires à celles de [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia). La seule différence est que [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) effectue une comparaison de chaînes respectant la casse.
-   [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) (Windows Vista et versions ultérieures). Effectue une comparaison de chaînes sur les paramètres régionaux fournis par l’application. [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) est similaire à [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), mais il identifie les paramètres régionaux par [nom de paramètres régionaux](locale-names.md) et non pas par [identificateur de paramètres régionaux](locale-identifiers.md). Ces fonctions sont similaires à [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) et [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) , à ceci près qu’elles opèrent sur des paramètres régionaux spécifiques au lieu des paramètres régionaux sélectionnés par l’utilisateur.
-   [**Comparestringordinal,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) (Windows Vista et versions ultérieures). Compare deux chaînes Unicode pour tester l’équivalence binaire. À l’exception de l’option de non-respect de la casse, cette fonction ignore toutes les équivalences non binaires et teste l’égalité de tous les points de code, y compris les points de code qui n’ont pas de poids dans les schémas de [Tri](sorting.md) linguistique. Notez que les autres fonctions de comparaison mentionnées dans cette rubrique ne testent pas l’égalité de tous les points de code.
-   [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) (Windows Vista et versions ultérieures). Recherchez une chaîne Unicode dans une autre chaîne Unicode. [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) est similaire à [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), à ceci près qu’il identifie les paramètres régionaux par nom de paramètres régionaux et non pas par identificateur de paramètres régionaux.
-   [**FindStringOrdinal**](/windows/desktop/api/Libloaderapi/nf-libloaderapi-findstringordinal) (Windows 7 et versions ultérieures). Localise une chaîne Unicode dans une autre chaîne Unicode. L’application doit utiliser cette fonction au lieu de [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring) pour toutes les comparaisons non linguistiques.

Comme [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) et [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) évalue les chaînes caractère par caractère. Toutefois, de nombreux langages ont des éléments à plusieurs caractères, par exemple, l’élément à deux caractères « CH » en espagnol traditionnel. Comme [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) utilise les paramètres régionaux fournis par l’application pour identifier les éléments à plusieurs caractères et [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) et [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) utiliser les paramètres régionaux de thread, les chaînes identiques peuvent ne pas être considérées comme égales.

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) ignore les caractères non définis et retourne donc zéro (ce qui indique que les chaînes sont égales) pour de nombreuses paires de chaînes qui sont assez distinctes. Une chaîne peut contenir des valeurs qui ne correspondent à aucun caractère ou elle peut contenir des caractères avec une sémantique en dehors du domaine de l’application, tels que des caractères de contrôle dans une URL. Les applications qui utilisent cette fonction doivent fournir des gestionnaires d’erreurs et des chaînes de test pour s’assurer qu’elles sont valides avant de les utiliser.

> [!Note]  
> Pour Windows Vista et versions ultérieures, [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) est similaire à [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw). Les problèmes de sécurité sont identiques pour ces fonctions.

 

Des problèmes de sécurité similaires s’appliquent aux fonctions, telles que [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), qui effectuent des comparaisons implicites. Selon les indicateurs définis, les résultats de l’appel de [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring) pour rechercher une chaîne dans une autre chaîne peuvent varier considérablement.

> [!Note]  
> Pour Windows Vista et versions ultérieures, [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) est similaire à [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring). Les problèmes de sécurité sont identiques pour ces fonctions.

 

## <a name="security-considerations-for-character-sets-in-file-names"></a>Considérations relatives à la sécurité pour les jeux de caractères dans les noms de fichiers

La page de codes Windows et les jeux de caractères OEM utilisés sur les systèmes en langue japonaise contiennent le symbole yen (¥) au lieu d’une barre oblique inverse ( \\ ). Par conséquent, le caractère yen est un caractère interdit pour les systèmes de fichiers NTFS et FAT. Lors du mappage Unicode sur une page de codes en japonais, les fonctions de conversion mappent la barre oblique inverse (U + 005C) et le symbole de yen Unicode normal (U + 00A5) à ce même caractère. Pour des raisons de sécurité, les applications ne doivent pas, en général, autoriser le caractère U + 00A5 dans une chaîne Unicode qui peut être convertie pour être utilisée comme nom de fichier FAT.

## <a name="security-considerations-for-internationalized-domain-names"></a>Considérations relatives à la sécurité pour les noms de domaine internationaux

Les noms de domaine internationaux (IDNs) sont spécifiés par le groupe de travail réseau [RFC 3490 : internationalisation des noms de domaine dans les applications (IDNA)](http://www.faqs.org/rfcs/rfc3490.html). La norme introduit un certain nombre de problèmes de sécurité.

Les glyphes représentant certains caractères de scripts différents peuvent apparaître similaires ou même identiques. Par exemple, dans de nombreuses polices, le minuscule cyrillique A ("a") ne peut pas être différenciée de la minuscule latine A ("a"). Il n’existe aucun moyen de dire visuellement que « example.com » et « example.com » sont deux noms de domaine différents, l’un avec un minuscule latin A dans le nom, l’autre avec un minuscule cyrillique A. Un site hôte non scrupuleux peut utiliser cette ambiguïté visuelle pour être un autre site dans une attaque par usurpation d’identité.

Le jeu de caractères étendus que IDNA autorise pour IDNs présente également un risque d’usurpation d’identité dans un script particulier. Par exemple, il existe une forte ressemblance entre le trait d’Union-moins (« - » U + 002D). le trait d’Union (« - » U + 2010), le trait d’Union insécable (« - » U + 2011), le tiret de la figure (« \u2012 » U + 2012), le tiret demi-cadratin (« – » U + 2013) et le signe moins (« − » U + 2212).

Certaines compositions de compatibilité présentent des problèmes similaires. Par exemple, le seul caractère Unicode numéro 20 STOP (« 20 », U + 249B) est converti en « 20 ». (U + 0032 U + 0030 U + 002E) dans une étape NamePrep, avant la conversion en Punycode. En d’autres termes, cette composition insère un point (Full Stop). Ces compositions présentent un risque d’usurpation d’identité.

La combinaison de différents scripts dans un IDN n’indique pas nécessairement l’usurpation ou l’intention trompeuse. [Rapport technique \# 36 : les considérations relatives à la sécurité Unicode](https://www.unicode.org/reports/tr36/#international_domain_names) offrent plusieurs exemples de IDNs raisonnables qui contiennent une combinaison de scripts, tels que XML-Документы. com (« Документы » est russe pour « documents »).

Les attaques par usurpation d’identité ne sont pas limitées à IDNs. Par exemple, « rnicrosoft.com » ressemble plus à « microsoft.com », mais il s’agit d’un nom ASCII. En outre, une attaque par usurpation d’identité peut être générée par l’altération d’un nom. L’ajout d’étiquettes supplémentaires après un nom de marque bien connu, ou l’inclusion du nom de marque dans le chemin d’accès d’une URL étiquetée sécurisée, peut dérouter les utilisateurs débutants, indépendamment de l’utilisation des IDN. Pour certains paramètres régionaux, IDNs est requis et la forme Punycode de ces noms est inacceptable, car les noms semblent incompréhensibles.

Pour plus d’informations sur les problèmes de sécurité mentionnés ici, ainsi qu’un grand nombre d’autres problèmes liés à IDNA, consultez le [rapport technique \# 36 : considérations sur la sécurité Unicode](https://www.unicode.org/reports/tr36/#international_domain_names). Outre les discussions détaillées sur les problèmes de sécurité liés à IDNA, ce rapport propose des suggestions pour traiter les IDNs suspectes dans vos applications.

## <a name="security-considerations-for-ansi-functions"></a>Considérations sur la sécurité pour les fonctions ANSI

> [!Note]  
> Il est recommandé d’utiliser Unicode dans vos applications globalisées, en particulier les nouvelles, si possible. Vous devez utiliser les fonctions ANSI uniquement si vous avez des raisons de substitution pour ne pas utiliser Unicode, par exemple, la conformité à un protocole plus ancien qui ne prend pas en charge Unicode.

 

De nombreuses fonctions NLS (National Language Support), telles que [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) et [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa), ont des versions ANSI spécifiques, en l’occurrence, **GetLocaleInfoA** et **GetCalendarInfoA**, respectivement. Lorsque votre application utilise la version ANSI d’une fonction avec un système d’exploitation Unicode, tel que Windows NT, Windows 2000, Windows XP ou Windows Vista, la fonction peut échouer ou produire des résultats indéfinis. Si vous avez une bonne raison d’utiliser des fonctions ANSI avec un tel système d’exploitation, assurez-vous que les données transmises par votre application sont valides pour ANSI.

## <a name="security-considerations-for-unicode-normalization"></a>Considérations relatives à la sécurité pour la normalisation Unicode

Étant donné que la normalisation Unicode peut modifier la forme d’une chaîne, les mécanismes de sécurité ou les algorithmes de validation de caractères doivent généralement être implémentés après la normalisation. Par exemple, considérez une application avec une interface Web qui accepte un nom de fichier, mais qui n’accepte pas de nom de chemin d’accès. Une valeur u + FF43 U + FF1A U + FF3C U + FF57 U + FF49 u + FF4E u + FF44 U + FF4F U + FF57 u + FF53 est `(c : \ w i n d o w s)` remplacée par u + 0063 u + 001A u + 003C u + 0077 u + 0069 u + 006E u + 0064 u + 006F u + 0077 u + 0073 `(c:\windows)` avec la normalisation KC. Si une application teste la présence des deux points et des barres obliques inverses avant d’implémenter la normalisation, le résultat peut être un accès non intentionnel aux fichiers.

Alors que la normalisation Unicode est un élément qui consiste à sécuriser les systèmes d’exploitation, n’oubliez pas que la normalisation ne remplace pas une stratégie de sécurité complète.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Jeux de caractères utilisés dans les noms de fichiers](character-sets-used-in-file-names.md)
</dt> <dt>

[Conventions pour les prototypes de fonctions](conventions-for-function-prototypes.md)
</dt> <dt>

[Gestion du tri dans vos applications](handling-sorting-in-your-applications.md)
</dt> <dt>

[Gestion des noms de domaine internationaux (IDNs)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[Unicode](unicode.md)
</dt> </dl>

 

 
