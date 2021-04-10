---
title: Constantes WINBIO_BIOMETRIC_SUBTYPE ( \_ types WINBIO. h)
description: Fournissez des informations sur une mesure biométrique.
ms.assetid: 019569A9-6184-4E75-9B82-C98F4F45F61A
topic_type:
- apiref
api_name:
- WINBIO_SUBTYPE_NO_INFORMATION
- WINBIO_SUBTYPE_ANY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba1bc25337bf49a48b54b6b2426673daf8a15bd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942350"
---
# <a name="winbio_biometric_subtype-constants"></a><span data-ttu-id="3204b-103">\_Constantes de sous-type biométrique WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="3204b-103">WINBIO\_BIOMETRIC\_SUBTYPE Constants</span></span>

<span data-ttu-id="3204b-104">**WINBIO \_ Les constantes de \_ sous-type BIOmétriques** sont utilisées dans l’Windows Biometric Framework pour fournir des informations supplémentaires sur une mesure biométrique.</span><span class="sxs-lookup"><span data-stu-id="3204b-104">**WINBIO\_BIOMETRIC\_SUBTYPE** constants are used throughout the Windows Biometric Framework to provide additional information about a biometric measurement.</span></span> <span data-ttu-id="3204b-105">Les constantes suivantes peuvent être utilisées quand aucun sous-type n’est requis ou lorsqu’un sous-type est requis.</span><span class="sxs-lookup"><span data-stu-id="3204b-105">The following constants can be used when no subtype is required or when any subtype is required.</span></span>



| <span data-ttu-id="3204b-106">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="3204b-106">Constant/value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="3204b-107">Description</span><span class="sxs-lookup"><span data-stu-id="3204b-107">Description</span></span>                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span id="WINBIO_SUBTYPE_NO_INFORMATION"></span><span id="winbio_subtype_no_information"></span><dl> <span data-ttu-id="3204b-108"><dt>**WINBIO \_ SubType \_ no \_ information**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="3204b-108"><dt>**WINBIO\_SUBTYPE\_NO\_INFORMATION**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="3204b-109">Aucune information de sous-type.</span><span class="sxs-lookup"><span data-stu-id="3204b-109">No subtype information.</span></span><br/> |
| <span id="WINBIO_SUBTYPE_ANY"></span><span id="winbio_subtype_any"></span><dl> <span data-ttu-id="3204b-110"><dt>**WINBIO \_ SOUS-TYPE \_ n’importe quel**</dt> <dt>0xFF</dt></span><span class="sxs-lookup"><span data-stu-id="3204b-110"><dt>**WINBIO\_SUBTYPE\_ANY**</dt> <dt>0xFF</dt></span></span> </dl>                                   | <span data-ttu-id="3204b-111">Tout sous-type.</span><span class="sxs-lookup"><span data-stu-id="3204b-111">Any subtype.</span></span><br/>            |



## <a name="remarks"></a><span data-ttu-id="3204b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="3204b-112">Remarks</span></span>

