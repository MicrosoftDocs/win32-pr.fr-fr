---
title: Configuration de stratégie de groupe SNMP
description: Si vous utilisez le composant logiciel enfichable MMC (Microsoft Management Console) pour stratégie de groupe d’administrer les paramètres de stratégie basés sur le Registre qui s’appliquent à SNMP, une ou plusieurs des sous-clés suivantes peuvent exister.
ms.assetid: de21d2f5-3337-47ba-afcf-347e289873d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 817797dbc0e67f6006e12751beca533cbbec3656
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102113"
---
# <a name="configuring-snmp-group-policy"></a><span data-ttu-id="d36a1-103">Configuration de stratégie de groupe SNMP</span><span class="sxs-lookup"><span data-stu-id="d36a1-103">Configuring SNMP Group Policy</span></span>

<span data-ttu-id="d36a1-104">Si vous utilisez le composant logiciel enfichable MMC (Microsoft Management Console) pour stratégie de groupe d’administrer les paramètres de stratégie basés sur le Registre qui s’appliquent à SNMP, une ou plusieurs des sous-clés suivantes peuvent exister.</span><span class="sxs-lookup"><span data-stu-id="d36a1-104">If you use the Microsoft Management Console (MMC) snap-in for Group Policy to administer registry-based policy settings that apply to SNMP, one or more of the following subkeys may exist.</span></span>

<span data-ttu-id="d36a1-105">**HKEY \_ \_** \\  \\  \\  \\ **Paramètres** SNMP des stratégies \\  de logiciel de l’ordinateur local ValidCommunities</span><span class="sxs-lookup"><span data-stu-id="d36a1-105">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Policies**\\**SNMP**\\**Parameters**\\**ValidCommunities**</span></span>

<span data-ttu-id="d36a1-106">**HKEY \_ \_** \\  \\  \\  \\ **Paramètres** SNMP des stratégies \\  de logiciel de l’ordinateur local PermittedManagers</span><span class="sxs-lookup"><span data-stu-id="d36a1-106">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Policies**\\**SNMP**\\**Parameters**\\**PermittedManagers**</span></span>

<span data-ttu-id="d36a1-107">**HKEY \_ \_** \\  \\  \\  \\ **Paramètres** SNMP des stratégies \\  de logiciel de l’ordinateur local TrapConfiguration</span><span class="sxs-lookup"><span data-stu-id="d36a1-107">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Policies**\\**SNMP**\\**Parameters**\\**TrapConfiguration**</span></span>

<span data-ttu-id="d36a1-108">En règle générale, seuls les membres du groupe local administrateurs peuvent accéder aux sous-clés de Registre suivantes qui stockent les données de configuration du service SNMP :</span><span class="sxs-lookup"><span data-stu-id="d36a1-108">Typically, only members of the Administrators local group can access the following registry subkeys that store configuration data for the SNMP service:</span></span>

<span data-ttu-id="d36a1-109">**HKEY \_ \_** \\  \\  \\  \\  \\ **Paramètres** SNMP des services \\  de CurrentControlSet de système d’ordinateur local ValidCommunities</span><span class="sxs-lookup"><span data-stu-id="d36a1-109">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**SNMP**\\**Parameters**\\**ValidCommunities**</span></span>

<span data-ttu-id="d36a1-110">**HKEY \_ \_** \\  \\  \\  \\  \\ **Paramètres** SNMP des services \\  de CurrentControlSet de système d’ordinateur local PermittedManagers</span><span class="sxs-lookup"><span data-stu-id="d36a1-110">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**SNMP**\\**Parameters**\\**PermittedManagers**</span></span>

<span data-ttu-id="d36a1-111">Pour plus d’informations sur les paramètres de stratégie basés sur le registre, consultez [à propos de stratégie de groupe](/previous-versions/windows/desktop/Policy/about-group-policy).</span><span class="sxs-lookup"><span data-stu-id="d36a1-111">For more information about registry-based policy settings, see [About Group Policy](/previous-versions/windows/desktop/Policy/about-group-policy).</span></span>

 

 