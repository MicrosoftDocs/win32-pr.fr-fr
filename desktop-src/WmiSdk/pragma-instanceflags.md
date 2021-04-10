---
description: Contrôle la façon dont les instances sont créées ou mises à jour en fonction des indicateurs spécifiés.
ms.assetid: 9932edf2-2e5f-4c5e-9889-f2be4af11bf2
ms.tgt_platform: multiple
title: pragma instanceflags
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: acc05e201fcf153ab2156d4a360ce36b4539cd57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210562"
---
# <a name="pragma-instanceflags"></a><span data-ttu-id="63fc5-103">pragma instanceflags</span><span class="sxs-lookup"><span data-stu-id="63fc5-103">pragma instanceflags</span></span>

<span data-ttu-id="63fc5-104">La commande de préprocesseur **pragma instanceflags** contrôle la manière dont les instances sont créées ou mises à jour en fonction des indicateurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="63fc5-104">The **pragma instanceflags** preprocessor command controls the way instances are created or updated depending on the flags specified.</span></span>

<span data-ttu-id="63fc5-105">Les éléments suivants décrivent la syntaxe :</span><span class="sxs-lookup"><span data-stu-id="63fc5-105">The following describes the syntax:</span></span>


```mof
#pragma instanceflags ([Flag])
```



<span data-ttu-id="63fc5-106">L' *\[ indicateur \]* doit être l’un des arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="63fc5-106">*\[Flag\]* must be one of the following arguments.</span></span>



| <span data-ttu-id="63fc5-107">Indicateur</span><span class="sxs-lookup"><span data-stu-id="63fc5-107">Flag</span></span>       | <span data-ttu-id="63fc5-108">Description</span><span class="sxs-lookup"><span data-stu-id="63fc5-108">Description</span></span>                                                                                                |
|------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63fc5-109">CreateOnly</span><span class="sxs-lookup"><span data-stu-id="63fc5-109">createonly</span></span> | <span data-ttu-id="63fc5-110">Empêche le compilateur de modifier les instances existantes dans le fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="63fc5-110">Prevents the compiler from changing any existing instances in the MOF file.</span></span>                                |
| <span data-ttu-id="63fc5-111">updateonly</span><span class="sxs-lookup"><span data-stu-id="63fc5-111">updateonly</span></span> | <span data-ttu-id="63fc5-112">Empêche le compilateur de créer de nouvelles instances si une instance spécifiée dans le fichier MOF n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="63fc5-112">Prevents the compiler from creating new instances if an instance specified in the MOF file does not exist.</span></span> |



 

## <a name="examples"></a><span data-ttu-id="63fc5-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="63fc5-113">Examples</span></span>

<span data-ttu-id="63fc5-114">L’exemple suivant montre comment utiliser cette commande.</span><span class="sxs-lookup"><span data-stu-id="63fc5-114">The following example shows how to use this command.</span></span>


```mof
#pragma instanceflags("createonly")
```



## <a name="requirements"></a><span data-ttu-id="63fc5-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63fc5-115">Requirements</span></span>



| <span data-ttu-id="63fc5-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63fc5-116">Requirement</span></span> | <span data-ttu-id="63fc5-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="63fc5-117">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="63fc5-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63fc5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="63fc5-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63fc5-119">Windows Vista</span></span><br/>       |
| <span data-ttu-id="63fc5-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63fc5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="63fc5-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63fc5-121">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="63fc5-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63fc5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63fc5-123">Commandes de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="63fc5-123">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




