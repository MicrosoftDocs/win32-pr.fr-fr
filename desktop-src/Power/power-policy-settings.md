---
description: Décrit les paramètres de stratégie d’alimentation qui composent un mode de gestion de l’alimentation.
ms.assetid: cd515cd6-67f4-45d0-b769-3abc7a56faa8
title: Paramètres de stratégie d’alimentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f490c758a890faf314be1ddffe9ac7a503bd473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756573"
---
# <a name="power-policy-settings"></a><span data-ttu-id="568e6-103">Paramètres de stratégie d’alimentation</span><span class="sxs-lookup"><span data-stu-id="568e6-103">Power Policy Settings</span></span>

<span data-ttu-id="568e6-104">Les modes de gestion de l’alimentation et les schémas sont des préférences et des paramètres de stratégie.</span><span class="sxs-lookup"><span data-stu-id="568e6-104">Power plans and schemes consist of preferences and policy settings.</span></span>

<span data-ttu-id="568e6-105">Un mode de gestion de l’alimentation se compose d’un groupe de préférences de paramètres d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="568e6-105">A power plan consists of a group of power setting preferences.</span></span> <span data-ttu-id="568e6-106">Ces préférences se composent à la fois d’une valeur AC et DC pour chacun des paramètres d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="568e6-106">These preferences consist of both an AC and DC value for each of the power settings.</span></span> <span data-ttu-id="568e6-107">Chaque mode de gestion de l’alimentation est identifié par un **GUID** unique, ainsi qu’un nom convivial.</span><span class="sxs-lookup"><span data-stu-id="568e6-107">Each power plan is identified through a unique **GUID** as well as a friendly name.</span></span> <span data-ttu-id="568e6-108">Windows Vista offre trois modes de gestion de l’alimentation par défaut : l’économiseur d’énergie, l’équilibre et les performances élevées.</span><span class="sxs-lookup"><span data-stu-id="568e6-108">Windows Vista has three default power plans: Power Saver, Balanced, and High Performance.</span></span> <span data-ttu-id="568e6-109">Ces plans peuvent être personnalisés et des plans supplémentaires peuvent être créés.</span><span class="sxs-lookup"><span data-stu-id="568e6-109">These plans can be customized, and additional plans can be created.</span></span> <span data-ttu-id="568e6-110">Tous les modes de gestion de l’alimentation ont un attribut de personnalité qui indique le comportement d’économie d’énergie global du plan.</span><span class="sxs-lookup"><span data-stu-id="568e6-110">All power plans have a personality attribute that indicates the overall power savings behavior of the plan.</span></span>

<span data-ttu-id="568e6-111">Le tableau suivant présente les trois personnalités du mode de gestion de l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="568e6-111">The following table shows the three power plan personalities.</span></span> 

| <span data-ttu-id="568e6-112">Nom complet</span><span class="sxs-lookup"><span data-stu-id="568e6-112">Display name</span></span>     | <span data-ttu-id="568e6-113">Description</span><span class="sxs-lookup"><span data-stu-id="568e6-113">Description</span></span>                                                                   | <span data-ttu-id="568e6-114">**GUID**</span><span class="sxs-lookup"><span data-stu-id="568e6-114">**GUID**</span></span>                             |
|------------------|-------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="568e6-115">Économiseur d’énergie</span><span class="sxs-lookup"><span data-stu-id="568e6-115">Power Saver</span></span>      | <span data-ttu-id="568e6-116">Offre des performances réduites, ce qui peut augmenter les économies d’énergie.</span><span class="sxs-lookup"><span data-stu-id="568e6-116">Delivers reduced performance which may increase power savings.</span></span>                | <span data-ttu-id="568e6-117">a1841308-3541-4fab-bc81-f71556f20b4a</span><span class="sxs-lookup"><span data-stu-id="568e6-117">a1841308-3541-4fab-bc81-f71556f20b4a</span></span> |
| <span data-ttu-id="568e6-118">Équilibrée</span><span class="sxs-lookup"><span data-stu-id="568e6-118">Balanced</span></span>         | <span data-ttu-id="568e6-119">Équilibre automatiquement les performances et la consommation d’énergie en fonction de la demande.</span><span class="sxs-lookup"><span data-stu-id="568e6-119">Automatically balances performance and power consumption according to demand.</span></span> | <span data-ttu-id="568e6-120">381b4222-f694-41f0-9685-ff5bb260df2e</span><span class="sxs-lookup"><span data-stu-id="568e6-120">381b4222-f694-41f0-9685-ff5bb260df2e</span></span> |
| <span data-ttu-id="568e6-121">Hautes performances</span><span class="sxs-lookup"><span data-stu-id="568e6-121">High Performance</span></span> | <span data-ttu-id="568e6-122">Offre des performances maximales au détriment de la consommation d’énergie.</span><span class="sxs-lookup"><span data-stu-id="568e6-122">Delivers maximum performance at the expense of higher power consumption.</span></span>      | <span data-ttu-id="568e6-123">8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c</span><span class="sxs-lookup"><span data-stu-id="568e6-123">8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c</span></span> |



 

> [!Note]  
> <span data-ttu-id="568e6-124">Les appareils qui prennent en charge le mode [veille moderne](/windows-hardware/design/device-experiences/modern-standby) autorisent uniquement le mode de gestion de l’alimentation **équilibré** .</span><span class="sxs-lookup"><span data-stu-id="568e6-124">Devices that support [Modern Standby](/windows-hardware/design/device-experiences/modern-standby) mode only allow the **Balanced** power plan.</span></span> <span data-ttu-id="568e6-125">La **mise en veille moderne** est la solution la plus récente et rationalisée pour la gestion des paramètres d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="568e6-125">**Modern Standby** is the newer, more streamlined solution to power settings management.</span></span>

 

<span data-ttu-id="568e6-126">Chaque ordinateur dispose d’un mode de gestion de l’alimentation unique et actif.</span><span class="sxs-lookup"><span data-stu-id="568e6-126">Each computer has a single, active power plan.</span></span> <span data-ttu-id="568e6-127">Par défaut, les utilisateurs non privilégiés sont en mesure d’accéder aux paramètres d’alimentation du système.</span><span class="sxs-lookup"><span data-stu-id="568e6-127">By default, nonprivileged users are able to access system power settings.</span></span> <span data-ttu-id="568e6-128">L’accès à tous les paramètres d’alimentation ou individuels peut être contrôlé via des ACL sur les paramètres d’alimentation ou par le biais de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="568e6-128">Access to all or individual power settings can be controlled through ACLs on the power settings or through Group Policy.</span></span> <span data-ttu-id="568e6-129">Les applications doivent appeler [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) pour déterminer si l’utilisateur a accès au paramètre d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="568e6-129">Applications should call [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) to determine if the user has access to the power setting.</span></span>

<span data-ttu-id="568e6-130">Chaque paramètre d’alimentation est identifié par un **GUID** unique et comprend un nom convivial, une description, des valeurs autorisées et des valeurs par défaut pour AC et DC.</span><span class="sxs-lookup"><span data-stu-id="568e6-130">Each power setting is identified by a unique **GUID** and includes a friendly name, description, allowable values, and default values for AC and DC.</span></span> <span data-ttu-id="568e6-131">Les paramètres d’alimentation personnalisés peuvent être créés à l’aide de la fonction [**PowerCreateSetting**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting) .</span><span class="sxs-lookup"><span data-stu-id="568e6-131">Custom power settings can be created using the [**PowerCreateSetting**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="568e6-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="568e6-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="568e6-133">Modes de gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="568e6-133">Power Schemes</span></span>](power-schemes.md)
</dt> </dl>

 

 
