---
description: Supprime une instance existante d’une classe du référentiel.
ms.assetid: 4389f831-a60e-4198-a55a-79189d10a38a
ms.tgt_platform: multiple
title: pragma DeleteInstance
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
ms.openlocfilehash: 10d4c735f1e59533b57ae1814cfb8e36b2c1ad76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034141"
---
# <a name="pragma-deleteinstance"></a><span data-ttu-id="43225-103">pragma DeleteInstance</span><span class="sxs-lookup"><span data-stu-id="43225-103">pragma deleteinstance</span></span>

<span data-ttu-id="43225-104">La commande **pragma DeleteInstance** supprime une instance existante d’une classe du référentiel.</span><span class="sxs-lookup"><span data-stu-id="43225-104">The **pragma deleteinstance** command deletes an existing instance of a class from the repository.</span></span>

<span data-ttu-id="43225-105">La syntaxe de cette commande est décrite ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="43225-105">The following describes the syntax for this command:</span></span>


```mof
#pragma deleteinstance("InstanceId", [Flag])
```



<span data-ttu-id="43225-106">*InstanceID* est un identificateur unique de l’instance que le compilateur MOF supprime de l’espace de noms actuel.</span><span class="sxs-lookup"><span data-stu-id="43225-106">*InstanceId* is a unique identifier of the instance the MOF compiler deletes from the current namespace.</span></span>

<span data-ttu-id="43225-107">L' *\[ indicateur \]* doit être l’un des arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="43225-107">*\[Flag\]* must be one of the following arguments.</span></span>



| <span data-ttu-id="43225-108">Indicateur</span><span class="sxs-lookup"><span data-stu-id="43225-108">Flag</span></span>   | <span data-ttu-id="43225-109">Description</span><span class="sxs-lookup"><span data-stu-id="43225-109">Description</span></span>                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43225-110">Échec</span><span class="sxs-lookup"><span data-stu-id="43225-110">fail</span></span>   | <span data-ttu-id="43225-111">Provoque la fermeture du compilateur MOF avec un message d’erreur si la classe n’existe pas déjà dans le référentiel.</span><span class="sxs-lookup"><span data-stu-id="43225-111">Causes the MOF compiler to quit with an error message if the class does not already exist in the repository.</span></span> |
| <span data-ttu-id="43225-112">nofail</span><span class="sxs-lookup"><span data-stu-id="43225-112">nofail</span></span> | <span data-ttu-id="43225-113">Fait en sorte que le compilateur MOF continue même si la classe n’existe pas déjà.</span><span class="sxs-lookup"><span data-stu-id="43225-113">Causes the MOF compiler to continue even if the class does not already exist.</span></span>                                |



 

## <a name="examples"></a><span data-ttu-id="43225-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="43225-114">Examples</span></span>

<span data-ttu-id="43225-115">L’exemple suivant montre comment utiliser cette commande.</span><span class="sxs-lookup"><span data-stu-id="43225-115">The following example shows how to use this command.</span></span>


```mof
#pragma deleteinstance(
    "MSFT_RisingFallingTemplate.id='TestRisingFallingCorrId'",
    nofail)
```



## <a name="requirements"></a><span data-ttu-id="43225-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43225-116">Requirements</span></span>



| <span data-ttu-id="43225-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43225-117">Requirement</span></span> | <span data-ttu-id="43225-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="43225-118">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="43225-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43225-119">Minimum supported client</span></span><br/> | <span data-ttu-id="43225-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43225-120">Windows Vista</span></span><br/>       |
| <span data-ttu-id="43225-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43225-121">Minimum supported server</span></span><br/> | <span data-ttu-id="43225-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43225-122">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43225-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43225-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43225-124">Commandes de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="43225-124">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




