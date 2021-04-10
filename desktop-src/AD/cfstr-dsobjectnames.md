---
title: CFSTR_DSOBJECTNAMES (DSClient. h)
description: Le \_ format de presse-papiers CFSTR DSOBJECTNAMES fournit un handle de mémoire globale (HGLOBAL) qui contient la structure DSOBJECTNAMES.
ms.assetid: b28428fa-1504-4dcc-9b2b-32ca1ae30ec5
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSOBJECTNAMES
api_location:
- DSClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816f99f1b50f97ac362706cc46e4dbe4edf5f486
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103377"
---
# <a name="cfstr_dsobjectnames"></a><span data-ttu-id="ebd77-103">CFSTR \_ DSOBJECTNAMES</span><span class="sxs-lookup"><span data-stu-id="ebd77-103">CFSTR\_DSOBJECTNAMES</span></span>

<dl> <dt>

<span data-ttu-id="ebd77-104"><span id="CFSTR_DSOBJECTNAMES"></span><span id="cfstr_dsobjectnames"></span>**CFSTR \_ DSOBJECTNAMES**</span><span class="sxs-lookup"><span data-stu-id="ebd77-104"><span id="CFSTR_DSOBJECTNAMES"></span><span id="cfstr_dsobjectnames"></span>**CFSTR\_DSOBJECTNAMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ebd77-105">"DsObjectNames"</span><span class="sxs-lookup"><span data-stu-id="ebd77-105">"DsObjectNames"</span></span>
</dt> <dt>



<span data-ttu-id="ebd77-106">Le format de presse-papiers **CFSTR \_ DSOBJECTNAMES** est pris en charge par l' [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) fourni par la méthode [**ICommonQuery :: OpenQueryWindow**](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow) .</span><span class="sxs-lookup"><span data-stu-id="ebd77-106">The **CFSTR\_DSOBJECTNAMES** clipboard format is supported by the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) provided by the [**ICommonQuery::OpenQueryWindow**](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow) method.</span></span> <span data-ttu-id="ebd77-107">Le format de presse-papiers **CFSTR \_ DSOBJECTNAMES** fournit un handle de mémoire globale (**HGLOBAL**) qui contient la structure [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) .</span><span class="sxs-lookup"><span data-stu-id="ebd77-107">The **CFSTR\_DSOBJECTNAMES** clipboard format provides a global memory handle (**HGLOBAL**) that contains [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) structure.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ebd77-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebd77-108">Requirements</span></span>



| <span data-ttu-id="ebd77-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebd77-109">Requirement</span></span> | <span data-ttu-id="ebd77-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebd77-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ebd77-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebd77-111">Minimum supported client</span></span><br/> | <span data-ttu-id="ebd77-112">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ebd77-112">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="ebd77-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebd77-113">Minimum supported server</span></span><br/> | <span data-ttu-id="ebd77-114">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebd77-114">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="ebd77-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebd77-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebd77-116"><dt>DSClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebd77-116"><dt>DSClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebd77-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebd77-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebd77-118">**IDataObject**</span><span class="sxs-lookup"><span data-stu-id="ebd77-118">**IDataObject**</span></span>](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> <dt>

[<span data-ttu-id="ebd77-119">**ICommonQuery::OpenQueryWindow**</span><span class="sxs-lookup"><span data-stu-id="ebd77-119">**ICommonQuery::OpenQueryWindow**</span></span>](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow)
</dt> <dt>

[<span data-ttu-id="ebd77-120">**DSOBJECTNAMES**</span><span class="sxs-lookup"><span data-stu-id="ebd77-120">**DSOBJECTNAMES**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> </dl>

 

