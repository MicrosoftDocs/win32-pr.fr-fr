---
description: Les GUID des paramètres d’alimentation identifient les événements de changement d’alimentation.
ms.assetid: 39D432A7-54F8-4135-B98C-7290F95B054A
title: GUID des paramètres d’alimentation (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b67dfd619d93f4318dbcfe2b44b5f8ba24460bd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541492"
---
# <a name="power-setting-guids"></a><span data-ttu-id="a3b4a-103">GUID des paramètres d’alimentation</span><span class="sxs-lookup"><span data-stu-id="a3b4a-103">Power Setting GUIDs</span></span>

<span data-ttu-id="a3b4a-104">Les **GUID** des paramètres d’alimentation identifient les événements de changement d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-104">Power setting **GUID** s identify power change events.</span></span> <span data-ttu-id="a3b4a-105">Cette rubrique répertorie les **GUID** des paramètres d’alimentation pour les notifications les plus utiles pour les applications.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-105">This topic lists power setting **GUID** s for notifications that are most useful to applications.</span></span> <span data-ttu-id="a3b4a-106">Une application doit s’inscrire à chaque événement de changement d’alimentation qui peut avoir un impact sur son comportement.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-106">An application should register for each power change event that might impact its behavior.</span></span> <span data-ttu-id="a3b4a-107">La notification est envoyée chaque fois qu’un paramètre change.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-107">Notification is sent each time a setting changes.</span></span>

<span data-ttu-id="a3b4a-108">Les **GUID** des paramètres d’alimentation sont définis dans Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-108">Power setting **GUID** s are defined in WinNT.h.</span></span>

<dl> <dt>

<span data-ttu-id="a3b4a-109"><span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**\_ \_ source d’alimentation du GUID ACDC \_**</span><span class="sxs-lookup"><span data-stu-id="a3b4a-109"><span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**GUID\_ACDC\_POWER\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3b4a-110">5D3E9A59-E9D5-4B00-A6BD-FF34FF516548</span><span class="sxs-lookup"><span data-stu-id="a3b4a-110">5D3E9A59-E9D5-4B00-A6BD-FF34FF516548</span></span>
</dt> <dt>



<span data-ttu-id="a3b4a-111">La source d’alimentation du système a changé.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-111">The system power source has changed.</span></span> <span data-ttu-id="a3b4a-112">Le membre de **données** est une **valeur DWORD** avec les valeurs de l’énumération des [**\_ \_ conditions d’alimentation du système**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition) qui indiquent la source d’alimentation actuelle.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-112">The **Data** member is a **DWORD** with values from the [**SYSTEM\_POWER\_CONDITION**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition) enumeration that indicates the current power source.</span></span>

<dl> <dt>

<span data-ttu-id="a3b4a-113">**PoAc** (0) : l’ordinateur est alimenté par une source d’alimentation secteur (ou similaire, par exemple un ordinateur portable équipé d’un adaptateur d’automobile 12V).</span><span class="sxs-lookup"><span data-stu-id="a3b4a-113">**PoAc** (0) - The computer is powered by an AC power source (or similar, such as a laptop powered by a 12V automotive adapter).</span></span>
</dt> <dt>

<span data-ttu-id="a3b4a-114">**PoDc** (1) : l’ordinateur est alimenté par une source d’alimentation de batterie intégrée.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-114">**PoDc** (1) - The computer is powered by an onboard battery power source.</span></span>
</dt> <dt>

<span data-ttu-id="a3b4a-115">**PoHot** (2) : l’ordinateur est alimenté par une source d’alimentation à faible terme, par exemple un appareil UPS.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-115">**PoHot** (2) - The computer is powered by a short-term power source such as a UPS device.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="a3b4a-116"><span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**pourcentage de batterie du GUID \_ \_ \_ restant**</span><span class="sxs-lookup"><span data-stu-id="a3b4a-116"><span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**GUID\_BATTERY\_PERCENTAGE\_REMAINING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3b4a-117">A7AD8041-B45A-4CAE-87A3-EECBB468A9E1</span><span class="sxs-lookup"><span data-stu-id="a3b4a-117">A7AD8041-B45A-4CAE-87A3-EECBB468A9E1</span></span>
</dt> <dt>



<span data-ttu-id="a3b4a-118">La capacité restante de la batterie a changé.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-118">The remaining battery capacity has changed.</span></span> <span data-ttu-id="a3b4a-119">La granularité varie d’un système à l’autres, mais la granularité la plus fine est de 1%.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-119">The granularity varies from system to system but the finest granularity is 1 percent.</span></span> <span data-ttu-id="a3b4a-120">Le membre de **données** est une **valeur DWORD** qui indique la capacité actuelle de la batterie restante en pourcentage compris entre 0 et 100.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-120">The **Data** member is a **DWORD** that indicates the current battery capacity remaining as a percentage from 0 through 100.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3b4a-121"><span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**État d’affichage de la \_ console GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a3b4a-121"><span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**GUID\_CONSOLE\_DISPLAY\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3b4a-122">6FE69556-704A-47A0-8F24-C28D936FDA47</span><span class="sxs-lookup"><span data-stu-id="a3b4a-122">6FE69556-704A-47A0-8F24-C28D936FDA47</span></span>
</dt> <dt>



<span data-ttu-id="a3b4a-123">L’état d’affichage de l’analyseur actuel a changé.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-123">The current monitor's display state has changed.</span></span>

<span data-ttu-id="a3b4a-124">**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette notification est disponible à partir de Windows 8 et de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-124">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="a3b4a-125">Le membre de **données** est une **valeur DWORD** avec l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-125">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a3b4a-126">0x0-l’affichage est désactivé.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-126">0x0 - The display is off.</span></span>
</dt> <dt>

<span data-ttu-id="a3b4a-127">0x1 : l’affichage est activé.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-127">0x1 - The display is on.</span></span>
</dt> <dt>

<span data-ttu-id="a3b4a-128">0X2-l’affichage est grisé.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-128">0x2 - The display is dimmed.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="a3b4a-129"><span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**\_présence globale de l' \_ utilisateur GUID \_**</span><span class="sxs-lookup"><span data-stu-id="a3b4a-129"><span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**GUID\_GLOBAL\_USER\_PRESENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3b4a-130">786E8A1D-B427-4344-9207-09E70BDCBEA9</span><span class="sxs-lookup"><span data-stu-id="a3b4a-130">786E8A1D-B427-4344-9207-09E70BDCBEA9</span></span>
</dt> <dt>



<span data-ttu-id="a3b4a-131">L’état de l’utilisateur associé à n’importe quelle session a changé.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-131">The user status associated with any session has changed.</span></span> <span data-ttu-id="a3b4a-132">Cela représente l’état combiné de la présence de l’utilisateur sur toutes les sessions locales et distantes sur le système.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-132">This represents the combined status of user presence across all local and remote sessions on the system.</span></span>

<span data-ttu-id="a3b4a-133">Cette notification est envoyée uniquement aux services et autres programmes s’exécutant dans la session 0.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-133">This notification is sent only services and other programs running in session 0.</span></span> <span data-ttu-id="a3b4a-134">Les applications en mode utilisateur doivent s’inscrire à la présence d’un **\_ utilisateur de session \_ \_ GUID** à la place.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-134">User-mode applications should register for **GUID\_SESSION\_USER\_PRESENCE** instead.</span></span>

<span data-ttu-id="a3b4a-135">**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette notification est disponible à partir de Windows 8 et de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-135">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="a3b4a-136">Le membre de **données** est une **valeur DWORD** avec l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-136">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a3b4a-137">**PowerUserPresent** (0)-l’utilisateur est présent dans une session locale ou distante sur le système.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-137">**PowerUserPresent** (0) - The user is present in any local or remote session on the system.</span></span>
</dt> <dt>

<span data-ttu-id="a3b4a-138">**PowerUserInactive** (2)-l’utilisateur n’est pas présent dans une session locale ou distante sur le système.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-138">**PowerUserInactive** (2) - The user is not present in any local or remote session on the system.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="a3b4a-139"><span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**\_tâche en \_ arrière-plan du GUID inactif \_**</span><span class="sxs-lookup"><span data-stu-id="a3b4a-139"><span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**GUID\_IDLE\_BACKGROUND\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3b4a-140">515C31D8-F734-163D-A0FD-11A08C91E8F1</span><span class="sxs-lookup"><span data-stu-id="a3b4a-140">515C31D8-F734-163D-A0FD-11A08C91E8F1</span></span>
</dt> <dt>



<span data-ttu-id="a3b4a-141">Le système est occupé.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-141">The system is busy.</span></span> <span data-ttu-id="a3b4a-142">Cela indique que le système ne passera pas dans un état d’inactivité dans un avenir proche et que l’heure actuelle est un bon moment pour que les composants exécutent des tâches d’arrière-plan ou inactives qui pourraient empêcher l’ordinateur d’entrer dans un état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-142">This indicates that the system will not be moving into an idle state in the near future and that the current time is a good time for components to perform background or idle tasks that would otherwise prevent the computer from entering an idle state.</span></span>

<span data-ttu-id="a3b4a-143">Il n’y a aucune notification lorsque le système est en mesure de passer à un état d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-143">There is no notification when the system is able to move into an idle state.</span></span> <span data-ttu-id="a3b4a-144">La notification de tâche en arrière-plan Idle n’indique pas si un utilisateur est présent sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-144">The idle background task notification does not indicate whether a user is present at the computer.</span></span> <span data-ttu-id="a3b4a-145">Les **données** membres n’ont pas d’informations et peuvent être ignorées.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-145">The **Data** member has no information and can be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a3b4a-146"><span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**\_mise sous \_ tension \_ du moniteur GUID**</span><span class="sxs-lookup"><span data-stu-id="a3b4a-146"><span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**GUID\_MONITOR\_POWER\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3b4a-147">02731015-4510-4526-99E6-E5A17EBD1AEA</span><span class="sxs-lookup"><span data-stu-id="a3b4a-147">02731015-4510-4526-99E6-E5A17EBD1AEA</span></span>
</dt> <dt>



<span data-ttu-id="a3b4a-148">Le moniteur système principal a été mis sous tension ou hors tension.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-148">The primary system monitor has been powered on or off.</span></span> <span data-ttu-id="a3b4a-149">Cette notification est utile pour les composants qui affichent activement le contenu sur le périphérique d’affichage, comme la visualisation des médias.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-149">This notification is useful for components that actively render content to the display device, such as media visualization.</span></span> <span data-ttu-id="a3b4a-150">Ces applications doivent s’inscrire à cette notification et arrêter le rendu du contenu des graphiques lorsque l’analyse est désactivée pour réduire la consommation d’énergie du système.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-150">These applications should register for this notification and stop rendering graphics content when the monitor is off to reduce system power consumption.</span></span> <span data-ttu-id="a3b4a-151">Le membre de **données** est une **valeur DWORD** qui indique l’état actuel de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-151">The **Data** member is a **DWORD** that indicates the current monitor state.</span></span>

<dl> <dt>

<span data-ttu-id="a3b4a-152">0x0-l’analyse est désactivée.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-152">0x0 - The monitor is off.</span></span>
</dt> <dt>

<span data-ttu-id="a3b4a-153">0x1-l’analyse est activée.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-153">0x1 - The monitor is on.</span></span>
</dt> </dl>

<span data-ttu-id="a3b4a-154">**Windows 8 et Windows Server 2012 :** Les nouvelles applications doivent utiliser l’état d’affichage de la **\_ console \_ \_ GUID** au lieu de cette notification.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-154">**Windows 8 and Windows Server 2012:** New applications should use **GUID\_CONSOLE\_DISPLAY\_STATE** instead of this notification.</span></span>

</dl> </dd> <dt>

<span data-ttu-id="a3b4a-155"><span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**\_État de \_ l’économie d’énergie GUID \_**</span><span class="sxs-lookup"><span data-stu-id="a3b4a-155"><span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**GUID\_POWER\_SAVING\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3b4a-156">E00958C0-C213-4ACE-AC77-FECCED2EEEA5</span><span class="sxs-lookup"><span data-stu-id="a3b4a-156">E00958C0-C213-4ACE-AC77-FECCED2EEEA5</span></span>
</dt> <dt>



<span data-ttu-id="a3b4a-157">L’économiseur de batterie a été désactivé ou activé en réponse à la modification des conditions d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-157">Battery saver has been turned off or on in response to changing power conditions.</span></span> <span data-ttu-id="a3b4a-158">Cette notification est utile pour les composants qui participent à la conservation de l’énergie.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-158">This notification is useful for components that participate in energy conservation.</span></span> <span data-ttu-id="a3b4a-159">Ces applications doivent s’inscrire à cette notification et économiser de l’énergie lorsque l’économiseur de batterie est activé.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-159">These applications should register for this notification and save power when battery saver is on.</span></span>

<span data-ttu-id="a3b4a-160">Le membre de **données** est une **valeur DWORD** qui indique l’état de l’économiseur de batterie.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-160">The **Data** member is a **DWORD** that indicates battery saver state.</span></span>

<dl> <dt>

<span data-ttu-id="a3b4a-161">0x0-l’économiseur de batterie est désactivé.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-161">0x0 - Battery saver is off.</span></span>
</dt> <dt>

<span data-ttu-id="a3b4a-162">0x1-l’économiseur de batterie est activé.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-162">0x1 - Battery saver is on.</span></span> <span data-ttu-id="a3b4a-163">Économisez de l’énergie dans la mesure du possible.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-163">Save energy where possible.</span></span>
</dt> </dl>

<span data-ttu-id="a3b4a-164">Pour obtenir des informations générales sur l’économiseur de batterie, consultez [économiseur de batterie (dans les instructions relatives aux composants matériels)](/windows-hardware/design/component-guidelines/battery-saver).</span><span class="sxs-lookup"><span data-stu-id="a3b4a-164">For general information about battery saver, see [battery saver (in the hardware component guidelines)](/windows-hardware/design/component-guidelines/battery-saver).</span></span>

</dl> </dd> <dt>

<span data-ttu-id="a3b4a-165"><span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**POWERSCHEME de GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a3b4a-165"><span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**GUID\_POWERSCHEME\_PERSONALITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3b4a-166">245d8541-3943-4422-b025-13A784F679B7</span><span class="sxs-lookup"><span data-stu-id="a3b4a-166">245d8541-3943-4422-b025-13A784F679B7</span></span>
</dt> <dt>



<span data-ttu-id="a3b4a-167">La personnalité active du mode de gestion de l’alimentation a changé.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-167">The active power scheme personality has changed.</span></span> <span data-ttu-id="a3b4a-168">Tous les modes de gestion de l’alimentation sont mappés à l’une de ces personnalités.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-168">All power schemes map to one of these personalities.</span></span> <span data-ttu-id="a3b4a-169">Le membre de **données** est un **GUID** qui indique la nouvelle personnalité active du mode de gestion de l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-169">The **Data** member is a **GUID** that indicates the new active power scheme personality.</span></span>

<dl> <dt>



<span data-ttu-id="a3b4a-170">**GUID \_ \_ \_ Économie d’énergie minimale** (8C5E7FDA-E8BF-4A96-9A85-A6E23A8C635C)</span><span class="sxs-lookup"><span data-stu-id="a3b4a-170">**GUID\_MIN\_POWER\_SAVINGS** (8C5E7FDA-E8BF-4A96-9A85-A6E23A8C635C)</span></span>

<span data-ttu-id="a3b4a-171">Hautes performances : le schéma est conçu pour offrir des performances maximales au détriment des économies de la consommation énergétique.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-171">High Performance - The scheme is designed to deliver maximum performance at the expense of power consumption savings.</span></span>


</dt> <dt>



<span data-ttu-id="a3b4a-172">**GUID \_ \_ \_ Économies d’énergie max** . (A1841308-3541-4FAB-BC81-F71556F20B4A)</span><span class="sxs-lookup"><span data-stu-id="a3b4a-172">**GUID\_MAX\_POWER\_SAVINGS** (A1841308-3541-4FAB-BC81-F71556F20B4A)</span></span>

<span data-ttu-id="a3b4a-173">Économiseur d’énergie : le schéma est conçu pour offrir des économies d’énergie maximales au détriment des performances et de la réactivité du système.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-173">Power Saver - The scheme is designed to deliver maximum power consumption savings at the expense of system performance and responsiveness.</span></span>


</dt> <dt>



<span data-ttu-id="a3b4a-174">**GUID \_ \_ \_ Économie d’énergie classique** (381B4222-F694-41F0-9685-FF5BB260DF2E)</span><span class="sxs-lookup"><span data-stu-id="a3b4a-174">**GUID\_TYPICAL\_POWER\_SAVINGS** (381B4222-F694-41F0-9685-FF5BB260DF2E)</span></span>

<span data-ttu-id="a3b4a-175">Automatique-le schéma est conçu pour équilibrer automatiquement les performances et les économies de consommation énergétique.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-175">Automatic - The scheme is designed to automatically balance performance and power consumption savings.</span></span>


</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="a3b4a-176"><span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**État d’affichage de la \_ session GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a3b4a-176"><span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**GUID\_SESSION\_DISPLAY\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3b4a-177">2B84C20E-AD23-4ddf-93DB-05FFBD7EFCA5</span><span class="sxs-lookup"><span data-stu-id="a3b4a-177">2B84C20E-AD23-4ddf-93DB-05FFBD7EFCA5</span></span>
</dt> <dt>



<span data-ttu-id="a3b4a-178">L’affichage associé à la session de l’application a été activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-178">The display associated with the application's session has been powered on or off.</span></span>

<span data-ttu-id="a3b4a-179">**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette notification est disponible à partir de Windows 8 et de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-179">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="a3b4a-180">Cette notification est envoyée uniquement aux applications en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-180">This notification is sent only to user-mode applications.</span></span> <span data-ttu-id="a3b4a-181">Les services et autres programmes s’exécutant dans la session 0 ne reçoivent pas cette notification.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-181">Services and other programs running in session 0 do not receive this notification.</span></span> <span data-ttu-id="a3b4a-182">Le membre de **données** est une **valeur DWORD** avec l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-182">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a3b4a-183">0x0-l’affichage est désactivé.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-183">0x0 - The display is off.</span></span>
</dt> <dt>

<span data-ttu-id="a3b4a-184">0x1 : l’affichage est activé.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-184">0x1 - The display is on.</span></span>
</dt> <dt>

<span data-ttu-id="a3b4a-185">0X2-l’affichage est grisé.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-185">0x2 - The display is dimmed.</span></span>
</dt> </dl>

</dl> </dd> <dt>

<span data-ttu-id="a3b4a-186"><span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**présence d’un \_ utilisateur de session GUID \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a3b4a-186"><span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**GUID\_SESSION\_USER\_PRESENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3b4a-187">3C0F4548-C03F-4c4d-B9F2-237EDE686376</span><span class="sxs-lookup"><span data-stu-id="a3b4a-187">3C0F4548-C03F-4c4d-B9F2-237EDE686376</span></span>
</dt> <dt>



<span data-ttu-id="a3b4a-188">L’état de l’utilisateur associé à la session de l’application a changé.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-188">The user status associated with the application's session has changed.</span></span>

<span data-ttu-id="a3b4a-189">**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette notification est disponible à partir de Windows 8 et de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-189">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This notification is available starting with Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="a3b4a-190">Cette notification est envoyée uniquement aux applications en mode utilisateur qui s’exécutent dans une session interactive.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-190">This notification is sent only to user-mode applications running in an interactive session.</span></span> <span data-ttu-id="a3b4a-191">Les services et autres programmes en cours d’exécution dans la session 0 doivent s’inscrire à la **\_ \_ \_ présence globale de l’utilisateur GUID**.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-191">Services and other programs running in session 0 should register for **GUID\_GLOBAL\_USER\_PRESENCE**.</span></span> <span data-ttu-id="a3b4a-192">Le membre de **données** est une **valeur DWORD** avec l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-192">The **Data** member is a **DWORD** with one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a3b4a-193">**PowerUserPresent** (0)-l’utilisateur fournit une entrée à la session.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-193">**PowerUserPresent** (0) - The user is providing input to the session.</span></span>
</dt> <dt>

<span data-ttu-id="a3b4a-194">**PowerUserInactive** (2)-le délai d’attente de l’activité de l’utilisateur s’est écoulé sans interaction de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-194">**PowerUserInactive** (2) - The user activity timeout has elapsed with no interaction from the user.</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="a3b4a-195">Toutes les applications qui s’exécutent dans une session interactive en mode utilisateur doivent utiliser ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-195">All applications that run in an interactive user-mode session should use this setting.</span></span> <span data-ttu-id="a3b4a-196">Lorsque les applications en mode noyau s’inscrivent pour surveiller l’État, elles doivent utiliser l’état d’affichage de la **\_ console \_ \_ GUID** à la place.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-196">When kernel mode applications register for monitor status they should use **GUID\_CONSOLE\_DISPLAY\_STATUS** instead.</span></span>

 

</dl> </dd> <dt>

<span data-ttu-id="a3b4a-197"><span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**\_mode absence système \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="a3b4a-197"><span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**GUID\_SYSTEM\_AWAYMODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3b4a-198">98A7F580-01F7-48AA-9C0F-44352C29E5C0</span><span class="sxs-lookup"><span data-stu-id="a3b4a-198">98A7F580-01F7-48AA-9C0F-44352C29E5C0</span></span>
</dt> <dt>



<span data-ttu-id="a3b4a-199">Le système est en cours d’entrée ou de sortie.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-199">The system is entering or exiting away mode.</span></span> <span data-ttu-id="a3b4a-200">Le membre de **données** est une **valeur DWORD** qui indique l’état actuel du mode absence.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-200">The **Data** member is a **DWORD** that indicates the current away mode state.</span></span>

<dl> <dt>

<span data-ttu-id="a3b4a-201">0x0-l’ordinateur quitte le mode away.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-201">0x0 - The computer is exiting away mode.</span></span>
</dt> <dt>

<span data-ttu-id="a3b4a-202">0x1-l’ordinateur entre en mode absence.</span><span class="sxs-lookup"><span data-stu-id="a3b4a-202">0x1 - The computer is entering away mode.</span></span>
</dt> </dl>

</dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a3b4a-203">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3b4a-203">Requirements</span></span>



| <span data-ttu-id="a3b4a-204">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3b4a-204">Requirement</span></span> | <span data-ttu-id="a3b4a-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3b4a-205">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a3b4a-206">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3b4a-206">Header</span></span><br/> | <dl> <span data-ttu-id="a3b4a-207"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3b4a-207"><dt>WinNT.h</dt></span></span> </dl> |



 

