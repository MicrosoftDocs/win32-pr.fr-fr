---
title: ITsSbTarget propriété FarmName
description: Récupère ou spécifie le nom de la batterie de serveurs à laquelle cette cible est jointe.
ms.assetid: 83e168ae-f985-40f9-912b-496c0695f82a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété FarmName
- Services Bureau à distance de la propriété FarmName, interface ITsSbTarget
- Services Bureau à distance de l’interface ITsSbTarget, propriété FarmName
- Services Bureau à distance de la propriété FarmName, interface ITsSbTargetEx
- Services Bureau à distance de l’interface ITsSbTargetEx, propriété FarmName
topic_type:
- apiref
api_name:
- ITsSbTarget.FarmName
- ITsSbTarget.get_FarmName
- ITsSbTarget.put_FarmName
- ITsSbTargetEx.FarmName
- ITsSbTargetEx.get_FarmName
- ITsSbTargetEx.put_FarmName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94f86b2cf0ec257be9fe9b801e6fceae364a46e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678413"
---
# <a name="itssbtargetfarmname-property"></a><span data-ttu-id="c6d02-108">ITsSbTarget :: FarmName, propriété</span><span class="sxs-lookup"><span data-stu-id="c6d02-108">ITsSbTarget::FarmName property</span></span>

<span data-ttu-id="c6d02-109">Récupère ou spécifie le nom de la batterie de serveurs à laquelle cette cible est jointe.</span><span class="sxs-lookup"><span data-stu-id="c6d02-109">Retrieves or specifies the name of the farm to which this target is joined.</span></span>

<span data-ttu-id="c6d02-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c6d02-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6d02-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6d02-111">Syntax</span></span>


```C++
HRESULT put_FarmName(
  [in]          BSTR Val
);

HRESULT get_FarmName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="c6d02-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c6d02-112">Property value</span></span>

<span data-ttu-id="c6d02-113">Variable **BSTR** qui contient le nom de la batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="c6d02-113">A **BSTR** variable that contains the farm name.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6d02-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6d02-114">Requirements</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c6d02-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6d02-115">Minimum supported client</span></span><br/></td>
<td><span data-ttu-id="c6d02-116">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6d02-116">None supported</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6d02-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6d02-117">Minimum supported server</span></span><br/></td>
<td><span data-ttu-id="c6d02-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c6d02-118">Windows Server 2012</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6d02-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="c6d02-119">IDL</span></span><br/></td>
<td><dl> <span data-ttu-id="c6d02-120"><dt>Sbtsv. idl</dt> </span><span class="sxs-lookup"><span data-stu-id="c6d02-120"><dt>Sbtsv.idl</dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6d02-121">IID</span><span class="sxs-lookup"><span data-stu-id="c6d02-121">IID</span></span><br/></td>
<td><span data-ttu-id="c6d02-122">IID_ITsSbTarget est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="c6d02-122">IID_ITsSbTarget is defined as:</span></span>
<ul>
<li><span data-ttu-id="c6d02-123">16616ECC-272D-411D-B324-126893033856</span><span class="sxs-lookup"><span data-stu-id="c6d02-123">16616ECC-272D-411D-B324-126893033856</span></span></li>
<li><span data-ttu-id="c6d02-124">e85e10ea-DB0B-4752-B456-5fd5840901c0 sur Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c6d02-124">e85e10ea-db0b-4752-b456-5fd5840901c0 on Windows Server 2008 R2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="c6d02-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6d02-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6d02-126">**ITsSbTargetEx**</span><span class="sxs-lookup"><span data-stu-id="c6d02-126">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dt>

[<span data-ttu-id="c6d02-127">**ITsSbTarget**</span><span class="sxs-lookup"><span data-stu-id="c6d02-127">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





