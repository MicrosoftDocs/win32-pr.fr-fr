---
description: Contient les collections de niveau supérieur dans le catalogue.
ms.assetid: 6cd23e6a-53b8-42ec-97df-59281f019252
title: Collection racine
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Root
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0aba7a308a37ee531adf0886b8d06d4fd8c17369f73bd2bddf3211c2c184a4fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547016"
---
# <a name="root-collection"></a>Collection racine

Contient les collections de niveau supérieur dans le catalogue. Il ne contient pas d’objets [**COMAdminCatalogObject**](comadmincatalogobject.md) ou ne prend en charge aucune propriété.

La collection **racine** ne prend pas en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

Vous ne pouvez pas accéder à la collection **racine** à partir d’une collection.

## <a name="members"></a>Membres

La collection **racine** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) mais n’a pas de membres supplémentaires.

## <a name="related-collections"></a>Regroupements connexes

Voici les collections de niveau supérieur dans le catalogue :

-   [**ApplicationCluster**](applicationcluster.md)
-   [**ApplicationInstances**](applicationinstances.md)
-   [**Applications**](applications.md)
-   [**ComputerList**](computerlist.md)
-   [**DCOMProtocols**](dcomprotocols.md)
-   [**EventClassesForIID**](eventclassesforiid.md)
-   [**FilesForImport**](filesforimport.md)
-   [**InprocServers**](inprocservers.md)
-   [**LegacyServers**](legacyservers.md)
-   [**LocalComputer**](localcomputer.md)
-   [**Partitions**](partitions.md)
-   [**PartitionUsers**](partitionusers.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**TransientSubscriptions**](transientsubscriptions.md)
-   [**WOWInprocServers**](wowinprocservers.md)
-   [**WOWLegacyServers**](wowlegacyservers.md)

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Regroupements d’administration COM+](com--administration-collections.md)
</dt> </dl>

 

 
