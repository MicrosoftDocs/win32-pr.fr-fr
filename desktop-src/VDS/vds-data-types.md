---
description: Les types de données pris en charge par VDS définissent les valeurs de retour de fonction, les paramètres de fonction et les membres de structure. Les types de données définissent la taille et la signification de ces éléments.
ms.assetid: f17e8c7e-e3cb-49ca-9060-2299dda55770
title: Types de données VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83a0f3586cb73b823feb6b41990d1f305056a23f9ac0e47ef8fbfc1e4853267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007929"
---
# <a name="vds-data-types"></a>Types de données VDS

\[à partir de Windows 8 et Windows Server 2012, l’interface COM du [Service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion des Stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Les types de données pris en charge par VDS définissent les valeurs de retour de fonction, les paramètres de fonction et les membres de structure. Les types de données définissent la taille et la signification de ces éléments.



| Type de données                                                                                      | Description                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**\_ID d’objet VDS \_**<br/> | ID de l’objet VDS. Il n’est pas garanti que ces valeurs soient uniques entre les redémarrages. <br/> Ce type est déclaré dans VDS. h (VdsHwPrv. h pour les fournisseurs de matériel) en tant que GUID. <br/> |
| <span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**\_ID de chemin VDS \_**<br/>       | ID de chemin d’accès VDS pour MPIO (Multipath I/O). <br/> Ce type est déclaré dans VDS. h (VdsHwPrv. h pour les fournisseurs de matériel) en tant que UINT64.<br/>                                      |



 

 

