---
description: Service pour créer, détruire et exporter des points de référence.
ms.assetid: 88a76319-b5a7-44a3-8a31-83ade999b255
title: Classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6ba56fcb75a177521b8f3ea3ae0675cfdd8a8dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543673"
---
# <a name="msvm_collectionreferencepointservice-class"></a>MSVM \_ CollectionReferencePointService, classe

Service pour créer, détruire et exporter des points de référence

de collections de systèmes virtuels.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointService : CIM_Service
{
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ CollectionReferencePointService** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

La classe **MSVM \_ CollectionReferencePointService** possède ces méthodes.



| Méthode                                                                                      | Description                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateReferencePoint**](msvm-collectionreferencepointservice-createreferencepoint.md)   | Crée un point de référence d’une collection de systèmes virtuels.<br/>                                                                                                                                            |
| [**DestroyReferencePoint**](msvm-collectionreferencepointservice-destroyreferencepoint.md) | Détruit une collection de points de référence existante. Cette méthode peut, en tant qu’effet secondaire, détruire d’autres points de référence qui dépendent de la collection de points de référence affectés.<br/>                      |
| [**ExportReferencePoint**](msvm-collectionreferencepointservice-exportreferencepoint.md)   | Exporte une collection de points de référence dans un fichier. La collection de points de référence, ses paramètres de configuration associés et les paramètres de ressources qui lui sont associés sont conservés dans le fichier résultant.<br/> |
| [**RemoveAssociatedData**](msvm-collectionreferencepointservice-removeassociateddata.md)   | Supprime le journal de données associé au point de référence.<br/>                                                                                                                                            |



 

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

 

 




