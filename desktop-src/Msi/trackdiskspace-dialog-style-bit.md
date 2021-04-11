---
description: Si ce bit est défini, la boîte de dialogue appelle régulièrement le programme d’installation.
ms.assetid: 7798cb50-72e4-4530-bf06-1927dd963a01
title: TrackDiskSpace bit de style de boîte de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eab0cf234071ace41432e20a598b38fb1fc431e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111994"
---
# <a name="trackdiskspace-dialog-style-bit"></a>TrackDiskSpace bit de style de boîte de dialogue

Si ce bit est défini, la boîte de dialogue appelle régulièrement le programme d’installation. Si la propriété change, elle avertit les contrôles sur la boîte de dialogue. Ce style peut être utilisé s’il existe un contrôle sur la boîte de dialogue indiquant l’espace disque. Si l’utilisateur bascule vers une autre application, ajoute ou supprime des fichiers, ou modifie l’espace disque disponible, vous pouvez implémenter rapidement la modification à l’aide de ce style.

Toute boîte de dialogue reposant sur la propriété [**OutOfDiskSpace**](outofdiskspace.md) pour déterminer s’il faut afficher une boîte de dialogue doit définir le bit de style de la boîte de dialogue TrackDiskSpace pour la boîte de dialogue afin de mettre à jour dynamiquement l’espace sur les volumes cibles.

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                                |
|---------|-------------|-----------------------------------------|
| 32      | 0x00000020  | **msidbDialogAttributesTrackDiskSpace** |



 

 

 



