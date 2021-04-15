---
description: Interfaces utilisées avec les quotas de disque.
ms.assetid: 422d93d9-f4aa-428d-94c1-fdf2dcf4c974
title: Interfaces de quota de disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bbcd4240a6a5910942aad71c7ea080da40918a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485624"
---
# <a name="disk-quota-interfaces"></a>Interfaces de quota de disque

Les interfaces suivantes sont utilisées avec les quotas de disque.



| Interface                                          | Description                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IDiskQuotaControl**](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)     | Contrôle les fonctionnalités de quota de disque d’un volume de système de fichiers NTFS unique.<br/>                             |
| [**IDiskQuotaEvents**](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)       | Reçoit des notifications d’événements liés au quota.<br/>                                                         |
| [**IDiskQuotaUser**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)           | Représente une entrée de quota d’utilisateur unique dans le fichier d’informations de quota de volume.<br/>                          |
| [**IDiskQuotaUserBatch**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch) | Ajoute plusieurs objets utilisateur de quota à un conteneur qui est ensuite envoyé pour la mise à jour en un seul appel.<br/> |
| [**IEnumDiskQuotaUsers**](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers) | Énumère les entrées de quota utilisateur sur le volume.<br/>                                                        |



 

 

