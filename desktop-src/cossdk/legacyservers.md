---
description: Identique à la collection InprocServers, à ceci près que cette collection comprend également des serveurs locaux.
ms.assetid: b185f568-ec97-4710-b744-5d69e71d6f60
title: Collection LegacyServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3968b3cb7068f994d3ff44e7182add2b1e3cb7a44c0d73019cf583a0e8c7f70f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306357"
---
# <a name="legacyservers-collection"></a>Collection LegacyServers

Identique à la collection [**InprocServers**](inprocservers.md) , à ceci près que cette collection comprend également des serveurs locaux.

Cette collection ne prend pas en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **LegacyServers** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Vous pouvez accéder à cette collection à partir des regroupements suivants :

-   [**Causes**](root.md)

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [NomClasse](#classname)
-   [IDENTIFICATEUR](#clsid)
-   [InprocServer32](#inprocserver32)
-   [LocalServer32](#localserver32)
-   [ProgID](#progid)

### <a name="classname"></a>ClassName



| Entrée | Valeur |
|----------------|------------------------|
| Description    | Nom de la classe. |
| Accès         | Lecture seule               |
| Type           | String                 |
| Valeur par défaut        | N/A                    |
| Système minimal | Windows XP             |



 

### <a name="clsid"></a>CLSID



| Entrée | Valeur |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | GUID du composant. Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection. |
| Accès         | Lecture seule                                                                                                                                                  |
| Type           | String                                                                                                                                                    |
| Valeur par défaut        | N/A                                                                                                                                                       |
| Système minimal | Windows XP                                                                                                                                                |



 

### <a name="inprocserver32"></a>InprocServer32



| Entrée | Valeur |
|----------------|----------------------------------|
| Description    | Chemin d’accès du fichier pour le composant. |
| Accès         | Lecture seule                         |
| Type           | String                           |
| Valeur par défaut        | N/A                              |
| Système minimal | Windows XP                       |



 

### <a name="localserver32"></a>LocalServer32



| Entrée | Valeur |
|----------------|---------------------------------------------------------------|
| Description    | Spécifie le chemin d’accès complet à une application serveur locale 32 bits. |
| Accès         | Lecture seule                                                      |
| Type           | String                                                        |
| Valeur par défaut        | N/A                                                           |
| Système minimal | Windows XP                                                    |



 

### <a name="progid"></a>ProgID



| Entrée | Valeur |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom identifiant le composant. Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Accès         | Lecture seule                                                                                                                                                            |
| Type           | String                                                                                                                                                              |
| Valeur par défaut        | N/A                                                                                                                                                                 |
| Système minimal | Windows XP                                                                                                                                                          |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
