---
description: Unicode est une norme internationale d’encodage de caractères. Le système utilise uniquement Unicode pour la manipulation de caractères et de chaînes. Pour obtenir une description détaillée de tous les aspects d’Unicode, reportez-vous à la norme Unicode.
ms.assetid: ca5bcdee-ea13-4745-a565-5426c462892d
title: Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88facae63fbb365fd6f38cb09464de735e0759b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224177"
---
# <a name="unicode"></a>Unicode

Unicode est une norme internationale d’encodage de caractères. Le système utilise uniquement Unicode pour la manipulation de caractères et de chaînes. Pour obtenir une description détaillée de tous les aspects d’Unicode, reportez-vous à [la norme Unicode](https://www.unicode.org/standard/standard.html).

Comparé aux mécanismes plus anciens pour la gestion des données de type caractère et chaîne, Unicode simplifie la localisation de logiciels et améliore le traitement de texte multilingue. En utilisant Unicode pour représenter des données de type caractère et chaîne dans vos applications, vous pouvez activer les fonctionnalités d’échange de données universelles pour le marketing global, à l’aide d’un seul fichier binaire pour chaque code de caractère possible. Unicode effectue les opérations suivantes :

-   Permet à n’importe quelle combinaison de caractères, tirée d’une combinaison de scripts et de langages, de coexister dans un document unique.
-   Définit la sémantique pour chaque caractère.
-   Normalise le comportement des scripts.
-   Fournit un algorithme standard pour le texte bidirectionnel.
-   Définit des mappages croisés à d’autres normes.
-   Définit plusieurs encodages de son jeu de caractères unique : UTF-7, UTF-8, UTF-16 et UTF-32. La conversion des données entre ces encodages est sans perte.

Unicode prend en charge de nombreux scripts utilisés par les langages dans le monde entier, ainsi qu’un grand nombre de symboles techniques et de caractères spéciaux utilisés dans la publication. Les scripts pris en charge incluent, mais ne sont pas limités à, latin, grec, cyrillique, hébreu, arabe, DÉVANÂGARÎ, thaï, Han, Hangul, Hiragana et Katakana. Les langues prises en charge incluent, entre autres, l’allemand, le français, l’anglais, le grec, le russe, l’hébreu, l’arabe, l’hindi, le thaï, le chinois, le coréen et le japonais. Unicode peut actuellement représenter la grande majorité des caractères dans l’utilisation moderne des ordinateurs dans le monde entier et continue à être mis à jour pour le rendre encore plus complet.

Les fonctions compatibles Unicode sont décrites dans [conventions pour les prototypes de fonction](conventions-for-function-prototypes.md). ces fonctions utilisent l’encodage UTF-16 (caractères larges), qui est l’encodage le plus courant d’unicode et celui utilisé pour l’encodage unicode natif sur les systèmes d’exploitation Windows. Chaque valeur de code est d’une largeur de 16 bits, contrairement à l’approche de [page de codes](code-pages.md) plus ancienne pour les données de type caractère et chaîne, qui utilise des valeurs de code de 8 bits. L’utilisation de 16 bits autorise l’encodage direct de 65 536 caractères. En fait, l’univers des symboles utilisés pour transcrire les langues humaines est encore plus grand que cela, et les points de code UTF-16 dans la plage U + D800 à U + DFFF sont utilisés pour former des paires de substitution, qui constituent des encodages 32 bits de caractères supplémentaires. Pour plus d’informations [, consultez substituts et caractères supplémentaires](surrogates-and-supplementary-characters.md) .

Le jeu de caractères Unicode comprend de nombreux caractères d’association, tels que U + 0308 (« ̈ »), une combinaison d’un tréma ou d’un tréma. Unicode peut souvent représenter le même glyphe dans une forme « » composée de « » ou une forme « décomposée » : par exemple, la forme composée de « Ä » est le point de code Unicode unique « Ä » (U + 00C4), tandis que sa forme décomposée est « A » + « ̈ » (U + 0041 U + 0308). Unicode ne définit pas un formulaire composé pour chaque glyphe. Par exemple, le « o » minuscule vietnamien et le tilde (« ỗ ») sont représentés par U + 006F U + 0302 U + 0303 (o + circonflexe + tilde). Pour plus d’informations sur la combinaison de caractères et de problèmes connexes, consultez Utilisation de la [normalisation Unicode pour représenter des chaînes](using-unicode-normalization-to-represent-strings.md).

Pour la compatibilité avec les environnements 8 bits et 7 bits, Unicode peut également être encodé au format UTF-8 et UTF-7, respectivement. alors que les fonctions compatibles Unicode dans Windows utilisent utf-16, il est également possible d’utiliser des données encodées au format utf-8 ou utf-7, qui sont prises en charge dans les Windows en tant que [pages de codes](code-pages.md)du jeu de caractères multioctets.

les nouvelles applications Windows doivent utiliser UTF-16 comme représentation interne des données. Windows fournit également une prise en charge étendue des pages de codes, et l’utilisation mixte dans la même application est possible. Même les nouvelles applications basées sur Unicode doivent parfois fonctionner avec des pages de codes. Les raisons sont décrites dans les [pages de codes](code-pages.md).

Une application peut utiliser les fonctions [**MultiByteToWideChar**](/windows/win32/api/Stringapiset/nf-stringapiset-multibytetowidechar) et [**WideCharToMultiByte**](/windows/win32/api/Stringapiset/nf-stringapiset-widechartomultibyte) pour effectuer une conversion entre des chaînes basées sur des pages de codes et des chaînes Unicode. Bien que leurs noms fassent référence à « multioctet », ces fonctions fonctionnent aussi bien avec le jeu de caractères codés sur [un octet](single-byte-character-sets.md) (SBCS), [le jeu de caractères codés sur deux octets](double-byte-character-sets.md) (DBCS) et les pages de codes du jeu de caractères multioctets (MBCS).

en règle générale, une application Windows doit utiliser UTF-16 en interne, en convertissant uniquement dans le cadre d’une « couche mince » sur l’interface qui doit utiliser un autre format. Cette technique protège contre la perte et l’endommagement des données. Chaque page de codes prend en charge différents caractères, mais aucun d’entre eux ne prend en charge la gamme complète des caractères fournis par Unicode. La plupart des pages de codes prennent en charge des sous-ensembles différents, codés différemment. Les pages de codes UTF-8 et UTF-7 constituent une exception, car elles prennent en charge le jeu de caractères Unicode complet, et la conversion entre ces encodages et UTF-16 est sans perte.

Les données converties directement à partir de l’encodage utilisé par une page de codes vers l’encodage utilisé par une autre sont susceptibles d’être endommagées, car la même valeur de données sur des pages de codes différentes peut encoder un caractère différent. Même lorsque votre application est convertie aussi près que possible de l’interface, vous devez réfléchir soigneusement à la plage de données à gérer.

Les données converties d’Unicode en page de codes sont sujettes à une perte de données, car une page de codes donnée peut ne pas être en mesure de représenter chaque caractère utilisé dans ces données Unicode particulières. Par conséquent, Notez que [**WideCharToMultiByte**](/windows/win32/api/Stringapiset/nf-stringapiset-widechartomultibyte) peut perdre des données si la page de codes cible ne peut pas représenter tous les caractères de la chaîne Unicode.

Lors de la modernisation d’applications héritées basées sur des pages de code pour utiliser Unicode, vous pouvez utiliser des fonctions génériques et la macro de [**texte**](/windows/win32/api/Winnt/nf-winnt-text) pour conserver un ensemble unique de sources à partir desquelles compiler deux versions de votre application. une version prend en charge Unicode et l’autre fonctionne avec Windows pages de codes. à l’aide de ce mécanisme, vous pouvez convertir des applications très volumineuses d’Windows pages de codes au format Unicode tout en conservant des sources d’application qui peuvent être compilées, générées et testées à toutes les phases de la conversion. Pour plus d’informations, consultez [conventions pour les prototypes de fonction](conventions-for-function-prototypes.md).

Les chaînes et les caractères Unicode utilisent des types de données qui sont différents de ceux pour les chaînes et les caractères basés sur une page de codes. Outre une série de macros et de conventions de nommage, cette distinction réduit le risque de mélanger accidentellement les deux types de données de type caractère. Elle facilite la vérification du type de compilateur pour s’assurer que seules les valeurs de paramètre Unicode sont utilisées avec les fonctions qui attendent des chaînes Unicode.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Jeux de caractères](character-sets.md)
</dt> <dt>

[Tri](sorting.md)
</dt> <dt>

[Substituts et caractères supplémentaires](surrogates-and-supplementary-characters.md)
</dt> <dt>

[Utilisation de la normalisation Unicode pour représenter des chaînes](using-unicode-normalization-to-represent-strings.md)
</dt> </dl>

 

 



