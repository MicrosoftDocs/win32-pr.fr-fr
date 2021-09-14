---
description: Liste de certains des codes de retour possibles pour les méthodes et les fonctions.
ms.assetid: 391b56a1-d0aa-4d35-8dba-cf7de66513d8
title: S_PRESENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6cd860fcc8268bf2b63a9498b9960da359ca210
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916643"
---
# <a name="s_present"></a>\_présente

Liste de certains des codes de retour possibles pour les méthodes et les fonctions.



| \#définition                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_OK                     | L’appareil s’exécute normalement et peut être utilisé pour le rendu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \_bloqués présente \_      | La zone de présentation est bloqués. L’occlusion signifie que la fenêtre de présentation est réduite ou qu’un autre périphérique est passé en mode plein écran sur le même moniteur que la fenêtre de présentation et que la fenêtre de présentation est entièrement sur ce moniteur. L’occlusion ne se produira pas si la zone cliente est couverte par une autre fenêtre.<br/> Les applications bloqués peuvent continuer le rendu et tous les appels échouent, mais la fenêtre de présentation bloqués ne sera pas mise à jour. De préférence, l’application doit arrêter le rendu dans la fenêtre de présentation à l’aide de l’appareil et continuer l’appel de [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) jusqu’à ce que la valeur de l’appel de la \_ méthode s OK ou du \_ \_ mode actuel \_<br/> |
| le \_ mode actuel des S est \_ \_ modifié | Le mode d’affichage du Bureau a été modifié. L’application peut continuer le rendu, mais il peut y avoir une conversion/étirement de couleurs. Choisissez un format de mémoire tampon d’arrière-plan similaire au mode d’affichage actuel et appelez Reset pour recréer les chaînes de permutation. L’appareil restera dans cet État après l’appel d’une réinitialisation.                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Les autres codes d’erreur sont contenus dans [D3DERR](d3derr.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




