---
description: Contient une liste des ordinateurs serveurs dans le cluster d’applications. Il contient un objet pour chaque serveur.
ms.assetid: 8722080a-cf95-4c29-9eb7-99c6df93611f
title: Collection ApplicationCluster
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationCluster
api_type:
- COM
api_location: ''
ms.openlocfilehash: 00a54f5c79bcbaf4ef61b130db556fc27f264101
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110566"
---
# <a name="applicationcluster-collection"></a>Collection ApplicationCluster

Contient une liste des ordinateurs serveurs dans le cluster d’applications. Il contient un objet pour chaque serveur. Il s’agit d’une collection de niveau supérieur.

Le cluster d’applications est défini dans le cadre du service d’équilibrage de charge des composants (CLB). Pour l’utilisation de la collection de clusters d’applications, le service CLB doit être installé sur l’ordinateur.

Vous désignez un routeur dans le cluster d’applications à l’aide de la propriété IsRouter sur l’objet de collection [**LocalComputer**](localcomputer.md) , et vous désignez qu’un composant donné doit faire l’objet d’un équilibrage de charge avec la propriété LoadBalancingSupported sur un objet de collection de [**composants**](components.md) .

Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membres

La collection **ApplicationCluster** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Vous pouvez accéder à cette collection à partir des regroupements suivants :

-   [**Causes**](root.md)

## <a name="properties"></a>Propriétés

Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :

-   [Nom](#name)

### <a name="name"></a>Nom



| Entrée | Valeur |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | Nom du serveur. Les espaces supplémentaires au début et à la fin de la chaîne sont supprimés. Cette propriété est retournée lorsque la méthode de propriété [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection. |
| Accès         | WriteOnce                                                                                                                                                                                                                                                            |
| Type           | String                                                                                                                                                                                                                                                               |
| Valeur par défaut        | « Nouvel ordinateur »                                                                                                                                                                                                                                                       |
| Système minimal | Windows 2000                                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
