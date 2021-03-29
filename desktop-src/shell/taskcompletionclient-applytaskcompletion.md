---
description: Commence l’achèvement de la tâche.
ms.assetid: 75C84DD9-D815-45C2-A28E-EAE437EAFF89
title: 'TaskCompletionClient :: ApplyTaskCompletion, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient.ApplyTaskCompletion
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: 950d96ac46c18d741d5cf2337326f116fb79e36a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991705"
---
# <a name="taskcompletionclientapplytaskcompletion-method"></a><span data-ttu-id="eb603-103">TaskCompletionClient :: ApplyTaskCompletion, méthode</span><span class="sxs-lookup"><span data-stu-id="eb603-103">TaskCompletionClient::ApplyTaskCompletion method</span></span>

<span data-ttu-id="eb603-104">Commence l’achèvement de la tâche.</span><span class="sxs-lookup"><span data-stu-id="eb603-104">Begins the task completion.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb603-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb603-105">Syntax</span></span>


```C++
HRESULT ApplyTaskCompletion(
    UINT32   ptcfCategory
);
```



## <a name="parameters"></a><span data-ttu-id="eb603-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb603-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb603-107">*ptcfCategory*</span><span class="sxs-lookup"><span data-stu-id="eb603-107">*ptcfCategory*</span></span> 
</dt> <dd>

<span data-ttu-id="eb603-108">Valeur qui indique la catégorie de la tâche.</span><span class="sxs-lookup"><span data-stu-id="eb603-108">A value indicating the category of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb603-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb603-109">Return value</span></span>

<span data-ttu-id="eb603-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="eb603-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eb603-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eb603-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb603-112">Notes</span><span class="sxs-lookup"><span data-stu-id="eb603-112">Remarks</span></span>

<span data-ttu-id="eb603-113">La seule valeur prise en charge pour *ptcfCategory* est 0x08000000.</span><span class="sxs-lookup"><span data-stu-id="eb603-113">The only supported value for *ptcfCategory* is 0x08000000.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb603-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="eb603-114">Requirements</span></span>



| <span data-ttu-id="eb603-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb603-115">Requirement</span></span> | <span data-ttu-id="eb603-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb603-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb603-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb603-117">Minimum supported client</span></span><br/> | <span data-ttu-id="eb603-118">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb603-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eb603-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb603-119">Minimum supported server</span></span><br/> | <span data-ttu-id="eb603-120">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb603-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="eb603-121">DLL</span><span class="sxs-lookup"><span data-stu-id="eb603-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb603-122"><dt>ExecModelClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb603-122"><dt>ExecModelClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb603-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb603-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb603-124">**TaskCompletionClient**</span><span class="sxs-lookup"><span data-stu-id="eb603-124">**TaskCompletionClient**</span></span>](taskcompletionclient.md)
</dt> </dl>

 

 




