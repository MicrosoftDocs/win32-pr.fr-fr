---
description: L’interface IAutomaticUpdatesSettings définit les propriétés suivantes.
ms.assetid: 663aaf7d-c701-4da8-ba92-7e0a6d0f35ba
title: Propriétés IAutomaticUpdatesSettings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2463fdc69fc93960ee45c0003a65894eaaf7399
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951240"
---
# <a name="iautomaticupdatessettings-properties"></a><span data-ttu-id="1cae6-103">Propriétés IAutomaticUpdatesSettings</span><span class="sxs-lookup"><span data-stu-id="1cae6-103">IAutomaticUpdatesSettings Properties</span></span>

<span data-ttu-id="1cae6-104">L’interface [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) définit les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="1cae6-104">The [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) interface defines the following properties.</span></span>



| <span data-ttu-id="1cae6-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="1cae6-105">Property</span></span>                                                                                 | <span data-ttu-id="1cae6-106">Description</span><span class="sxs-lookup"><span data-stu-id="1cae6-106">Description</span></span>                                                                                      |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1cae6-107">**NotificationLevel**</span><span class="sxs-lookup"><span data-stu-id="1cae6-107">**NotificationLevel**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)                 | <span data-ttu-id="1cae6-108">Obtient et définit la manière dont les utilisateurs sont avertis des événements de mise à jour automatique.</span><span class="sxs-lookup"><span data-stu-id="1cae6-108">Gets and sets how users are notified about Automatic Update events.</span></span>                              |
| [<span data-ttu-id="1cae6-109">**Seulement**</span><span class="sxs-lookup"><span data-stu-id="1cae6-109">**ReadOnly**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_readonly)                                   | <span data-ttu-id="1cae6-110">Obtient une valeur booléenne qui indique si les paramètres de mise à jour automatique sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1cae6-110">Gets a Boolean value that indicates whether the Automatic Update settings are read-only.</span></span>         |
| [<span data-ttu-id="1cae6-111">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="1cae6-111">**Required**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_required)                                   | <span data-ttu-id="1cae6-112">Obtient une valeur booléenne qui indique si stratégie de groupe requiert le service Mises à jour automatiques.</span><span class="sxs-lookup"><span data-stu-id="1cae6-112">Gets a Boolean value that indicates whether Group Policy requires the Automatic Updates service.</span></span> |
| [<span data-ttu-id="1cae6-113">**ScheduledInstallationDay**</span><span class="sxs-lookup"><span data-stu-id="1cae6-113">**ScheduledInstallationDay**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)   | <span data-ttu-id="1cae6-114">Obtient et définit les jours de la semaine où Mises à jour automatiques installe ou désinstalle des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="1cae6-114">Gets and sets the days of the week on which Automatic Updates installs or uninstalls updates.</span></span>    |
| [<span data-ttu-id="1cae6-115">**ScheduledInstallationTime**</span><span class="sxs-lookup"><span data-stu-id="1cae6-115">**ScheduledInstallationTime**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime) | <span data-ttu-id="1cae6-116">Obtient et définit l’heure à laquelle Mises à jour automatiques installe ou désinstalle des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="1cae6-116">Gets and sets the time at which Automatic Updates installs or uninstalls updates.</span></span>                |



 

> [!Note]  
> <span data-ttu-id="1cae6-117">Windows 8, Windows 8.1, Windows Server 2012 et Windows Server 2012 R2 offrent uniquement une prise en charge limitée de [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) et [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span><span class="sxs-lookup"><span data-stu-id="1cae6-117">Windows 8, Windows 8.1, Windows Server 2012, and Windows Server 2012 R2 provide only limited support for [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) and [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span></span> <span data-ttu-id="1cae6-118">Si l’ordinateur a été configuré par le biais d’stratégie de groupe pour utiliser un jour et une heure d’installation planifiés, les propriétés **ScheduledInstallationDay** et **ScheduledInstallationTime** retournent ce jour et cette heure planifiés.</span><span class="sxs-lookup"><span data-stu-id="1cae6-118">If the computer has been configured through Group Policy to use a scheduled installation day and time, the **ScheduledInstallationDay** and **ScheduledInstallationTime** properties return this scheduled day and time.</span></span> <span data-ttu-id="1cae6-119">Si l’ordinateur n’a pas été configuré à l’aide de la stratégie de groupe de cette manière, les propriétés **ScheduledInstallationDay** et **ScheduledInstallationTime** retournent des valeurs par défaut et non fiables.</span><span class="sxs-lookup"><span data-stu-id="1cae6-119">If the computer hasn't been configured through Group Policy in this way, the **ScheduledInstallationDay** and **ScheduledInstallationTime** properties return default and unreliable values.</span></span> <span data-ttu-id="1cae6-120">Si vous essayez de modifier le jour et l’heure d’installation planifiés sur ces systèmes d’exploitation, **ScheduledInstallationDay** et **ScheduledInstallationTime** semblent être exécutés, mais n’ont aucun effet.</span><span class="sxs-lookup"><span data-stu-id="1cae6-120">If you try to modify the scheduled installation day and time on these operating systems, **ScheduledInstallationDay** and **ScheduledInstallationTime** appear to succeed but have no effect.</span></span>

 

 

 



