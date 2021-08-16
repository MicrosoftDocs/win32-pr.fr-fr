---
description: Représente un service qui contrôle la migration des systèmes virtuels entre les systèmes hôtes. Cette classe vérifie également si une migration en attente est susceptible de se dérouler correctement.
ms.assetid: 28948a36-3b92-4d52-9a48-aaa155e7fad5
title: Classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44b034c5b91eb024bdbcde0b0d835ba12f0367bedc6dbd9c5c2d52dca1029f87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068539"
---
# <a name="cim_virtualsystemmigrationservice-class"></a>\_Classe CIM VirtualSystemMigrationService

Représente un service qui contrôle la migration des systèmes virtuels entre les systèmes hôtes. Cette classe vérifie également si une migration en attente est susceptible de se dérouler correctement.

## <a name="syntax"></a>Syntaxe

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationService : CIM_Service
{
};
```

## <a name="members"></a>Membres

La classe **CIM \_ VirtualSystemMigrationService** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

La classe **CIM \_ VirtualSystemMigrationService** possède ces méthodes.



| Méthode                                                                                                                     | Description                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**CheckVirtualSystemIsMigratableToHost**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md)     | Vérifie si la migration d’un système virtuel en attente vers un ordinateur hôte est susceptible d’être effectuée.<br/>   |
| [**CheckVirtualSystemIsMigratableToSystem**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletosystem.md) | Vérifie si la migration d’un système virtuel en attente vers un système est susceptible d’être effectuée.<br/> |
| [**MigrateVirtualSystemToHost**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md)                         | Migre un système virtuel vers un ordinateur hôte cible.<br/>                                           |
| [**MigrateVirtualSystemToSystem**](cim-virtualsystemmigrationservice-migratevirtualsystemtosystem.md)                     | Migre un système virtuel vers le système cible.<br/>                                           |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Service CIM**](cim-service.md)
</dt> </dl>

 

 




