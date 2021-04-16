---
description: Moniteur réseau capture le trafic réseau à des fins d’affichage et d’analyse. Elle vous permet d’effectuer des tâches telles que l’analyse de données capturées précédemment dans des méthodes définies par l’utilisateur et l’extraction de données à partir d’analyseurs de protocole définis.
ms.assetid: a70b6e22-e744-4760-b878-9ee35428fed5
title: Moniteur réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51a57dd2373d7a10fedd68a72dbc4021efdb921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529745"
---
# <a name="network-monitor"></a><span data-ttu-id="a4bcb-104">Moniteur réseau</span><span class="sxs-lookup"><span data-stu-id="a4bcb-104">Network Monitor</span></span>

## <a name="purpose"></a><span data-ttu-id="a4bcb-105">Objectif</span><span class="sxs-lookup"><span data-stu-id="a4bcb-105">Purpose</span></span>

<span data-ttu-id="a4bcb-106">Moniteur réseau capture le trafic réseau à des fins d’affichage et d’analyse.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-106">Network Monitor captures network traffic for display and analysis.</span></span> <span data-ttu-id="a4bcb-107">Elle vous permet d’effectuer des tâches telles que l’analyse de données capturées précédemment dans des méthodes définies par l’utilisateur et l’extraction de données à partir d’analyseurs de protocole définis.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-107">It enables you to perform tasks such as analyzing previously captured data in user-defined methods and extract data from defined protocol parsers.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a4bcb-108">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="a4bcb-108">Developer audience</span></span>

<span data-ttu-id="a4bcb-109">Tous les jeux d’API fournis par Moniteur réseau sont accessibles à l’aide de C/C++.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-109">All API sets provided by Network Monitor can be accessed using C/C++.</span></span> <span data-ttu-id="a4bcb-110">Les développeurs qui travaillent également avec des [*fournisseurs de paquets réseau*](n.md) doivent également être familiarisés avec com.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-110">Those developers also working with [*network packet providers*](n.md) must also be familiar with COM.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a4bcb-111">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="a4bcb-111">Run-time requirements</span></span>

<span data-ttu-id="a4bcb-112">Pour appeler à partir de l’API Moniteur réseau, vous devez exécuter Windows NT Server 4,0, Windows 2000 Server ou Windows Server 2003, ou disposer de Microsoft Systems Management Server installé.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-112">To call from the Network Monitor API, you must be running on Windows NT Server 4.0, Windows 2000 Server, or Windows Server 2003, or have Microsoft Systems Management Server installed.</span></span>

<span data-ttu-id="a4bcb-113">Le pilote NPP et les fonctionnalités prises en charge incluent toutes les versions de Windows NT 4,0 et Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-113">The NPP driver and supported features include all versions of Windows NT 4.0 and Windows 2000 Server.</span></span>

> [!Note]  
> <span data-ttu-id="a4bcb-114">Moniteur réseau 2,1 et versions antérieures ne sont pas pris en charge sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-114">Network Monitor 2.1 and earlier are not supported on Windows Vista and later.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="a4bcb-115">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="a4bcb-115">In this section</span></span>



| <span data-ttu-id="a4bcb-116">Rubrique</span><span class="sxs-lookup"><span data-stu-id="a4bcb-116">Topic</span></span>                                                                 | <span data-ttu-id="a4bcb-117">Description</span><span class="sxs-lookup"><span data-stu-id="a4bcb-117">Description</span></span>                                                                                           |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4bcb-118">Le kit de développement logiciel Moniteur réseau</span><span class="sxs-lookup"><span data-stu-id="a4bcb-118">The Network Monitor SDK</span></span>](the-network-monitor-sdk.md)<br/>     | <span data-ttu-id="a4bcb-119">Présentation du kit de développement logiciel (SDK) Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-119">Introduction to the Network Monitor SDK.</span></span><br/>                                                   |
| [<span data-ttu-id="a4bcb-120">À propos de Moniteur réseau 2,1</span><span class="sxs-lookup"><span data-stu-id="a4bcb-120">About Network Monitor 2.1</span></span>](about-network-monitor-2-1.md)<br/> | <span data-ttu-id="a4bcb-121">Moniteur réseau les concepts et les services.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-121">Network Monitor concepts and services.</span></span><br/>                                                     |
| [<span data-ttu-id="a4bcb-122">Utilisation de Moniteur réseau 2,1</span><span class="sxs-lookup"><span data-stu-id="a4bcb-122">Using Network Monitor 2.1</span></span>](using-network-monitor-2-1.md)<br/> | <span data-ttu-id="a4bcb-123">Rubriques relatives aux tâches qui décrivent comment utiliser Moniteur réseau fonctions et des composants COM.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-123">Task-related topics that describe how to use Network Monitor functions and COM components.</span></span><br/> |
| [<span data-ttu-id="a4bcb-124">Référence</span><span class="sxs-lookup"><span data-stu-id="a4bcb-124">Reference</span></span>](reference.md)<br/>                                 | <span data-ttu-id="a4bcb-125">Rubriques de référence pour Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-125">Reference topics for Network Monitor.</span></span><br/>                                                      |
| [<span data-ttu-id="a4bcb-126">Glossaire</span><span class="sxs-lookup"><span data-stu-id="a4bcb-126">Glossary</span></span>](glossary.md)<br/>                                   | <span data-ttu-id="a4bcb-127">Définitions et terminologie pour Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="a4bcb-127">Definitions and terminology for Network Monitor.</span></span><br/>                                           |



 

 

 




