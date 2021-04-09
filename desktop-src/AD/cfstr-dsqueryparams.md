---
title: CFSTR_DSQUERYPARAMS (DSQuery. h)
description: Le \_ format de presse-papiers CFSTR DSQUERYPARAMS fournit un handle de mémoire globale (HGLOBAL) qui contient une structure DSQUERYPARAMS.
ms.assetid: bb8aea98-8309-42bf-993d-fa408bb4deb2
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSQUERYPARAMS
api_location:
- DSQuery.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a330d228778f34118d232b2004e7294ab493ed77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941966"
---
# <a name="cfstr_dsqueryparams"></a><span data-ttu-id="e2bc8-103">CFSTR \_ DSQUERYPARAMS</span><span class="sxs-lookup"><span data-stu-id="e2bc8-103">CFSTR\_DSQUERYPARAMS</span></span>

<dl> <dt>

<span data-ttu-id="e2bc8-104"><span id="CFSTR_DSQUERYPARAMS"></span><span id="cfstr_dsqueryparams"></span>**CFSTR \_ DSQUERYPARAMS**</span><span class="sxs-lookup"><span data-stu-id="e2bc8-104"><span id="CFSTR_DSQUERYPARAMS"></span><span id="cfstr_dsqueryparams"></span>**CFSTR\_DSQUERYPARAMS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2bc8-105">"DsQueryParameters"</span><span class="sxs-lookup"><span data-stu-id="e2bc8-105">"DsQueryParameters"</span></span>
</dt> <dt>



<span data-ttu-id="e2bc8-106">Le format de presse-papiers **CFSTR \_ DSQUERYPARAMS** est pris en charge par l' [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) fourni par la méthode [**ICommonQuery :: OpenQueryWindow**](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow) .</span><span class="sxs-lookup"><span data-stu-id="e2bc8-106">The **CFSTR\_DSQUERYPARAMS** clipboard format is supported by the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) provided by the [**ICommonQuery::OpenQueryWindow**](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow) method.</span></span> <span data-ttu-id="e2bc8-107">Le format de presse-papiers **CFSTR \_ DSQUERYPARAMS** fournit un handle de mémoire globale (**HGLOBAL**) qui contient une structure [**DSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) .</span><span class="sxs-lookup"><span data-stu-id="e2bc8-107">The **CFSTR\_DSQUERYPARAMS** clipboard format provides a global memory handle (**HGLOBAL**) that contains a [**DSQUERYPARAMS**](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams) structure.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2bc8-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2bc8-108">Requirements</span></span>



| <span data-ttu-id="e2bc8-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2bc8-109">Requirement</span></span> | <span data-ttu-id="e2bc8-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2bc8-110">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e2bc8-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2bc8-111">Minimum supported client</span></span><br/> | <span data-ttu-id="e2bc8-112">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2bc8-112">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="e2bc8-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2bc8-113">Minimum supported server</span></span><br/> | <span data-ttu-id="e2bc8-114">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2bc8-114">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="e2bc8-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2bc8-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2bc8-116"><dt>DSQuery. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2bc8-116"><dt>DSQuery.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2bc8-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2bc8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2bc8-118">**IDataObject**</span><span class="sxs-lookup"><span data-stu-id="e2bc8-118">**IDataObject**</span></span>](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> <dt>

[<span data-ttu-id="e2bc8-119">**ICommonQuery::OpenQueryWindow**</span><span class="sxs-lookup"><span data-stu-id="e2bc8-119">**ICommonQuery::OpenQueryWindow**</span></span>](/windows/win32/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow)
</dt> <dt>

[<span data-ttu-id="e2bc8-120">**DSQUERYPARAMS**</span><span class="sxs-lookup"><span data-stu-id="e2bc8-120">**DSQUERYPARAMS**</span></span>](/windows/desktop/api/Dsquery/ns-dsquery-dsqueryparams)
</dt> </dl>

 

