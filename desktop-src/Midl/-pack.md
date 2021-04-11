---
title: commutateur/Pack
description: Le commutateur/Pack est le même que l’option/zp.
ms.assetid: 381e3099-adb4-4219-bbb4-89c9e1dd3928
keywords:
- MIDL du commutateur/Pack
topic_type:
- apiref
api_name:
- /pack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c807846148d81e0e59620046d9f24380fe647c11
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030356"
---
# <a name="pack-switch"></a><span data-ttu-id="d99c4-104">commutateur/Pack</span><span class="sxs-lookup"><span data-stu-id="d99c4-104">/pack switch</span></span>

<span data-ttu-id="d99c4-105">Le commutateur **/Pack** est le même que l’option [**/ZP**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="d99c4-105">The **/pack** switch is the same as the [**/Zp**](-zp.md) option.</span></span>

``` syntax
midl /pack packing_level
```

## <a name="switch-options"></a><span data-ttu-id="d99c4-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="d99c4-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="d99c4-107">*niveau de compression \_*</span><span class="sxs-lookup"><span data-stu-id="d99c4-107">*packing\_level*</span></span> 
</dt> <dd>

<span data-ttu-id="d99c4-108">Spécifie le niveau de compression des structures dans le système cible.</span><span class="sxs-lookup"><span data-stu-id="d99c4-108">Specifies the packing level of structures in the target system.</span></span> <span data-ttu-id="d99c4-109">La valeur de niveau d’empaquetage peut être définie sur 1, 2, 4 ou 8.</span><span class="sxs-lookup"><span data-stu-id="d99c4-109">The packing-level value can be set to 1, 2, 4, or 8.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d99c4-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d99c4-110">Remarks</span></span>

<span data-ttu-id="d99c4-111">Le commutateur **/Pack** désigne le niveau de compression des structures dans le système cible.</span><span class="sxs-lookup"><span data-stu-id="d99c4-111">The **/pack** switch designates the packing level of structures in the target system.</span></span> <span data-ttu-id="d99c4-112">La valeur de niveau d’empaquetage correspond à la valeur de l’option [**/ZP**](-zp.md) utilisée par le compilateur Microsoft C/C++ version 7,0.</span><span class="sxs-lookup"><span data-stu-id="d99c4-112">The packing-level value corresponds to the [**/Zp**](-zp.md) option value used by the Microsoft C/C++ version 7.0 compiler.</span></span> <span data-ttu-id="d99c4-113">Pour plus d’informations, consultez la documentation de programmation de Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="d99c4-113">For more information, see your Microsoft C/C++ programming documentation.</span></span>

<span data-ttu-id="d99c4-114">Spécifiez le même niveau de compression lorsque vous appelez le compilateur MIDL et le compilateur C.</span><span class="sxs-lookup"><span data-stu-id="d99c4-114">Specify the same packing level when you invoke the MIDL compiler and the C compiler.</span></span> <span data-ttu-id="d99c4-115">Le niveau de compression par défaut utilisé lorsque le commutateur [**/ZP**](-zp.md) ou **/Pack** n’est pas spécifié est 8, dans tous les environnements de génération.</span><span class="sxs-lookup"><span data-stu-id="d99c4-115">The default packing level used when neither the [**/Zp**](-zp.md) nor **/pack** switch is specified is 8, in both all build environments.</span></span>

<span data-ttu-id="d99c4-116">Pour plus d’informations sur les risques potentiels liés à l’utilisation de niveaux de compression non standard, consultez la rubrique d’aide [**/ZP**](-zp.md) .</span><span class="sxs-lookup"><span data-stu-id="d99c4-116">For a discussion of the potential dangers in using nonstandard packing levels, see the [**/Zp**](-zp.md) help topic.</span></span>

## <a name="examples"></a><span data-ttu-id="d99c4-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="d99c4-117">Examples</span></span>

<span data-ttu-id="d99c4-118">**MIDL/Pack 2 nom de fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="d99c4-118">**midl /pack 2 filename.idl**</span></span>

<span data-ttu-id="d99c4-119">**MIDL/Pack 8 bar. idl**</span><span class="sxs-lookup"><span data-stu-id="d99c4-119">**midl /pack 8 bar.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="d99c4-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d99c4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d99c4-121">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="d99c4-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="d99c4-122">**/env**</span><span class="sxs-lookup"><span data-stu-id="d99c4-122">**/env**</span></span>](-env.md)
</dt> <dt>

[<span data-ttu-id="d99c4-123">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="d99c4-123">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 




