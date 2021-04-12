---
title: Utilisation du compilateur MIDL
description: Le compilateur MIDL est installé automatiquement dans le cadre de l’installation du kit de développement logiciel (SDK) de la plateforme.
ms.assetid: 6c001b06-01f3-42bd-85db-5d53aab54903
keywords:
- Microsoft Interface Definition Language MIDL, tâches
- MIDL du compilateur MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fd6630a8e3fcb5c46325b5258da567fcbd0eec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381905"
---
# <a name="using-the-midl-compiler"></a><span data-ttu-id="ce1c0-105">Utilisation du compilateur MIDL</span><span class="sxs-lookup"><span data-stu-id="ce1c0-105">Using the MIDL Compiler</span></span>

<span data-ttu-id="ce1c0-106">Le compilateur MIDL est installé automatiquement dans le cadre de l’installation du kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="ce1c0-106">The MIDL compiler is automatically installed as part of the Platform Software Development Kit (SDK) setup.</span></span> <span data-ttu-id="ce1c0-107">Les rubriques suivantes décrivent les conditions requises pour le compilateur C MIDL et le préprocesseur C, les bibliothèques de liens qui font partie du produit d’appel de procédure distante (RPC) et les fichiers générés par MIDL pour les interfaces DCOM, les interfaces RPC et les interfaces de la bibliothèque de types OLE Automation.</span><span class="sxs-lookup"><span data-stu-id="ce1c0-107">The following topics describe the MIDL C compiler and C preprocessor requirements, the link libraries that are part of the Remote Procedure Call (RPC) product, and the files that MIDL generates for DCOM interfaces, RPC interfaces, and OLE Automation type library interfaces.</span></span>

-   [<span data-ttu-id="ce1c0-108">Appel du compilateur MIDL</span><span class="sxs-lookup"><span data-stu-id="ce1c0-108">Invoking the MIDL Compiler</span></span>](invoking-the-midl-compiler.md)
-   [<span data-ttu-id="ce1c0-109">Fichiers réponse</span><span class="sxs-lookup"><span data-stu-id="ce1c0-109">Response Files</span></span>](response-files.md)
-   [<span data-ttu-id="ce1c0-110">C-Configuration requise pour le préprocesseur pour MIDL</span><span class="sxs-lookup"><span data-stu-id="ce1c0-110">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
-   [<span data-ttu-id="ce1c0-111">C/C++-considérations relatives au compilateur</span><span class="sxs-lookup"><span data-stu-id="ce1c0-111">C/C++-Compiler Considerations</span></span>](c-c-compiler-considerations.md)
-   [<span data-ttu-id="ce1c0-112">Utilisation de la \_ \_ constante prédéfinie MIDL</span><span class="sxs-lookup"><span data-stu-id="ce1c0-112">Using the \_\_midl Predefined Constant</span></span>](using-the---midl-predefined-constant.md)
-   [<span data-ttu-id="ce1c0-113">MIDL et RPC</span><span class="sxs-lookup"><span data-stu-id="ce1c0-113">MIDL and RPC</span></span>](midl-and-rpc.md)
-   [<span data-ttu-id="ce1c0-114">MIDL et COM</span><span class="sxs-lookup"><span data-stu-id="ce1c0-114">MIDL and COM</span></span>](midl-and-com.md)
-   [<span data-ttu-id="ce1c0-115">MIDL et ODL</span><span class="sxs-lookup"><span data-stu-id="ce1c0-115">MIDL and ODL</span></span>](midl-and-odl.md)

<span data-ttu-id="ce1c0-116">Pour plus d’informations sur les fichiers qui composent le produit RPC, consultez [installation de l’environnement de programmation RPC](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span><span class="sxs-lookup"><span data-stu-id="ce1c0-116">For more information about the files that make up the RPC product, see [Installing the RPC Programming Environment](/windows/desktop/Rpc/installing-the-rpc-programming-environment).</span></span>

 

 