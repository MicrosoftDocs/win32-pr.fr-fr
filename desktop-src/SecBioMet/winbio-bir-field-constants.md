---
title: Constantes WINBIO_BIR_FIELD ( \_ types WINBIO. h)
description: Spécifiez un masque de masque.
ms.assetid: D8D12BCF-FEB3-4E02-B751-9F3AE5048BC1
topic_type:
- apiref
api_name:
- WINBIO_BIR_FIELD_SUBHEAD_COUNT
- WINBIO_BIR_FIELD_PRODUCT_ID
- WINBIO_BIR_FIELD_PATRON_ID
- WINBIO_BIR_FIELD_INDEX
- WINBIO_BIR_FIELD_CREATION_DATE
- WINBIO_BIR_FIELD_VALIDITY_PERIOD
- WINBIO_BIR_FIELD_BIOMETRIC_TYPE
- WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE
- WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION
- WINBIO_BIR_FIELD_PATRON_HEADER_VERSION
- WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE
- WINBIO_BIR_FIELD_BIOMETRIC_CONDITION
- WINBIO_BIR_FIELD_QUALITY
- WINBIO_BIR_FIELD_CREATOR
- WINBIO_BIR_FIELD_CHALLENGE
- WINBIO_BIR_FIELD_PAYLOAD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 104710f1686f13227fbe65782c2baf9c13149650
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317269"
---
# <a name="winbio_bir_field-constants"></a><span data-ttu-id="9f72b-103">\_ \_ Constantes de champ WINBIO Bir</span><span class="sxs-lookup"><span data-stu-id="9f72b-103">WINBIO\_BIR\_FIELD Constants</span></span>

<span data-ttu-id="9f72b-104">Les constantes suivantes sont utilisées pour créer un masque de masque pour le membre **ValidFields** de la structure d' [**\_ \_ en-tête Bir WINBIO**](winbio-bir-header.md) .</span><span class="sxs-lookup"><span data-stu-id="9f72b-104">The following constants are used to create a bitmask for the **ValidFields** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure.</span></span>



