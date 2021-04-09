---
description: Les classes de gestion de service WMI sont utilisées pour gérer le service WMI lui-même, et non le système informatique ou le réseau d’entreprise. La gestion de WMI englobe la configuration du service WMI et la gestion des opérations WMI.
ms.assetid: EF58AC04-FE04-4D0C-A5F7-3491C885A0E4
ms.tgt_platform: multiple
title: Classes de gestion des services WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502abebbddfd2ce90562045a8b0d7acd3974171
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110214"
---
# <a name="wmi-service-management-classes"></a><span data-ttu-id="63529-104">Classes de gestion des services WMI</span><span class="sxs-lookup"><span data-stu-id="63529-104">WMI Service Management Classes</span></span>

<span data-ttu-id="63529-105">Les classes de gestion de service WMI sont utilisées pour gérer le service WMI lui-même, et non le système informatique ou le réseau d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="63529-105">WMI service management classes are used to manage the WMI service itself and not the computer system or enterprise network.</span></span> <span data-ttu-id="63529-106">La gestion de WMI englobe la configuration du service WMI et la gestion des opérations WMI.</span><span class="sxs-lookup"><span data-stu-id="63529-106">Managing WMI encompasses both configuring the WMI service and managing WMI operations.</span></span>

<span data-ttu-id="63529-107">La catégorie gestion des services WMI comprend les sous-catégories de classes suivantes :</span><span class="sxs-lookup"><span data-stu-id="63529-107">The WMI Service Management category includes the following subcategories of classes:</span></span>

-   [<span data-ttu-id="63529-108">Classes de configuration WMI</span><span class="sxs-lookup"><span data-stu-id="63529-108">WMI configuration classes</span></span>](#wmi-configuration-classes)
-   [<span data-ttu-id="63529-109">Classes de gestion WMI</span><span class="sxs-lookup"><span data-stu-id="63529-109">WMI management classes</span></span>](#wmi-management-classes)

## <a name="wmi-configuration-classes"></a><span data-ttu-id="63529-110">Classes de configuration WMI</span><span class="sxs-lookup"><span data-stu-id="63529-110">WMI Configuration Classes</span></span>

<span data-ttu-id="63529-111">La classe de configuration WMI dérive les méthodes qui configurent le service WMI.</span><span class="sxs-lookup"><span data-stu-id="63529-111">The WMI Configuration class derives methods that configure the WMI service.</span></span>

<span data-ttu-id="63529-112">Voici un tableau des classes de configuration WMI.</span><span class="sxs-lookup"><span data-stu-id="63529-112">The following is a table of WMI configuration classes.</span></span>



| <span data-ttu-id="63529-113">Classe</span><span class="sxs-lookup"><span data-stu-id="63529-113">Class</span></span>                                                             | <span data-ttu-id="63529-114">Description</span><span class="sxs-lookup"><span data-stu-id="63529-114">Description</span></span>                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="63529-115">**\_MethodParameterClass Win32**</span><span class="sxs-lookup"><span data-stu-id="63529-115">**Win32\_MethodParameterClass**</span></span>](win32-methodparameterclass.md) | <span data-ttu-id="63529-116">Abstraite, classe de base qui implémente les paramètres de méthode dérivés de cette classe.</span><span class="sxs-lookup"><span data-stu-id="63529-116">Abstract, base class that implements method parameters derived from this class.</span></span> |



 

## <a name="wmi-management-classes"></a><span data-ttu-id="63529-117">Classes de gestion WMI</span><span class="sxs-lookup"><span data-stu-id="63529-117">WMI Management Classes</span></span>

<span data-ttu-id="63529-118">Les classes de gestion WMI représentent les paramètres opérationnels du service WMI.</span><span class="sxs-lookup"><span data-stu-id="63529-118">The WMI management classes represent operational parameters for the WMI service.</span></span>

<span data-ttu-id="63529-119">Voici un tableau des classes de gestion WMI.</span><span class="sxs-lookup"><span data-stu-id="63529-119">The following is a table of WMI management classes.</span></span>



| <span data-ttu-id="63529-120">Classe</span><span class="sxs-lookup"><span data-stu-id="63529-120">Class</span></span>                                                       | <span data-ttu-id="63529-121">Description</span><span class="sxs-lookup"><span data-stu-id="63529-121">Description</span></span>                                                                                   |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63529-122">**\_WMISetting Win32**</span><span class="sxs-lookup"><span data-stu-id="63529-122">**Win32\_WMISetting**</span></span>](win32-wmisetting.md)               | <span data-ttu-id="63529-123">Contient les paramètres opérationnels du service WMI.</span><span class="sxs-lookup"><span data-stu-id="63529-123">Contains the operational parameters for the WMI service.</span></span>                                      |
| [<span data-ttu-id="63529-124">**\_WMIElementSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="63529-124">**Win32\_WMIElementSetting**</span></span>](win32-wmielementsetting.md) | <span data-ttu-id="63529-125">Association entre un service s’exécutant dans le système Windows et les paramètres WMI qu’il peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="63529-125">Association between a service running in the Windows system, and the WMI settings it can use.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="63529-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="63529-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63529-127">Classes Win32</span><span class="sxs-lookup"><span data-stu-id="63529-127">Win32 Classes</span></span>](./win32-provider.md)
</dt> </dl>

 

 
