---
description: Le profil de mise en réseau décrit les objets utilisés pour configurer le système afin de permettre aux ordinateurs virtuels de communiquer sur le réseau.
ms.assetid: A5C4866B-0F65-47B5-8FC4-B92943842B86
title: Service de mise en réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc85b7a5121a3e7e42f333f829816184b57bd8eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512958"
---
# <a name="networking-service"></a>Service de mise en réseau

Le profil de mise en réseau décrit les objets utilisés pour configurer le système afin de permettre aux ordinateurs virtuels de communiquer sur le réseau. Les objets réseau globaux, utilisés pour configurer le commutateur réseau dans le système d’exploitation de gestion, incluent les classes [**MSVM \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md), [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)et [**MSVM \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) . Les objets réseau de la machine virtuelle, utilisés pour configurer la carte d’interface réseau (NIC) de l’ordinateur virtuel, incluent les classes [**MSVM \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md), [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md)et [**MSVM \_ LANEndpoint**](msvm-lanendpoint.md) .

La racine du profil de mise en réseau globale est la classe [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) . Cette classe représente un périphérique de commutateur virtuel dans le système d’exploitation de gestion. **MSVM \_ VirtualEthernetSwitch** est associé aux instances de la [**classe \_ switchport MSVM**](https://www.bing.com/search?q=**Msvm\_SwitchPort**) , qui représente les ports sur le commutateur virtuel. Les instances des classes **MSVM \_ VirtualEthernetSwitch** et [**MSVM \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) sont créées, supprimées et connectées via la classe MSVM [**\_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) (qui n’est pas indiquée dans l’illustration ci-dessus).

Le service de gestion de commutateur virtuel (VSMS) représente le service de mise en réseau présent sur un seul hôte Hyper-V et contient des méthodes pour [**MSVM \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) utilisées pour contrôler la définition, la modification et la destruction des ressources réseau globales, telles que les commutateurs virtuels, les ports de commutateur et les ports Ethernet internes.

La représentation du périphérique Ethernet sur la machine virtuelle ressemble beaucoup à celle de tout autre périphérique, comme décrit dans le [**service de gestion du système virtuel**](virtual-system-management-service.md). Les classes [**MSVM \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md) et [**MSVM \_ SyntheticEthernetPort**](msvm-syntheticethernetport.md) représentent le périphérique de carte réseau virtuelle et sont configurées via une [**instance MSVM ResourceAllocationSettingData (RASD \_**](msvm-resourceallocationsettingdata.md) ) associée. La seule caractéristique inhabituelle de cette représentation est que, lorsque l’ordinateur virtuel est instancié et crée à son tour les appareils **MSVM \_ EmulatedEthernetPort** et **MSVM \_ SyntheticEthernetPort** , il crée également une instance MSVM [**\_ LANEndpoint**](msvm-lanendpoint.md) associée pour la carte réseau virtuelle. De même, lorsque l’ordinateur virtuel est enregistré ou désactivé et que les instances **MSVM \_ EmulatedEthernetPort** et **MSVM \_ SyntheticEthernetPort** sont détruites, l' [**instance \_ MSVM VmLANEndpoint associée**](https://www.bing.com/search?q=**Msvm\_VmLANEndpoint**) est également détruite. L’objectif du **\_ LANEndpoint MSVM** est de servir de pont pour connecter deux ports réseau entre eux. Dans ce cas, il est utilisé pour connecter une carte réseau virtuelle à un port sur l’appareil de commutateur virtuel. En d’autres termes, il connecte les instances **MSVM \_ EmulatedEthernetPort** et **MSVM \_ SyntheticEthernetPort** sur la machine virtuelle à [**une \_ instance MSVM EthernetSwitchPort particulière sur**](msvm-ethernetswitchport.md) le commutateur virtuel. Pour connecter un commutateur à l’extérieur, vous devez lier le port Ethernet physique au [**\_ VirtualSwitch MSVM**](https://www.bing.com/search?q=**Msvm\_VirtualSwitch**) via [**BindExternalEthernetPort**](https://www.bing.com/search?q=**BindExternalEthernetPort**). Défavorablement, lors de la connexion d’un commutateur à la pile de mise en réseau de l’ordinateur hôte ou de la carte réseau interne, utilisez ConnectInternal pour qu’un ordinateur virtuel communique avec l’hôte et non dans le monde extérieur. [**MSVM \_ ActiveConnection**](msvm-activeconnection.md) connecte un port de commutateur [**au \_ SwitchLANEndpoint MSVM**](https://www.bing.com/search?q=**Msvm\_SwitchLANEndpoint**) auquel le port est connecté à l’intérieur d’Hyper-V. L’existence de cet objet signifie que le port de commutateur et **les \_ SwitchLANEndpoint MSVM** sont connectés activement et que le port Ethernet associé à **MSVM \_ LANEndpoint** peut communiquer avec le réseau via le port de commutateur.

 

 



