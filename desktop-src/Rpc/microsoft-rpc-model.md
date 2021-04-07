---
title: Le modèle RPC
description: L’appel de procédure distante (RPC) pour les langages de programmation C et C++ est conçu pour répondre aux besoins des développeurs qui travaillent sur la nouvelle génération de logiciels pour les systèmes d’exploitation Windows.
ms.assetid: ebab41a5-e841-4e0f-8acd-d0aab94f01c1
keywords:
- Appel de procédure distante RPC, décrit, modèle RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e72048b12329133fcc8ce4ee82bce266ed29162
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729413"
---
# <a name="the-rpc-model"></a><span data-ttu-id="080ab-104">Le modèle RPC</span><span class="sxs-lookup"><span data-stu-id="080ab-104">The RPC Model</span></span>

<span data-ttu-id="080ab-105">L’appel de procédure distante (RPC) pour les langages de programmation C et C++ est conçu pour répondre aux besoins des développeurs qui travaillent sur la nouvelle génération de logiciels pour les systèmes d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="080ab-105">Remote Procedure Call (RPC) for the C and C++ programming languages is designed to help meet the needs of developers working on the next generation of software for Windows operating systems.</span></span>

<span data-ttu-id="080ab-106">RPC est un mécanisme de communication interprocessus (IPC) puissant, robuste, efficace et sécurisé qui permet l’échange de données et l’appel de fonctionnalités résidant dans un processus différent.</span><span class="sxs-lookup"><span data-stu-id="080ab-106">RPC is a powerful, robust, efficient, and secure interprocess communication (IPC) mechanism that enables data exchange and invocation of functionality residing in a different process.</span></span> <span data-ttu-id="080ab-107">Ce processus peut se trouver sur le même ordinateur, sur le réseau local ou sur Internet.</span><span class="sxs-lookup"><span data-stu-id="080ab-107">That different process can be on the same machine, on the local area network, or across the Internet.</span></span> <span data-ttu-id="080ab-108">Cette section décrit le modèle de programmation RPC et le modèle pour les systèmes distribués qui peuvent être implémentés à l’aide de RPC.</span><span class="sxs-lookup"><span data-stu-id="080ab-108">This section explains the RPC programming model and the model for distributed systems that can be implemented using RPC.</span></span>

<span data-ttu-id="080ab-109">RPC prend entièrement en charge Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="080ab-109">RPC fully supports 64-bit Windows.</span></span> <span data-ttu-id="080ab-110">Il existe trois types de processus : les processus natifs 32 bits, les processus natifs de 64 bits et les processus 32 bits s’exécutant sous l’émulateur de processus 32 bits sur un système 64 bits (souvent appelé processus WOW64).</span><span class="sxs-lookup"><span data-stu-id="080ab-110">There are three types of processes: native 32-bit processes, native 64-bit processes, and 32-bit processes running under the 32-bit process emulator on a 64-bit system (often referred to as WOW64 processes).</span></span> <span data-ttu-id="080ab-111">Pour plus d’informations sur WOW64, consultez [exécution d’Applications 32 bits](/windows/desktop/WinProg64/running-32-bit-applications).</span><span class="sxs-lookup"><span data-stu-id="080ab-111">For more information about WOW64, see [Running 32-bit Applications](/windows/desktop/WinProg64/running-32-bit-applications).</span></span> <span data-ttu-id="080ab-112">À l’aide de RPC, les développeurs peuvent communiquer en toute transparence entre les différents types de processus ; RPC gère automatiquement les différences de processus en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="080ab-112">Using RPC, developers can transparently communicate between different types of process; RPC automatically manages process differences behind the scenes.</span></span>

<span data-ttu-id="080ab-113">Le RPC a été initialement développé en tant qu’extension de l’appel RPC OSF.</span><span class="sxs-lookup"><span data-stu-id="080ab-113">RPC was initially developed as an extension to OSF RPC.</span></span> <span data-ttu-id="080ab-114">À l’exception de certaines de ses fonctionnalités avancées, RPC est interopérable avec les implémentations d’autres fournisseurs de RPC OSF.</span><span class="sxs-lookup"><span data-stu-id="080ab-114">With the exception of some of its advanced features, RPC is interoperable with other vendors' implementations of OSF RPC.</span></span>

<span data-ttu-id="080ab-115">Cette section fournit également une vue d’ensemble des composants RPC et de leur fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="080ab-115">This section also provides an overview of RPC components and their operation.</span></span> <span data-ttu-id="080ab-116">Les informations sont présentées dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="080ab-116">The information is presented in the following topics:</span></span>

-   [<span data-ttu-id="080ab-117">Le modèle de programmation</span><span class="sxs-lookup"><span data-stu-id="080ab-117">The Programming Model</span></span>](the-programming-model.md)
-   [<span data-ttu-id="080ab-118">Modèle pour les systèmes distribués</span><span class="sxs-lookup"><span data-stu-id="080ab-118">The Model for Distributed Systems</span></span>](the-model-for-distributed-systems.md)
-   [<span data-ttu-id="080ab-119">Fonctionnement de RPC</span><span class="sxs-lookup"><span data-stu-id="080ab-119">How RPC Works</span></span>](how-rpc-works.md)
-   [<span data-ttu-id="080ab-120">Composants Microsoft RPC</span><span class="sxs-lookup"><span data-stu-id="080ab-120">Microsoft RPC Components</span></span>](microsoft-rpc-components.md)

 

 