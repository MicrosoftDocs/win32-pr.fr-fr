---
title: Classe Win32_RDMSManagementData
description: Synchronise les données de publication pour les services de gestion de Bureau à distance (RDMS).
ms.assetid: 17f06294-6580-4297-9301-f88314db7775
ms.tgt_platform: multiple
keywords:
- Win32_RDMSManagementData de la classe Services Bureau à distance
- Win32_RDMSManagementData de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dddf2a73673e886456eb43bfbd2cefc72250cc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032452"
---
# <a name="win32_rdmsmanagementdata-class"></a>\_Classe RDMSManagementData Win32

Synchronise les données de publication pour les services de gestion de Bureau à distance (RDMS).

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSManagementData
{
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ RDMSManagementData** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ RDMSManagementData** possède ces méthodes.



| Méthode                                                                                        | Description                                                            |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**SynchronizeAllPublishingData**](synchronizeallpublishingdata-win32-rdmsmanagementdata.md) | Synchronise toutes les données de publication pour les RDM.<br/>                  |
| [**SynchronizePublishingData**](synchronizepublishingdata-win32-rdmsmanagementdata.md)       | Synchronise le jeu de données de publication spécifié pour les RDMS.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                              |
| Espace de noms<br/>                | Racine \\ cimv2 cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fournisseur de services de gestion Bureau à distance](rdms-api-reference.md)
</dt> </dl>

 

 





