---
title: Toucher la couleur RVB
description: Toucher la couleur RVB
ms.assetid: b71a0a66-11aa-4a21-b78a-3bd90f80a428
keywords:
- Apparences mobiles du lecteur Windows Media, couleurs de bouton
- apparences, couleurs de bouton
- informations de référence sur les apparences, les boutons
- boutons dans les apparences, couleurs
- Référence des couleurs pour les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c69863c4197702383f729c8d7e8d30d3cb52bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512679"
---
# <a name="hit-rgb-color"></a>Toucher la couleur RVB

Si vous utilisez des boutons de région (PushHit, ToggleHit et 2PushHit), vous devez définir la couleur qui sera utilisée par le lecteur Windows Media pour déterminer la zone d’accès de votre bouton. Cette valeur doit être spécifiée à l’aide de trois entiers positifs séparés par des virgules. Ces entiers représentent la quantité de rouge, de vert et de bleu pour une image bitmap, et sont comprises entre 0 et 255.

> [!Note]  
> Les types de boutons sont déconseillés dans les habillages pour Windows Media Player 10 mobile ou version ultérieure.

 

Vous pouvez utiliser n’importe quelle couleur pour les valeurs, mais assurez-vous que chaque bouton de région que vous définissez a une couleur unique dans le fichier image de la région et que la valeur de couleur que vous définissez ici comme nombre correspond à la couleur réelle utilisée dans l’image de la région.

Le tableau suivant répertorie les couleurs typiques que vous pouvez utiliser.



| Valeur       | Description |
|-------------|-------------|
| 0, 0, 0       | Noir       |
| 255 255 255 | Blancs       |
| 255, 0, 0     | Rouge         |
| 0255, 0     | Vert       |
| 0, 0255     | Bleu        |



 

Si vous n’utilisez pas de boutons de région, vous devez entrer les éléments suivants :


```C++
0,0,0

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Boutons**](buttons.md)
</dt> </dl>

 

 




