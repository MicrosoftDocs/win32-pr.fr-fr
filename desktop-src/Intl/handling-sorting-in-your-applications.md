---
description: Certaines applications, telles que Microsoft Active Directory, Microsoft Exchange et Microsoft Access, gèrent une base de données pouvant être triée des paramètres régionaux et des chaînes de langue indexées par nom (chaîne UTF-16) et leurs pondérations de tri associées.
ms.assetid: c8fc32bd-02bd-4a40-a836-d9ad9f69c209
title: Gestion du tri dans vos applications
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: c0bba3d78a5219781226ecf58292ed461c902090
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869081"
---
# <a name="handling-sorting-in-your-applications"></a>Gestion du tri dans vos applications

Certaines applications, telles que Microsoft Active Directory, Microsoft Exchange et Microsoft Access, gèrent une base de données pouvant être triée des paramètres régionaux et des chaînes de langue indexées par nom (chaîne UTF-16) et leurs pondérations de tri associées.

Le [Tri](sorting.md) est généralement intuitif pour les utilisateurs dans leurs propres paramètres régionaux. Toutefois, il peut être non intuitif pour les développeurs d’applications. Cette rubrique décrit les considérations relatives à la gestion du tri dans vos applications. Le tri peut être linguistique ou ordinal (non linguistique).

## <a name="sorting-functions"></a>Fonctions de tri

Vous pouvez utiliser diverses fonctions de tri dans vos applications :

-   Fonctions de comparaison de chaînes NLS. Exemples : [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) et [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**comparestringordinal,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal), [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex), [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)et [**FindStringOrdinal**](/windows/desktop/api/Libloaderapi/nf-libloaderapi-findstringordinal). Consultez [considérations relatives à la sécurité : fonctionnalités internationales](security-considerations--international-features.md) pour une discussion sur les problèmes de sécurité liés aux fonctions de comparaison de chaînes.
-   Fonctions wrapper qui appellent en interne les fonctions de comparaison de chaînes. Les fonctions les plus courantes sont [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) et [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia), qui appellent [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw).

En règle générale, les fonctions de tri évaluent les chaînes caractère par caractère. Toutefois, de nombreux langages ont des éléments à plusieurs caractères, tels que la paire de deux caractères « CH » en espagnol traditionnel. [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) et [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) utilisent l’identificateur de paramètres régionaux fourni par l’application ou le nom pour identifier les éléments à plusieurs caractères. À l’inverse, [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)et [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) utilisent les paramètres régionaux de l’utilisateur.

Un autre exemple est vietnamien, qui contient de nombreux éléments à deux caractères, tels que les majuscules, les majuscules et les formes minuscules de « GI », respectivement « GI », « GI » et « GI ». L’un de ces formulaires est traité comme un élément de tri unique et, si la casse est ignorée, la comparaison est équivalente. Toutefois, étant donné que « gI » n’est pas valide en tant qu’élément unique, [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)et [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) considèrent « GI » comme deux éléments distincts.

Les fonctions [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa), [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia), [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa), [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex), [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)et [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) utilisent toutes par défaut une technique « tri de mot ». Pour ce type de tri, tous les signes de ponctuation et autres caractères non alphanumériques, à l’exception du trait d’Union et de l’apostrophe, sont placés avant tout caractère alphanumérique. Le trait d’Union et l’apostrophe sont traités différemment des autres caractères non alphanumériques pour garantir que les mots tels que « Coop » et « co-op » restent ensemble dans une liste triée.

Au lieu d’un tri par mot, l’application peut demander une technique de tri de chaîne à partir des fonctions de tri en spécifiant l’indicateur de tri \_ STRINGSORT. Un tri de chaîne traite le trait d’Union et l’apostrophe comme n’importe quel autre caractère non alphanumérique. Leurs positions dans la séquence de tri sont avant les caractères alphanumériques.

Le tableau suivant compare les résultats d’un tri de mot avec les résultats d’un tri de chaîne. 

| Tri par mot | Tri de chaîne |
|-----------|-------------|
| Billets    | facture      |
| traite     | Billets      |
| facture    | traite       |
| être    | arrive       |
| cant      | être      |
| arrive     | cant        |
| &       | Co-op       |
| Coop      | &         |
| Co-op     | Coop        |



 

