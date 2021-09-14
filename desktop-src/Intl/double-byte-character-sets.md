---
description: Un jeu de caractères codés sur deux octets (DBCS), également connu sous le nom de &\# 0034 ; jeu de caractères 8 bits développé&\# 0034 ;, est un jeu de caractères codés sur un octet étendu (SBCS), implémenté comme page de codes.
ms.assetid: df049d22-02e2-48b2-8b74-52f71c00c549
title: Jeux de caractères codés sur deux octets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 431b762b19f5531644e4bbaace548f34245c9d5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240360"
---
# <a name="double-byte-character-sets"></a>Jeux de caractères codés sur deux octets

Un jeu de caractères codés sur deux octets (DBCS), également appelé « jeu de caractères 8 bits développé », est un [jeu de caractères](single-byte-character-sets.md) codés sur un octet étendu (SBCS), implémenté comme page de codes. Les DBCS ont été développés à l’origine pour étendre la conception SBCS afin de gérer des langues telles que le japonais et le chinois. Certains caractères d’un DBCS, y compris les chiffres et les lettres utilisés pour écrire l’anglais, ont des valeurs de code codés sur un octet. Les autres caractères, tels que les idéogrammes chinois ou le Kanji japonais, ont des valeurs de code codés sur deux octets. un DBCS peut correspondre à une Windows page de codes ou à une page de codes OEM. Une page de codes DBCS peut également inclure une page de codes non native, par exemple, une page de codes EBCDIC. Pour obtenir les définitions de ces pages de codes, consultez [pages de codes](code-pages.md).

> [!Note]  
> les nouvelles Windows applications doivent utiliser [Unicode](unicode.md) pour éviter les incohérences de pages de codes variées et pour faciliter la localisation. Toutefois, certains protocoles hérités peuvent nécessiter l’utilisation de pages de codes DBCS. Chaque page de codes DBCS prend en charge des caractères différents, mais aucune page ne prend en charge l’intégralité des caractères fournis par Unicode. Chaque page de codes DBCS prend en charge un sous-ensemble différent, encodé différemment. Les données converties d’une page de codes DBCS vers une autre sont susceptibles d’être endommagées, car la même valeur de données sur des pages de codes différentes peut encoder un caractère différent. Les données converties d’Unicode en DBCS sont sujettes à des pertes de données, car une page de codes donnée peut ne pas être en mesure de représenter chaque caractère utilisé dans ces données Unicode particulières.

 

Pour interpréter une chaîne DBCS, une application doit commencer au début de la chaîne et effectuer une analyse par progression. Il effectue le suivi lorsqu’il rencontre un octet de tête dans la chaîne et traite l’octet suivant comme la partie de fin du même caractère. Si l’application analyse simplement la chaîne un octet à la fois et rencontre un octet qui semble être la valeur de code représentant une barre oblique inverse (« \\ »), cet octet peut simplement être l’octet de fin d’un caractère de deux octets. L’application ne peut pas simplement sauvegarder un octet pour voir si l’octet précédent est un octet de tête, car cette valeur d’octet peut être éligible pour être utilisée à la fois comme un octet de tête et un octet de fin. L’application a donc essentiellement le même problème qu’avec la barre oblique inverse possible. En d’autres termes, les recherches de sous-chaînes sont bien plus compliquées avec un DBCS qu’avec SBCSs ou Unicode. Par conséquent, les applications qui prennent en charge un DBCS doivent utiliser des fonctions spéciales, telles que [ \_ mbsstr](/cpp/c-runtime-library/reference/strstr-wcsstr-mbsstr-mbsstr-l), au lieu de la fonction [**strstr**](https://msdn.microsoft.com/library/z9da80kz(v=VS.71).aspx) .

vos applications utilisent des pages de codes DBCS Windows avec les versions « A » de Windows fonctions. Consultez [conventions pour les prototypes de fonction](conventions-for-function-prototypes.md) et les [pages de codes](code-pages.md). Pour faciliter l’identification d’une page de codes DBCS, une application peut utiliser la fonction [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) ou [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) . Une application peut utiliser la fonction [**IsDBCSLeadByte**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte) pour déterminer si une valeur donnée peut être utilisée comme octet de tête d’un caractère de 2 octets. En outre, une application peut utiliser les fonctions [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) et [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) pour effectuer un mappage entre les chaînes Unicode et DBCS.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Jeux de caractères](character-sets.md)
</dt> <dt>

[Jeux de caractères codés sur un octet](single-byte-character-sets.md)
</dt> </dl>

 

 
