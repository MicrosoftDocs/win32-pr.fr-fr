---
title: /commutateur système
description: Le commutateur/système indique au compilateur MIDL de générer une bibliothèque de types pour le système spécifié. La valeur par défaut est le système d’exploitation actuel.
ms.assetid: 0fb69ffc-5ab4-49f3-b34d-859da776ce9e
keywords:
- /commutateur du système MIDL
topic_type:
- apiref
api_name:
- / system
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e09f2cf97f8edb86ad831cff35420fad9a07d76
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312655"
---
# <a name="system-switch"></a><span data-ttu-id="68bdc-105">/<system> Utilisez</span><span class="sxs-lookup"><span data-stu-id="68bdc-105">/<system> switch</span></span>

<span data-ttu-id="68bdc-106">Le **/<system>** commutateur indique au compilateur MIDL de générer une bibliothèque de types pour le système spécifié.</span><span class="sxs-lookup"><span data-stu-id="68bdc-106">The **/<system>** switch directs the MIDL compiler to generate a type library for the specified system.</span></span> <span data-ttu-id="68bdc-107">La valeur par défaut est le système d’exploitation actuel.</span><span class="sxs-lookup"><span data-stu-id="68bdc-107">The default is the current operating system.</span></span>

``` syntax
midl /{win32 | ia64 | amd64}
```

## <a name="switch-options"></a><span data-ttu-id="68bdc-108">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="68bdc-108">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span data-ttu-id="68bdc-109"><span id="win32"></span><span id="WIN32"></span>Win32 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="68bdc-109"><span id="win32"></span><span id="WIN32"></span>\*\*\*\*win32\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="68bdc-110">Windows 2000, Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="68bdc-110">Windows 2000, Windows XP, Windows Vista, Windows 7</span></span>

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span data-ttu-id="68bdc-111"><span id="ia64"></span><span id="IA64"></span>ia64 \* \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="68bdc-111"><span id="ia64"></span><span id="IA64"></span>\*\*\*\*ia64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="68bdc-112">Environnement Windows 64 bits basé sur Intel, tel que Windows 2000, Windows Server 2003, Windows XP Professionnel Édition x64, Windows Vista ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="68bdc-112">An Intel-based 64-bit Windows environment such as Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista, or Windows 7.</span></span>

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span data-ttu-id="68bdc-113"><span id="amd64"></span><span id="AMD64"></span>amd64 \* \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="68bdc-113"><span id="amd64"></span><span id="AMD64"></span>\*\*\*\*amd64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="68bdc-114">Un environnement Windows 64 bits basé sur des micro-appareils américain, tel que Windows 2000, Windows Server 2003, Windows XP Professionnel Édition x64, Windows Vista ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="68bdc-114">An American Micro Devices-based 64-bit Windows environment such as Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista, or Windows 7.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68bdc-115">Notes</span><span class="sxs-lookup"><span data-stu-id="68bdc-115">Remarks</span></span>

<span data-ttu-id="68bdc-116">Le **/<system>** commutateur est fonctionnellement identique à l’option de MIDL [**/env**](-env.md) et est reconnu par le compilateur MIDL uniquement pour la compatibilité descendante avec mktyplib.</span><span class="sxs-lookup"><span data-stu-id="68bdc-116">The **/<system>** switch is functionally the same as the MIDL [**/env**](-env.md) option and is recognized by the MIDL compiler solely for backward compatibility with MkTypLib.</span></span> <span data-ttu-id="68bdc-117">Si vous générez un nouveau Makefile, utilisez le commutateur **/env** .</span><span class="sxs-lookup"><span data-stu-id="68bdc-117">If you are generating a new makefile, use the **/env** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="68bdc-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="68bdc-118">Examples</span></span>

<span data-ttu-id="68bdc-119">**MIDL/Win32 NomFichier. idl**</span><span class="sxs-lookup"><span data-stu-id="68bdc-119">**midl /win32 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="68bdc-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68bdc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68bdc-121">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="68bdc-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="68bdc-122">**/env**</span><span class="sxs-lookup"><span data-stu-id="68bdc-122">**/env**</span></span>](-env.md)
</dt> </dl>

 

 