## <a name="sort-strings-linguistically"></a>Trier les chaînes linguistiquement

Les fonctions [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) et [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) testent l’égalité linguistique. Vos applications doivent utiliser ces fonctions avec les paramètres régionaux appropriés pour trier les chaînes linguistiquement.

> [!Note]  
> Pour la compatibilité avec Unicode, une application doit préférer [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) ou la version Unicode de [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw). Une autre raison pour préférer [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) est que Microsoft migre vers l’utilisation des noms de paramètres régionaux au lieu des identificateurs de paramètres régionaux pour les nouveaux paramètres régionaux, pour des raisons d’interopérabilité. Toutes les applications qui s’exécutent uniquement sous Windows Vista et versions ultérieures doivent utiliser [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex).

 

Une autre façon de tester l’égalité linguistique consiste à utiliser [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) ou [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia), qui utilisent toujours un tri de mot. La fonction [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) appelle [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) avec l' \_ indicateur IGNORECASE normal, tandis que [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) l’appelle sans cet indicateur. Pour obtenir une vue d’ensemble de l’utilisation des fonctions wrapper, consultez [**chaînes**](../menurc/strings.md).

Les fonctions récupèrent les résultats linguistiques appropriés pour tous les paramètres régionaux. Les attentes des utilisateurs pour les différents paramètres régionaux peuvent varier considérablement selon le comportement de tri, comme indiqué dans les exemples suivants.

-   De nombreux paramètres régionaux associent la ligature AE (æ) aux lettres AE. Toutefois, islandais (Islande) considère qu’il s’agit d’une lettre distincte et le place après Z dans la séquence de tri.
-   L’anneau A (Å) est normalement trié avec une simple différence par rapport à un. Toutefois, suédois (Suède) place l’anneau A après Z dans la séquence de tri.

Les fonctions essaient de vérifier rigoureusement que les points de code définis dans la norme Unicode sont canoniquement égaux à une chaîne de points de code équivalents. Par exemple, le point de code qui représente un « u » minuscule avec un ditréma (ü) est égal de façon canonique à un « u » minuscule associé à ditréma (̈). Notez cependant que l’équivalence canonique n’est pas toujours possible.

Comme presque toutes les données entrées à l’aide des claviers Windows et des éditeurs de méthode d’entrée (IME) sont conformes à la normalisation de formulaire C définie dans la norme Unicode, la conversion des données entrantes à partir d’autres plateformes à l’aide des fonctions de normalisation Unicode NLS fournit des résultats plus cohérents, en particulier pour les paramètres régionaux qui utilisent le script tibétain ou le script Hangul pour Pour plus d’informations sur la prise en charge de la normalisation Unicode dans Windows Vista et versions ultérieures, consultez [utilisation de la normalisation Unicode pour représenter des chaînes](using-unicode-normalization-to-represent-strings.md).

Lorsque la comparaison de chaînes suit la préférence de langue de l’utilisateur, par exemple, lors du tri d’éléments pour un contrôle ListView ordonné, l’application peut effectuer l’une des opérations suivantes :

-   Appelez [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) ou [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) avec les paramètres régionaux de l’utilisateur.
-   Appelez [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) ou [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) pour définir des paramètres régionaux pour la comparaison, passer des indicateurs supplémentaires, incorporer des caractères null ou passer des longueurs explicites pour faire correspondre des parties d’une chaîne.

Lorsque les résultats de la comparaison doivent être cohérents indépendamment des paramètres régionaux, par exemple, lors de la comparaison de données récupérées à une liste prédéfinie ou d’une valeur interne, l’application doit utiliser [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) ou [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) avec les paramètres *régionaux* définis sur les paramètres régionaux \_ invariants. Pour [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), l’un des appels suivants correspondra même si myStr est « INLAP ». Dans ce cas, un appel sensible aux paramètres régionaux à [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) échoue si les paramètres régionaux actuels sont vietnamiens.

Sur Windows XP :


```C++
int iReturn = CompareString(LOCALE_INVARIANT, NORM_IGNORECASE, mystr, -1, _T("InLap"), -1);
```



Sur les systèmes d’exploitation antérieurs :


