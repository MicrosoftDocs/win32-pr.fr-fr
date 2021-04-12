---
title: commutateur/env
description: Le commutateur/env sélectionne l’environnement dans lequel l’application s’exécute.
ms.assetid: 70a548c8-fdc3-48f3-a865-14ba9b29fb02
keywords:
- MIDL du commutateur/env
topic_type:
- apiref
api_name:
- /env
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59da7185900d4b75781916bd6b4a9d70bf39dc85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381824"
---
# <a name="env-switch"></a><span data-ttu-id="6a0ff-104">commutateur/env</span><span class="sxs-lookup"><span data-stu-id="6a0ff-104">/env switch</span></span>

<span data-ttu-id="6a0ff-105">Le commutateur **/env** sélectionne l’environnement dans lequel l’application s’exécute.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-105">The **/env** switch selects the environment in which the application runs.</span></span>

``` syntax
midl /env { win32 | ia64 | amd64 | win64 }
```

## <a name="switch-options"></a><span data-ttu-id="6a0ff-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="6a0ff-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span data-ttu-id="6a0ff-107"><span id="win32"></span><span id="WIN32"></span>Win32 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="6a0ff-107"><span id="win32"></span><span id="WIN32"></span>\*\*\*\*win32\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="6a0ff-108">Indique au compilateur MIDL de générer des fichiers stub, ou un fichier bibliothèque de types, pour un environnement 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-108">Directs the MIDL compiler to generate stub files, or a type library file, for a 32-bit environment.</span></span>

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span data-ttu-id="6a0ff-109"><span id="ia64"></span><span id="IA64"></span>ia64 \* \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="6a0ff-109"><span id="ia64"></span><span id="IA64"></span>\*\*\*\*ia64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="6a0ff-110">Indique au compilateur MIDL de générer des fichiers stub, ou un fichier bibliothèque de types, pour un environnement Intel architecture 64 bits (IA64).</span><span class="sxs-lookup"><span data-stu-id="6a0ff-110">Directs the MIDL compiler to generate stub files, or a type library file, for a Intel Architecture 64-bit (IA64) environment.</span></span>

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span data-ttu-id="6a0ff-111"><span id="amd64"></span><span id="AMD64"></span>amd64 \* \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="6a0ff-111"><span id="amd64"></span><span id="AMD64"></span>\*\*\*\*amd64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="6a0ff-112">Indique au compilateur MIDL de générer des fichiers stub, ou un fichier bibliothèque de types, pour un environnement Advanced Micro Devices 64 bits (AMD64).</span><span class="sxs-lookup"><span data-stu-id="6a0ff-112">Directs the MIDL compiler to generate stub files, or a type library file, for an Advanced Micro Devices 64-bit (AMD64) environment.</span></span>

</dd> <dt>

<span id="win64"></span><span id="WIN64"></span>

<span data-ttu-id="6a0ff-113"><span id="win64"></span><span id="WIN64"></span>Win64 \* \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="6a0ff-113"><span id="win64"></span><span id="WIN64"></span>\*\*\*\*win64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="6a0ff-114">Même comportement que *ia64*.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-114">Same behavior as *ia64*.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a0ff-115">Notes</span><span class="sxs-lookup"><span data-stu-id="6a0ff-115">Remarks</span></span>

<span data-ttu-id="6a0ff-116">Le commutateur **/env** affecte principalement le niveau de compression utilisé pour les structures dans cet environnement.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-116">The **/env** switch primarily affects the packing level used for structures in that environment.</span></span> <span data-ttu-id="6a0ff-117">Veillez à spécifier le même paramètre de niveau d’empaquetage pour le compilateur MIDL et le compilateur C.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-117">Be sure you specify the same packing-level setting for both the MIDL compiler and the C compiler.</span></span>

<span data-ttu-id="6a0ff-118">Le commutateur **/env** détermine le niveau de compression et d’autres paramètres comme suit :</span><span class="sxs-lookup"><span data-stu-id="6a0ff-118">The **/env** switch determines the packing level and other settings as follows:</span></span>

