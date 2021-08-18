---
description: Le profil de virtualisation des ressources permet à un client de découvrir les ressources virtuelles prises en charge par le système de virtualisation.
ms.assetid: CEF58153-F634-4E32-9C1D-385F1C740314
title: Service de gestion des ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f593af3c440ad15add50445a3b05f41d44c8c396a1334635aeaf141838e82e64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746213"
---
# <a name="resource-management-service"></a>Service de gestion des ressources

Le profil de virtualisation des ressources permet à un client de découvrir les ressources virtuelles prises en charge par le système de virtualisation. Elle décrit également la capacité (ou le nombre d’allocations) qui est prise en charge pour chaque type de ressource virtuelle. L’illustration suivante montre le profil de virtualisation des ressources.

![Profil de virtualisation des ressources](images/resourcemanagement.png)

Deux classes de ressources virtuelles différentes sont définies par le profil de virtualisation des ressources :

-   Ressource partagée : représente les ressources de l’hôte qui sont ou peuvent être partagées entre plusieurs ordinateurs virtuels. [**MSVM \_ Le processeur**](msvm-processor.md) est un exemple de ressource partagée.
-   Ressource synthétique : représente les ressources virtuelles qui n’ont aucune ressource hôte correspondante. [**MSVM \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md) est un exemple de ressource synthétique.

Le pool de ressources est utilisé pour collecter une classe de ressources hôtes afin qu’il puisse être facilement découvert, tandis que ses fonctionnalités et ses paramètres peuvent être décrits dans un emplacement central. Il n’existe aucune limite quant à la façon dont une implémentation de la ressource collectée peut être de base ou avancée.

À partir du pool de ressources, le client peut accéder aux fonctionnalités d’allocation (AC) associées. Cette classe décrit les fonctionnalités de la ressource décrite par ce pool de ressources. Par exemple, il peut indiquer si le [**\_ EmulatedEthernetPort MSVM**](msvm-emulatedethernetport.md) représenté par ce pool de ressources prend en charge les réseaux locaux virtuels (VLAN) ou les filtres.

Le profil AC définit les moyens par lesquels un client peut découvrir les paramètres par défaut et la plage valides pour une ressource virtuelle donnée. Un objet AC est associé à chaque liste de ressources partagées. Quatre objets de données de paramètre d’allocation de ressources (RASD) sont associés à l’objet AC pour décrire les valeurs minimale, maximale, par défaut et incrémentielle de l’allocation de la ressource donnée. Ensemble, ces classes décrivent la plage globale des fonctionnalités prises en charge. L’instance [**MSVM \_ AllocationCapabilities**](msvm-allocationcapabilities.md) fournit un point d’ancrage pour l’ensemble d’instances [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) qui spécifient la plage de paramètres par défaut et valide pour une ressource virtuelle. La classe d’association [**MSVM \_ SettingsDefineCapabilities**](msvm-settingsdefinecapabilities.md) fournit le lien entre l’instance AC et les paramètres minimum, maximum, incrémentiel et par défaut d’une ressource prise en charge par la plateforme de virtualisation.

 

 



