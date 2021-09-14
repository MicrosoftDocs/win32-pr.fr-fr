---
description: Pour éviter les collisions de nom entre les propriétés créées par différents objets, le gestionnaire de propriétés partagées (SPM) utilise des groupes de propriétés partagées.
ms.assetid: f73d631e-2552-4358-903a-739e2df3657d
title: Groupes de propriétés partagées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776dafe5c7e9752ce3ed1c88b01fd909b4b145de
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127310958"
---
# <a name="shared-property-groups"></a>Groupes de propriétés partagées

Pour éviter les collisions de nom entre les propriétés créées par différents objets, le gestionnaire de propriétés partagées (SPM) utilise des groupes de propriétés partagées. Un groupe de propriétés partagé est simplement un espace de noms pour un ensemble de propriétés partagées. Chaque propriété d’un groupe de propriétés partagé est constituée d’un nom, d’une valeur et d’une position dans le groupe de propriétés partagées. Le nom ou la position peut être utilisé pour récupérer la valeur de la propriété. Vous pouvez accéder aux groupes de propriétés partagés et les créer via le gestionnaire de groupes de propriétés partagées.

Le modèle objet SPM est illustré dans l’illustration suivante.

![Diagramme qui montre le modèle objet SPM : ISharedPropertyGroupManager, ISharedPropertyGroup, ISharedProperty.](images/1df31cd9-2fc4-48d3-ae68-cae38afb75a6.png)

Voici les interfaces du gestionnaire de propriétés partagées :

-   [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) est utilisé pour créer des groupes de propriétés partagées et pour obtenir l’accès aux groupes de propriétés partagés existants. Vous pouvez accéder à l’interface **ISharedPropertyGroupManager** en créant une instance de l’objet [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) en utilisant [**IObjectContext :: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance) ou [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

-   [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) est utilisé pour créer les propriétés partagées et y accéder dans un groupe de propriétés partagées. Vous pouvez accéder à l’interface **ISharedPropertyGroup** en créant un objet [**SharedPropertyGroup**](sharedpropertygroup.md) avec la méthode [**ISharedPropertyGroupManager :: CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) . Comme pour tout objet COM, vous devez libérer un objet **SharedPropertyGroup** lorsque vous avez fini de l’utiliser.

-   [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) permet de définir ou de récupérer la valeur d’une propriété partagée. Une propriété partagée peut contenir tout type de données qui peut être représenté par un variant. Vous pouvez accéder à l’interface **ISharedProperty** en créant un objet [**SharedProperty**](sharedproperty.md) avec la méthode [**ISharedPropertyGroup :: CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) ou la méthode [**ISharedPropertyGroup :: CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) . Un objet **SharedProperty** peut être créé ou accessible uniquement à partir d’un objet [**SharedPropertyGroup**](sharedpropertygroup.md) . Là encore, vous devez libérer un objet **SharedProperty** lorsque vous avez fini de l’utiliser.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestionnaire de propriétés partagé COM+](com--shared-property-manager.md)
</dt> </dl>

 

 
