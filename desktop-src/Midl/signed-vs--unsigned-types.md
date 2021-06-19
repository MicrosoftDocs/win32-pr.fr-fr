---
title: Types signés et non signés (MIDL)
description: En savoir plus sur les types signés et non signés dans MIDL. Les compilateurs qui utilisent différents types par défaut peuvent provoquer des erreurs logicielles dans votre application distribuée.
ms.assetid: a4c2d811-6cf4-4c0b-af12-bf8247152984
keywords:
- types de données MIDL, signés et non signés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a3ed3c9f7022123f162fe0240ae190cdb4c8f8
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407382"
---
# <a name="signed-and-unsigned-types-midl"></a><span data-ttu-id="cd016-105">Types signés et non signés (MIDL)</span><span class="sxs-lookup"><span data-stu-id="cd016-105">Signed and Unsigned Types (MIDL)</span></span>

<span data-ttu-id="cd016-106">Les compilateurs qui utilisent des valeurs par défaut différentes pour les types signés et non signés peuvent provoquer des erreurs logicielles dans votre application distribuée.</span><span class="sxs-lookup"><span data-stu-id="cd016-106">Compilers that use different defaults for signed and unsigned types can cause software errors in your distributed application.</span></span> <span data-ttu-id="cd016-107">Vous pouvez éviter ces problèmes en déclarant explicitement vos types de caractères comme étant signés ou non signés.</span><span class="sxs-lookup"><span data-stu-id="cd016-107">You can avoid these problems by explicitly declaring your character types as signed or unsigned.</span></span> <span data-ttu-id="cd016-108">Notez que les compilateurs IDL DCE ne reconnaissent pas le mot clé [**signed**](signed.md).</span><span class="sxs-lookup"><span data-stu-id="cd016-108">Note that DCE IDL compilers do not recognize the keyword [**signed**](signed.md).</span></span> <span data-ttu-id="cd016-109">Par conséquent, cette fonctionnalité n’est pas disponible lorsque vous utilisez le commutateur/**OSF** du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="cd016-109">Therefore, this feature is not available when you use the MIDL compiler /**osf** switch.</span></span>

<span data-ttu-id="cd016-110">MIDL définit le [**petit**](small.md) type pour qu’il prenne le même signe par défaut que le type [**char**](char-idl.md) dans le compilateur C cible.</span><span class="sxs-lookup"><span data-stu-id="cd016-110">MIDL defines the [**small**](small.md) type to take the same default sign as the [**char**](char-idl.md) type in the target C compiler.</span></span> <span data-ttu-id="cd016-111">Si le compilateur suppose que **char** n’est pas signé, **Small** sera également défini comme non signé.</span><span class="sxs-lookup"><span data-stu-id="cd016-111">If the compiler assumes that **char** is unsigned, **small** will also be defined as unsigned.</span></span> <span data-ttu-id="cd016-112">De nombreux compilateurs C vous permettent de modifier la valeur par défaut en tant qu’option de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="cd016-112">Many C compilers let you change the default as a command-line option.</span></span> <span data-ttu-id="cd016-113">Par exemple, dans l’environnement de développement Microsoft Visual C++, l’option de ligne de commande **/j** modifie la signature par défaut de **char** de signed en non signé.</span><span class="sxs-lookup"><span data-stu-id="cd016-113">For example, in the Microsoft Visual C++ development environment, the **/J** command-line option changes the default sign of **char** from signed to unsigned.</span></span>

<span data-ttu-id="cd016-114">Vous pouvez également contrôler le signe des variables de type [**char**](char-idl.md) et [**Small**](small.md) avec le commutateur de ligne de commande du compilateur MIDL [**/char**](-char.md).</span><span class="sxs-lookup"><span data-stu-id="cd016-114">You can also control the sign of variables of type [**char**](char-idl.md) and [**small**](small.md) with the MIDL compiler command-line switch [**/char**](-char.md).</span></span> <span data-ttu-id="cd016-115">Ce commutateur vous permet de spécifier le signe par défaut utilisé par votre compilateur.</span><span class="sxs-lookup"><span data-stu-id="cd016-115">This switch allows you to specify the default sign used by your compiler.</span></span> <span data-ttu-id="cd016-116">Le compilateur MIDL déclare explicitement le signe de tous les types **char** qui ne correspondent pas à votre type par défaut du compilateur C dans le fichier d’en-tête généré.</span><span class="sxs-lookup"><span data-stu-id="cd016-116">The MIDL compiler explicitly declares the sign of all **char** types that do not match your C-compiler default type in the generated header file.</span></span>

 

 




