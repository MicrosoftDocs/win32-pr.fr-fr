---
title: /ZP (commutateur)
description: Le commutateur/ZP est le même que l’option/Pack.
ms.assetid: ccdae6a5-e53c-4ddc-9f5f-2b2118709fdb
keywords:
- Le commutateur/ZP MIDL
topic_type:
- apiref
api_name:
- /Zp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553d99dee7dd08218680fc0b43e6e12237c4f8fa
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678306"
---
# <a name="zp-switch"></a><span data-ttu-id="b12a2-104">/ZP (commutateur)</span><span class="sxs-lookup"><span data-stu-id="b12a2-104">/Zp switch</span></span>

<span data-ttu-id="b12a2-105">Le commutateur **/ZP** est le même que l’option [**/Pack**](-pack.md) .</span><span class="sxs-lookup"><span data-stu-id="b12a2-105">The **/Zp** switch is the same as the [**/pack**](-pack.md) option.</span></span>

``` syntax
midl /Zp packing_level
```

## <a name="switch-options"></a><span data-ttu-id="b12a2-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="b12a2-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="b12a2-107">*niveau de compression \_*</span><span class="sxs-lookup"><span data-stu-id="b12a2-107">*packing\_level*</span></span> 
</dt> <dd>

<span data-ttu-id="b12a2-108">Spécifie le niveau de compression des structures dans le système cible.</span><span class="sxs-lookup"><span data-stu-id="b12a2-108">Specifies the packing level of structures in the target system.</span></span> <span data-ttu-id="b12a2-109">La valeur de niveau d’empaquetage peut être définie sur 1, 2, 4 ou 8.</span><span class="sxs-lookup"><span data-stu-id="b12a2-109">The packing-level value can be set to 1, 2, 4, or 8.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b12a2-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b12a2-110">Remarks</span></span>

<span data-ttu-id="b12a2-111">Le commutateur **/ZP** désigne le niveau de compression des structures dans le système cible.</span><span class="sxs-lookup"><span data-stu-id="b12a2-111">The **/Zp** switch designates the packing level of structures in the target system.</span></span> <span data-ttu-id="b12a2-112">La valeur de niveau d’empaquetage correspond à la valeur de l’option **/ZP** utilisée par le compilateur Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="b12a2-112">The packing-level value corresponds to the **/Zp** option value used by the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="b12a2-113">Pour plus d’informations, consultez la documentation de programmation de Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="b12a2-113">For more information, see your Microsoft C/C++ programming documentation.</span></span>

<span data-ttu-id="b12a2-114">Spécifiez le même niveau de compression lorsque vous appelez le compilateur MIDL et le compilateur C.</span><span class="sxs-lookup"><span data-stu-id="b12a2-114">Specify the same packing level when you invoke the MIDL compiler and the C compiler.</span></span>

<span data-ttu-id="b12a2-115">Le niveau de compression par défaut utilisé lorsque le commutateur **/ZP** ou [**/Pack**](-pack.md) n’est pas spécifié est 8 dans tous les environnements de génération.</span><span class="sxs-lookup"><span data-stu-id="b12a2-115">The default packing level used when neither the **/Zp** nor [**/pack**](-pack.md) switch is specified is 8 in all build environments.</span></span>

> [!Note]  
> <span data-ttu-id="b12a2-116">N’utilisez pas **/Zp1** ou **/ZP2** sur des plateformes MIPS ou alpha et n’utilisez pas **/zp4** ou **/Zp8** sur les plateformes 16 bits.</span><span class="sxs-lookup"><span data-stu-id="b12a2-116">Do not use **/Zp1** or **/Zp2** on MIPS or Alpha platforms and do not use **/Zp4** or **/Zp8** on 16-bit platforms.</span></span> <span data-ttu-id="b12a2-117">En fonction du type de données et de l’emplacement de mémoire attribués par le compilateur C au moment de l’exécution, cela peut entraîner une exception de non-alignement des données sur les plateformes MIPS et alpha.</span><span class="sxs-lookup"><span data-stu-id="b12a2-117">Depending on the data type and memory location assigned by the C compiler at run time, this can result in a data misalignment exception on MIPS and Alpha platforms.</span></span> <span data-ttu-id="b12a2-118">Sur les plateformes MS-DOS, le compilateur C ne garantit pas l’alignement à 4 ou 8, et l’application peut donc se terminer.</span><span class="sxs-lookup"><span data-stu-id="b12a2-118">On MS-DOS platforms, the C compiler will not ensure the alignment at 4 or 8, and so the application may terminate.</span></span>

 

## <a name="examples"></a><span data-ttu-id="b12a2-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="b12a2-119">Examples</span></span>

<span data-ttu-id="b12a2-120">**MIDL/zp4 NomFichier. idl**</span><span class="sxs-lookup"><span data-stu-id="b12a2-120">**midl /Zp4 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="b12a2-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b12a2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b12a2-122">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="b12a2-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="b12a2-123">**/Pack**</span><span class="sxs-lookup"><span data-stu-id="b12a2-123">**/pack**</span></span>](-pack.md)
</dt> </dl>

 

 




