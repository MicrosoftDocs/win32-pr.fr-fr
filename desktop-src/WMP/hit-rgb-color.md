---
title: Toucher la couleur RVB
description: Toucher la couleur RVB
ms.assetid: b71a0a66-11aa-4a21-b78a-3bd90f80a428
keywords:
- Lecteur Windows Media Skins mobiles, couleurs de bouton
- apparences, couleurs de bouton
- informations de référence sur les apparences, les boutons
- boutons dans les apparences, couleurs
- Référence des couleurs pour les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3c33e4b7eb2af9c1305a6644559e162c581c27b6b11e5b709376663082042d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390869"
---
# <a name="hit-rgb-color"></a>Toucher la couleur RVB

si vous utilisez des boutons de région (PushHit, ToggleHit et 2PushHit), vous devez définir la couleur que Lecteur Windows Media utilisera pour déterminer la zone d’accès de votre bouton. Cette valeur doit être spécifiée à l’aide de trois entiers positifs séparés par des virgules. Ces entiers représentent la quantité de rouge, de vert et de bleu pour une image bitmap, et sont comprises entre 0 et 255.

> [!Note]  
> les types de boutons sont déconseillés dans les habillages pour Lecteur Windows Media 10 Mobile ou version ultérieure.

 

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

 

 