```C++
DWORD lcid = MAKELCID(MAKELANGID(LANG_ENGLISH, SUBLANG_ENGLISH_US), SORT_DEFAULT);
int iReturn = CompareString(lcid, NORM_IGNORECASE, mystr, -1, _T("InLap"), -1);
```



## <a name="sort-strings-ordinally"></a>Trier les chaînes de façon ordinale

Pour le tri ordinal (non linguistique), vos applications doivent toujours utiliser la fonction [**comparestringordinal,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) .

> [!Note]  
> Cette fonction est uniquement disponible pour Windows Vista et versions ultérieures.

 

[**Comparestringordinal,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) compare deux chaînes [Unicode](unicode.md) pour tester l’égalité binaire, par opposition à l’égalité linguistique. Les noms de fichiers NTFS, les variables d’environnement et les noms des mutex, des canaux nommés ou des mailslots sont des exemples de ces chaînes non linguistiques. À l’exception de l’option de non-respect de la casse, cette fonction ignore toutes les équivalences non binaires. Contrairement à d’autres fonctions de tri, il teste l’égalité de tous les points de code, y compris ceux qui n’ont pas de poids dans les schémas de tri linguistique.

Toutes les instructions suivantes s’appliquent à [**comparestringordinal,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) dans les comparaisons binaires, mais pas à [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)ou [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia).

-   Les séquences de caractères canoniques équivalentes en Unicode, telles que la lettre minuscule latine A avec un anneau au-dessus (U + 00E5) et la lettre minuscule latine A + (U + 0061 U + 030A), ne sont pas égales même si elles apparaissent identiques ("å").
-   Les chaînes canoniquement similaires en Unicode, telles que la lettre latine petite majuscule Y (U + 028F) et la lettre majuscule latine Y (U + 0059), qui ressemblent très similaires (« ʏ » et « Y ») et qui varient uniquement par certains poids spéciaux dans les tables linguistiques, sont considérées comme des caractères totalement différents. Même si l’application affecte la **valeur true** à *bIgnoreCase* , ces chaînes sont comparées.
-   Les points de code qui sont définis mais n’ont pas de poids de tri linguistique, tels que le sommet de largeur zéro (U + 200D), sont traités comme ayant leurs poids de point de code.
-   Les points de code qui sont définis dans les versions ultérieures d’Unicode, mais qui n’ont pas de poids dans les tables linguistiques actuelles, sont traités comme ayant leur poids de point de code.
-   Les points de code qui ne sont pas définis par Unicode sont traités comme ayant leur poids de point de code.
-   Lorsque l’application affecte à *bIgnoreCase* la **valeur true**, la fonction mappe la casse à l’aide de la table uppercasing du système d’exploitation, au lieu des informations contenues dans les tables de tri linguistique. Le mappage est donc indépendant des paramètres régionaux.

Pour plus d’informations sur les séquences canoniques équivalentes dans des chaînes Unicode et similaires au format Unicode, consultez Utilisation de la [normalisation Unicode pour représenter des chaînes](using-unicode-normalization-to-represent-strings.md).

## <a name="sort-code-points"></a>Trier les points de code

Certains points de code Unicode n’ont aucun poids, par exemple, un NON-joint de largeur nulle, U + 200C. Les fonctions de tri évaluent intentionnellement les points de code sans poids comme équivalents, car ils n’ont pas de poids dans le tri. Sur Windows Vista et versions ultérieures, l’application peut trier ces points de code en appelant les fonctions de comparaison de chaînes NLS, en particulier [**comparestringordinal,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal), pour l’évaluation de tous les points de code dans un littéral, sens binaire, par exemple, lors de la validation du mot de passe. Sur les systèmes d’exploitation antérieurs à Windows Vista, l’application doit utiliser la fonction C Runtime **strcmp** ou **wcscmp**.

Les fonctions de tri ignorent les signes diacritiques, tels que le NON-ESPACEment, U + 0306, lorsque l’application spécifie l’indicateur de NON- \_ espace hlink. De même, ces fonctions ignorent les symboles, par exemple, signe égal, U + 003d, lorsque l' \_ indicateur de symboles Hlink est spécifié. Sur Windows Vista et versions ultérieures, l’application appelle [**comparestringordinal,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) pour l’évaluation des signes diacritiques et des points de code de symbole dans un littéral binaire. Sur les systèmes d’exploitation antérieurs à Windows Vista, l’application doit utiliser **strcmp** ou **wcscmp**.

