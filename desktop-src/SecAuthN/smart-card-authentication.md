---
description: Authentification par carte à puce
ms.assetid: cb5c80ea-c15e-4f68-a94b-b458d69ff474
title: Authentification par carte à puce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241d323f4c5e982fee96f44002da316d5d645d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521112"
---
# <a name="smart-card-authentication"></a>Authentification par carte à puce

Les composants de base du [*sous-système de carte à puce*](../secgloss/s-gly.md) sont basés sur les normes PC/SC (voir les spécifications à l’adresse [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ). Ces éléments de base sont les suivants :

-   [*Gestionnaire de ressources*](../secgloss/r-gly.md) qui utilise une API Windows.
-   [*Interface utilisateur*](../secgloss/u-gly.md) (IU) qui fonctionne avec le gestionnaire de ressources.
-   Plusieurs [*fournisseurs de services*](../secgloss/s-gly.md) de base qui fournissent un accès à des services spécifiques. Contrairement à l’API Windows du gestionnaire de ressources, les fournisseurs de services utilisent un modèle d’interface COM pour fournir des services de [*carte à puce*](../secgloss/s-gly.md) .

L’illustration suivante montre les relations de ces parties dans l’architecture globale de la carte à puce.

![architecture des cartes à puce](images/smartovr2a.png)

Pour plus d’informations sur le fonctionnement du [*sous-système de carte à puce*](../secgloss/s-gly.md) avec d’autres services disponibles dans Microsoft Internet Security Framework, consultez [relation avec d’autres services](relation-to-other-services.md).

Pour plus d’informations sur l’authentification par carte à puce, consultez les rubriques suivantes.



| Rubriques                                                                      | Contenu                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Concepts de carte à puce](smart-card-concepts.md)<br/>                   | Concepts de base et description de l’interaction entre les utilisateurs et les cartes à puce.<br/>                                                                                                                                                        |
| [Gestionnaire des ressources de carte à puce](smart-card-resource-manager.md)<br/>   | Informations sur l’API Resource Manager, qui gère l’accès aux [*lecteurs*](../secgloss/r-gly.md) et aux [*cartes à puce*](../secgloss/s-gly.md).<br/> |
| [Interface utilisateur de carte à puce](smart-card-user-interface.md)<br/>       | Informations sur la [*boîte de dialogue commune de la carte à puce*](../secgloss/s-gly.md).<br/>                                                                                   |
| [Fournisseurs de services de carte à puce](smart-card-service-providers.md)<br/> | Informations sur les interfaces, les commandes et les wrappers qui fournissent des fonctionnalités de carte à puce.<br/>                                                                                                                                              |



 

En outre, les développements des cartes à puce Microsoft sont disponibles à l’adresse [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx) .

 

 
