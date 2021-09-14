---
description: Un jeu de caractères codés sur un octet (SBCS) est un mappage de 256 caractères individuels à leurs valeurs de code d’identification, implémenté comme une page de codes.
ms.assetid: 53f74132-91aa-4257-846a-f6e1f2f9ae0b
title: Jeux de caractères codés sur un octet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5618b191b83e33333dce2a290d8c9a7181233df4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121885"
---
# <a name="single-byte-character-sets"></a>Jeux de caractères codés sur un octet

Un jeu de caractères codés sur un octet (SBCS) est un mappage de 256 caractères individuels à leurs valeurs de code d’identification, implémenté comme une page de codes. un SBCS peut correspondre à une page de codes Windows ou à une page de codes OEM. Une page de codes SBCS peut également inclure une page de codes non native, par exemple, une page de codes EBCDIC. Pour obtenir les définitions de ces pages de codes, consultez [pages de codes](code-pages.md).

> [!Note]  
> les nouvelles Windows applications doivent utiliser [Unicode](unicode.md) pour éviter les incohérences de pages de codes variées et pour faciliter la localisation. Toutefois, certains protocoles hérités requièrent l’utilisation d’un SBCS. Chaque page de codes SBCS prend en charge des caractères différents, mais aucune page ne prend en charge l’intégralité des caractères fournis par Unicode. Chaque page de codes SBCS prend en charge un sous-ensemble différent, encodé différemment. Les données converties d’une page de codes SBCS vers une autre sont susceptibles d’être endommagées, car la même valeur de données sur des pages de codes différentes peut encoder un caractère différent. Les données converties d’Unicode en SBCS sont sujettes à des pertes de données, car une page de codes donnée peut ne pas être en mesure de représenter chaque caractère utilisé dans ces données Unicode particulières.

 

vos applications utilisent des pages de codes SBCS Windows avec les versions « A » de Windows fonctions. Consultez [conventions pour les prototypes de fonction](conventions-for-function-prototypes.md) et les [pages de codes](code-pages.md). Pour faciliter l’identification d’une page de codes SBCS, une application peut utiliser la fonction [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) ou [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) . En outre, une application peut utiliser les fonctions [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) et [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) pour effectuer un mappage entre les chaînes Unicode et SBCS.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Jeux de caractères](character-sets.md)
</dt> <dt>

[Jeux de caractères codés sur deux octets](double-byte-character-sets.md)
</dt> </dl>

 

 



