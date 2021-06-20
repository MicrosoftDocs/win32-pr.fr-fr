---
title: Unités VML
description: Cet article décrit les unités VML. VML est une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.
ms.assetid: f95e65ad-d92a-460f-baeb-30fd8a35f84e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 184d577052412bde4a97148b51cab12a87b3672e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406942"
---
# <a name="vml-units"></a>Unités VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Les unités CSS suivantes sont utilisées par VML.



Unités de longueur relative

carré

Hauteur de la police de l’élément.

ex

Hauteur de la lettre « x ».

px

Hauteur.

%

Cent.

Unités de longueur absolue

in

Pouces (1 pouce = 2,54 centimètres).

cm

Centimètres.

mm

Millimètres.

pt

Points (1 point = 1/72 pouces).

pc

Picas (1 pica = 12 points).



 

Les mesures et les positions dans les propriétés de feuille de style en cascade (CSS) sont établies à l’aide d’unités de longueur. Internet Explorer prend en charge deux types d’unités de longueur : relatif et absolu.

Une unité de longueur relative spécifie une longueur par rapport à une autre propriété de longueur. Les unités de longueur relative sont mieux adaptées d’un périphérique de sortie à un autre, par exemple d’une analyse à une imprimante. Les pourcentages et les mots clés fonctionnent de la même façon.

Une unité de longueur absolue spécifie une mesure absolue, telle que des pouces ou des centimètres. Les unités de longueur absolue sont utiles lorsque les propriétés physiques du périphérique de sortie sont connues.

## <a name="other-units-of-measurement"></a>Autres unités de mesure

**UME**

L’UEM (unité métrique anglaise) est la plus petite unité de mesure utile et est utilisée par VML pour le stockage d’unités interne. Il y a 914400 UME par pouce et 12700 UME en un point. La EMU ne peut pas être fractionnaire.

Étant donné que la EMU est définie par des nombres entiers signés 32 bits, le plus grand nombre de EMU est de 2348 pouces (environ 59 mètres ou 65 mètres). Étant donné que les mesures sont toujours adaptées à un appareil de sortie à l’écran ou à la taille de la page, elles sont toujours comprises dans cette plage.

**Angles**

Les mesures d’angle peuvent être définies avec les suffixes suivants.



Suffixe

FD

Fractions de seconde.

aucun

Degrés

deg

Degrés

rad

Radians



 

 

 