<span data-ttu-id="3204b-113">Pour rechercher les sous-types biométriques disponibles pour un type biométrique particulier, utilisez le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="3204b-113">To find the available biometric subtypes for a particular biometric type, use the following table:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3204b-114">Valeur <strong>WINBIO_BIOMETRIC_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="3204b-114"><strong>WINBIO_BIOMETRIC_TYPE</strong> value</span></span></th>
<th><span data-ttu-id="3204b-115">Rubrique (s) pour rechercher <strong>WINBIO_BIOMETRIC_SUBTYPE</strong> valeurs</span><span class="sxs-lookup"><span data-stu-id="3204b-115">Topic(s) to find <strong>WINBIO_BIOMETRIC_SUBTYPE</strong> values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3204b-116"><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></span><span class="sxs-lookup"><span data-stu-id="3204b-116"><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></span></span></td>
<td><span data-ttu-id="3204b-117"><a href="winbio-ansi-385-face-constants.md"><strong>Constantes WINBIO_ANSI_385_FACE</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="3204b-117"><a href="winbio-ansi-385-face-constants.md"><strong>WINBIO_ANSI_385_FACE Constants</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="3204b-118">Ces valeurs s’appliquent uniquement à Windows 10 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3204b-118">These values apply only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3204b-119"><strong>WINBIO_TYPE_FINGERPRINT</strong></span><span class="sxs-lookup"><span data-stu-id="3204b-119"><strong>WINBIO_TYPE_FINGERPRINT</strong></span></span></td>
<td><span data-ttu-id="3204b-120">Une des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="3204b-120">One of the following topics:</span></span>
<ul>
<li><span data-ttu-id="3204b-121"><a href="winbio-ansi-381-format-constants.md"><strong>Constantes WINBIO_ANSI_381_FORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="3204b-121"><a href="winbio-ansi-381-format-constants.md"><strong>WINBIO_ANSI_381_FORMAT Constants</strong></a></span></span></li>
<li><span data-ttu-id="3204b-122"><a href="winbio-ansi-381-img-constants.md"><strong>Constantes WINBIO_ANSI_381_IMG</strong></a></span><span class="sxs-lookup"><span data-stu-id="3204b-122"><a href="winbio-ansi-381-img-constants.md"><strong>WINBIO_ANSI_381_IMG Constants</strong></a></span></span></li>
<li><span data-ttu-id="3204b-123"><a href="winbio-ansi-381-img-acq-constants.md"><strong>Constantes WINBIO_ANSI_381_IMG_ACQ</strong></a></span><span class="sxs-lookup"><span data-stu-id="3204b-123"><a href="winbio-ansi-381-img-acq-constants.md"><strong>WINBIO_ANSI_381_IMG_ACQ Constants</strong></a></span></span></li>
<li><span data-ttu-id="3204b-124"><a href="winbio-ansi-381-imp-type-constants.md"><strong>Constantes WINBIO_ANSI_381_IMP_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="3204b-124"><a href="winbio-ansi-381-imp-type-constants.md"><strong>WINBIO_ANSI_381_IMP_TYPE Constants</strong></a></span></span></li>
<li><span data-ttu-id="3204b-125"><a href="winbio-ansi-381-pixels-constants.md"><strong>Constantes WINBIO_ANSI_381_PIXELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="3204b-125"><a href="winbio-ansi-381-pixels-constants.md"><strong>WINBIO_ANSI_381_PIXELS Constants</strong></a></span></span></li>
<li><span data-ttu-id="3204b-126"><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>WINBIO_ANSI_381_POS les constantes d’empreinte digitale</strong></a></span><span class="sxs-lookup"><span data-stu-id="3204b-126"><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>WINBIO_ANSI_381_POS Fingerprint Constants</strong></a></span></span></li>
<li><span data-ttu-id="3204b-127"><a href="winbio-ansi-381-pos-palm-constants.md"><strong>Constantes WINBIO_ANSI_381_POS_Palm</strong></a></span><span class="sxs-lookup"><span data-stu-id="3204b-127"><a href="winbio-ansi-381-pos-palm-constants.md"><strong>WINBIO_ANSI_381_POS_Palm Constants</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3204b-128"><strong>WINBIO_TYPE_IRIS</strong></span><span class="sxs-lookup"><span data-stu-id="3204b-128"><strong>WINBIO_TYPE_IRIS</strong></span></span></td>
<td><span data-ttu-id="3204b-129"><a href="winbio-iris-constants.md"><strong>Constantes WINBIO_IRIS</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="3204b-129"><a href="winbio-iris-constants.md"><strong>WINBIO_IRIS Constants</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="3204b-130">Ces valeurs s’appliquent uniquement à Windows 10 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3204b-130">These values apply only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3204b-131"><strong>WINBIO_TYPE_VOICE</strong></span><span class="sxs-lookup"><span data-stu-id="3204b-131"><strong>WINBIO_TYPE_VOICE</strong></span></span></td>
<td><span data-ttu-id="3204b-132"><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>Constantes WINBIO_VOICE</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="3204b-132"><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>WINBIO_VOICE Constants</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="3204b-133">Ces valeurs s’appliquent uniquement à Windows 10 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3204b-133">These values apply only for Windows 10 and later.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3204b-134">Pour plus d’informations, consultez [constantes d’application cliente](client-application-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3204b-134">For more information, see [Client Application Constants](client-application-constants.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3204b-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3204b-135">Requirements</span></span>



| <span data-ttu-id="3204b-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3204b-136">Requirement</span></span> | <span data-ttu-id="3204b-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="3204b-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3204b-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3204b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="3204b-139">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3204b-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="3204b-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3204b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="3204b-141">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3204b-141">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3204b-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="3204b-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="3204b-143"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3204b-143"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





