---
title: Microsoft Interface Definition Language
description: Le Microsoft Interface Definition Language (MIDL) définit des interfaces entre les programmes client et serveur.
ms.assetid: 5ed1ff94-bbcb-4c6e-83aa-63d24eb84859
keywords:
- MIDL MIDL
- MIDL MIDL, (voir Microsoft Interface Definition Language MIDL)
- Microsoft Interface Definition Language MIDL
- Microsoft Interface Definition Language MIDL, page de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e274d66ae234205f5db1f41b2d191ea409561bd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031137"
---
# <a name="microsoft-interface-definition-language"></a><span data-ttu-id="8a12f-107">Microsoft Interface Definition Language</span><span class="sxs-lookup"><span data-stu-id="8a12f-107">Microsoft Interface Definition Language</span></span>

## <a name="purpose"></a><span data-ttu-id="8a12f-108">Objectif</span><span class="sxs-lookup"><span data-stu-id="8a12f-108">Purpose</span></span>

<span data-ttu-id="8a12f-109">Le Microsoft Interface Definition Language (MIDL) définit des interfaces entre les programmes client et serveur.</span><span class="sxs-lookup"><span data-stu-id="8a12f-109">The Microsoft Interface Definition Language (MIDL) defines interfaces between client and server programs.</span></span> <span data-ttu-id="8a12f-110">Microsoft comprend le compilateur MIDL avec le kit de développement logiciel (SDK) de la plateforme pour permettre aux développeurs de créer les fichiers IDL (Interface Definition Language) et les fichiers de configuration d’application (ACF) requis pour les interfaces RPC (Remote Procedure Call) et les interfaces COM/DCOM.</span><span class="sxs-lookup"><span data-stu-id="8a12f-110">Microsoft includes the MIDL compiler with the Platform Software Development Kit (SDK) to enable developers to create the interface definition language (IDL) files and application configuration files (ACF) required for remote procedure call (RPC) interfaces and COM/DCOM interfaces.</span></span> <span data-ttu-id="8a12f-111">MIDL prend également en charge la génération de bibliothèques de types pour OLE Automation.</span><span class="sxs-lookup"><span data-stu-id="8a12f-111">MIDL also supports the generation of type libraries for OLE Automation.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="8a12f-112">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="8a12f-112">Where applicable</span></span>

<span data-ttu-id="8a12f-113">MIDL peut être utilisé dans toutes les applications client/serveur basées sur les systèmes d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="8a12f-113">MIDL can be used in all client/server applications based on Windows operating systems.</span></span> <span data-ttu-id="8a12f-114">Il peut également être utilisé pour créer des programmes client et serveur pour les environnements réseau hétérogènes qui incluent des systèmes d’exploitation tels que UNIX et Apple.</span><span class="sxs-lookup"><span data-stu-id="8a12f-114">It can also be used to create client and server programs for heterogeneous network environments that include such operating systems as Unix and Apple.</span></span> <span data-ttu-id="8a12f-115">Microsoft prend en charge la norme DCE Open Group (anciennement Open Software Foundation) pour l’interopérabilité RPC.</span><span class="sxs-lookup"><span data-stu-id="8a12f-115">Microsoft supports the Open Group (formerly known as the Open Software Foundation) DCE standard for RPC interoperability.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="8a12f-116">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="8a12f-116">Developer audience</span></span>

<span data-ttu-id="8a12f-117">Lors de l’utilisation de MIDL avec RPC, vous devez vous familiariser avec la programmation C/C++ et le paradigme RPC.</span><span class="sxs-lookup"><span data-stu-id="8a12f-117">When using MIDL with RPC, familiarity with C/C++ programming and the RPC paradigm is required.</span></span> <span data-ttu-id="8a12f-118">Lors de l’utilisation de MIDL avec COM, vous devez vous familiariser avec la programmation C++ et le paradigme RPC tel qu’il s’applique à COM. vous pouvez également vous familiariser avec les bibliothèques de types et de scripts de modèle OLE Automation.</span><span class="sxs-lookup"><span data-stu-id="8a12f-118">When using MIDL with COM, familiarity with C++ programming and the RPC paradigm as it applies to COM is required, or alternatively, familiarity with OLE Automation model scripting and type libraries is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="8a12f-119">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="8a12f-119">Run-time requirements</span></span>

