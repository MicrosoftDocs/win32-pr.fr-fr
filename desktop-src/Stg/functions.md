---
title: Fonctions (STG)
description: Les fonctions sont des routines ou des sous-routines qui retournent une ou plusieurs valeurs spécifiques. Les fonctions de stockage structuré sont décrites dans les sections suivantes.
ms.assetid: 5fbb05ae-594d-4fa5-97d2-a2371e94c054
keywords:
- Stockage structuré Strctd STG, référence, fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f49c091b5ba9619b649e620da7b436ebac4ccb
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "106521783"
---
# <a name="structured-storage-functions"></a><span data-ttu-id="67217-105">Fonctions de stockage structuré</span><span class="sxs-lookup"><span data-stu-id="67217-105">Structured Storage functions</span></span>

<span data-ttu-id="67217-106">Les fonctions sont des routines ou des sous-routines qui retournent une ou plusieurs valeurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="67217-106">Functions are routines or subroutines that return a specific value or values.</span></span> <span data-ttu-id="67217-107">Les fonctions de stockage structuré sont décrites dans les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="67217-107">Structured Storage functions are described in the following sections:</span></span>

-   [<span data-ttu-id="67217-108">**CreateILockBytesOnHGlobal**</span><span class="sxs-lookup"><span data-stu-id="67217-108">**CreateILockBytesOnHGlobal**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-createilockbytesonhglobal)
-   [<span data-ttu-id="67217-109">**CreateStreamOnHGlobal**</span><span class="sxs-lookup"><span data-stu-id="67217-109">**CreateStreamOnHGlobal**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
-   [<span data-ttu-id="67217-110">**FmtIdToPropStgName**</span><span class="sxs-lookup"><span data-stu-id="67217-110">**FmtIdToPropStgName**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-fmtidtopropstgname)
-   [<span data-ttu-id="67217-111">**FreePropVariantArray**</span><span class="sxs-lookup"><span data-stu-id="67217-111">**FreePropVariantArray**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-freepropvariantarray)
-   [<span data-ttu-id="67217-112">**GetConvertStg**</span><span class="sxs-lookup"><span data-stu-id="67217-112">**GetConvertStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-getconvertstg)
-   [<span data-ttu-id="67217-113">**GetHGlobalFromILockBytes**</span><span class="sxs-lookup"><span data-stu-id="67217-113">**GetHGlobalFromILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-gethglobalfromilockbytes)
-   [<span data-ttu-id="67217-114">**GetHGlobalFromStream**</span><span class="sxs-lookup"><span data-stu-id="67217-114">**GetHGlobalFromStream**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-gethglobalfromstream)
-   [<span data-ttu-id="67217-115">**OleConvertIStorageToOLESTREAM**</span><span class="sxs-lookup"><span data-stu-id="67217-115">**OleConvertIStorageToOLESTREAM**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oleconvertistoragetoolestream)
-   [<span data-ttu-id="67217-116">**OleConvertIStorageToOLESTREAMEx**</span><span class="sxs-lookup"><span data-stu-id="67217-116">**OleConvertIStorageToOLESTREAMEx**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oleconvertistoragetoolestreamex)
-   [<span data-ttu-id="67217-117">**OleConvertOLESTREAMToIStorage**</span><span class="sxs-lookup"><span data-stu-id="67217-117">**OleConvertOLESTREAMToIStorage**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oleconvertolestreamtoistorage)
-   [<span data-ttu-id="67217-118">**OleConvertOLESTREAMToIStorageEx**</span><span class="sxs-lookup"><span data-stu-id="67217-118">**OleConvertOLESTREAMToIStorageEx**</span></span>](/windows/desktop/api/Ole2/nf-ole2-oleconvertolestreamtoistorageex)
-   [<span data-ttu-id="67217-119">**PropStgNameToFmtId**</span><span class="sxs-lookup"><span data-stu-id="67217-119">**PropStgNameToFmtId**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-propstgnametofmtid)
-   [<span data-ttu-id="67217-120">**PropVariantClear**</span><span class="sxs-lookup"><span data-stu-id="67217-120">**PropVariantClear**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)
-   [<span data-ttu-id="67217-121">**PropVariantCopy**</span><span class="sxs-lookup"><span data-stu-id="67217-121">**PropVariantCopy**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-propvariantcopy)
-   [<span data-ttu-id="67217-122">**PropVariantInit**</span><span class="sxs-lookup"><span data-stu-id="67217-122">**PropVariantInit**</span></span>](/windows/desktop/api/PropIdl/nf-propidl-propvariantinit)
-   [<span data-ttu-id="67217-123">**ReadClassStg**</span><span class="sxs-lookup"><span data-stu-id="67217-123">**ReadClassStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-readclassstg)
-   [<span data-ttu-id="67217-124">**ReadClassStm**</span><span class="sxs-lookup"><span data-stu-id="67217-124">**ReadClassStm**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-readclassstm)
-   [<span data-ttu-id="67217-125">**ReadFmtUserTypeStg**</span><span class="sxs-lookup"><span data-stu-id="67217-125">**ReadFmtUserTypeStg**</span></span>](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg)
-   [<span data-ttu-id="67217-126">**StgConvertPropertyToVariant**</span><span class="sxs-lookup"><span data-stu-id="67217-126">**StgConvertPropertyToVariant**</span></span>](/windows/desktop/api/Propidl/nf-propidl-stgconvertpropertytovariant)
-   [<span data-ttu-id="67217-127">**SetConvertStg**</span><span class="sxs-lookup"><span data-stu-id="67217-127">**SetConvertStg**</span></span>](/windows/desktop/api/Ole2/nf-ole2-setconvertstg)
-   [<span data-ttu-id="67217-128">**StgConvertVariantToProperty**</span><span class="sxs-lookup"><span data-stu-id="67217-128">**StgConvertVariantToProperty**</span></span>](/windows/desktop/api/Propidl/nf-propidl-stgconvertvarianttoproperty)
-   [<span data-ttu-id="67217-129">**StgCreateDocfile**</span><span class="sxs-lookup"><span data-stu-id="67217-129">**StgCreateDocfile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
-   [<span data-ttu-id="67217-130">**StgCreateDocfileOnILockBytes**</span><span class="sxs-lookup"><span data-stu-id="67217-130">**StgCreateDocfileOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)
-   [<span data-ttu-id="67217-131">**StgCreatePropSetStg**</span><span class="sxs-lookup"><span data-stu-id="67217-131">**StgCreatePropSetStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
-   [<span data-ttu-id="67217-132">**StgCreatePropStg**</span><span class="sxs-lookup"><span data-stu-id="67217-132">**StgCreatePropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
-   [<span data-ttu-id="67217-133">**StgCreateStorageEx**</span><span class="sxs-lookup"><span data-stu-id="67217-133">**StgCreateStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
-   [<span data-ttu-id="67217-134">**StgDeserializePropVariant**</span><span class="sxs-lookup"><span data-stu-id="67217-134">**StgDeserializePropVariant**</span></span>](/windows/desktop/api/Propvarutil/nf-propvarutil-stgdeserializepropvariant)
-   [<span data-ttu-id="67217-135">**StgGetIFillLockBytesOnFile**</span><span class="sxs-lookup"><span data-stu-id="67217-135">**StgGetIFillLockBytesOnFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile)
-   [<span data-ttu-id="67217-136">**StgGetIFillLockBytesOnILockBytes**</span><span class="sxs-lookup"><span data-stu-id="67217-136">**StgGetIFillLockBytesOnILockBytes**</span></span>](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes)
-   [<span data-ttu-id="67217-137">**StgIsStorageFile**</span><span class="sxs-lookup"><span data-stu-id="67217-137">**StgIsStorageFile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile)
-   [<span data-ttu-id="67217-138">**StgIsStorageILockBytes**</span><span class="sxs-lookup"><span data-stu-id="67217-138">**StgIsStorageILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgisstorageilockbytes)
-   [<span data-ttu-id="67217-139">**StgOpenAsyncDocfileOnIFillLockBytes**</span><span class="sxs-lookup"><span data-stu-id="67217-139">**StgOpenAsyncDocfileOnIFillLockBytes**</span></span>](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes)
-   [<span data-ttu-id="67217-140">**StgOpenLayoutDocfile**</span><span class="sxs-lookup"><span data-stu-id="67217-140">**StgOpenLayoutDocfile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-stgopenlayoutdocfile)
-   [<span data-ttu-id="67217-141">**StgOpenPropStg**</span><span class="sxs-lookup"><span data-stu-id="67217-141">**StgOpenPropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
-   [<span data-ttu-id="67217-142">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="67217-142">**StgOpenStorage**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
-   [<span data-ttu-id="67217-143">**StgOpenStorageEx**</span><span class="sxs-lookup"><span data-stu-id="67217-143">**StgOpenStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
-   [<span data-ttu-id="67217-144">**StgOpenStorageOnILockBytes**</span><span class="sxs-lookup"><span data-stu-id="67217-144">**StgOpenStorageOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes)
-   [<span data-ttu-id="67217-145">**StgPropertyLengthAsVariant**</span><span class="sxs-lookup"><span data-stu-id="67217-145">**StgPropertyLengthAsVariant**</span></span>](/windows/desktop/api/Propapi/nf-propapi-stgpropertylengthasvariant)
-   [<span data-ttu-id="67217-146">**StgSerializePropVariant**</span><span class="sxs-lookup"><span data-stu-id="67217-146">**StgSerializePropVariant**</span></span>](/windows/desktop/api/propvarutil/nf-propvarutil-stgserializepropvariant)
-   [<span data-ttu-id="67217-147">**StgSetTimes**</span><span class="sxs-lookup"><span data-stu-id="67217-147">**StgSetTimes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgsettimes)
-   [<span data-ttu-id="67217-148">**WriteClassStg**</span><span class="sxs-lookup"><span data-stu-id="67217-148">**WriteClassStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg)
-   [<span data-ttu-id="67217-149">**WriteClassStm**</span><span class="sxs-lookup"><span data-stu-id="67217-149">**WriteClassStm**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-writeclassstm)
-   [<span data-ttu-id="67217-150">**WriteFmtUserTypeStg**</span><span class="sxs-lookup"><span data-stu-id="67217-150">**WriteFmtUserTypeStg**</span></span>](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg)

 

 
