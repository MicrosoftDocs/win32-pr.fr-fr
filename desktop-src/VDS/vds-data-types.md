---
description: Les types de données pris en charge par VDS définissent les valeurs de retour de fonction, les paramètres de fonction et les membres de structure. Les types de données définissent la taille et la signification de ces éléments.
ms.assetid: f17e8c7e-e3cb-49ca-9060-2299dda55770
title: Types de données VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a868606110d9cf1c3cad5c3036789d041a5d86c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541995"
---
# <a name="vds-data-types"></a>Types de données VDS

\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Les types de données pris en charge par VDS définissent les valeurs de retour de fonction, les paramètres de fonction et les membres de structure. Les types de données définissent la taille et la signification de ces éléments.



| Type de données                                                                                      | Description                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**\_ID d’objet VDS \_**<br/> | ID de l’objet VDS. Il n’est pas garanti que ces valeurs soient uniques entre les redémarrages. <br/> Ce type est déclaré dans VDS. h (VdsHwPrv. h pour les fournisseurs de matériel) en tant que GUID. <br/> |
| <span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**\_ID de chemin VDS \_**<br/>       | ID de chemin d’accès VDS pour MPIO (Multipath I/O). <br/> Ce type est déclaré dans VDS. h (VdsHwPrv. h pour les fournisseurs de matériel) en tant que UINT64.<br/>                                      |



 

 

