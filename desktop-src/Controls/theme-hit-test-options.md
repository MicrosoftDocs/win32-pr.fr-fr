---
title: Options de test de positionnement
description: Cette section répertorie les valeurs d’option utilisées avec le paramètre dwOptions de la fonction HitTestThemeBackground. Pour obtenir la liste des valeurs retournées lorsque vous spécifiez l’une de ces options, consultez valeurs de retour de test de positionnement.
ms.assetid: a0d5c6c8-bb50-46e1-98ae-2374842344c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 638a7aaca83c658ad852b195cdb9514210a14c16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115998"
---
# <a name="hit-test-options"></a>Options de test de positionnement

Cette section répertorie les valeurs d’option utilisées avec le paramètre *dwOptions* de la fonction [**HitTestThemeBackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-hittestthemebackground) . Pour obtenir la liste des valeurs retournées lorsque vous spécifiez l’une de ces options, consultez [valeurs de retour de test de positionnement](theme-hit-test-retval.md).

## <a name="option-values"></a>Valeurs d’option

Le tableau suivant répertorie les options de test de positionnement.



| Option                       | Valeur                                                                                                                    | Description                                                                                                                                                                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HTTB \_ BACKGROUNDSEG          | 0x00000000                                                                                                               | Option de test de positionnement du segment d’arrière-plan du thème.                                                                                                                                           |
| HTTB \_ FIXEDBORDER            | 0x00000002                                                                                                               | Option de test de positionnement à bordure fixe.                                                                                                                                                       |
| \_légende HTTB                | 0x00000004                                                                                                               | Option de test de positionnement de légende.                                                                                                                                                            |
| HTTB \_ RESIZINGBORDER         | (HTTB \_ RESIZINGBORDER \_ gauche \| HTTB \_ RESIZINGBORDER \_ haut \| HTTB \_ RESIZINGBORDER \_ droite \| HTTB \_ RESIZINGBORDER \_ Bas) | Redimensionnement des options de test d’atteinte de bordure.                                                                                                                                                   |
| HTTB \_ RESIZINGBORDER \_ gauche   | 0x00000010                                                                                                               | Redimensionnement de l’option de test d’atteinte de bordure gauche.                                                                                                                                               |
| HTTB \_ RESIZINGBORDER \_ Top    | 0x00000020                                                                                                               | Redimensionnement de l’option de test d’atteinte de bordure supérieure.                                                                                                                                                |
| HTTB \_ RESIZINGBORDER \_ Right  | 0x00000040                                                                                                               | Redimensionnement de l’option de test d’atteinte à la bordure droite.                                                                                                                                              |
| HTTB \_ RESIZINGBORDER \_ bas | 0x00000080                                                                                                               | Redimensionnement de l’option de test d’atteinte de bordure inférieure.                                                                                                                                             |
| HTTB \_ SIZINGTEMPLATE         | 0x00000100                                                                                                               | La bordure de redimensionnement est spécifiée en tant que modèle, pas seulement les bords de la fenêtre. Cette option s’exclut mutuellement avec HTTB \_ SYSTEMSIZINGMARGINS ; HTTB \_ SIZINGTEMPLATE est prioritaire.         |
| HTTB \_ SYSTEMSIZINGMARGINS    | 0x00000200                                                                                                               | Utilise la largeur de bordure de redimensionnement du système plutôt que les marges de contenu de style visuel. Cette option s’exclut mutuellement avec HTTB \_ SIZINGTEMPLATE ; HTTB \_ SIZINGTEMPLATE est prioritaire. |



 

 

 




