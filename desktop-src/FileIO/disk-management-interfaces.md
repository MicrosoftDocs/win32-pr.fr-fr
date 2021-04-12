---
description: Interfaces utilisées dans la gestion des disques.
ms.assetid: c1f79e2e-834b-41dc-a15f-6dd1034d021b
title: Interfaces de gestion des disques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c86881ff3bf6232da68c4cf1539dbbedf87c50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209904"
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



 

 

