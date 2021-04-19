---
description: Suivez les instructions générales relatives à l’application des modules de fusion décrits dans application de fusion modules.
ms.assetid: 6035b1a9-d452-4020-9fe3-c20ba874a2ed
title: Application d’un module de fusion configurable avec des personnalisations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f1e3da426ba5ca13e149814ab9bb927e83d4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517799"
---
# <a name="applying-a-configurable-merge-module-with-customizations"></a><span data-ttu-id="a1f02-103">Application d’un module de fusion configurable avec des personnalisations</span><span class="sxs-lookup"><span data-stu-id="a1f02-103">Applying a Configurable Merge Module with Customizations</span></span>

<span data-ttu-id="a1f02-104">Suivez les instructions générales relatives à l’application des modules de fusion décrits dans [application de fusion modules](applying-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="a1f02-104">Follow the general guidelines for applying merge modules described in [Applying Merge Modules](applying-merge-modules.md).</span></span> <span data-ttu-id="a1f02-105">En outre, les consommateurs de module de fusion doivent effectuer les opérations suivantes pour configurer un module de fusion au moment de l’installation :</span><span class="sxs-lookup"><span data-stu-id="a1f02-105">In addition, merge module consumers must do the following to configure a merge module at the time of installation:</span></span>

-   <span data-ttu-id="a1f02-106">Utilisez un module de fusion créé pour avoir des paramètres configurables.</span><span class="sxs-lookup"><span data-stu-id="a1f02-106">Use a merge module that is authored to have configurable settings.</span></span> <span data-ttu-id="a1f02-107">Pour plus d’informations, consultez [création d’un module de fusion qui peut être configuré par l’utilisateur final](creating-a-merge-module-that-can-be-configured-by-the-end-user.md) .</span><span class="sxs-lookup"><span data-stu-id="a1f02-107">For more information, see [Creating a Merge Module that Can Be Configured by the End-User](creating-a-merge-module-that-can-be-configured-by-the-end-user.md)</span></span>
-   <span data-ttu-id="a1f02-108">Utilisez un outil de fusion et de configuration qui appelle Mergemod.dll version 2,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a1f02-108">Use a merge and configuration tool that calls Mergemod.dll version 2.0 or later.</span></span> <span data-ttu-id="a1f02-109">Les versions antérieures de Mergmod.dll ne peuvent pas configurer les paramètres de module de fusion.</span><span class="sxs-lookup"><span data-stu-id="a1f02-109">Earlier versions of Mergmod.dll cannot configure merge module settings.</span></span> <span data-ttu-id="a1f02-110">Les auteurs doivent créer des modules de fusion qui fournissent des valeurs par défaut et sont compatibles avec les versions antérieures de Mergmod.dll.</span><span class="sxs-lookup"><span data-stu-id="a1f02-110">Authors should create merge modules that provide default values and are compatible with earlier versions of Mergmod.dll.</span></span>
-   <span data-ttu-id="a1f02-111">Fournissez des informations de personnalisation lorsque l’outil client de configuration vous y invite.</span><span class="sxs-lookup"><span data-stu-id="a1f02-111">Provide customization information when prompted by the configuration client tool.</span></span> <span data-ttu-id="a1f02-112">Les auteurs doivent créer des modules de fusion qui utilisent des valeurs par défaut lorsqu’un utilisateur refuse de fournir des informations.</span><span class="sxs-lookup"><span data-stu-id="a1f02-112">Authors should create merge modules that use default values when a user declines to provide information.</span></span>

 

 