| <span data-ttu-id="9f72b-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="9f72b-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="9f72b-106">Description</span><span class="sxs-lookup"><span data-stu-id="9f72b-106">Description</span></span>                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_BIR_FIELD_SUBHEAD_COUNT"></span><span id="winbio_bir_field_subhead_count"></span><dl> <span data-ttu-id="9f72b-107"><dt>**WINBIO \_ BIR \_ \_ \_ nombre**</dt> de sous-valeur de champ <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="9f72b-107"><dt>**WINBIO\_BIR\_FIELD\_SUBHEAD\_COUNT**</dt> <dt>0x0001</dt></span></span> </dl>                          | <span data-ttu-id="9f72b-108">Fourni pour la conformité avec le NISTIR 6529-A, le format d’un patron CBEFF (Common Exchange formats) est un format, mais non utilisé.</span><span class="sxs-lookup"><span data-stu-id="9f72b-108">Provided for conformity with NISTIR 6529-A, the Common Biometric Exchange Formats Framework (CBEFF) Patron Format A, but not used.</span></span><br/> |
| <span id="WINBIO_BIR_FIELD_PRODUCT_ID"></span><span id="winbio_bir_field_product_id"></span><dl> <span data-ttu-id="9f72b-109"><dt>**WINBIO \_ BIR \_ champ \_ \_ ID produit**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="9f72b-109"><dt>**WINBIO\_BIR\_FIELD\_PRODUCT\_ID**</dt> <dt>0x0002</dt></span></span> </dl>                                   | <span data-ttu-id="9f72b-110">Le membre **ProductID** est valide.</span><span class="sxs-lookup"><span data-stu-id="9f72b-110">The **ProductId** member is valid.</span></span><br/>                                                                                                 |
| <span id="WINBIO_BIR_FIELD_PATRON_ID"></span><span id="winbio_bir_field_patron_id"></span><dl> <span data-ttu-id="9f72b-111"><dt>**WINBIO \_ \_ID d' \_ \_ acheteur du champ Bir**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="9f72b-111"><dt>**WINBIO\_BIR\_FIELD\_PATRON\_ID**</dt> <dt>0x0004</dt></span></span> </dl>                                      | <span data-ttu-id="9f72b-112">Fourni pour la conformité avec NISTIR 6529-A, CBEFF patron format A, mais n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="9f72b-112">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_INDEX"></span><span id="winbio_bir_field_index"></span><dl> <span data-ttu-id="9f72b-113"><dt>**WINBIO \_ BIR \_ \_ index de champ**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="9f72b-113"><dt>**WINBIO\_BIR\_FIELD\_INDEX**</dt> <dt>0x0008</dt></span></span> </dl>                                                   | <span data-ttu-id="9f72b-114">Fourni pour la conformité avec NISTIR 6529-A, CBEFF patron format A, mais n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="9f72b-114">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CREATION_DATE"></span><span id="winbio_bir_field_creation_date"></span><dl> <span data-ttu-id="9f72b-115"><dt>**WINBIO \_ \_Date de \_ création \_ du champ Bir**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="9f72b-115"><dt>**WINBIO\_BIR\_FIELD\_CREATION\_DATE**</dt> <dt>0x0010</dt></span></span> </dl>                          | <span data-ttu-id="9f72b-116">Le membre **CreationDate** est valide.</span><span class="sxs-lookup"><span data-stu-id="9f72b-116">The **CreationDate** member is valid.</span></span><br/>                                                                                              |
| <span id="WINBIO_BIR_FIELD_VALIDITY_PERIOD"></span><span id="winbio_bir_field_validity_period"></span><dl> <span data-ttu-id="9f72b-117"><dt>**WINBIO \_ \_Période de \_ validité \_ du champ Bir**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="9f72b-117"><dt>**WINBIO\_BIR\_FIELD\_VALIDITY\_PERIOD**</dt> <dt>0x0020</dt></span></span> </dl>                    | <span data-ttu-id="9f72b-118">Le membre **ValidityPeriod** est valide.</span><span class="sxs-lookup"><span data-stu-id="9f72b-118">The **ValidityPeriod** member is valid.</span></span><br/>                                                                                            |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_TYPE"></span><span id="winbio_bir_field_biometric_type"></span><dl> <span data-ttu-id="9f72b-119"><dt>**WINBIO \_ \_ \_ \_ Type biométrique du champ Bir**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="9f72b-119"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_TYPE**</dt> <dt>0x0040</dt></span></span> </dl>                       | <span data-ttu-id="9f72b-120">Le membre de **type** est valide.</span><span class="sxs-lookup"><span data-stu-id="9f72b-120">The **Type** member is valid.</span></span><br/>                                                                                                      |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE"></span><span id="winbio_bir_field_biometric_subtype"></span><dl> <span data-ttu-id="9f72b-121"><dt>**WINBIO \_ BIR, \_ champ de \_ sous- \_ type biométrique**</dt> <dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="9f72b-121"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_SUBTYPE**</dt> <dt>0x0080</dt></span></span> </dl>              | <span data-ttu-id="9f72b-122">Le membre de **sous-type** est valide.</span><span class="sxs-lookup"><span data-stu-id="9f72b-122">The **Subtype** member is valid.</span></span><br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION"></span><span id="winbio_bir_field_cbeff_header_version"></span><dl> <span data-ttu-id="9f72b-123"><dt>**WINBIO \_ BIR \_ champ \_ CBEFF \_ \_ version d’en-tête**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="9f72b-123"><dt>**WINBIO\_BIR\_FIELD\_CBEFF\_HEADER\_VERSION**</dt> <dt>0x0100</dt></span></span> </dl>    | <span data-ttu-id="9f72b-124">Le membre **HeaderVersion** est valide.</span><span class="sxs-lookup"><span data-stu-id="9f72b-124">The **HeaderVersion** member is valid.</span></span><br/>                                                                                             |
| <span id="WINBIO_BIR_FIELD_PATRON_HEADER_VERSION"></span><span id="winbio_bir_field_patron_header_version"></span><dl> <span data-ttu-id="9f72b-125"><dt>**WINBIO \_ BIR \_ d' \_ en-tête d’un champ d' \_ en-tête \_**</dt> <dt>0x0200</dt></span><span class="sxs-lookup"><span data-stu-id="9f72b-125"><dt>**WINBIO\_BIR\_FIELD\_PATRON\_HEADER\_VERSION**</dt> <dt>0x0200</dt></span></span> </dl> | <span data-ttu-id="9f72b-126">Le membre **PatronHeaderVersion** est valide.</span><span class="sxs-lookup"><span data-stu-id="9f72b-126">The **PatronHeaderVersion** member is valid.</span></span><br/>                                                                                       |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE"></span><span id="winbio_bir_field_biometric_purpose"></span><dl> <span data-ttu-id="9f72b-127"><dt>**WINBIO \_ \_Champ Bir \_ \_ objet biométrique**</dt> <dt>0x0400</dt></span><span class="sxs-lookup"><span data-stu-id="9f72b-127"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_PURPOSE**</dt> <dt>0x0400</dt></span></span> </dl>              | <span data-ttu-id="9f72b-128">Le membre **objectif** est valide.</span><span class="sxs-lookup"><span data-stu-id="9f72b-128">The **Purpose** member is valid.</span></span><br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_CONDITION"></span><span id="winbio_bir_field_biometric_condition"></span><dl> <span data-ttu-id="9f72b-129"><dt>**WINBIO \_ \_ \_ \_ Condition biométrique du champ Bir**</dt> <dt>0x0800</dt></span><span class="sxs-lookup"><span data-stu-id="9f72b-129"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_CONDITION**</dt> <dt>0x0800</dt></span></span> </dl>        | <span data-ttu-id="9f72b-130">Fourni pour la conformité avec NISTIR 6529-A, CBEFF patron format A, mais n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="9f72b-130">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_QUALITY"></span><span id="winbio_bir_field_quality"></span><dl> <span data-ttu-id="9f72b-131"><dt>**WINBIO \_ BIR \_ \_ qualité du champ**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="9f72b-131"><dt>**WINBIO\_BIR\_FIELD\_QUALITY**</dt> <dt>0x1000</dt></span></span> </dl>                                             | <span data-ttu-id="9f72b-132">Le membre **DataQuality** est valide.</span><span class="sxs-lookup"><span data-stu-id="9f72b-132">The **DataQuality** member is valid.</span></span><br/>                                                                                               |
| <span id="WINBIO_BIR_FIELD_CREATOR"></span><span id="winbio_bir_field_creator"></span><dl> <span data-ttu-id="9f72b-133"><dt>**WINBIO \_ BIR \_ du \_ créateur du champ**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9f72b-133"><dt>**WINBIO\_BIR\_FIELD\_CREATOR**</dt> <dt>0x2000</dt></span></span> </dl>                                             | <span data-ttu-id="9f72b-134">Fourni pour la conformité avec NISTIR 6529-A, CBEFF patron format A, mais n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="9f72b-134">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CHALLENGE"></span><span id="winbio_bir_field_challenge"></span><dl> <span data-ttu-id="9f72b-135"><dt>**WINBIO \_ BIR \_ de \_ stimulation de champ**</dt> <dt>0x4000</dt></span><span class="sxs-lookup"><span data-stu-id="9f72b-135"><dt>**WINBIO\_BIR\_FIELD\_CHALLENGE**</dt> <dt>0x4000</dt></span></span> </dl>                                       | <span data-ttu-id="9f72b-136">Fourni pour la conformité avec NISTIR 6529-A, CBEFF patron format A, mais n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="9f72b-136">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_PAYLOAD"></span><span id="winbio_bir_field_payload"></span><dl> <span data-ttu-id="9f72b-137"><dt>**WINBIO \_ \_ \_ Charge utile du champ Bir**</dt> <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="9f72b-137"><dt>**WINBIO\_BIR\_FIELD\_PAYLOAD**</dt> <dt>0x8000</dt></span></span> </dl>                                             | <span data-ttu-id="9f72b-138">Fourni pour la conformité avec NISTIR 6529-A, CBEFF patron format A, mais n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="9f72b-138">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="9f72b-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f72b-139">Requirements</span></span>



| <span data-ttu-id="9f72b-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f72b-140">Requirement</span></span> | <span data-ttu-id="9f72b-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f72b-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f72b-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f72b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="9f72b-143">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f72b-143">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="9f72b-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f72b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="9f72b-145">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f72b-145">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9f72b-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="9f72b-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f72b-147"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f72b-147"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f72b-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f72b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f72b-149">Constantes d’application cliente</span><span class="sxs-lookup"><span data-stu-id="9f72b-149">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





