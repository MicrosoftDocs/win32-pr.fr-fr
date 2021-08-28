---
description: Si ce bit est défini, la boîte de dialogue appelle régulièrement le programme d’installation.
ms.assetid: 7798cb50-72e4-4530-bf06-1927dd963a01
title: TrackDiskSpace bit de style de boîte de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd8e12a77f0b7e67bd82e094953a2bacd8204d93b444dc6bd1dc378602e67809
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810569"
---
# <a name="trackdiskspace-dialog-style-bit"></a>TrackDiskSpace bit de style de boîte de dialogue

Si ce bit est défini, la boîte de dialogue appelle régulièrement le programme d’installation. Si la propriété change, elle avertit les contrôles sur la boîte de dialogue. Ce style peut être utilisé s’il existe un contrôle sur la boîte de dialogue indiquant l’espace disque. Si l’utilisateur bascule vers une autre application, ajoute ou supprime des fichiers, ou modifie l’espace disque disponible, vous pouvez implémenter rapidement la modification à l’aide de ce style.

Toute boîte de dialogue reposant sur la propriété [**OutOfDiskSpace**](outofdiskspace.md) pour déterminer s’il faut afficher une boîte de dialogue doit définir le bit de style de la boîte de dialogue TrackDiskSpace pour la boîte de dialogue afin de mettre à jour dynamiquement l’espace sur les volumes cibles.

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                                |
|---------|-------------|-----------------------------------------|
| 32      | 0x00000020  | **msidbDialogAttributesTrackDiskSpace** |



 

 

 



