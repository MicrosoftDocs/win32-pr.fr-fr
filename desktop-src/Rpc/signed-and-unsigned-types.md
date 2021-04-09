---
title: Types signés et non signés (RPC)
description: Les compilateurs qui utilisent des valeurs par défaut différentes pour les types signés et non signés peuvent provoquer des erreurs logicielles dans votre application distribuée.
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453d45d0a4c29a2e30449fb645e6f40338eac546
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103842997"
---
# <a name="signed-and-unsigned-types-rpc"></a><span data-ttu-id="2e680-103">Types signés et non signés (RPC)</span><span class="sxs-lookup"><span data-stu-id="2e680-103">Signed and Unsigned Types (RPC)</span></span>

<span data-ttu-id="2e680-104">Les compilateurs qui utilisent des valeurs par défaut différentes pour les types signés et non signés peuvent provoquer des erreurs logicielles dans votre application distribuée.</span><span class="sxs-lookup"><span data-stu-id="2e680-104">Compilers that use different defaults for signed and unsigned types can cause software errors in your distributed application.</span></span> <span data-ttu-id="2e680-105">Vous pouvez éviter ces problèmes en déclarant explicitement vos types de caractères comme étant **signés** ou **non signés**.</span><span class="sxs-lookup"><span data-stu-id="2e680-105">You can avoid these problems by explicitly declaring your character types as **signed** or **unsigned**.</span></span>

<span data-ttu-id="2e680-106">MIDL définit le [**petit**](/windows/desktop/Midl/small) type pour qu’il prenne le même signe par défaut que le type **char** dans le compilateur C cible.</span><span class="sxs-lookup"><span data-stu-id="2e680-106">MIDL defines the [**small**](/windows/desktop/Midl/small) type to take the same default sign as the **char** type in the target C compiler.</span></span> <span data-ttu-id="2e680-107">Si le compilateur suppose que **char** n’est pas signé, **Small** sera également défini comme non signé.</span><span class="sxs-lookup"><span data-stu-id="2e680-107">If the compiler assumes that **char** is unsigned, **small** will also be defined as unsigned.</span></span> <span data-ttu-id="2e680-108">De nombreux compilateurs C vous permettent de modifier la valeur par défaut en tant qu’option de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="2e680-108">Many C compilers let you change the default as a command-line option.</span></span> <span data-ttu-id="2e680-109">Par exemple, l’option de ligne de commande de Microsoft C compiler **/j** change la signature par défaut de **char** de signed en non signé.</span><span class="sxs-lookup"><span data-stu-id="2e680-109">For example, the Microsoft C compiler **/J** command-line option changes the default sign of **char** from signed to unsigned.</span></span>

<span data-ttu-id="2e680-110">Vous pouvez également contrôler le signe des variables de type **char** et **Small** avec le commutateur de ligne de commande du compilateur MIDL [**/char**](/windows/desktop/Midl/-char).</span><span class="sxs-lookup"><span data-stu-id="2e680-110">You can also control the sign of variables of type **char** and **small** with the MIDL compiler command-line switch [**/char**](/windows/desktop/Midl/-char).</span></span> <span data-ttu-id="2e680-111">Ce commutateur vous permet de spécifier le signe par défaut utilisé par votre compilateur.</span><span class="sxs-lookup"><span data-stu-id="2e680-111">This switch allows you to specify the default sign used by your compiler.</span></span> <span data-ttu-id="2e680-112">Le compilateur MIDL déclare explicitement le signe de tous les types **char** qui ne correspondent pas à votre type par défaut du compilateur C dans le fichier d’en-tête généré.</span><span class="sxs-lookup"><span data-stu-id="2e680-112">The MIDL compiler explicitly declares the sign of all **char** types that do not match your C-compiler default type in the generated header file.</span></span>

 

 
