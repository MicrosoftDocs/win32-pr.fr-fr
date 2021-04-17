---
description: Demande pour indiquer que le journal de graphisme contient de nouvelles données.
MS-HAID: vspixengine.IPixEngine2\_OnNewDataAvailable\_BOOL\_BOOL\_INT64\_INT64\_INT32\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine2 :: OnNewDataAvailable, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B99FC54C-9395-4B14-93D5-B6408D655DC3
api_name:
- IPixEngine2.OnNewDataAvailable
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3de880153eec5b41849167f3a87a3f77f31aeffd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521527"
---
# <a name="span-idvspixengineipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arrspanipixengine2onnewdataavailable-method"></a><span data-ttu-id="9d545-103"><span id="vspixengine.ipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arr"></span>IPixEngine2 :: OnNewDataAvailable, méthode</span><span class="sxs-lookup"><span data-stu-id="9d545-103"><span id="vspixengine.ipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arr"></span>IPixEngine2::OnNewDataAvailable method</span></span>

<span data-ttu-id="9d545-104">Demande pour indiquer que le journal de graphisme contient de nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="9d545-104">Requests to indicate that the graphics log has new data inside of it.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d545-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d545-105">Syntax</span></span>


```C++
HRESULT OnNewDataAvailable(
   BOOL    fSessionEnd,
   BOOL    fUnloadCurFrame,
   INT64   i64FilePositionStart,
   INT64   i64FilePositionEnd,
   INT32   iObjectTableDataSize,
   BYTE [] count4_pObjectTableData
);
```

## <a name="parameters"></a><span data-ttu-id="9d545-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d545-106">Parameters</span></span>

<span data-ttu-id="9d545-107">*fSessionEnd* </span><span class="sxs-lookup"><span data-stu-id="9d545-107">*fSessionEnd* </span></span>  
<span data-ttu-id="9d545-108">true si la session s’est terminée ; sinon, false.</span><span class="sxs-lookup"><span data-stu-id="9d545-108">true if the session has ended, otherwise false.</span></span>

<span data-ttu-id="9d545-109">*fUnloadCurFrame* </span><span class="sxs-lookup"><span data-stu-id="9d545-109">*fUnloadCurFrame* </span></span>  
<span data-ttu-id="9d545-110">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="9d545-110">Not used.</span></span>

<span data-ttu-id="9d545-111">*i64FilePositionStart* </span><span class="sxs-lookup"><span data-stu-id="9d545-111">*i64FilePositionStart* </span></span>  
<span data-ttu-id="9d545-112">Position du fichier, en octets, au niveau de laquelle les nouvelles données commencent.</span><span class="sxs-lookup"><span data-stu-id="9d545-112">The file position, in bytes, at which the new data begins.</span></span>

<span data-ttu-id="9d545-113">*i64FilePositionEnd* </span><span class="sxs-lookup"><span data-stu-id="9d545-113">*i64FilePositionEnd* </span></span>  
<span data-ttu-id="9d545-114">Position du fichier, en octets, à laquelle les nouvelles données se terminent.</span><span class="sxs-lookup"><span data-stu-id="9d545-114">The file position, in bytes, at which the new data ends.</span></span>

<span data-ttu-id="9d545-115">*iObjectTableDataSize* </span><span class="sxs-lookup"><span data-stu-id="9d545-115">*iObjectTableDataSize* </span></span>  
<span data-ttu-id="9d545-116">Nombre d’octets contenus dans count4 \_ pObjectTableData.</span><span class="sxs-lookup"><span data-stu-id="9d545-116">The number of bytes contained in count4\_pObjectTableData.</span></span>

<span data-ttu-id="9d545-117">*count4 \_ pObjectTableData* </span><span class="sxs-lookup"><span data-stu-id="9d545-117">*count4\_pObjectTableData* </span></span>  
<span data-ttu-id="9d545-118">Mémoire tampon qui contient les données de la table des objets.</span><span class="sxs-lookup"><span data-stu-id="9d545-118">An buffer containing data for the object table.</span></span>

## <a name="return-value"></a><span data-ttu-id="9d545-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d545-119">Return value</span></span>

<span data-ttu-id="9d545-120">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9d545-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9d545-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9d545-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d545-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d545-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9d545-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d545-123">Header</span></span></p></td><td><span data-ttu-id="9d545-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="9d545-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="9d545-125"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d545-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="9d545-126">**IPixEngine2**</span><span class="sxs-lookup"><span data-stu-id="9d545-126">**IPixEngine2**</span></span>](/windows/desktop/direct3dtools/ipixengine2)

 

 
