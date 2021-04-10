---
description: La fonction RKeyCloseKeyService n’est pas prise en charge.
ms.assetid: 3a3d41d4-d8ce-4ed8-a70b-dd3629ab7b44
title: RKeyCloseKeyService, fonction (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyCloseKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 3a35362876c067de011ec69a858e20150308cbd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862622"
---
# <a name="rkeyclosekeyservice-function"></a><span data-ttu-id="0d0a3-103">RKeyCloseKeyService fonction)</span><span class="sxs-lookup"><span data-stu-id="0d0a3-103">RKeyCloseKeyService function</span></span>

<span data-ttu-id="0d0a3-104">La fonction **RKeyCloseKeyService** n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0d0a3-104">The **RKeyCloseKeyService** function is not supported.</span></span>

<span data-ttu-id="0d0a3-105">**Windows Server 2003 :** La fonction **RKeyCloseKeyService** ferme un handle de service de clé ouvert par un appel précédent à la fonction [**RKeyOpenKeyService**](rkeyopenkeyservice.md) .</span><span class="sxs-lookup"><span data-stu-id="0d0a3-105">**Windows Server 2003:** The **RKeyCloseKeyService** function closes a key service handle opened by a previous call to the [**RKeyOpenKeyService**](rkeyopenkeyservice.md) function.</span></span> <span data-ttu-id="0d0a3-106">Notez que ce comportement a changé avec Windows Server 2003 avec Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="0d0a3-106">Note that this behavior has changed with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="syntax"></a><span data-ttu-id="0d0a3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d0a3-107">Syntax</span></span>


```C++
ULONG RKeyCloseKeyService(
  _In_    KEYSVCC_HANDLE hKeySvcCli,
  _Inout_ void           *pReserved
);
```



## <a name="parameters"></a><span data-ttu-id="0d0a3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d0a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d0a3-109">*hKeySvcCli* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d0a3-109">*hKeySvcCli* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d0a3-110">Handle [**de \_ handle KEYSVCC**](keysvcc-handle.md) précédemment ouvert par [**RKeyOpenKeyService**](rkeyopenkeyservice.md).</span><span class="sxs-lookup"><span data-stu-id="0d0a3-110">A [**KEYSVCC\_HANDLE**](keysvcc-handle.md) handle previously opened by [**RKeyOpenKeyService**](rkeyopenkeyservice.md).</span></span> <span data-ttu-id="0d0a3-111">Cette valeur ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="0d0a3-111">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0d0a3-112">*conservé* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0d0a3-112">*pReserved* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d0a3-113">Réservé.</span><span class="sxs-lookup"><span data-stu-id="0d0a3-113">Reserved.</span></span> <span data-ttu-id="0d0a3-114">Définissez cette valeur sur **null**.</span><span class="sxs-lookup"><span data-stu-id="0d0a3-114">Set this value to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d0a3-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d0a3-115">Return value</span></span>

<span data-ttu-id="0d0a3-116">Si la fonction réussit, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0d0a3-116">If the function is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="0d0a3-117">Si la fonction échoue, la valeur de retour est un **ULong** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="0d0a3-117">If the function fails, the return value is a **ULONG** that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d0a3-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d0a3-118">Requirements</span></span>



| <span data-ttu-id="0d0a3-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d0a3-119">Requirement</span></span> | <span data-ttu-id="0d0a3-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d0a3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d0a3-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d0a3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0d0a3-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d0a3-122">None supported</span></span><br/>                                                             |
| <span data-ttu-id="0d0a3-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d0a3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0d0a3-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d0a3-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0d0a3-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d0a3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d0a3-126"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d0a3-126"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d0a3-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d0a3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d0a3-128">**RKeyOpenKeyService**</span><span class="sxs-lookup"><span data-stu-id="0d0a3-128">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> <dt>

[<span data-ttu-id="0d0a3-129">**RKeyPFXInstall**</span><span class="sxs-lookup"><span data-stu-id="0d0a3-129">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> </dl>

 

 




