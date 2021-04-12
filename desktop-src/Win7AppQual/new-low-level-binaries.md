---
description: .
ms.assetid: 8c883462-29d8-46c4-b1c6-3ae8b8d3b397
title: Nouveaux binaires de Low-Level
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6b6e197f22df9fb3d6e12aeeff3c5f4a2a0e41c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209660"
---
# <a name="new-low-level-binaries"></a><span data-ttu-id="6ec61-103">Nouveaux binaires de Low-Level</span><span class="sxs-lookup"><span data-stu-id="6ec61-103">New Low-Level Binaries</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="6ec61-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="6ec61-104">Affected Platforms</span></span>

<span data-ttu-id="6ec61-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="6ec61-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="6ec61-106">**Serveurs** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6ec61-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="6ec61-107">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="6ec61-107">Feature Impact</span></span>

<span data-ttu-id="6ec61-108">**Gravité** -moyenne</span><span class="sxs-lookup"><span data-stu-id="6ec61-108">**Severity** - Medium</span></span>  
<span data-ttu-id="6ec61-109">**Fréquence** -élevée</span><span class="sxs-lookup"><span data-stu-id="6ec61-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="6ec61-110">Description</span><span class="sxs-lookup"><span data-stu-id="6ec61-110">Description</span></span>

<span data-ttu-id="6ec61-111">Pour améliorer l’efficacité de l’ingénierie interne et améliorer les fondations pour un travail futur, nous avons déplacé certaines fonctionnalités vers de nouveaux binaires de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="6ec61-111">To improve internal engineering efficiencies and improve foundations for future work, we have relocated some functionality to new low-level binaries.</span></span> <span data-ttu-id="6ec61-112">Cette refactorisation permettra aux futures installations de Windows de fournir des sous-ensembles de fonctionnalités pour réduire la surface d’exposition (exigences en termes de disque et de mémoire, de maintenance et de surface d’attaque).</span><span class="sxs-lookup"><span data-stu-id="6ec61-112">This refactoring will make it possible for future installs of Windows to provide subsets of functionality to reduce surface area (disk and memory requirements, servicing, and attack surface).</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="6ec61-113">Manifeste de l’impact</span><span class="sxs-lookup"><span data-stu-id="6ec61-113">Manifestation of Impact</span></span>

<span data-ttu-id="6ec61-114">En guise d’exemple de fonctionnalité que nous avons déplacée vers des binaires de bas niveau, kernelbase.dll obtient les fonctionnalités de kernel32.dll et de advapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="6ec61-114">As an example of functionality that we moved to low-level binaries, kernelbase.dll gets functionality from kernel32.dll and advapi32.dll.</span></span> <span data-ttu-id="6ec61-115">Cela signifie que le fichier binaire existant transfère désormais les appels vers le nouveau fichier binaire plutôt que de les gérer directement. le transfert peut être statique (la table d’exportation indique la redirection) ou le runtime (la dll a une routine stub qui appelle le nouveau binaire).</span><span class="sxs-lookup"><span data-stu-id="6ec61-115">This means that the existing binary now forwards calls down to the new binary rather than handling them directly; the forwarding can be static (the export table shows the redirection), or runtime (the dll has a stub routine that calls down to the new binary).</span></span> <span data-ttu-id="6ec61-116">Cela aura un impact sur les applications de bas niveau, telles que la sécurité et les applications de sauvegarde, qui dépendent des API internes et des décalages.</span><span class="sxs-lookup"><span data-stu-id="6ec61-116">This will impact low-level applications such as security and backup applications that are dependent upon internal APIs and offsets.</span></span>

## <a name="solution"></a><span data-ttu-id="6ec61-117">Solution</span><span class="sxs-lookup"><span data-stu-id="6ec61-117">Solution</span></span>

<span data-ttu-id="6ec61-118">Le seul impact est le code qui émet des hypothèses lorsqu’il tente d’examiner la kernel32.dll ou la table d’exportation advapi32.dll en mémoire, par exemple une application antivirus.</span><span class="sxs-lookup"><span data-stu-id="6ec61-118">The only impact is to code that makes assumptions when attempting to look at the kernel32.dll or the advapi32.dll export table in memory, such as an anti-virus application might do.</span></span> <span data-ttu-id="6ec61-119">Utilisez les API publiées et non les détails de leur implémentation.</span><span class="sxs-lookup"><span data-stu-id="6ec61-119">Use published APIs and not the details of their implementation.</span></span> <span data-ttu-id="6ec61-120">Il ne s’agit là que d’un exemple de mise en œuvre d’un détail d’implémentation pour une API.</span><span class="sxs-lookup"><span data-stu-id="6ec61-120">This is just one example of implementing around a detail of implementation for an API.</span></span>

 

 



