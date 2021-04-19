---
description: Les structures suivantes sont définies dans l’API de cliché instantané des volumes.
ms.assetid: 20cf12e4-4611-4e39-9f6f-e29f15e58b36
title: Structures de l’API de cliché instantané des volumes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1bb699277faa30c6a570203cd820d552cc9f1b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514828"
---
# <a name="volume-shadow-copy-api-structures"></a>Structures de l’API de cliché instantané des volumes

Les structures suivantes sont définies dans l’API de cliché instantané des volumes.



| Structure                                                           | Description                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_COMPONENTINFO VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)                     | Contient des informations sur un composant donné.                                                                                                                                                                                                                       |
| [**PROP. de la \_ zone diff. VSS \_ \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_area_prop)                 | Décrit les associations entre les volumes sources contenant les données de fichier d’origine et les volumes contenant la zone de stockage des clichés instantanés.                                                                                                                                |
| [**PROP VSS du \_ \_ volume diff \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_volume_prop)             | Décrit un volume de la zone de stockage de clichés instantanés.                                                                                                                                                                                                                        |
| [**PROP de l' \_ objet de gestion VSS \_ \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop)             | Décrit les propriétés d’un volume, d’un volume de stockage de clichés instantanés ou d’une zone de stockage de clichés instantanés.                                                                                                                                                                    |
| [**\_Union d' \_ objets de gestion VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-__midl___midl_itf_vsmgmt_0000_0000_0001)           | Union de structures [**de \_ volume VSS \_ prop**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_prop), [**VSS \_ diff \_ volume \_ prop**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_volume_prop)et [**VSS \_ \_ \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_area_prop) utilisées par la structure prop de l' [**\_ \_ objet \_ de gestion VSS**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop) . |
| [**PROP de l' \_ objet VSS \_**](/windows/desktop/api/Vss/ns-vss-vss_object_prop)                        | Décrit les propriétés d’un fournisseur, d’un volume, d’un cliché instantané ou d’un jeu de clichés instantanés.                                                                                                                                                                                    |
| [**\_Union d’objets VSS \_**](/windows/desktop/api/Vss/ns-vss-__midl___midl_itf_vss_0000_0000_0001)                      | Union de structures [**de \_ capture \_ instantanée VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) et de structures du [**\_ \_ fournisseur VSS**](/windows/desktop/api/Vss/ns-vss-vss_provider_prop) , utilisée par la structure prop de l' [**\_ \_ objet VSS**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) .                                                                    |
| [**\_prop fournisseur \_ VSS**](/windows/desktop/api/Vss/ns-vss-vss_provider_prop)                    | Spécifie les propriétés du fournisseur de clichés instantanés.                                                                                                                                                                                                                          |
| [**\_prop instantané \_ VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)                    | Contient les propriétés d’un cliché instantané ou d’un jeu de clichés instantanés.                                                                                                                                                                                                        |
| [**\_prop du volume VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_prop)                        | Décrit les propriétés d’un volume source de clichés instantanés.                                                                                                                                                                                                            |
| [**\_ \_ informations sur la protection du volume VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info) | Contient des informations sur le niveau de protection des clichés instantanés d’un volume.                                                                                                                                                                                                 |



 

 

 