-   <span data-ttu-id="6a0ff-119">Lorsque vous spécifiez **Win32**, les stubs générés utilisent le niveau de compactage du compilateur C 8 pour tous les types impliqués dans les opérations distantes.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-119">When you specify **win32**, generated stubs use C-compiler packing-level 8 for all types involved in remote operations.</span></span> <span data-ttu-id="6a0ff-120">Les types de données [**int**](int.md) sont à la fois 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-120">The [**int**](int.md) data types are both 32 bits.</span></span> <span data-ttu-id="6a0ff-121">Les pointeurs sont 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-121">Pointers are 32 bits.</span></span>
-   <span data-ttu-id="6a0ff-122">Lorsque vous spécifiez **ia64** ou **amd64**, le compilateur MIDL s’exécute en mode cross-compiler pour la plateforme (Intel ou AMD) 64 bits indiquée.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-122">When you specify **ia64** or **amd64**, the MIDL compiler runs in a cross-compiler mode for the indicated (Intel or AMD) 64-bit platform.</span></span> <span data-ttu-id="6a0ff-123">Les stubs générés utilisent le niveau de compactage du compilateur C 8 pour tous les types impliqués dans les opérations distantes.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-123">The generated stubs use C-compiler packing-level 8 for all types involved in remote operations.</span></span> <span data-ttu-id="6a0ff-124">Les types de données [**long**](long.md) et [**int**](int.md) sont 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-124">The [**long**](long.md) and [**int**](int.md) data types are 32 bits.</span></span> <span data-ttu-id="6a0ff-125">Les pointeurs sont 64 bits.</span><span class="sxs-lookup"><span data-stu-id="6a0ff-125">Pointers are 64 bits.</span></span>

<span data-ttu-id="6a0ff-126">Les commutateurs [**/align**](-align.md), [**/Pack**](-pack.md)et [**/ZP**](-zp.md) ont la priorité sur les paramètres **/env** .</span><span class="sxs-lookup"><span data-stu-id="6a0ff-126">The [**/align**](-align.md), [**/pack**](-pack.md), and [**/Zp**](-zp.md) switches take precedence over the **/env** settings.</span></span>

<span data-ttu-id="6a0ff-127">Pour plus d’informations sur la prise en charge de 64 bits pour MIDL et RPC, consultez [conception d’interfaces compatibles avec 64 bits](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces).</span><span class="sxs-lookup"><span data-stu-id="6a0ff-127">For more information on 64 bit support for MIDL and RPC see [Designing 64-bit-Compatible Interfaces](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces).</span></span>

## <a name="examples"></a><span data-ttu-id="6a0ff-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="6a0ff-128">Examples</span></span>

<span data-ttu-id="6a0ff-129">**MIDL/env Win32 nom_fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="6a0ff-129">**midl /env win32 filename.idl**</span></span>

<span data-ttu-id="6a0ff-130">**MIDL/env ia64 NomFichier. idl**</span><span class="sxs-lookup"><span data-stu-id="6a0ff-130">**midl /env ia64 filename.idl**</span></span>

<span data-ttu-id="6a0ff-131">**MIDL/env fichier amd64. idl**</span><span class="sxs-lookup"><span data-stu-id="6a0ff-131">**midl /env amd64 filename.idl**</span></span>

<span data-ttu-id="6a0ff-132">**MIDL/env Win64 NomFichier. idl**</span><span class="sxs-lookup"><span data-stu-id="6a0ff-132">**midl /env win64 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="6a0ff-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a0ff-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a0ff-134">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="6a0ff-134">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="6a0ff-135">**/Pack**</span><span class="sxs-lookup"><span data-stu-id="6a0ff-135">**/pack**</span></span>](-pack.md)
</dt> <dt>

[<span data-ttu-id="6a0ff-136">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="6a0ff-136">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 