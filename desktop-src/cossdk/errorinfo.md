---
description: Récupère des informations d’erreur étendues concernant les méthodes qui traitent plusieurs objets, tels que remplir et SaveChanges sur l’objet COMAdminCatalogCollection, et les méthodes pour installer, importer ou exporter des applications ou des composants sur l’objet COMAdminCatalog.
ms.assetid: cf612fc4-55dd-4706-8c41-2654ca922b9a
title: ErrorInfo, collection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ErrorInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9953bc1119d7e203936ca7e78048a4083a996ec2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095422"
---
# <a name="errorinfo-collection"></a>ErrorInfo, collection

Récupère des informations d’erreur étendues concernant les méthodes qui traitent plusieurs objets, tels que [**remplir**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) et [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) sur l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , et les méthodes pour installer, importer ou exporter des applications ou des composants sur l’objet [**COMAdminCatalog**](comadmincatalog.md) .

Utilisez la méthode [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) sur un [**COMAdminCatalogCollection**](comadmincatalogcollection.md) pour accéder à la collection **errorInfo** associée à la collection d’origine qui a une erreur.

Vous devez appeler [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) sur **errorInfo** immédiatement après qu’une erreur s’est produite ; dans le cas contraire, les informations sur l’erreur sont perdues.

Cette collection ne prend pas en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **errorInfo** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Vous pouvez accéder à cette collection à partir de chaque collection à l’exception de **errorInfo**, [**InprocServers**](inprocservers.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md), [**root**](root.md)et [**WOWInprocServers**](wowinprocservers.md).

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [ErrorCode](#errorcode)
-   [MajorRef](#majorref)
-   [MinorRef](#minorref)
-   [Nom](#name)

### <a name="errorcode"></a>ErrorCode



| Entrée | Valeur |
|----------------|----------------------------------------|
| Description    | Code d'erreur pour l'objet ou le fichier. |
| Access         | Lecture seule                               |
| Type           | String                                 |
| Default        | None                                   |
| Système minimal | Windows 2000                           |



 

### <a name="majorref"></a>MajorRef



| Entrée | Valeur |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Valeur de la propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) pour l’objet qui contient une erreur. Par exemple, si un appel de [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) pour une collection échoue sur un objet particulier dans la collection, la valeur de la propriété de **clé** pour cet objet est signalée comme valeur MajorRef. Utilisez cette propriété pour examiner l’élément qui ne parvient pas à mettre à jour ou pour trouver le composant ou la DLL dont l’installation échoue. |
| Access         | Lecture seule                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Type           | String                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Default        | None                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Système minimal | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="minorref"></a>MinorRef



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Spécification précise de l’élément qui a une erreur, telle qu’un nom de propriété. Si plusieurs erreurs se produisent ou dans des contextes où cela ne s’applique pas, MinorRef n’est &lt; pas valide &gt; . |
| Access         | Lecture seule                                                                                                                                                                          |
| Type           | String                                                                                                                                                                            |
| Default        | None                                                                                                                                                                              |
| Système minimal | Windows 2000                                                                                                                                                                      |



 

### <a name="name"></a>Nom



| Entrée | Valeur |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom de l’objet ou du fichier qui contient une erreur. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Access         | Lecture seule                                                                                                                                                                                                                 |
| Type           | String                                                                                                                                                                                                                   |
| Default        | None                                                                                                                                                                                                                     |
| Système minimal | Windows 2000                                                                                                                                                                                                             |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
