---
description: Étend les applications écrites à l’aide de technologies basées sur COM.
ms.assetid: b21a6b08-c17c-4fcc-bc60-39037bc9902f
title: COM+ (services de composants)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b778c31957ddfe3f71db23b2f5be2a3ee681fde0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950604"
---
# <a name="com-component-services"></a><span data-ttu-id="61c36-103">COM+ (services de composants)</span><span class="sxs-lookup"><span data-stu-id="61c36-103">COM+ (Component Services)</span></span>

## <a name="purpose"></a><span data-ttu-id="61c36-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="61c36-104">Purpose</span></span>

<span data-ttu-id="61c36-105">COM+ est une évolution de Microsoft Component Object Model (COM) et de Microsoft Transaction Server (MTS).</span><span class="sxs-lookup"><span data-stu-id="61c36-105">COM+ is an evolution of Microsoft Component Object Model (COM) and Microsoft Transaction Server (MTS).</span></span> <span data-ttu-id="61c36-106">COM+ s’appuie sur et étend les applications écrites à l’aide de COM, MTS et d’autres technologies basées sur COM.</span><span class="sxs-lookup"><span data-stu-id="61c36-106">COM+ builds on and extends applications written using COM, MTS, and other COM-based technologies.</span></span> <span data-ttu-id="61c36-107">COM+ gère de nombreuses tâches de gestion des ressources que vous deviez programmer vous-même, telles que l’allocation et la sécurité des threads.</span><span class="sxs-lookup"><span data-stu-id="61c36-107">COM+ handles many of the resource management tasks that you previously had to program yourself, such as thread allocation and security.</span></span> <span data-ttu-id="61c36-108">COM+ rend également vos applications plus évolutives en fournissant le regroupement des threads, le regroupement d’objets et l’activation d’objets juste-à-temps.</span><span class="sxs-lookup"><span data-stu-id="61c36-108">COM+ also makes your applications more scalable by providing thread pooling, object pooling, and just-in-time object activation.</span></span> <span data-ttu-id="61c36-109">COM+ vous aide également à protéger l’intégrité de vos données en assurant la prise en charge des transactions, même si une transaction s’étend sur plusieurs bases de données sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="61c36-109">COM+ also helps protect the integrity of your data by providing transaction support, even if a transaction spans multiple databases over a network.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="61c36-110">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="61c36-110">Where applicable</span></span>

<span data-ttu-id="61c36-111">COM+ peut être utilisé pour développer des applications distribuées à l’ensemble de l’entreprise et stratégiques pour Windows.</span><span class="sxs-lookup"><span data-stu-id="61c36-111">COM+ can be used to develop enterprise-wide, mission-critical, distributed applications for Windows.</span></span>

<span data-ttu-id="61c36-112">Si vous êtes un administrateur système, vous allez installer, déployer et configurer des applications COM+ et leurs composants.</span><span class="sxs-lookup"><span data-stu-id="61c36-112">If you are a system administrator, you will be installing, deploying, and configuring COM+ applications and their components.</span></span> <span data-ttu-id="61c36-113">Si vous êtes programmeur d’applications, vous allez écrire des composants et les intégrer en tant qu’applications.</span><span class="sxs-lookup"><span data-stu-id="61c36-113">If you are an application programmer, you will be writing components and integrating them as applications.</span></span> <span data-ttu-id="61c36-114">Si vous êtes un fournisseur d’outils, vous allez développer ou modifier des outils pour travailler dans l’environnement COM+.</span><span class="sxs-lookup"><span data-stu-id="61c36-114">If you are a tools vendor, you will be developing or modifying tools to work in the COM+ environment.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="61c36-115">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="61c36-115">Developer audience</span></span>

<span data-ttu-id="61c36-116">COM+ est principalement conçu pour les développeurs de Microsoft Visual C++ et Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="61c36-116">COM+ is designed primarily for Microsoft Visual C++ and Microsoft Visual Basic developers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="61c36-117">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="61c36-117">Run-time requirements</span></span>

<span data-ttu-id="61c36-118">La version 1,5 de COM+ est incluse dans Windows à partir de Windows XP et de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="61c36-118">COM+ version 1.5 is included in Windows starting with Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="61c36-119">COM+ version 1,0 est inclus dans Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="61c36-119">COM+ version 1.0 is included in Windows 2000.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="61c36-120">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="61c36-120">In this section</span></span>

-   [<span data-ttu-id="61c36-121">Nouveautés de COM+ 1,5</span><span class="sxs-lookup"><span data-stu-id="61c36-121">What's New in COM+ 1.5</span></span>](what-s-new-in-com--1-5.md)
-   [<span data-ttu-id="61c36-122">Vue d’ensemble des développeurs COM+</span><span class="sxs-lookup"><span data-stu-id="61c36-122">COM+ Developers Overview</span></span>](com--developers-overview.md)
-   [<span data-ttu-id="61c36-123">Services COM+</span><span class="sxs-lookup"><span data-stu-id="61c36-123">COM+ Services</span></span>](com--services.md)
-   [<span data-ttu-id="61c36-124">Tâches générales de COM+</span><span class="sxs-lookup"><span data-stu-id="61c36-124">COM+ General Tasks</span></span>](com--general-tasks.md)
-   [<span data-ttu-id="61c36-125">Référence COM+</span><span class="sxs-lookup"><span data-stu-id="61c36-125">COM+ Reference</span></span>](com--reference.md)

## <a name="related-topics"></a><span data-ttu-id="61c36-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="61c36-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61c36-127">COM</span><span class="sxs-lookup"><span data-stu-id="61c36-127">COM</span></span>](/windows/desktop/com/component-object-model--com--portal)
</dt> </dl>

 

 
