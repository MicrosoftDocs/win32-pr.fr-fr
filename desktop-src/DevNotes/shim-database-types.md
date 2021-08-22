---
description: Représente les types de bases de données de shims principales et personnalisées.
ms.assetid: e893963a-6130-4f65-b925-6f3d292fc86d
title: Types de bases de données shim
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cc36cbb198570618fbd1a6524e4e7c6dc6812fb01bd74fe04cf1bd91b31f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075923"
---
# <a name="shim-database-types"></a>Types de bases de données shim

Représente les types de bases de données de shims principales et personnalisées.



| Constante/valeur                                                                                                                                                                                                                                                | Description                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SDB_DATABASE_MAIN"></span><span id="sdb_database_main"></span><dl> <dt>**Sdb \_ BASE de données \_ principale**</dt> <dt>0x80000000</dt> </dl>                    | Base de données principale. Si cet indicateur n’est pas présent, la base de données est une base de données personnalisée.<br/> |
| <span id="SDB_DATABASE_SHIM"></span><span id="sdb_database_shim"></span><dl> <dt>**Sdb \_ 0x00010000 \_ shim de base de données**</dt> <dt></dt> </dl>                    | La base de données contient des entrées d’application à shim.<br/>                           |
| <span id="SDB_DATABASE_MSI"></span><span id="sdb_database_msi"></span><dl> <dt>**Sdb \_ BASE de données \_ MSI**</dt> <dt>0x00020000</dt> </dl>                       | La base de données contient des entrées MSI.<br/>                                                 |
| <span id="SDB_DATABASE_DRIVERS"></span><span id="sdb_database_drivers"></span><dl> <dt>**Sdb \_ \_Pilotes de base de données**</dt> <dt>0x00040000</dt> </dl>           | La base de données contient des entrées de bloc de pilote.<br/>                                        |
| <span id="SDB_DATABASE_DETAILS"></span><span id="sdb_database_details"></span><dl> <dt>**Sdb \_ \_Détails de la base de données**</dt> <dt>0x00080000</dt> </dl>           | La base de données contient les détails du AppHelp.<br/>                                             |
| <span id="SDB_DATABASE_SP_DETAILS"></span><span id="sdb_database_sp_details"></span><dl> <dt>**Sdb \_ \_ \_ Détails du SP de base de données**</dt> <dt>0x00100000</dt> </dl> | La base de données contient les détails du fournisseur de données SP.<br/>                                          |
| <span id="SDB_DATABASE_RESOURCE"></span><span id="sdb_database_resource"></span><dl> <dt>**Sdb \_ \_Ressource de base de données**</dt> <dt>0x00200000</dt> </dl>        | La DLL de ressource contient les détails du fichier AppHelp.<br/>                                         |
| <span id="SDB_DATABASE_TYPE_MASK"></span><span id="sdb_database_type_mask"></span><dl> <dt>**Sdb \_ \_ \_ Masque de type de base de données**</dt> <dt>0xF02F0000</dt> </dl>    | Masque utilisé pour extraire les informations de la base de données principale.<br/>                                  |
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <dt>**\_shim principal de base de données sdb \_ \_**</dt> </dl>                                                                    | SDB \_ Database \_ shim \| sdb \_ base de données \_ MSI \| sdb base de données \_ \_ principale<br/>                   |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <dt>**fichier \_ \_ MSI principal de la base de données sdb \_**</dt> </dl>                                                                       | SDB \_ base de données \_ MSI \| sdb \_ base de données \_ principale<br/>                                          |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <dt>**\_pilotes principaux de la base de données sdb \_ \_**</dt> </dl>                                                           | SDB \_ Database \_ drivers \| sdb \_ Database \_ main<br/>                                      |
| <span id="SDB_DATABASE_MAIN_DETAILS"></span><span id="sdb_database_main_details"></span><dl> <dt>**\_Détails principaux de la base de données sdb \_ \_**</dt> </dl>                                                           | \_informations de base de données sdb \_ \| sdb \_ base de données \_ principale<br/>                                      |
| <span id="SDB_DATABASE_MAIN_SP_DETAILS"></span><span id="sdb_database_main_sp_details"></span><dl> <dt>**\_Détails du \_ SP principal de la base de données sdb \_ \_**</dt> </dl>                                                 | SDB \_ base de données \_ SP \_ Détails \| sdb \_ base de données \_ principale<br/>                                  |
| <span id="SDB_DATABASE_MAIN_RESOURCE"></span><span id="sdb_database_main_resource"></span><dl> <dt>**\_ressource principale de base de données sdb \_ \_**</dt> </dl>                                                        | SDB \_ Database \_ Resource \| sdb \_ Database \_ main<br/>                                     |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




