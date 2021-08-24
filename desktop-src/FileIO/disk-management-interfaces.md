---
description: Interfaces utilisées dans la gestion des disques.
ms.assetid: c1f79e2e-834b-41dc-a15f-6dd1034d021b
title: Interfaces de gestion des disques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a7314de976b1a5228a8b537da5d09be3df66936ed57915d86d78b0a84c4361e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823209"
---
# <a name="disk-management-interfaces"></a>Interfaces de gestion des disques

Les interfaces suivantes sont utilisées dans gestion des disques.

## <a name="in-this-section"></a>Dans cette section



| Interface                                                     | Description                                                                                                    |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IDiskQuotaControl**](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)<br/>     | Contrôle les fonctionnalités de quota de disque d’un volume de système de fichiers NTFS unique.<br/>                             |
| [**IDiskQuotaEvents**](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)<br/>       | Reçoit des notifications d’événements liés au quota.<br/>                                                         |
| [**IDiskQuotaUser**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)<br/>           | Représente une entrée de quota d’utilisateur unique dans le fichier d’informations de quota de volume.<br/>                          |
| [**IDiskQuotaUserBatch**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch)<br/> | Ajoute plusieurs objets utilisateur de quota à un conteneur qui est ensuite envoyé pour la mise à jour en un seul appel.<br/> |
| [**IEnumDiskQuotaUsers**](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers)<br/> | Énumère les entrées de quota utilisateur sur le volume.<br/>                                                        |



 

 

