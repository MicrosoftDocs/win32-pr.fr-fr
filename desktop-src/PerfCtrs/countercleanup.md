---
description: Supprime l’inscription des fournisseurs.
ms.assetid: e52c1ee0-140a-4277-bddd-d93338a512bc
title: CounterCleanup fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterCleanup
api_type:
- NA
api_location: ''
ms.openlocfilehash: eb768d3152aad5401c30b18a3f1ff13d1ef2397d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519902"
---
# <a name="countercleanup-function"></a><span data-ttu-id="1cd4b-103">CounterCleanup fonction)</span><span class="sxs-lookup"><span data-stu-id="1cd4b-103">CounterCleanup function</span></span>

<span data-ttu-id="1cd4b-104">Supprime l’inscription du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-104">Removes the provider's registration.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cd4b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cd4b-105">Syntax</span></span>


```C++
void WINAPI CounterCleanup(void);
```



## <a name="parameters"></a><span data-ttu-id="1cd4b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cd4b-106">Parameters</span></span>

<span data-ttu-id="1cd4b-107">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1cd4b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1cd4b-108">Return value</span></span>

<span data-ttu-id="1cd4b-109">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-109">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cd4b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1cd4b-110">Remarks</span></span>

<span data-ttu-id="1cd4b-111">Votre fournisseur appelle cette fonction.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-111">Your provider calls this function.</span></span> <span data-ttu-id="1cd4b-112">La fonction appelle la fonction [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) pour supprimer l’inscription du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-112">The function calls the [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) function to remove the provider's registration.</span></span>

<span data-ttu-id="1cd4b-113">L’outil [**CTRPP**](ctrpp.md) génère cette fonction inline lorsque vous spécifiez l’argument **-o** .</span><span class="sxs-lookup"><span data-stu-id="1cd4b-113">The [**CTRPP**](ctrpp.md) tool generates this inline function when you specify the **-o** argument.</span></span> <span data-ttu-id="1cd4b-114">Le nom de la fonction comprend une chaîne de *préfixe* si vous spécifiez l’argument **-prefix** (par exemple, **_prefix_CounterCleanup**.</span><span class="sxs-lookup"><span data-stu-id="1cd4b-114">The function's name includes a *prefix* string if you specify the **-prefix** argument (for example, **_prefix_CounterCleanup**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cd4b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cd4b-115">Requirements</span></span>



| <span data-ttu-id="1cd4b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cd4b-116">Requirement</span></span> | <span data-ttu-id="1cd4b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cd4b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="1cd4b-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cd4b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1cd4b-119">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cd4b-119">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="1cd4b-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cd4b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1cd4b-121">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cd4b-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 