Certains points de code, tels que 0xFFFF et 0x058b, ne sont actuellement pas assignés en Unicode. Ces points de code ne reçoivent aucun poids en tri et ne doivent jamais être passés aux fonctions de tri. L’application doit utiliser [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) pour détecter les points de code non-Unicode dans un flux de données.

> [!Note]  
> Les résultats de [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) peuvent varier en fonction de la version Unicode passée si un caractère est ajouté à Unicode dans une version ultérieure et est ensuite ajouté aux tables de tri Windows. Pour plus d’informations, consultez utiliser le contrôle de [version de tri](#use-sort-versioning).

 

## <a name="sort-digits-as-numbers"></a>Trier les chiffres en tant que nombres

Sur Windows 7 et versions ultérieures, l’application peut appeler [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)ou [**LCMAPSTRINGEX**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) à l’aide de l' \_ indicateur sort DIGITSASNUMBERS. Cet indicateur prend en charge le tri qui traite les chiffres comme des nombres, par exemple le tri de « 2 » avant « 10 ».

Notez que l’utilisation de cet indicateur n’est pas appropriée pour les chiffres hexadécimaux tels que ce qui suit. <dl> 01AF  
1BCD  
002A  
12FA  
AB1C  
AB02  
AB12  
</dl>

Dans ce cas, les « nombres » sont triés dans l’ordre, mais l’utilisateur perçoit une liste hexadécimale mal triée.

## <a name="map-strings"></a>Chaînes de mappage

L’application utilise la fonction [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) ou [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) pour mapper des chaînes, si la valeur SortKey de LCMAP \_ n’est pas spécifiée. Une chaîne mappée se termine par un caractère NULL si la chaîne source se termine par un caractère null.

Lors de la transformation entre les majuscules et les minuscules, la fonction ne garantit pas qu’un seul caractère sera mappé à un seul caractère. Par exemple, les \_ \_ indicateurs en majuscules et en minuscules LCMAP peuvent mapper l’allemand Sharp S (« ß ») à lui-même. L' \_ indicateur majuscule LCMAP peut également mapper « ß » à « SS » et l' \_ indicateur LCMAP en minuscules peut mapper « SS » à « ß ». Le comportement dépend de la version NLS.

Lors de la transformation entre les majuscules et les minuscules, la fonction n’est pas sensible au contexte. Par exemple, si l' \_ indicateur majuscule LCMAP mappe correctement à la fois le Sigma minuscule grec (« σ ») et le Sigma final grec (« σ ») à la lettre minuscule grecque Sigma (« σ »), l' \_ indicateur en minuscules LCMAP mappe toujours « σ » à « σ », jamais à « σ ».

Par défaut, la fonction mappe la lettre « i » en minuscules à la majuscule « I », même lorsque les paramètres *régionaux* spécifient le turc ou l’azerbaïdjanais. Pour remplacer ce comportement pour le turc ou l’azerbaïdjanais, l’application doit spécifier \_ la \_ casse linguistique LCMAP. Si cet indicateur est spécifié avec les paramètres régionaux appropriés, « ı » (I sans point minuscule) est la forme minuscule de « I » (majuscule sans point) et « i » (i en minuscules) est la forme minuscule de « i » (i en majuscules).

Si l' \_ indicateur Hiragana LCMAP est spécifié pour mapper les caractères katakana aux caractères Hiragana et \_ que la pleine chasse LCMAP n’est pas spécifiée, [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) ou [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) mappe uniquement les caractères pleine chasse à Hiragana. Dans ce cas, tous les caractères katakana à demi-chasse sont placés comme dans la chaîne de destination, sans mappage à Hiragana. L’application doit spécifier LCMAP \_ pleine chasse pour mapper les caractères katakana demi-chasse à Hiragana. La raison de cette restriction est que tous les caractères Hiragana sont des caractères à pleine chasse.

Si l’application doit supprimer les caractères de la chaîne source, elle peut appeler la fonction de mappage avec les \_ indicateurs IGNORESYMBOLS et normal \_ IGNORENONSPACE définis, et tous les autres indicateurs sont effacés. Si l’application effectue cette opération avec une chaîne source qui ne se termine pas par un caractère null, il est possible que la fonction retourne une chaîne vide et ne retourne pas d’erreur.

## <a name="create-sort-keys"></a>Créer des clés de tri

Lorsque l’application spécifie LCMAP \_ SortKey, [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) ou [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) génère une clé de tri, un tableau binaire de valeurs d’octets. La clé de tri n’est pas une véritable chaîne et ses valeurs représentent le comportement de tri de la chaîne source, mais elles ne sont pas des valeurs d’affichage significatives.

> [!Note]  
> La fonction ignore les kachidés arabes lors de la génération d’une clé de tri. Si une application appelle la fonction pour créer une clé de tri pour une chaîne contenant des signes kachidé arabes, la fonction ne crée aucune valeur de clé de tri.

 

La clé de tri peut contenir un nombre impair d’octets. L' \_ indicateur LCMAP BYTEREV inverse uniquement un nombre pair d’octets. Le dernier octet (à positionnement impair) dans la clé de tri n’est pas inversé. Si l’octet de fin 0x00 est un octet à positionnement impair, il reste le dernier octet dans la clé de tri. Si l’octet de fin 0x00 est un octet positionné uniformément, il échange des positions avec l’octet qui le précède.

Lors de la génération de la clé de tri, la fonction traite le trait d’Union et l’apostrophe différemment des autres signes de ponctuation, de sorte que les mots tels que « Coop » et « co-op » restent ensemble dans une liste. Tous les symboles de ponctuation autres que le trait d’Union et l’apostrophe sont triés avant les caractères alphanumériques. L’application peut modifier ce comportement en définissant l' \_ indicateur de tri STRINGSORT, comme décrit dans [fonctions de tri](#sorting-functions).

En cas d’utilisation dans [memcmp](/cpp/c-runtime-library/reference/memcmp-wmemcmp), la clé de tri produit le même ordre que lorsque la chaîne source est utilisée dans [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) ou [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex). La fonction [memcmp](/cpp/c-runtime-library/reference/memcmp-wmemcmp) doit être utilisée à la place de [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp), car la clé de tri peut comporter des octets null incorporés.

## <a name="use-sort-versioning"></a>Utiliser le contrôle de version de tri

Une table de [Tri](sorting.md) comporte deux nombres identifiant sa version : la version définie et la version nls. Les deux nombres sont des valeurs DWORD, composés d’une valeur majeure et d’une valeur mineure. Le premier octet d’une valeur est réservé, les deux octets suivants représentent la version principale et le dernier octet représente la version mineure. En termes hexadécimaux, le modèle est 0xRRMMMMmm, où R est égal à réservé, M est égal à principal et m est égal à mineur. Par exemple, une version majeure de 3 avec une version mineure de 4 est représentée sous la forme 0x304.

La version définie identifie le répertoire des points de code et est identique pour tous les paramètres régionaux. La version principale incrémente pour indiquer les modifications apportées aux points de code existants. La version mineure s’incrémente pour indiquer que des points de code ont été ajoutés, mais qu’aucun point de code précédemment existant n’a été modifié.

La version NLS est spécifique à un [identificateur](locale-identifiers.md) de paramètres régionaux ou à un [nom de paramètres régionaux](locale-names.md), et suit les modifications apportées aux pondérations des points de code pour les paramètres régionaux affectés. La version principale incrémente lorsque les pondérations sont modifiées pour les points de code qui étaient déjà triables. La version mineure est incrémentée lorsque les pondérations sont affectées aux nouveaux points de code, mais tous les autres poids des points de code précédemment pouvant être triés restent inchangés.

> [!Note]  
> Pour une version majeure, un ou plusieurs points de code sont modifiés afin que l’application doive réindexer toutes les données pour que les comparaisons soient valides. Pour une version mineure, rien n’est déplacé, mais des points de code sont ajoutés. Pour ce type de version, l’application doit uniquement réindexer les chaînes avec des valeurs précédemment non triées.

 

> [!IMPORTANT]
> La version principale a été modifiée dans Windows 8. Les données créées sous des versions antérieures de Windows doivent être réindexées.

 

Les versions définie et NLS s’appliquent aux points de code triable récupérés à l’aide de la fonction [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) ou [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex) avec l' \_ indicateur SortKey LCMAP, ainsi qu’aux fonctions [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex), [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)et [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) . Si un ou plusieurs points de code d’une chaîne ne sont pas triés, la fonction [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) retourne la **valeur false** lorsque cette chaîne lui est transmise en tant que paramètre.

L’application peut appeler [**GetNLSVersion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion) ou [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex) pour récupérer la version définie et la version nls pour une table de tri.

## <a name="index-the-database"></a>Indexer la base de données

Pour des raisons de performances, l’application doit suivre cette procédure lors de l’indexation de la base de données.

**Pour indexer correctement la base de données**

1.  Pour chaque fonction, stockez la version NLS, les clés de tri de cette version et une indication de la tri pour chaque chaîne indexée.
2.  Lorsque la version mineure augmente, réindexe les chaînes précédemment non triées. Les chaînes affectées dans cette mise à jour doivent être limitées à celles pour lesquelles [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) a précédemment retourné la **valeur false**.
3.  Lorsque la version principale incrémente, réindexe toutes les chaînes, car les poids mis à jour peuvent modifier le comportement de n’importe quelle chaîne. Les versions majeures de version sont très rares.

Des problèmes d’indexation de base de données peuvent se produire pour les raisons suivantes :

-   Un système d’exploitation ultérieur peut définir des points de code qui ne sont pas définis pour un système d’exploitation antérieur, modifiant ainsi le tri.
-   Les points de code peuvent avoir des pondérations de tri différentes selon les systèmes d’exploitation, en raison des corrections apportées à la prise en charge linguistique.

Pour limiter la nécessité de réindexer la base de données dans ces circonstances, l’application peut utiliser [**IsNLSDefinedString**](/windows/desktop/api/Winnls/nf-winnls-isnlsdefinedstring) pour différencier les chaînes définies par des chaînes non définies de sorte que l’application puisse rejeter des chaînes avec des points de code non définis. L’utilisation de [**GetNLSVersion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion) ou [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex) permet à l’application de déterminer si une modification nls affecte les paramètres régionaux utilisés pour une table d’index particulière. Si la modification n’a aucun effet sur les paramètres régionaux, l’application n’a pas besoin de réindexer la table.

## <a name="examples"></a>Exemples

Le tableau suivant illustre les effets de certains indicateurs utilisés avec les fonctions de tri. Dans chaque cas, la sélection des indicateurs détermine si deux caractères différents sont considérés comme égaux à des fins de tri.



| Caractère 1                                                        | Caractère 2                                             | Default | \_IGNOREWIDTH normale | \_IGNOREKANA normale | \_IGNOREWIDTH normale \| NORMIGNOREKANA |
|--------------------------------------------------------------------|---------------------------------------------------------|---------|-------------------|------------------|------------------------------------|
| "あ"<br/> LETTRE HIRAGANA U + 3042 A<br/>                | "ガ"<br/> LETTRE KATAKANA U + 30A2 A<br/>     | Inégaux | Inégaux           | Égal à            | Égal à                              |
| "ｵ"<br/> LETTRE KATAKANA O + FF75 DEMI-CHASSE<br/>       | "オ"<br/> LETTRE KATAKANA U + 30AA O<br/>     | Inégaux | Égal à             | Inégaux          | Égal à                              |
| P<br/> LETTRE MAJUSCULE LATINE B PLEINE CHASSE U + FF22<br/> | « B »<br/> LETTRE MAJUSCULE LATINE B U + 0042<br/> | Inégaux | Égal à             | Inégaux          | Égal à                              |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la prise en charge linguistique nationale](using-national-language-support.md)
</dt> <dt>

[Tri](sorting.md)
</dt> <dt>

[Récupération et définition des informations relatives aux paramètres régionaux](retrieving-and-setting-locale-information.md)
</dt> <dt>

[Utilisation de la normalisation Unicode pour représenter des chaînes](using-unicode-normalization-to-represent-strings.md)
</dt> <dt>

[Considérations relatives à la sécurité : fonctionnalités internationales](security-considerations--international-features.md)
</dt> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)
</dt> <dt>

[**Comparestringordinal,**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal)
</dt> <dt>

[**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)
</dt> <dt>

[**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)
</dt> <dt>

[**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> <dt>

[**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex)
</dt> </dl>

 

 
