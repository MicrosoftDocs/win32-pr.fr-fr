---
title: commutateur/prefix
description: Le commutateur/prefix indique au compilateur MIDL d’ajouter des chaînes de préfixe aux noms de routines du client et/ou du stub serveur.
ms.assetid: 5530e972-08bf-4cca-9bb4-9631db824bdb
keywords:
- MIDL du commutateur/prefix
topic_type:
- apiref
api_name:
- /prefix
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79885a57f257fe2648a27fd67a014421b2c1c13a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104507626"
---
# <a name="prefix-switch"></a><span data-ttu-id="5bc94-104">commutateur/prefix</span><span class="sxs-lookup"><span data-stu-id="5bc94-104">/prefix switch</span></span>

<span data-ttu-id="5bc94-105">Le commutateur **/prefix** indique au compilateur MIDL d’ajouter des chaînes de préfixe aux noms de routines du client et/ou du stub serveur.</span><span class="sxs-lookup"><span data-stu-id="5bc94-105">The **/prefix** switch directs the MIDL compiler to add prefix strings to the client and/or server stub routine names.</span></span> <span data-ttu-id="5bc94-106">Cela peut être utilisé pour permettre à un seul programme d’être à la fois un client et un serveur de la même interface, sans que les noms de routines côté client et côté serveur ne soient en conflit.</span><span class="sxs-lookup"><span data-stu-id="5bc94-106">This can be used to allow a single program to be both a client and server of the same interface, without having the client- and server-side routine names conflict with each other.</span></span>

``` syntax
midl /prefix { client | cstub | server | sstub | switch | all }
```

## <a name="switch-options"></a><span data-ttu-id="5bc94-107">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="5bc94-107">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="client"></span><span id="CLIENT"></span>

<span data-ttu-id="5bc94-108"><span id="client"></span><span id="CLIENT"></span>client \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="5bc94-108"><span id="client"></span><span id="CLIENT"></span>\*\*\*\*client\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="5bc94-109">Affecte uniquement les noms de routines stub client.</span><span class="sxs-lookup"><span data-stu-id="5bc94-109">Affects only the client stub routine names.</span></span>

</dd> <dt>

<span id="cstub"></span><span id="CSTUB"></span>

<span data-ttu-id="5bc94-110"><span id="cstub"></span><span id="CSTUB"></span>cstub\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5bc94-110"><span id="cstub"></span><span id="CSTUB"></span>\*\*\*\*cstub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="5bc94-111">Identique au *client*.</span><span class="sxs-lookup"><span data-stu-id="5bc94-111">Same as *client*.</span></span> <span data-ttu-id="5bc94-112">Affecte uniquement les noms de routines stub client.</span><span class="sxs-lookup"><span data-stu-id="5bc94-112">Affects only the client stub routine names.</span></span>

</dd> <dt>

<span id="server"></span><span id="SERVER"></span>

<span data-ttu-id="5bc94-113"><span id="server"></span><span id="SERVER"></span>serveur \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="5bc94-113"><span id="server"></span><span id="SERVER"></span>\*\*\*\*server\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="5bc94-114">Affecte uniquement les noms de routines appelés par la routine de stub serveur.</span><span class="sxs-lookup"><span data-stu-id="5bc94-114">Affects only the routine names called by the server stub routine.</span></span>

</dd> <dt>

<span id="sstub"></span><span id="SSTUB"></span>

<span data-ttu-id="5bc94-115"><span id="sstub"></span><span id="SSTUB"></span>sstub\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5bc94-115"><span id="sstub"></span><span id="SSTUB"></span>\*\*\*\*sstub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="5bc94-116">Identique au *serveur*.</span><span class="sxs-lookup"><span data-stu-id="5bc94-116">Same as *server*.</span></span> <span data-ttu-id="5bc94-117">Affecte uniquement les noms de routines appelés par la routine de stub serveur.</span><span class="sxs-lookup"><span data-stu-id="5bc94-117">Affects only the routine names called by the server stub routine.</span></span>

</dd> <dt>

<span id="switch"></span><span id="SWITCH"></span>

<span data-ttu-id="5bc94-118"><span id="switch"></span><span id="SWITCH"></span>commutateur \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="5bc94-118"><span id="switch"></span><span id="SWITCH"></span>\*\*\*\*switch\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="5bc94-119">Affecte un prototype supplémentaire ajouté au fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="5bc94-119">Affects an extra prototype added to the header file.</span></span>

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span data-ttu-id="5bc94-120"><span id="all"></span><span id="ALL"></span>tous les \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="5bc94-120"><span id="all"></span><span id="ALL"></span>\*\*\*\*all\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="5bc94-121">Affecte à la fois les noms de routines du client et du serveur.</span><span class="sxs-lookup"><span data-stu-id="5bc94-121">Affects both the client and server stub routine names.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5bc94-122">Notes</span><span class="sxs-lookup"><span data-stu-id="5bc94-122">Remarks</span></span>

<span data-ttu-id="5bc94-123">Si le préfixe pour les routines côté client est différent du préfixe pour les routines côté serveur, le fichier d’en-tête généré aura à la fois des prototypes de routine côté client et des prototypes de routine côté serveur.</span><span class="sxs-lookup"><span data-stu-id="5bc94-123">If the prefix for the client-side routines is different from the prefix for the server-side routines, the generated header file will have both client-side routine prototypes and server-side routine prototypes.</span></span>

<span data-ttu-id="5bc94-124">Le commutateur **/prefix** est utile lorsqu’un seul fichier d’en-tête est utilisé avec les stubs de plusieurs exécutions du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="5bc94-124">The **/prefix** switch is useful when a single header file will be used with stubs from multiple runs of the MIDL compiler.</span></span> <span data-ttu-id="5bc94-125">Cela force des prototypes de routine supplémentaires dans le fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="5bc94-125">This forces additional routine prototypes in the header file.</span></span>

<span data-ttu-id="5bc94-126">Dans tous les cas, les préfixes client, serveur et commutateur remplacent un préfixe All.</span><span class="sxs-lookup"><span data-stu-id="5bc94-126">In all cases, the client, server, and switch prefixes will override an all prefix.</span></span>

## <a name="examples"></a><span data-ttu-id="5bc94-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="5bc94-127">Examples</span></span>

<span data-ttu-id="5bc94-128">**MIDL/prefix client « c \_ » serveur « s \_ »**</span><span class="sxs-lookup"><span data-stu-id="5bc94-128">**midl /prefix client "c\_" server "s\_"**</span></span>

<span data-ttu-id="5bc94-129">**MIDL/prefix tous « mugissement \_ »**</span><span class="sxs-lookup"><span data-stu-id="5bc94-129">**midl /prefix all "moo\_"**</span></span>

<span data-ttu-id="5bc94-130">**MIDL/prefix client « écorce \_ »**</span><span class="sxs-lookup"><span data-stu-id="5bc94-130">**midl /prefix client "bark\_"**</span></span>

## <a name="see-also"></a><span data-ttu-id="5bc94-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bc94-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bc94-132">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="5bc94-132">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




