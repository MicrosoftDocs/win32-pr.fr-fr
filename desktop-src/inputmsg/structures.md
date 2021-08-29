---
title: Structures (messages d’entrée de pointeur et notifications)
description: Les rubriques de cette section fournissent les spécifications de référence pour les messages d’entrée de pointeur et les structures de notifications.
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114801138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 3bc60fc6a78b248328e2bcc44bd8f598d12bd68cc2ed61d970faeed801f62191
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666112"
---
# <a name="pointer-input-messages-and-notifications-structures"></a>Messages d’entrée de pointeur et structures de notifications

Les rubriques de cette section fournissent les spécifications de référence pour les [messages d’entrée de pointeur et](messages-and-notifications-portal.md) les structures de notifications.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                            | Description                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INPUT_TRANSFORM**](/previous-versions/windows/desktop/api)<br/>                           | Définit la matrice qui représente une transformation sur un consommateur de messages. Cette matrice peut être utilisée pour transformer des données d’entrée de pointeur de coordonnées clientes en coordonnées d’écran, tandis que l’inverse peut être utilisé pour transformer des données d’entrée de pointeur de coordonnées d’écran en coordonnées clientes. <br/>                                                                 |
| [**POINTER_INFO**](/previous-versions/windows/desktop/api)<br/>                          | Contient les informations de pointeur de base communes à tous les types pointeur. Les applications peuvent récupérer ces informations à l’aide des fonctions [**GetPointerInfo**](/previous-versions/windows/desktop/api), [**GetPointerFrameInfo**](/previous-versions/windows/desktop/api), [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) et [**GetPointerFrameInfoHistory**](/previous-versions/windows/desktop/api) . <br/> |
| [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api)<br/>                 | Définit les informations de stylet de base communes à tous les types pointeur. <br/>                                                                                                                                                                                                                                                                                                |
| [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api)<br/>             | Définit les informations tactiles de base communes à tous les types pointeur.<br/>                                                                                                                                                                                                                                                                                               |
| [**TOUCHPREDICTIONPARAMETERS**](/previous-versions/windows/desktop/api)<br/> | Contient des détails d’entrée de matériel qui peuvent être utilisés pour prédire des cibles tactiles et aider à compenser la latence matérielle lors du traitement des entrées tactiles et de mouvement qui contiennent des données de distance et de vélocité.<br/>                                                                                                                                                       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de message d’entrée de pointeur](wmpointer-reference.md)
</dt> </dl>

 

 





