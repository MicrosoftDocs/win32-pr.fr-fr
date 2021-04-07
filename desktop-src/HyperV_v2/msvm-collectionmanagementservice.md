---
description: Gère les collections sur l’hôte Hyper-V.
ms.assetid: e895217e-352d-4d77-8f1d-7070012e6f60
title: Classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 89d63d9a210f8c1074296620f430117d6203e295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760497"
---
# <a name="msvm_collectionmanagementservice-class"></a>MSVM \_ CollectionManagementService, classe

Gère les collections sur l’hôte Hyper-V.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionManagementService : CIM_Service
{
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ CollectionManagementService** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

La classe **MSVM \_ CollectionManagementService** possède ces méthodes.



| Méthode                                                                          | Description                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddMember**](msvm-collectionmanagementservice-addmember.md)                 | Ajoute le propriété ManagedElement spécifié en tant que membre de l’objet [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) donné.<br/>                                                                                           |
| [**DefineCollection**](msvm-collectionmanagementservice-definecollection.md)   | Crée un nouvel objet [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) .<br/>                                                                                                                                        |
| [**DestroyCollection**](msvm-collectionmanagementservice-destroycollection.md) | Supprime l’objet [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) donné.<br/>                                                                                                                                    |
| [**RemoveMember**](msvm-collectionmanagementservice-removemember.md)           | Supprime le propriété ManagedElement spécifié en tant que membre de l’objet [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) donné.<br/>                                                                                        |
| [**RemoveMemberById**](msvm-collectionmanagementservice-removememberbyid.md)   | Supprime le propriété ManagedElement spécifié en tant que membre de l’élément [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) avec l’identificateur donné. Cela échoue même si l’objet avec cet identificateur n’est pas présent.<br/> |
| [**RenameCollection**](msvm-collectionmanagementservice-renamecollection.md)   | Met à jour le ElementName de l’objet [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) donné.<br/>                                                                                                                    |
| [**StartService**](msvm-collectionmanagementservice-startservice.md)           | démarre le service.<br/>                                                                                                                                                                                                |
| [**StopService**](msvm-collectionmanagementservice-stopservice.md)             | arrête le service.<br/>                                                                                                                                                                                                 |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Service CIM**](cim-service.md)
</dt> </dl>

 

 




