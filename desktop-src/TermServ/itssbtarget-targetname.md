---
title: Propriété TargetName de ITsSbTarget
description: Spécifie ou récupère le nom de la cible.
ms.assetid: ba5c3158-b4bc-457f-94ea-adb2e0852129
ms.tgt_platform: multiple
keywords:
- Propriété TargetName Services Bureau à distance
- TargetName, propriété Services Bureau à distance, ITsSbTarget, interface
- Services Bureau à distance de l’interface ITsSbTarget, propriété TargetName
- TargetName, propriété Services Bureau à distance, ITsSbTargetEx, interface
- Services Bureau à distance de l’interface ITsSbTargetEx, propriété TargetName
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetName
- ITsSbTarget.get_TargetName
- ITsSbTarget.put_TargetName
- ITsSbTargetEx.TargetName
- ITsSbTargetEx.get_TargetName
- ITsSbTargetEx.put_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dce949abee4ca00184a2b784ab154dbd75b9de6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030415"
---
# <a name="itssbtargettargetname-property"></a><span data-ttu-id="3104f-108">ITsSbTarget :: TargetName, propriété</span><span class="sxs-lookup"><span data-stu-id="3104f-108">ITsSbTarget::TargetName property</span></span>

<span data-ttu-id="3104f-109">Spécifie ou récupère le nom de la cible.</span><span class="sxs-lookup"><span data-stu-id="3104f-109">Specifies or retrieves the name of the target.</span></span>

<span data-ttu-id="3104f-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3104f-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3104f-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3104f-111">Syntax</span></span>


```C++
HRESULT put_TargetName(
  [in]          BSTR Val
);

HRESULT get_TargetName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="3104f-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3104f-112">Property value</span></span>

<span data-ttu-id="3104f-113">Variable **BSTR** qui spécifie le nom de la cible.</span><span class="sxs-lookup"><span data-stu-id="3104f-113">A **BSTR** variable that specifies the target name.</span></span>

## <a name="remarks"></a><span data-ttu-id="3104f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="3104f-114">Remarks</span></span>

<span data-ttu-id="3104f-115">Cette propriété était en lecture seule avant Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="3104f-115">This property was read-only prior to Windows Server 2012.</span></span>

## <a name="requirements"></a><span data-ttu-id="3104f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3104f-116">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3104f-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3104f-117">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="3104f-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3104f-118">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3104f-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3104f-119">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="3104f-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3104f-120">Windows Server 2012</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3104f-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="3104f-121">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="3104f-122"><dt>Sbtsv. idl</dt> </span><span class="sxs-lookup"><span data-stu-id="3104f-122"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3104f-123">IID</span><span class="sxs-lookup"><span data-stu-id="3104f-123">IID</span></span><br/></td>
<td><span data-ttu-id="3104f-124">IID_ITsSbTarget est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="3104f-124">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="3104f-125">16616ECC-272D-411D-B324-126893033856</span><span class="sxs-lookup"><span data-stu-id="3104f-125">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="3104f-126">e85e10ea-DB0B-4752-B456-5fd5840901c0 sur Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3104f-126">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="3104f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3104f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3104f-128">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="3104f-128">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="3104f-129">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="3104f-129">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





