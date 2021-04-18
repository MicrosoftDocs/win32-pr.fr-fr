---
description: Les propriétés exposées pour la collection WOWLegacyServers sont destinées à être identiques à la collection LegacyServers, à ceci près que la collection WOWLegacyServers est tirée du Registre 32 bits sur les ordinateurs 64 bits.
ms.assetid: 72380276-214c-4f12-b575-deb975d846d3
title: Collection WOWLegacyServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWLegacyServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: cf417193ea4cea861f585068d139a855f80242a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536312"
---
# <a name="wowlegacyservers-collection"></a>Collection WOWLegacyServers

Les propriétés exposées pour la collection **WOWLegacyServers** sont destinées à être identiques à la collection [**LegacyServers**](legacyservers.md) , à ceci près que la collection **WOWLegacyServers** est tirée du registre 32 bits sur les ordinateurs 64 bits.

Cette collection ne prend pas en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **WOWLegacyServers** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

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

 

 
