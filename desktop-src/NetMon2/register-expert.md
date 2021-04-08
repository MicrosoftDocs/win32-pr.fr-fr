---
description: L’expert doit implémenter la fonction d’expert d’inscription. Moniteur réseau appelle la fonction d’expert Register pour obtenir des informations sur l’expert.
ms.assetid: 58cfe525-99b1-40ce-b8d8-fa1c62a20c40
title: Inscrire la fonction de rappel d’expert (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 085d5c59b17b10949ad39d07354906f40e123988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864062"
---
# <a name="register-expert-callback-function"></a><span data-ttu-id="acb0a-104">Enregistrer la fonction de rappel d’expert</span><span class="sxs-lookup"><span data-stu-id="acb0a-104">Register Expert callback function</span></span>

<span data-ttu-id="acb0a-105">L’expert doit implémenter la fonction d’expert d' **inscription** .</span><span class="sxs-lookup"><span data-stu-id="acb0a-105">The expert must implement the **Register** expert function.</span></span> <span data-ttu-id="acb0a-106">Moniteur réseau appelle la fonction d’expert **Register** pour obtenir des informations sur l’expert.</span><span class="sxs-lookup"><span data-stu-id="acb0a-106">Network Monitor calls the **Register** expert function to obtain information about the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="acb0a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="acb0a-107">Syntax</span></span>


```C++
BOOL WINAPI Register(
  _Inout_ PEXPERTENUMINFO pExpertInfo
);
```



## <a name="parameters"></a><span data-ttu-id="acb0a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="acb0a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acb0a-109">*pExpertInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="acb0a-109">*pExpertInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="acb0a-110">Pointeur vers une structure [**EXPERTENUMINFO**](expertenuminfo.md) qui Moniteur réseau alloue.</span><span class="sxs-lookup"><span data-stu-id="acb0a-110">Pointer to an [**EXPERTENUMINFO**](expertenuminfo.md) structure that Network Monitor allocates.</span></span> <span data-ttu-id="acb0a-111">L’expert remplit la structure avec toutes les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="acb0a-111">The expert fills in the structure with all requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acb0a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="acb0a-112">Return value</span></span>

<span data-ttu-id="acb0a-113">Si la fonction réussit, la valeur de retour est **true** et la fonction retourne les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="acb0a-113">If the function is successful, the return value is **TRUE**, and the function returns the requested information.</span></span>

<span data-ttu-id="acb0a-114">Si la fonction échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="acb0a-114">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="acb0a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="acb0a-115">Remarks</span></span>

<span data-ttu-id="acb0a-116">Le membre **version** de la structure [**EXPERTENUMINFO**](expertenuminfo.md) doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="acb0a-116">The **Version** member of the [**EXPERTENUMINFO**](expertenuminfo.md) structure must be zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="acb0a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acb0a-117">Requirements</span></span>



| <span data-ttu-id="acb0a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="acb0a-118">Requirement</span></span> | <span data-ttu-id="acb0a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="acb0a-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="acb0a-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acb0a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="acb0a-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="acb0a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="acb0a-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acb0a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="acb0a-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="acb0a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="acb0a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="acb0a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="acb0a-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="acb0a-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




