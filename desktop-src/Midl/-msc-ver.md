---
title: commutateur/msc_ver
description: Le \_ commutateur/MSC ver est utilisé pour permettre à MIDL de générer du code qui comprend des optimisations pour les différentes versions des compilateurs Microsoft C/C++.
ms.assetid: cdcb8f3e-e791-44c2-8bea-e77f94cc1682
keywords:
- /commutateur msc_ver MIDL
topic_type:
- apiref
api_name:
- /msc_ver
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3620b3c8ffb1315a4d34eb0b4b2497c1cb3d805
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841429"
---
# <a name="msc_ver-switch"></a><span data-ttu-id="9a1eb-104">\_commutateur/MSC ver</span><span class="sxs-lookup"><span data-stu-id="9a1eb-104">/msc\_ver switch</span></span>

<span data-ttu-id="9a1eb-105">Le commutateur **/MSC \_ ver** est utilisé pour permettre à MIDL de générer du code qui comprend des optimisations pour les différentes versions des compilateurs Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="9a1eb-105">The **/msc\_ver** switch is used to allow MIDL to generate code that includes optimizations for different versions of Microsoft C/C++ compilers.</span></span>

``` syntax
midl /msc_ver version_number
```

## <a name="switch-options"></a><span data-ttu-id="9a1eb-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="9a1eb-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="9a1eb-107">*Numéro de version \_*</span><span class="sxs-lookup"><span data-stu-id="9a1eb-107">*version\_number*</span></span> 
</dt> <dd>

<span data-ttu-id="9a1eb-108">Spécifie un numéro de version entier du compilateur Microsoft Visual C++ qui sera utilisé pour compiler les stubs client et serveur de l’application distribuée.</span><span class="sxs-lookup"><span data-stu-id="9a1eb-108">Specifies an integer version number of the Microsoft Visual C++ compiler that will be used to compile the client and server stubs of the distributed application.</span></span> <span data-ttu-id="9a1eb-109">Le numéro de version par défaut est 1100, qui correspond à Visual C++ version 5,0.</span><span class="sxs-lookup"><span data-stu-id="9a1eb-109">The default version number is 1100, which corresponds to Visual C++ version 5.0.</span></span> <span data-ttu-id="9a1eb-110">Le numéro de version 1200 correspond à Visual C++ version 6,0, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="9a1eb-110">The version number 1200 corresponds to Visual C++ version 6.0, and so on.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a1eb-111">Notes</span><span class="sxs-lookup"><span data-stu-id="9a1eb-111">Remarks</span></span>

<span data-ttu-id="9a1eb-112">En particulier, les valeurs de version de 1100 ou plus font que le compilateur MIDL génère du code à l’aide de la directive **\_ \_ declspec (UUID ())** .</span><span class="sxs-lookup"><span data-stu-id="9a1eb-112">In particular, version values of 1100 or greater cause the MIDL compiler to generate code utilizing the **\_\_declspec(uuid())** directive.</span></span> <span data-ttu-id="9a1eb-113">Il active également les macros qui utilisent les directives **\_ \_ declspec (selectany)** et **\_ \_ declspec (novtable)** .</span><span class="sxs-lookup"><span data-stu-id="9a1eb-113">It also activates macros that use the **\_\_declspec(selectany)** and **\_\_declspec(novtable)** directives.</span></span>

 

 




