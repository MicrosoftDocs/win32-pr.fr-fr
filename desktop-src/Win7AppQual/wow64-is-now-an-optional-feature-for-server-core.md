---
description: .
ms.assetid: 9a918cd3-60a0-4231-975a-bee12de5c812
title: État WoW64 dans Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a121c6bb9c4fb2cd052825bb4c2d5e3dbd0183c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536650"
---
# <a name="wow64-is-now-an-optional-feature-for-server-core"></a><span data-ttu-id="fb18a-103">WoW64 est désormais une fonctionnalité facultative pour Server Core</span><span class="sxs-lookup"><span data-stu-id="fb18a-103">WoW64 Is Now an Optional Feature for Server Core</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="fb18a-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="fb18a-104">Affected Platforms</span></span>

<span data-ttu-id="fb18a-105">**Serveurs** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fb18a-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="fb18a-106">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="fb18a-106">Feature Impact</span></span>

 <span data-ttu-id="fb18a-107">**Gravité** -faible</span><span class="sxs-lookup"><span data-stu-id="fb18a-107">**Severity** - Low</span></span>  
<span data-ttu-id="fb18a-108">**Fréquence** -faible</span><span class="sxs-lookup"><span data-stu-id="fb18a-108">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="fb18a-109">Description</span><span class="sxs-lookup"><span data-stu-id="fb18a-109">Description</span></span>

<span data-ttu-id="fb18a-110">L’option d’installation Server Core pour Windows Server 2008 R2 vous permet de désinstaller WoW64.</span><span class="sxs-lookup"><span data-stu-id="fb18a-110">The Server Core installation option for Windows Server 2008 R2 allows you to uninstall WoW64.</span></span> <span data-ttu-id="fb18a-111">WoW64 est désormais une fonctionnalité facultative que vous pouvez désinstaller si vous n’avez pas besoin d’exécuter du code 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fb18a-111">WoW64 is now an optional feature that you can uninstall if it is not necessary to run 32-bit code.</span></span>

<span data-ttu-id="fb18a-112">En outre, les rôles Active Directory et services AD LDS (Active Directory Lightweight Directory Services) requièrent WoW64 pour s’exécuter dans Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="fb18a-112">In addition, the Active Directory and Active Directory Lightweight Directory Services roles require WoW64 in order to run in Windows Server 2008 R2.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="fb18a-113">Manifeste de l’impact</span><span class="sxs-lookup"><span data-stu-id="fb18a-113">Manifestation of Impact</span></span>

<span data-ttu-id="fb18a-114">Si vous désinstallez WoW64, les administrateurs qui exécutent le code 32 bits sur Server Core recevront un message d’erreur indiquant que l’application ne peut pas être exécutée.</span><span class="sxs-lookup"><span data-stu-id="fb18a-114">If you uninstall WoW64, Administrators running 32-bit code on Server Core will receive an error message that the application cannot be executed.</span></span> <span data-ttu-id="fb18a-115">Si les administrateurs essaient d’exécuter Active Directory et services AD LDS (Active Directory Lightweight Directory Services), ils recevront un message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="fb18a-115">If Administrators attempt to run Active Directory and Active Directory Lightweight Directory Services, they will receive an error message.</span></span>

## <a name="mitigation"></a><span data-ttu-id="fb18a-116">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="fb18a-116">Mitigation</span></span>

<span data-ttu-id="fb18a-117">Installez WoW64.</span><span class="sxs-lookup"><span data-stu-id="fb18a-117">Install WoW64.</span></span>

## <a name="solution"></a><span data-ttu-id="fb18a-118">Solution</span><span class="sxs-lookup"><span data-stu-id="fb18a-118">Solution</span></span>

<span data-ttu-id="fb18a-119">La solution recommandée consiste à fournir une version 64 bits du code pour lui permettre de s’exécuter sur Server Core sans avoir besoin de WoW64.</span><span class="sxs-lookup"><span data-stu-id="fb18a-119">The preferred solution is to provide a 64-bit version of the code to enable it to run on Server Core without needing WoW64.</span></span>

<span data-ttu-id="fb18a-120">Au minimum, fournissez une documentation utilisateur indiquant que pour exécuter le code 32 bits, ils doivent installer WoW64.</span><span class="sxs-lookup"><span data-stu-id="fb18a-120">At a minimum, provide user documentation noting that to run 32-bit code they must install WoW64.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="fb18a-121">Compatibilité, performances, fiabilité et test d’utilisabilité</span><span class="sxs-lookup"><span data-stu-id="fb18a-121">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="fb18a-122">Vérifiez que tout le code utilisé est 64 bits.</span><span class="sxs-lookup"><span data-stu-id="fb18a-122">Verify that all code used is 64-bit.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="fb18a-123">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="fb18a-123">Links to Other Resources</span></span>

-   [<span data-ttu-id="fb18a-124">Détails de l’implémentation WOW64</span><span class="sxs-lookup"><span data-stu-id="fb18a-124">WOW64 Implementation Details</span></span>](../winprog64/wow64-implementation-details.md)
-   [<span data-ttu-id="fb18a-125">Débogage de WOW64</span><span class="sxs-lookup"><span data-stu-id="fb18a-125">Debugging WOW64</span></span>](../winprog64/debugging-wow64.md)
-   <span data-ttu-id="fb18a-126">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fb18a-126">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span></span>

 

 
