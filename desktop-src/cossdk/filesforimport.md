---
description: Récupère des informations pour les applications qui sont importées.
ms.assetid: 9ed4bc3f-3490-4c36-ba94-bc803886a4d2
title: Collection FilesForImport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilesForImport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8e7ba3b0bd44cf2f6bb40ecf89f86dd68c21cf3c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403667"
---
# <a name="filesforimport-collection"></a>Collection FilesForImport

Récupère des informations pour les applications qui sont importées.

Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **FilesForImport** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Vous pouvez accéder à cette collection à partir des regroupements suivants :

-   [**Causes**](root.md)

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [ApplicationFileName](#applicationfilename)
-   [ApplicationName](#applicationname)
-   [Description](#partitiondescription)
-   [FileName](#applicationfilename)
-   [HasUsers](#hasusers)
-   [Proxy](#isproxy)
-   [IsService](#isservice)
-   [PartitionDescription](#partitiondescription)
-   [PartitionID](#partitionid)
-   [PartitionName](#partitionname)

### <a name="applicationfilename"></a>ApplicationFileName



| Entrée | Valeur |
|----------------|------------------------------------------------------------------------------|
| Description    | Nom du fichier MSI qui contient l’application qui peut être importée. |
| Access         | Lecture seule                                                                     |
| Type           | String                                                                       |
| Valeur par défaut        | N/A                                                                          |
| Système minimal | Windows XP                                                                   |



 

### <a name="applicationname"></a>ApplicationName



| Entrée | Valeur |
|----------------|------------------------------|
| Description    | Le nom de l’application. |
| Access         | Lecture seule                     |
| Type           | String                       |
| Valeur par défaut        | ""                           |
| Système minimal | Windows XP                   |



 

### <a name="description"></a>Description



| Entrée | Valeur |
|----------------|-----------------------------------|
| Description    | Description de l’application. |
| Access         | Lecture seule                          |
| Type           | String                            |
| Valeur par défaut        | ""                                |
| Système minimal | Windows XP                        |



 

### <a name="filename"></a>FileName



| Entrée | Valeur |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom de la DLL ou du fichier EXE qui contient l’application. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Access         | Lecture seule                                                                                                                                                                                                                              |
| Type           | String                                                                                                                                                                                                                                |
| Valeur par défaut        | ""                                                                                                                                                                                                                                    |
| Système minimal | Windows XP                                                                                                                                                                                                                            |



 

### <a name="hasusers"></a>HasUsers



| Entrée | Valeur |
|----------------|--------------------------------------------------|
| Description    | Indique si l’application possède des utilisateurs. |
| Access         | Lecture seule                                         |
| Type           | Bool                                             |
| Default        | False                                            |
| Système minimal | Windows XP                                       |



 

### <a name="isproxy"></a>Proxy



| Entrée | Valeur |
|----------------|-----------------------------------------------|
| Description    | Indique si l’application est un proxy. |
| Access         | Lecture seule                                      |
| Type           | Bool                                          |
| Default        | False                                         |
| Système minimal | Windows XP                                    |



 

### <a name="isservice"></a>IsService



| Entrée | Valeur |
|----------------|-------------------------------------------------|
| Description    | Indique si l’application est un service. |
| Access         | Lecture seule                                        |
| Type           | Bool                                            |
| Default        | False                                           |
| Système minimal | Windows XP                                      |



 

### <a name="partitiondescription"></a>PartitionDescription



| Entrée | Valeur |
|----------------|-----------------------------------------------|
| Description    | Description de la partition de l’application. |
| Access         | Lecture seule                                      |
| Type           | String                                        |
| Valeur par défaut        | ""                                            |
| Système minimal | Windows Server 2003                           |



 

### <a name="partitionid"></a>PartitionID



| Entrée | Valeur |
|----------------|------------------------------------------|
| Description    | GUID de la partition de l’application. |
| Access         | Lecture seule                                 |
| Type           | String                                   |
| Valeur par défaut        | ""                                       |
| Système minimal | Windows Server 2003                      |



 

### <a name="partitionname"></a>PartitionName



| Entrée | Valeur |
|----------------|------------------------------------------|
| Description    | Nom de la partition de l’application. |
| Access         | Lecture seule                                 |
| Type           | String                                   |
| Valeur par défaut        | ""                                       |
| Système minimal | Windows Server 2003                      |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
