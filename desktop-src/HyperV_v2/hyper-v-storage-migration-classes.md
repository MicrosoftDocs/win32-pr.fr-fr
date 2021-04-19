---
description: L’API de migration Hyper-V définit les éléments de programmation suivants.
ms.assetid: E1FE7351-2F14-4C8F-AF5C-9009CC61CE22
title: Informations de référence sur l’API de migration Hyper-V
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e40a05bc976cf1722aba558eeca9c7b04cdf7287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518600"
---
# <a name="hyper-v-migration-api-reference"></a><span data-ttu-id="d1c2e-103">Informations de référence sur l’API de migration Hyper-V</span><span class="sxs-lookup"><span data-stu-id="d1c2e-103">Hyper-V migration API reference</span></span>

<span data-ttu-id="d1c2e-104">L’API de migration Hyper-V définit les éléments de programmation suivants.</span><span class="sxs-lookup"><span data-stu-id="d1c2e-104">The Hyper-V migration API defines the following programming elements.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d1c2e-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="d1c2e-105">In this section</span></span>



| <span data-ttu-id="d1c2e-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="d1c2e-106">Topic</span></span>                                                                                                                                | <span data-ttu-id="d1c2e-107">Description</span><span class="sxs-lookup"><span data-stu-id="d1c2e-107">Description</span></span>                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1c2e-108">**MSVM \_ MigrationJob**</span><span class="sxs-lookup"><span data-stu-id="d1c2e-108">**Msvm\_MigrationJob**</span></span>](msvm-migrationjob.md)<br/>                                                                           | <span data-ttu-id="d1c2e-109">Cette classe représente un travail d’opération de migration créé pour le stockage ou la migration du système virtuel par le service de migration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="d1c2e-109">This class represents a migration operation job created for storage or virtual system migration by the virtual system migration service.</span></span><br/>                                                 |
| [<span data-ttu-id="d1c2e-110">**MSVM \_ VirtualSystemMigrationCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d1c2e-110">**Msvm\_VirtualSystemMigrationCapabilities**</span></span>](msvm-virtualsystemmigrationcapabilities.md)<br/>                               | <span data-ttu-id="d1c2e-111">Définit les moyens permettant à un client de découvrir les méthodes fournies par le service de migration, ainsi que la plage valide des données de paramètres de migration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="d1c2e-111">Defines the means by which a client can discover the methods provided by the migration service, and valid range of virtual system migration setting data.</span></span><br/>                                |
| [<span data-ttu-id="d1c2e-112">**MSVM \_ VirtualSystemMigrationNetworkSettingData**</span><span class="sxs-lookup"><span data-stu-id="d1c2e-112">**Msvm\_VirtualSystemMigrationNetworkSettingData**</span></span>](msvm-virtualsystemmigrationnetworksettingdata.md)<br/>                   | <span data-ttu-id="d1c2e-113">Représente le réseau sur lequel le service de migration de système virtuel écoute la migration du système virtuel entrant.</span><span class="sxs-lookup"><span data-stu-id="d1c2e-113">Represents the network on which the virtual system migration service is listening for incoming virtual system migration.</span></span><br/>                                                                 |
| [<span data-ttu-id="d1c2e-114">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="d1c2e-114">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)<br/>                                         | <span data-ttu-id="d1c2e-115">Représente le service de migration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="d1c2e-115">Represents the virtual system migration service.</span></span> <span data-ttu-id="d1c2e-116">Il est utilisé pour la migration d’un système virtuel ou pour la migration du stockage d’un système virtuel d’une plate-forme de virtualisation vers une autre.</span><span class="sxs-lookup"><span data-stu-id="d1c2e-116">It is used for migrating a virtual system or for migrating the storage of a virtual system from one virtualization platform to another.</span></span><br/> |
| [<span data-ttu-id="d1c2e-117">**MSVM \_ VirtualSystemMigrationServiceSettingData**</span><span class="sxs-lookup"><span data-stu-id="d1c2e-117">**Msvm\_VirtualSystemMigrationServiceSettingData**</span></span>](msvm-virtualsystemmigrationservicesettingdata.md)<br/>                   | <span data-ttu-id="d1c2e-118">Représente les paramètres pour le service de migration de système virtuel sur un ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="d1c2e-118">Represents the settings for the virtual system migration service on a host.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="d1c2e-119">**MSVM \_ VirtualSystemMigrationServiceSettingDataComponent**</span><span class="sxs-lookup"><span data-stu-id="d1c2e-119">**Msvm\_VirtualSystemMigrationServiceSettingDataComponent**</span></span>](msvm-virtualsystemmigrationservicesettingdatacomponent.md)<br/> | <span data-ttu-id="d1c2e-120">Association utilisée pour représenter les paramètres réseau de migration de système virtuel du service de migration de système virtuel.</span><span class="sxs-lookup"><span data-stu-id="d1c2e-120">An association used to represent virtual system migration network settings of the virtual system migration service.</span></span><br/>                                                                      |
| [<span data-ttu-id="d1c2e-121">**MSVM \_ VirtualSystemMigrationSettingData**</span><span class="sxs-lookup"><span data-stu-id="d1c2e-121">**Msvm\_VirtualSystemMigrationSettingData**</span></span>](msvm-virtualsystemmigrationsettingdata.md)<br/>                                 | <span data-ttu-id="d1c2e-122">Représente les paramètres de migration pour la migration d’un système virtuel et du stockage attaché à un système virtuel.</span><span class="sxs-lookup"><span data-stu-id="d1c2e-122">Represents the migration settings for migrating a virtual system and the storage attached to a virtual system.</span></span><br/>                                                                           |



 

 

 




