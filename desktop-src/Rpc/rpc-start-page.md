---
title: Appel de procédure distante
description: L’appel de procédure distante Microsoft (RPC) définit une technologie puissante pour la création de programmes clients/serveurs distribués.
ms.assetid: 27c7c352-5fc1-47cf-99b1-fdf3eca986bc
keywords:
- RPC
- RPC, (voir appel de procédure distante)
- Appel de procédure distante RPC, page de démarrage
- RPC appel de procédure distante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3461116468bf1d686d1a5695924e5fe66007b35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382495"
---
# <a name="remote-procedure-call"></a><span data-ttu-id="30904-107">Appel de procédure distante</span><span class="sxs-lookup"><span data-stu-id="30904-107">Remote Procedure Call</span></span>

## <a name="purpose"></a><span data-ttu-id="30904-108">Objectif</span><span class="sxs-lookup"><span data-stu-id="30904-108">Purpose</span></span>

<span data-ttu-id="30904-109">L’appel de procédure distante Microsoft (RPC) définit une technologie puissante pour la création de programmes clients/serveurs distribués.</span><span class="sxs-lookup"><span data-stu-id="30904-109">Microsoft Remote Procedure Call (RPC) defines a powerful technology for creating distributed client/server programs.</span></span> <span data-ttu-id="30904-110">Les stubs et les bibliothèques Runtime RPC gèrent la plupart des processus relatifs aux protocoles réseau et aux communications.</span><span class="sxs-lookup"><span data-stu-id="30904-110">The RPC run-time stubs and libraries manage most of the processes relating to network protocols and communication.</span></span> <span data-ttu-id="30904-111">Cela vous permet de vous concentrer sur les détails de l’application plutôt que sur les détails du réseau.</span><span class="sxs-lookup"><span data-stu-id="30904-111">This enables you to focus on the details of the application rather than the details of the network.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="30904-112">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="30904-112">Where applicable</span></span>

<span data-ttu-id="30904-113">RPC peut être utilisé dans toutes les applications client/serveur basées sur les systèmes d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="30904-113">RPC can be used in all client/server applications based on Windows operating systems.</span></span> <span data-ttu-id="30904-114">Il peut également être utilisé pour créer des programmes client et serveur pour les environnements réseau hétérogènes qui incluent des systèmes d’exploitation tels que UNIX et Apple.</span><span class="sxs-lookup"><span data-stu-id="30904-114">It can also be used to create client and server programs for heterogeneous network environments that include such operating systems as Unix and Apple.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="30904-115">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="30904-115">Developer audience</span></span>

<span data-ttu-id="30904-116">RPC est conçu pour être utilisé par les programmeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="30904-116">RPC is designed to be used by C/C++ programmers.</span></span> <span data-ttu-id="30904-117">Vous devez vous familiariser avec le Microsoft Interface Definition Language (MIDL) et le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="30904-117">Familiarity with the Microsoft Interface Definition Language (MIDL) and the MIDL compiler are required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="30904-118">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="30904-118">Run-time requirements</span></span>

<span data-ttu-id="30904-119">Les bibliothèques Runtime RPC sont incluses avec Windows.</span><span class="sxs-lookup"><span data-stu-id="30904-119">The RPC run-time libraries are included with Windows.</span></span> <span data-ttu-id="30904-120">Les composants de l’environnement de développement RPC sont installés lorsque vous installez le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="30904-120">The components of the RPC development environment are installed when you install the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="30904-121">Pour plus d’informations, consultez [installation de l’environnement de programmation RPC](installing-the-rpc-programming-environment.md).</span><span class="sxs-lookup"><span data-stu-id="30904-121">For details, see [Installing the RPC Programming Environment](installing-the-rpc-programming-environment.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="30904-122">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="30904-122">In this section</span></span>



| <span data-ttu-id="30904-123">Rubrique</span><span class="sxs-lookup"><span data-stu-id="30904-123">Topic</span></span>                                                                           | <span data-ttu-id="30904-124">Description</span><span class="sxs-lookup"><span data-stu-id="30904-124">Description</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30904-125">Meilleures pratiques de programmation RPC</span><span class="sxs-lookup"><span data-stu-id="30904-125">Best RPC Programming Practices</span></span>](best-rpc-programming-practices.md)<br/> | <span data-ttu-id="30904-126">Conseils sur les pratiques de programmation RPC qui permettent de créer les meilleures applications RPC possibles.</span><span class="sxs-lookup"><span data-stu-id="30904-126">Guidance on RPC programming practices that help create the best possible RPC applications.</span></span><br/>                            |
| [<span data-ttu-id="30904-127">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="30904-127">Overview</span></span>](overviews.md)<br/>                                            | <span data-ttu-id="30904-128">Informations générales sur l’incorporation de RPC dans vos applications client/serveur.</span><span class="sxs-lookup"><span data-stu-id="30904-128">General information about incorporating RPC into your client/server applications.</span></span><br/>                                     |
| [<span data-ttu-id="30904-129">Référence</span><span class="sxs-lookup"><span data-stu-id="30904-129">Reference</span></span>](reference.md)<br/>                                           | <span data-ttu-id="30904-130">Documentation des types, fonctions et constantes RPC.</span><span class="sxs-lookup"><span data-stu-id="30904-130">Documentation of RPC types, functions, and constants.</span></span><br/>                                                                 |
| [<span data-ttu-id="30904-131">Moteur de rapport de non-remise RPC</span><span class="sxs-lookup"><span data-stu-id="30904-131">RPC NDR Engine</span></span>](rpc-ndr-engine.md)<br/>                                 | <span data-ttu-id="30904-132">Documentation du moteur de marshaling pour les composants RPC et DCOM, le moteur de représentation de données réseau (NDR) RPC.</span><span class="sxs-lookup"><span data-stu-id="30904-132">Documentation of the marshaling engine for RPC and DCOM components, the RPC Network Data Representation (NDR) Engine.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="30904-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="30904-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30904-134">Microsoft Interface Definition Language (MIDL)</span><span class="sxs-lookup"><span data-stu-id="30904-134">Microsoft Interface Definition Language (MIDL)</span></span>](/windows/desktop/Midl/midl-start-page)
</dt> </dl>

 

