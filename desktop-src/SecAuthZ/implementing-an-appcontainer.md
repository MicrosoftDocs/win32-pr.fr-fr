---
description: Un AppContainer est implémenté en ajoutant de nouvelles informations au jeton de processus, en modifiant SeAccessCheck () afin que tous les objets de liste de contrôle d’accès (ACL) hérités et non modifiés bloquent les demandes d’accès des processus AppContainer par défaut, et les objets de réacl qui doivent être disponibles pour AppContainers.
ms.assetid: C70A2F8C-27CB-4298-AA31-8F5099616625
title: Implémentation d’un AppContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a6fc4c8d807d6a45f27f4f7a79d69ceb97edeb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867810"
---
# <a name="implementing-an-appcontainer"></a>Implémentation d’un AppContainer

Un AppContainer est implémenté en ajoutant de nouvelles informations au jeton de processus, en modifiant [**SeAccessCheck ()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) afin que tous les objets de liste de contrôle d’accès (ACL) hérités et non modifiés bloquent les demandes d’accès des processus AppContainer par défaut, et les objets de réacl qui doivent être disponibles pour AppContainers.

## <a name="the-process"></a>Processus

Commencez par ajouter de nouvelles informations pour le jeton de processus. Modifiez ensuite **SeAccessCheck ()** afin que toutes les listes de contrôle d’accès héritées non modifiées bloquent les demandes d’accès des processus AppContainer par défaut. Enfin, reconfigurez les ressources de liste de contrôle d’accès qui doivent être disponibles pour AppContainers

Le SID AppContainer est un identificateur unique persistant pour l’appcontainer. Les SID de capacité accordent l’accès à des groupes de ressources à des groupes de AppContainers. Un AppContainerNumber est un **DWORD** temporaire utilisé pour distinguer les AppContainers. Toutefois, il ne doit pas être utilisé en tant qu’identité pour l’AppContainer.

Pour autoriser un seul AppContainer à accéder à une ressource, ajoutez son AppContainerSID à la liste de contrôle d’accès pour cette ressource.

Pour permettre à plusieurs AppContainers spécifiques d’accéder à une ressource, ajoutez tous leurs AppContainerSIDs à la liste de contrôle d’accès pour cette ressource.

Pour gérer des groupes d’autorisations, créez un SID de capacité (un GUID) et placez ce SID de fonctionnalité sur toutes les ressources à accorder. Ajoutez ensuite le SID de fonctionnalité à votre jeton de processus.

Pour autoriser tous les AppContainers à accéder à une ressource, ajoutez le SID **tous les packages d’application** à la liste de contrôle d’accès de cette ressource. Cela agit comme un caractère générique.

AppContainerSID et CapabilitySID prennent tous deux en charge les masques d’accès dans les entrées Access Control (ACE). Définissez le cas échéant.

 

 
