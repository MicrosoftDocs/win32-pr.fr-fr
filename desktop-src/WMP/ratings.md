---
title: Évaluations
description: Évaluations
ms.assetid: babc9db5-2782-4261-a571-acb7be4ea770
keywords:
- Lecteur Windows Media Skins mobiles, évaluations
- apparences, évaluations
- informations de référence sur les apparences, les évaluations
- évaluations dans les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb90908c725fcb525e0be1547c27c588a4220c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403507"
---
# <a name="ratings"></a>Évaluations

lorsque vous créez une apparence pour Lecteur Windows Media Mobile 10,1, vous pouvez afficher l’évaluation associée au contenu Windows Media Audio en cours de diffusion. L’évaluation est affichée sous la forme d’une étoile avec un chiffre. L’étoile sera numérotée de 1 à 5, indiquant ainsi l’évaluation actuelle de ce contenu. Si le contenu n’est pas évalué, l’étoile sera numérotée à zéro.

La section ratings du fichier de définition d’apparence commence par cette ligne :


```C++
[ Ratings ]

```



Vous devez ensuite ajouter une ligne qui contient des informations sur la taille et l’emplacement de votre icône d’évaluation dans votre apparence.


```C++
147, 3, 22, 21       ratings96S.gif

```



Vous pouvez utiliser le modèle suivant pour la section évaluations de votre fichier de définition d’apparence :


```C++
// <Location>           <Image>
// ---------------      --------------------
```



vous pouvez également affecter une valeur de classement à un élément multimédia par le biais de l’interface utilisateur dans Lecteur Windows Media Mobile 10,1, et la prochaine fois que l’appareil se synchronise avec un ordinateur, la nouvelle valeur d’évaluation est propagée à cet élément multimédia s’il réside dans la bibliothèque Lecteur Windows Media 10.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence d’apparence**](skin-reference.md)
</dt> </dl>

 

 




