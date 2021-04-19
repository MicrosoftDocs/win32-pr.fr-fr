---
description: Service permettant de créer, de détruire et d’exporter la collection de captures instantanées de systèmes virtuels.
ms.assetid: 55a6c7b4-5352-4766-b5b7-6699b1f40b78
title: Classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f9e835ad54773d69fab19861c7a9c417ac7d8a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524571"
---
# <a name="msvm_collectionsnapshotservice-class"></a>MSVM \_ CollectionSnapshotService, classe

Service permettant de créer, de détruire et d’exporter la collection de captures instantanées de systèmes virtuels.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotService : CIM_Service
{
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ CollectionSnapshotService** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

La classe **MSVM \_ CollectionSnapshotService** possède ces méthodes.



| Méthode                                                                                    | Description                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplySnapshot**](msvm-collectionsnapshotservice-applysnapshot.md)                     | Applique une collection d’instantanés à la collection de systèmes d’ordinateurs virtuels.<br/>                                                                                                                                        |
| [**ConvertToReferencePoint**](msvm-collectionsnapshotservice-converttoreferencepoint.md) | Convertit une capture instantanée de collection existante en collection de points de référence. La collection d’instantanés est supprimée en tant qu’effet secondaire. Seuls les instantanés de récupération peuvent être convertis en points de référence.<br/>                      |
| [**CreateSnapshot**](msvm-collectionsnapshotservice-createsnapshot.md)                   | Crée une capture instantanée d’une collection de systèmes virtuels.<br/>                                                                                                                                                                 |
| [**DestroySnapshot**](msvm-collectionsnapshotservice-destroysnapshot.md)                 | Détruisez un instantané existant de la collection de systèmes virtuels. Cette méthode peut, en tant qu’effet secondaire, détruire d’autres instantanés qui dépendent de l’instantané affecté.<br/>                                                   |
| [**Temps**](msvm-collectionsnapshotservice-exportsnapshot.md)                   | Exporte une collection d’instantanés de systèmes d’ordinateurs virtuels dans un fichier. La collection d’instantanés, ses paramètres de configuration associés et les paramètres de ressources qui lui sont associés sont conservés dans le fichier résultant.<br/> |



 

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

 

 




