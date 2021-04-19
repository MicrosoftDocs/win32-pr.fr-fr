---
description: La plupart des applications écrites aujourd’hui gèrent les données de type caractère principalement en Unicode, à l’aide de l’encodage UTF-16.
ms.assetid: 866f09f4-629e-4097-a974-fbda9389d077
title: Pages de codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28528ba13e3db3f0c72dd7c071eb8b7886ab003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530868"
---
# <a name="code-pages"></a>Pages de codes

La plupart des applications écrites aujourd’hui gèrent les données de type caractère principalement en [Unicode](unicode.md), à l’aide de l’encodage UTF-16. Toutefois, de nombreuses applications héritées continuent d’utiliser des jeux de caractères basés sur des pages de codes. Même les nouvelles applications doivent parfois fonctionner avec les pages de code, souvent pour l’une des raisons suivantes :

-   Pour communiquer avec des applications héritées.
-   Pour communiquer avec des serveurs de messagerie et de News plus anciens, qui ne prennent peut-être pas toujours en charge Unicode.
-   Pour communiquer avec la console Windows.

> [!Note]  
> Les nouvelles applications Windows doivent utiliser [Unicode](unicode.md) pour éviter les incohérences de pages de codes variées et pour faciliter la localisation.

 

Chaque page de codes est représentée par un identificateur de page de codes, par exemple 1252, et est gérée par les fonctions d’API de jeu de caractères et Unicode. Pour obtenir la liste des identificateurs de page de codes pris en charge, consultez [identificateurs de page de codes](code-page-identifiers.md). La référence « pages de codes » sur le [Centre de développement Microsoft Go Global](https://msdn.microsoft.com/goglobal) fournit une description complète de nombreuses pages de codes.

Les pages de codes Windows, communément appelées « pages de codes ANSI », sont des pages de codes pour lesquelles des valeurs non-ASCII (valeurs supérieures à 127) représentent des caractères internationaux. Ces pages de codes sont utilisées en mode natif dans Windows me et sont également disponibles sur Windows NT et versions ultérieures.

> [!Note]  
> À l’origine, la page de codes Windows 1252, la page de codes couramment utilisée pour l’anglais et les autres langues d’Europe occidentale, était basée sur un projet de American National Standards Institute (ANSI). Ce brouillon finit par devenir ISO 8859-1, mais la page de codes Windows 1252 a été implémentée avant la fin de la norme, et n’est pas exactement identique à ISO 8859-1.

 

De nombreuses fonctions de l’API Windows ont des versions « A » (ANSI) et « W » (larges, Unicode). La version « A » gère le texte en fonction des pages de codes Windows, tandis que la version « W » gère le texte Unicode. Consultez [types de données Windows pour les chaînes](windows-data-types-for-strings.md) et les [conventions pour les prototypes de fonction](conventions-for-function-prototypes.md).

Les pages de codes Windows sont parfois appelées « pages de codes actives » ou « pages de codes actives système ». Un système d’exploitation Windows dispose toujours d’une page de codes Windows active. Toutes les [versions ANSI des fonctions API](conventions-for-function-prototypes.md) utilisent la page de codes active.

Les pages de codes OEM (Original Equipment Manufacturer) sont des pages de codes pour lesquelles des valeurs non-ASCII représentent des caractères de dessin et de ponctuation. Ces pages de codes utilisaient à l’origine pour MS-DOS et sont toujours utilisées pour les applications console. Ils sont également utilisés pour les noms de fichiers non étendus dans les systèmes de fichiers FAT12, FAT16 et FAT32, comme décrit dans [jeux de caractères utilisés dans les noms de fichiers](character-sets-used-in-file-names.md). La page de codes OEM habituelle pour l’anglais est la page de codes 437.

Pour les pages de codes Windows et les pages de codes OEM, les valeurs de code 0x00 à 0x7F correspondent au jeu de caractères ASCII 7 bits. Les valeurs de code 0x00 à 0x19 et 0x7F représentent toujours des caractères de contrôle standardisés et 0x20 à 0x7E représentent des caractères affichables standardisés. Les caractères représentés par les autres codes, de 0x80 à 0xFF, varient selon les jeux de caractères. Chaque jeu de caractères comprend des caractères spéciaux différents, généralement personnalisés pour une langue ou un groupe de langues. La page de codes Windows 1252 et la page de codes OEM 437 sont généralement utilisées dans le États-Unis.

En plus des pages de codes Windows et OEM, vos applications peuvent utiliser des pages de codes non natives. Exemples : pages de codes EBCDIC et Macintosh.

Deux encodages Unicode (UTF-7 et UTF-8) sont implémentés en tant que pages de codes. Comme les autres pages de codes, chaque page est connue par un identificateur numérique et peut être gérée avec un grand nombre des mêmes fonctions d’API de jeu de caractères et Unicode.

Les pages de codes peuvent être des pages SBCS ou [des](single-byte-character-sets.md) pages de jeu de caractères codés [sur deux octets](double-byte-character-sets.md) (DBCS). Dans les pages SBCS, chaque octet encode directement un caractère unique, de sorte qu’il est possible de représenter exactement 256 caractères distincts (y compris les caractères de contrôle, les lettres, les chiffres, la ponctuation, les symboles, etc.). Les pages de codes DBCS sont utilisées pour des langues telles que le japonais et le chinois. Dans ce type de page de codes, certains caractères ont des encodages de deux octets avec certaines valeurs d’octet (toujours supérieures à 127) servant de « octets de tête ». Au lieu d’encoder les caractères avec leur propre droit, les octets de tête peuvent être mappés à un caractère uniquement avec un « octet de fin ».

Certains protocoles hérités requièrent l’utilisation de pages de codes SBCS et DBCS. Chaque page de codes SBCS/DBCS prend en charge des caractères différents, mais aucune page de codes ne prend en charge l’intégralité des caractères fournis par Unicode. Chaque page de codes SBCS/DBCS prend en charge un sous-ensemble différent, encodé différemment.

> [!Note]  
> Les données converties d’une page de codes SBCS ou DBCS vers une autre sont susceptibles d’être endommagées, car la même valeur de données sur des pages de codes différentes peut encoder un caractère différent. Les données converties d’Unicode en SBCS ou DBCS sont sujettes à des pertes de données, car une page de codes donnée peut ne pas être en mesure de représenter chaque caractère utilisé dans ces données Unicode particulières.

 

En plus des pages de codes SBCS et DBCS, vos applications ont accès aux pages de codes du jeu de caractères multioctets 52936, 54936, 51949 et 5022x, qui utilisent une approche similaire à celle d’un DBCS. Toutefois, une page de codes de jeu de caractères multioctets va au-delà du codage sur deux octets de certains caractères. UTF-7 et UTF-8 utilisent une approche similaire pour encoder Unicode en fonction des octets 7 bits et 8 bits, respectivement. Pour plus d’informations, consultez [Unicode](unicode.md).

Plusieurs fonctions Unicode et de jeu de caractères permettent à vos applications de gérer des pages de codes. Une application peut utiliser les fonctions [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) et [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) pour obtenir des informations sur une page de codes. Ces informations incluent le caractère par défaut utilisé lorsqu’un caractère dans une chaîne convertie n’a pas d’entrée correspondante dans la page de codes.

Une application peut utiliser les fonctions [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) et [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) pour effectuer une conversion entre des chaînes basées sur des pages de codes Windows et des chaînes Unicode. Bien que leurs noms fassent référence à « multioctet », ces fonctions fonctionnent aussi bien avec les pages de codes SBCS, DBCS et multioctets.

> [!Note]  
> [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) peut perdre des données si la page de codes fournie ne peut pas représenter tous les caractères d’une chaîne Unicode.

 

Votre application peut effectuer une conversion entre les pages de codes Windows et les pages de codes OEM à l’aide des fonctions de la bibliothèque Runtime C standard. Toutefois, l’utilisation de ces fonctions présente un risque de perte de données, car les caractères qui peuvent être représentés par chaque page de codes ne correspondent pas exactement.

Vos applications peuvent également appeler la fonction [**GetACP**](/windows/desktop/api/Winnls/nf-winnls-getacp) . Cette fonction récupère l’identificateur de la page de codes Windows (ANSI) active.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Jeux de caractères](character-sets.md)
</dt> </dl>

 

 



