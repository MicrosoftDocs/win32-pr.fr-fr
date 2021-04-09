---
description: Gère la configuration des pools de ressources à l’aide de travaux.
ms.assetid: cc0f0236-2335-4dd9-9132-51b3e6b9fcf4
title: Classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e8dbbce21f7749b7f436e2f49acb7ce6c7340faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862865"
---
# <a name="cim_resourcepoolconfigurationservice-class"></a>\_Classe CIM ResourcePoolConfigurationService

Gère la configuration des pools de ressources à l’aide de travaux.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_ResourcePoolConfigurationService : CIM_Service
{
};
```

## <a name="members"></a>Membres

La classe **CIM \_ ResourcePoolConfigurationService** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

La classe **CIM \_ ResourcePoolConfigurationService** possède ces méthodes.



| Méthode                                                                                                          | Description                                                                   |
|:----------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**AddResourcesToResourcePool**](cim-resourcepoolconfigurationservice-addresourcestoresourcepool.md)           | Démarre un travail pour ajouter des ressources à un pool de ressources.<br/>                  |
| [**ChangeParentResourcePool**](cim-resourcepoolconfigurationservice-changeparentresourcepool.md)               | Démarrer un travail pour modifier le pool de ressources parent d’un pool de ressources.<br/> |
| [**CreateChildResourcePool**](cim-resourcepoolconfigurationservice-createchildresourcepool.md)                 | Démarrer un travail pour créer un pool de ressources à partir d’un pool de ressources parent.<br/> |
| [**CreateResourcePool**](cim-resourcepoolconfigurationservice-createresourcepool.md)                           | Démarre un travail pour créer un pool de ressources racine.<br/>                       |
| [**DeleteResourcePool**](cim-resourcepoolconfigurationservice-deleteresourcepool.md)                           | Démarrer un travail pour supprimer un pool de ressources.<br/>                             |
| [**RemoveResourcesFromResourcePool**](cim-resourcepoolconfigurationservice-removeresourcesfromresourcepool.md) | Démarre un travail pour supprimer des ressources d’un pool de ressources.<br/>             |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Service CIM**](cim-service.md)
</dt> </dl>

 

 




