---
description: Supprime une classe existante et ses instances du référentiel.
ms.assetid: 6f96d14a-16ab-4e83-a75f-5dbf162d1692
ms.tgt_platform: multiple
title: pragma deleteclass
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
ms.openlocfilehash: 0d3b5b1fa209be7fd472a87aec25a5e590d93c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868590"
---
# <a name="pragma-deleteclass"></a><span data-ttu-id="1d991-103">pragma deleteclass</span><span class="sxs-lookup"><span data-stu-id="1d991-103">pragma deleteclass</span></span>

<span data-ttu-id="1d991-104">La commande de préprocesseur **pragma deleteclass** supprime une classe existante et ses instances du référentiel.</span><span class="sxs-lookup"><span data-stu-id="1d991-104">The **pragma deleteclass** preprocessor command deletes an existing class and its instances from the repository.</span></span>

<span data-ttu-id="1d991-105">Les éléments suivants décrivent la syntaxe :</span><span class="sxs-lookup"><span data-stu-id="1d991-105">The following describes the syntax:</span></span>


```mof
#pragma deleteclass("ClassName", [Flag])
```



<span data-ttu-id="1d991-106">*ClassName* est le nom de la classe que le compilateur MOF supprime de l’espace de noms actuel.</span><span class="sxs-lookup"><span data-stu-id="1d991-106">*ClassName* is the name of the class that the MOF compiler deletes from the current namespace.</span></span>

<span data-ttu-id="1d991-107">L' *\[ indicateur \]* doit être l’un des arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="1d991-107">*\[Flag\]* must be one of the following arguments.</span></span>



| <span data-ttu-id="1d991-108">Indicateur</span><span class="sxs-lookup"><span data-stu-id="1d991-108">Flag</span></span>   | <span data-ttu-id="1d991-109">Description</span><span class="sxs-lookup"><span data-stu-id="1d991-109">Description</span></span>                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d991-110">Échec</span><span class="sxs-lookup"><span data-stu-id="1d991-110">fail</span></span>   | <span data-ttu-id="1d991-111">Provoque la fermeture du compilateur MOF avec un message d’erreur si la classe n’existe pas déjà dans le référentiel.</span><span class="sxs-lookup"><span data-stu-id="1d991-111">Causes the MOF compiler to quit with an error message if the class does not already exist in the repository.</span></span> |
| <span data-ttu-id="1d991-112">nofail</span><span class="sxs-lookup"><span data-stu-id="1d991-112">nofail</span></span> | <span data-ttu-id="1d991-113">Fait en sorte que le compilateur MOF continue même si la classe n’existe pas déjà.</span><span class="sxs-lookup"><span data-stu-id="1d991-113">Causes the MOF compiler to continue even if the class does not already exist.</span></span>                                |



 

## <a name="examples"></a><span data-ttu-id="1d991-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="1d991-114">Examples</span></span>

<span data-ttu-id="1d991-115">L’exemple suivant montre comment utiliser cette commande.</span><span class="sxs-lookup"><span data-stu-id="1d991-115">The following example shows how to use this command.</span></span>


```mof
#pragma deleteclass("MyClass1",FAIL)
```



## <a name="requirements"></a><span data-ttu-id="1d991-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d991-116">Requirements</span></span>



| <span data-ttu-id="1d991-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d991-117">Requirement</span></span> | <span data-ttu-id="1d991-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d991-118">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1d991-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d991-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1d991-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d991-120">Windows Vista</span></span><br/>       |
| <span data-ttu-id="1d991-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d991-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1d991-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d991-122">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1d991-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d991-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d991-124">Commandes de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="1d991-124">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




