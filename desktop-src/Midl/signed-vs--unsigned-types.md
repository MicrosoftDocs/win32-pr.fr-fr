---
title: Types signés et non signés (MIDL)
description: Les compilateurs qui utilisent des valeurs par défaut différentes pour les types signés et non signés peuvent provoquer des erreurs logicielles dans votre application distribuée.
ms.assetid: a4c2d811-6cf4-4c0b-af12-bf8247152984
keywords:
- types de données MIDL, signés et non signés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e38fbe1dc27eebae7c7933db1d699600370d960
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383551"
---
# <a name="signed-and-unsigned-types-midl"></a><span data-ttu-id="e5b40-104">Types signés et non signés (MIDL)</span><span class="sxs-lookup"><span data-stu-id="e5b40-104">Signed and Unsigned Types (MIDL)</span></span>

<span data-ttu-id="e5b40-105">Les compilateurs qui utilisent des valeurs par défaut différentes pour les types signés et non signés peuvent provoquer des erreurs logicielles dans votre application distribuée.</span><span class="sxs-lookup"><span data-stu-id="e5b40-105">Compilers that use different defaults for signed and unsigned types can cause software errors in your distributed application.</span></span> <span data-ttu-id="e5b40-106">Vous pouvez éviter ces problèmes en déclarant explicitement vos types de caractères comme étant signés ou non signés.</span><span class="sxs-lookup"><span data-stu-id="e5b40-106">You can avoid these problems by explicitly declaring your character types as signed or unsigned.</span></span> <span data-ttu-id="e5b40-107">Notez que les compilateurs IDL DCE ne reconnaissent pas le mot clé [**signed**](signed.md).</span><span class="sxs-lookup"><span data-stu-id="e5b40-107">Note that DCE IDL compilers do not recognize the keyword [**signed**](signed.md).</span></span> <span data-ttu-id="e5b40-108">Par conséquent, cette fonctionnalité n’est pas disponible lorsque vous utilisez le commutateur/**OSF** du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="e5b40-108">Therefore, this feature is not available when you use the MIDL compiler /**osf** switch.</span></span>

<span data-ttu-id="e5b40-109">MIDL définit le [**petit**](small.md) type pour qu’il prenne le même signe par défaut que le type [**char**](char-idl.md) dans le compilateur C cible.</span><span class="sxs-lookup"><span data-stu-id="e5b40-109">MIDL defines the [**small**](small.md) type to take the same default sign as the [**char**](char-idl.md) type in the target C compiler.</span></span> <span data-ttu-id="e5b40-110">Si le compilateur suppose que **char** n’est pas signé, **Small** sera également défini comme non signé.</span><span class="sxs-lookup"><span data-stu-id="e5b40-110">If the compiler assumes that **char** is unsigned, **small** will also be defined as unsigned.</span></span> <span data-ttu-id="e5b40-111">De nombreux compilateurs C vous permettent de modifier la valeur par défaut en tant qu’option de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="e5b40-111">Many C compilers let you change the default as a command-line option.</span></span> <span data-ttu-id="e5b40-112">Par exemple, dans l’environnement de développement Microsoft Visual C++, l’option de ligne de commande **/j** modifie la signature par défaut de **char** de signed en non signé.</span><span class="sxs-lookup"><span data-stu-id="e5b40-112">For example, in the Microsoft Visual C++ development environment, the **/J** command-line option changes the default sign of **char** from signed to unsigned.</span></span>

<span data-ttu-id="e5b40-113">Vous pouvez également contrôler le signe des variables de type [**char**](char-idl.md) et [**Small**](small.md) avec le commutateur de ligne de commande du compilateur MIDL [**/char**](-char.md).</span><span class="sxs-lookup"><span data-stu-id="e5b40-113">You can also control the sign of variables of type [**char**](char-idl.md) and [**small**](small.md) with the MIDL compiler command-line switch [**/char**](-char.md).</span></span> <span data-ttu-id="e5b40-114">Ce commutateur vous permet de spécifier le signe par défaut utilisé par votre compilateur.</span><span class="sxs-lookup"><span data-stu-id="e5b40-114">This switch allows you to specify the default sign used by your compiler.</span></span> <span data-ttu-id="e5b40-115">Le compilateur MIDL déclare explicitement le signe de tous les types **char** qui ne correspondent pas à votre type par défaut du compilateur C dans le fichier d’en-tête généré.</span><span class="sxs-lookup"><span data-stu-id="e5b40-115">The MIDL compiler explicitly declares the sign of all **char** types that do not match your C-compiler default type in the generated header file.</span></span>

 

 




