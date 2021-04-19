---
title: Évaluations
description: Évaluations
ms.assetid: babc9db5-2782-4261-a571-acb7be4ea770
keywords:
- Skins mobiles Windows Media Player, évaluations
- apparences, évaluations
- informations de référence sur les apparences, les évaluations
- évaluations dans les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb90908c725fcb525e0be1547c27c588a4220c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106517969"
---
# <a name="ratings"></a>Évaluations

Lorsque vous créez une apparence pour le lecteur Windows Media 10,1 mobile, vous pouvez afficher l’évaluation associée au contenu Windows Media Audio en cours de lecture. L’évaluation est affichée sous la forme d’une étoile avec un chiffre. L’étoile sera numérotée de 1 à 5, indiquant ainsi l’évaluation actuelle de ce contenu. Si le contenu n’est pas évalué, l’étoile sera numérotée à zéro.

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



Vous pouvez également affecter une valeur de classement à un élément multimédia par le biais de l’interface utilisateur dans le lecteur Windows Media 10,1 mobile, et la prochaine fois que l’appareil se synchronise avec un ordinateur, la nouvelle valeur d’évaluation est propagée à cet élément multimédia s’il réside dans la bibliothèque du lecteur Windows Media 10.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence d’apparence**](skin-reference.md)
</dt> </dl>

 

 




