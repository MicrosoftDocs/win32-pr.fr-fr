---
title: Structure WINBIO_BDB_ANSI_381_RECORD ( \_ types WINBIO. h)
description: Contient des informations sur une empreinte digitale ou un exemple Palm d’un utilisateur final.
ms.assetid: e0b32d05-3e96-4b42-9e18-57d10513f224
keywords:
- API de Windows Biometric Framework de structure de WINBIO_BDB_ANSI_381_RECORD
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_RECORD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30af31d88349dbe02066f231cdff21293aebe90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383975"
---
# <a name="winbio_bdb_ansi_381_record-structure"></a><span data-ttu-id="e322f-104">\_Structure d’enregistrement WINBIO BDB \_ ANSI \_ 381 \_</span><span class="sxs-lookup"><span data-stu-id="e322f-104">WINBIO\_BDB\_ANSI\_381\_RECORD structure</span></span>

<span data-ttu-id="e322f-105">La structure d' **\_ enregistrement WINBIO BDB \_ ANSI \_ 381 \_** contient des informations sur une empreinte digitale ou un exemple Palm d’un utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="e322f-105">The **WINBIO\_BDB\_ANSI\_381\_RECORD** structure contains information about a single fingerprint or palm sample from an end user.</span></span> <span data-ttu-id="e322f-106">Une collection de ces structures est incluse dans chaque structure d' [**\_ \_ \_ \_ en-tête WINBIO BDB ANSI 381**](winbio-bdb-ansi-381-header.md) .</span><span class="sxs-lookup"><span data-stu-id="e322f-106">A collection of these structures is included in each [**WINBIO\_BDB\_ANSI\_381\_HEADER**](winbio-bdb-ansi-381-header.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e322f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e322f-107">Syntax</span></span>


```C++
typedef struct _WINBIO_BDB_ANSI_381_RECORD {
  ULONG                    BlockLength;
  USHORT                   HorizontalLineLength;
  USHORT                   VerticalLineLength;
  WINBIO_BIOMETRIC_SUBTYPE Position;
  UCHAR                    CountOfViews;
  UCHAR                    ViewNumber;
  UCHAR                    ImageQuality;
  UCHAR                    ImpressionType;
  UCHAR                    Reserved;
} WINBIO_BDB_ANSI_381_RECORD;
```



## <a name="members"></a><span data-ttu-id="e322f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e322f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e322f-109">**BlockLength**</span><span class="sxs-lookup"><span data-stu-id="e322f-109">**BlockLength**</span></span>
</dt> <dd>

<span data-ttu-id="e322f-110">Contient le nombre d’octets dans cette structure, plus le nombre d’octets d’exemples de données d’image.</span><span class="sxs-lookup"><span data-stu-id="e322f-110">Contains the number of bytes in this structure plus the number of bytes of sample image data.</span></span>

</dd> <dt>

<span data-ttu-id="e322f-111">**HorizontalLineLength**</span><span class="sxs-lookup"><span data-stu-id="e322f-111">**HorizontalLineLength**</span></span>
</dt> <dd>

<span data-ttu-id="e322f-112">Spécifie le nombre de pixels sur une ligne horizontale de l’échantillon.</span><span class="sxs-lookup"><span data-stu-id="e322f-112">Specifies the number of pixels in a horizontal line of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="e322f-113">**VerticalLineLength**</span><span class="sxs-lookup"><span data-stu-id="e322f-113">**VerticalLineLength**</span></span>
</dt> <dd>

<span data-ttu-id="e322f-114">Spécifie le nombre de pixels dans une ligne verticale de l’échantillon.</span><span class="sxs-lookup"><span data-stu-id="e322f-114">Specifies the number of pixels in a vertical line of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="e322f-115">**Position**</span><span class="sxs-lookup"><span data-stu-id="e322f-115">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="e322f-116">Valeur **de \_ sous- \_ type biométrique WINBIO** qui spécifie le doigt ou le Palm utilisé pour générer l’échantillon biométrique.</span><span class="sxs-lookup"><span data-stu-id="e322f-116">A **WINBIO\_BIOMETRIC\_SUBTYPE** value that specifies the finger or palm used to generate the biometric sample.</span></span> <span data-ttu-id="e322f-117">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="e322f-117">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e322f-118">**CountOfViews**</span><span class="sxs-lookup"><span data-stu-id="e322f-118">**CountOfViews**</span></span>
</dt> <dd>

<span data-ttu-id="e322f-119">Doit être défini sur un (1);</span><span class="sxs-lookup"><span data-stu-id="e322f-119">This must be set to one (1);</span></span>

</dd> <dt>

<span data-ttu-id="e322f-120">**ViewNumber**</span><span class="sxs-lookup"><span data-stu-id="e322f-120">**ViewNumber**</span></span>
</dt> <dd>

<span data-ttu-id="e322f-121">Doit être défini sur un (1);</span><span class="sxs-lookup"><span data-stu-id="e322f-121">This must be set to one (1);</span></span>

</dd> <dt>

<span data-ttu-id="e322f-122">**ImageQuality**</span><span class="sxs-lookup"><span data-stu-id="e322f-122">**ImageQuality**</span></span>
</dt> <dd>

<span data-ttu-id="e322f-123">Réservé.</span><span class="sxs-lookup"><span data-stu-id="e322f-123">Reserved.</span></span> <span data-ttu-id="e322f-124">Il doit s’agir de 254 (0xFE).</span><span class="sxs-lookup"><span data-stu-id="e322f-124">This must be 254 (0xFE).</span></span>

</dd> <dt>

<span data-ttu-id="e322f-125">**ImpressionType**</span><span class="sxs-lookup"><span data-stu-id="e322f-125">**ImpressionType**</span></span>
</dt> <dd>

<span data-ttu-id="e322f-126">Réservé.</span><span class="sxs-lookup"><span data-stu-id="e322f-126">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="e322f-127">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="e322f-127">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="e322f-128">Réservé.</span><span class="sxs-lookup"><span data-stu-id="e322f-128">Reserved.</span></span> <span data-ttu-id="e322f-129">Doit être défini sur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="e322f-129">Must be set to zero (0).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e322f-130">Notes</span><span class="sxs-lookup"><span data-stu-id="e322f-130">Remarks</span></span>

<span data-ttu-id="e322f-131">Le membre *position* spécifie la zone de la main ou le Palm utilisé pour créer l’échantillon biométrique.</span><span class="sxs-lookup"><span data-stu-id="e322f-131">The *Position* member specifies the area of the hand or palm used to make the biometric sample.</span></span> <span data-ttu-id="e322f-132">Le Windows Biometric Framework (WBF) prend actuellement en charge uniquement la capture d’empreintes digitales et utilise les constantes suivantes pour représenter les informations de position.</span><span class="sxs-lookup"><span data-stu-id="e322f-132">The Windows Biometric Framework (WBF) currently supports only fingerprint capture and uses the following constants to represent position information.</span></span>

-   <span data-ttu-id="e322f-133">WINBIO \_ ANSI \_ 381 \_ pos \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="e322f-133">WINBIO\_ANSI\_381\_POS\_UNKNOWN</span></span>
-   <span data-ttu-id="e322f-134">WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_</span><span class="sxs-lookup"><span data-stu-id="e322f-134">WINBIO\_ANSI\_381\_POS\_RH\_THUMB</span></span>
-   <span data-ttu-id="e322f-135">WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ index \_ Finger</span><span class="sxs-lookup"><span data-stu-id="e322f-135">WINBIO\_ANSI\_381\_POS\_RH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="e322f-136">WINBIO \_ ANSI \_ 381 \_ pos \_ hr \_ \_ Finger Middle</span><span class="sxs-lookup"><span data-stu-id="e322f-136">WINBIO\_ANSI\_381\_POS\_RH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="e322f-137">WINBIO de l' \_ \_ \_ \_ anneau RH \_ du PDV ANSI 381 \_</span><span class="sxs-lookup"><span data-stu-id="e322f-137">WINBIO\_ANSI\_381\_POS\_RH\_RING\_FINGER</span></span>
-   <span data-ttu-id="e322f-138">WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ petit \_ Finger</span><span class="sxs-lookup"><span data-stu-id="e322f-138">WINBIO\_ANSI\_381\_POS\_RH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="e322f-139">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_</span><span class="sxs-lookup"><span data-stu-id="e322f-139">WINBIO\_ANSI\_381\_POS\_LH\_THUMB</span></span>
-   <span data-ttu-id="e322f-140">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ index \_ Finger</span><span class="sxs-lookup"><span data-stu-id="e322f-140">WINBIO\_ANSI\_381\_POS\_LH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="e322f-141">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ - \_ Finger</span><span class="sxs-lookup"><span data-stu-id="e322f-141">WINBIO\_ANSI\_381\_POS\_LH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="e322f-142">\_ \_ Doigt Ring WINBIO ANSI 381 \_ pos \_ LH \_ \_</span><span class="sxs-lookup"><span data-stu-id="e322f-142">WINBIO\_ANSI\_381\_POS\_LH\_RING\_FINGER</span></span>
-   <span data-ttu-id="e322f-143">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ petit \_ doigt</span><span class="sxs-lookup"><span data-stu-id="e322f-143">WINBIO\_ANSI\_381\_POS\_LH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="e322f-144">WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ quatre \_ doigts</span><span class="sxs-lookup"><span data-stu-id="e322f-144">WINBIO\_ANSI\_381\_POS\_RH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="e322f-145">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ quatre \_ doigts</span><span class="sxs-lookup"><span data-stu-id="e322f-145">WINBIO\_ANSI\_381\_POS\_LH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="e322f-146">WINBIO \_ ANSI \_ 381 \_ pos \_ deux \_ pouces</span><span class="sxs-lookup"><span data-stu-id="e322f-146">WINBIO\_ANSI\_381\_POS\_TWO\_THUMBS</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="e322f-147">N’essayez pas de valider la valeur fournie pour la valeur de *position* .</span><span class="sxs-lookup"><span data-stu-id="e322f-147">Do not attempt to validate the value supplied for the *Position* value.</span></span> <span data-ttu-id="e322f-148">Le service de biométrie Windows validera la valeur fournie avant de la passer à votre implémentation.</span><span class="sxs-lookup"><span data-stu-id="e322f-148">The Windows Biometrics Service will validate the supplied value before passing it through to your implementation.</span></span> <span data-ttu-id="e322f-149">Si la valeur est **WINBIO \_ sous-type \_ aucune \_ information** ou **WINBIO sous- \_ type \_ any**, validez le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="e322f-149">If the value is **WINBIO\_SUBTYPE\_NO\_INFORMATION** or **WINBIO\_SUBTYPE\_ANY**, then validate where appropriate.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e322f-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e322f-150">Requirements</span></span>



| <span data-ttu-id="e322f-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e322f-151">Requirement</span></span> | <span data-ttu-id="e322f-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="e322f-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e322f-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e322f-153">Minimum supported client</span></span><br/> | <span data-ttu-id="e322f-154">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e322f-154">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="e322f-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e322f-155">Minimum supported server</span></span><br/> | <span data-ttu-id="e322f-156">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e322f-156">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e322f-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="e322f-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="e322f-158"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e322f-158"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e322f-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e322f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e322f-160">Structures d’application cliente</span><span class="sxs-lookup"><span data-stu-id="e322f-160">Client Application Structures</span></span>](client-application-structures.md)
</dt> </dl>

 

 





