---
title: Classe Win32_RdvhManagement
description: Décrit un service de gestion d’hôte virtuel Bureau à distance (RDVH).
ms.assetid: 2a81786c-e772-4596-9846-a46828f9b48b
ms.tgt_platform: multiple
keywords:
- Win32_RdvhManagement de la classe Services Bureau à distance
- Win32_RdvhManagement de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RdvhManagement
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01e2cde81173035d00587782dc45d9ddeb66fcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511947"
---
# <a name="win32_rdvhmanagement-class"></a>\_Classe RdvhManagement Win32

Décrit un service de gestion d’hôte virtuel Bureau à distance (RDVH).

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_RdvhManagement
{
};
```

## <a name="members"></a>Membres

La classe **Win32 \_ RdvhManagement** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

La classe **Win32 \_ RdvhManagement** possède ces méthodes.



| Méthode                                                                                  | Description                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RdvCreateUserDiskTemplate**](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | Crée un modèle de disque utilisateur de taille maximale spécifiée et à l’emplacement spécifié. Tous les disques utilisateur créés auront des tailles maximales correspondant à la taille maximale du modèle.<br/> |
| [**RdvMigrateVmToDifferentHost**](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | Lance une migration dynamique de machine virtuelle dans des scénarios VDI<br/>                                                                                               |
| [**RdvCopyBaseVmLocally**](rdvcopybasevmlocally-win32-rdvhmanagement.md)               | Copie l’emplacement de la machine virtuelle de base localement sur le serveur de Hôte de virtualisation des services Bureau à distance<br/>                                                                                                           |
| [**RdvCreateUserDiskTemplate**](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | Crée un modèle de disque utilisateur de taille maximale spécifiée et à l’emplacement spécifié. Tous les disques utilisateur créés auront des tailles maximales correspondant à la taille maximale du modèle.<br/> |
| [**RdvMigrateVmToDifferentHost**](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | Lance une migration dynamique de machine virtuelle dans des scénarios VDI.<br/>                                                                                              |
| [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md)             | Définit les autorisations dans la machine virtuelle pour l’appelant<br/>                                                                                                                        |
| [**RdvUndoVMPermissions**](rdvundovmpermissions-win32-rdvhmanagement.md)               | Restaure les autorisations dans la machine virtuelle définie par RdvSetupVMPermissions<br/>                                                                                                       |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                             |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

 