<span data-ttu-id="8a12f-120">Les bibliothèques Runtime appropriées pour l’utilisation de MIDL sont fournies avec Windows.</span><span class="sxs-lookup"><span data-stu-id="8a12f-120">The appropriate run-time libraries for using MIDL are included with Windows.</span></span> <span data-ttu-id="8a12f-121">Le compilateur MIDL et les composants de l’environnement de développement RPC sont installés lorsque vous installez le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="8a12f-121">The MIDL compiler and the components of the RPC development environment are installed when you install the Windows SDK.</span></span> <span data-ttu-id="8a12f-122">Pour plus d’informations, consultez [utilisation du compilateur MIDL](using-the-midl-compiler-2.md) et [installation de l’environnement de programmation RPC](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span><span class="sxs-lookup"><span data-stu-id="8a12f-122">For more information, see [Using the MIDL Compiler](using-the-midl-compiler-2.md) and [Installing the RPC Programming Environment](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8a12f-123">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="8a12f-123">In this section</span></span>



| <span data-ttu-id="8a12f-124">Rubrique</span><span class="sxs-lookup"><span data-stu-id="8a12f-124">Topic</span></span>                                                                                               | <span data-ttu-id="8a12f-125">Description</span><span class="sxs-lookup"><span data-stu-id="8a12f-125">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a12f-126">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="8a12f-126">Overview</span></span>](about-this-guide-2.md)<br/>                                                       | <span data-ttu-id="8a12f-127">Informations générales sur MIDL et le compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="8a12f-127">General information about MIDL and the MIDL compiler.</span></span><br/>                   |
| [<span data-ttu-id="8a12f-128">Utilisation du compilateur MIDL</span><span class="sxs-lookup"><span data-stu-id="8a12f-128">Using the MIDL Compiler</span></span>](using-the-midl-compiler-2.md)<br/>                                 | <span data-ttu-id="8a12f-129">Informations sur l’utilisation du compilateur prend MIDL pour générer des stubs RPC.</span><span class="sxs-lookup"><span data-stu-id="8a12f-129">Information about using the MIDL compilter to generate RPC stubs.</span></span><br/>       |
| [<span data-ttu-id="8a12f-130">Définitions d’interface et bibliothèques de types</span><span class="sxs-lookup"><span data-stu-id="8a12f-130">Interface Definitions and Type Libraries</span></span>](interface-definitions-and-type-libraries.md)<br/> | <span data-ttu-id="8a12f-131">Documentation des définitions d’interface spécifiques à RPC et des bibliothèques de types.</span><span class="sxs-lookup"><span data-stu-id="8a12f-131">Documentation of RPC-specific interface definitions and type libraries.</span></span><br/> |
| [<span data-ttu-id="8a12f-132">Référence de Command-Line MIDL</span><span class="sxs-lookup"><span data-stu-id="8a12f-132">MIDL Command-Line Reference</span></span>](midl-command-line-reference.md)<br/>                           | <span data-ttu-id="8a12f-133">Documentation des commutateurs de ligne de commande du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="8a12f-133">Documentation of the MIDL compiler command-line switches.</span></span><br/>               |
| [<span data-ttu-id="8a12f-134">Référence du langage MIDL</span><span class="sxs-lookup"><span data-stu-id="8a12f-134">MIDL Language Reference</span></span>](midl-language-reference.md)<br/>                                   | <span data-ttu-id="8a12f-135">Référence du langage du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="8a12f-135">The MIDL compiler language reference.</span></span><br/>                                   |



 

## <a name="related-topics"></a><span data-ttu-id="8a12f-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8a12f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a12f-137">Appel de procédure distante (RPC)</span><span class="sxs-lookup"><span data-stu-id="8a12f-137">Remote Procedure Call (RPC)</span></span>](/windows/desktop/Rpc/rpc-start-page)
</dt> </dl>

 

