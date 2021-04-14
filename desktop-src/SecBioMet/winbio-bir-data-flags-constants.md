---
title: Constantes WINBIO_BIR_DATA_FLAGS ( \_ types WINBIO. h)
description: Spécifiez la condition des données.
ms.assetid: F6F7F68A-3294-4AF8-A1A7-C6A869A2CC3C
topic_type:
- apiref
api_name:
- WINBIO_DATA_FLAG_PRIVACY
- WINBIO_DATA_FLAG_INTEGRITY
- WINBIO_DATA_FLAG_SIGNED
- WINBIO_DATA_FLAG_RAW
- WINBIO_DATA_FLAG_INTERMEDIATE
- WINBIO_DATA_FLAG_PROCESSED
- WINBIO_DATA_FLAG_OPTION_MASK_PRESENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8195cf17040c35b9e42f8977b36c5ddc6f2ea33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385263"
---
# <a name="winbio_bir_data_flags-constants"></a><span data-ttu-id="97f4b-103">\_ \_ Constantes d’indicateurs de données WINBIO Bir \_</span><span class="sxs-lookup"><span data-stu-id="97f4b-103">WINBIO\_BIR\_DATA\_FLAGS Constants</span></span>

<span data-ttu-id="97f4b-104">Les constantes suivantes sont utilisées par le membre **DataFlags** de la structure d' [**\_ \_ en-tête Bir WINBIO**](winbio-bir-header.md) .</span><span class="sxs-lookup"><span data-stu-id="97f4b-104">The following constants are used by the **DataFlags** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure.</span></span>



| <span data-ttu-id="97f4b-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="97f4b-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                   | <span data-ttu-id="97f4b-106">Description</span><span class="sxs-lookup"><span data-stu-id="97f4b-106">Description</span></span>                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <span data-ttu-id="97f4b-107"><dt>**WINBIO \_ \_ \_ Confidentialité**</dt> de l’indicateur de données <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="97f4b-107"><dt>**WINBIO\_DATA\_FLAG\_PRIVACY**</dt> <dt>0x02</dt></span></span> </dl>                                       | <span data-ttu-id="97f4b-108">Les données sont chiffrées.</span><span class="sxs-lookup"><span data-stu-id="97f4b-108">The data is encrypted.</span></span><br/>                                                                                                                                                                                 |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <span data-ttu-id="97f4b-109"><dt>**WINBIO \_ \_ \_ Intégrité des indicateurs de données**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="97f4b-109"><dt>**WINBIO\_DATA\_FLAG\_INTEGRITY**</dt> <dt>0x01</dt></span></span> </dl>                                 | <span data-ttu-id="97f4b-110">Les données sont signées numériquement ou sont protégées par un code d’authentification de message (MAC).</span><span class="sxs-lookup"><span data-stu-id="97f4b-110">The data is digitally signed or is protected by a message authentication code (MAC).</span></span><br/>                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <span data-ttu-id="97f4b-111"><dt>**WINBIO \_ Indicateur de données \_ \_ signé**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="97f4b-111"><dt>**WINBIO\_DATA\_FLAG\_SIGNED**</dt> <dt>0x04</dt></span></span> </dl>                                          | <span data-ttu-id="97f4b-112">Si cet indicateur et l’indicateur d’intégrité de l' **\_ indicateur de données \_ \_ WINBIO** sont définis, les données sont signées.</span><span class="sxs-lookup"><span data-stu-id="97f4b-112">If this flag and the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag are set, the data is signed.</span></span> <span data-ttu-id="97f4b-113">Si cet indicateur n’est pas défini, mais que l’indicateur d’intégrité de l' **\_ indicateur de données \_ \_ WINBIO** est défini, un Mac est calculé sur les données.</span><span class="sxs-lookup"><span data-stu-id="97f4b-113">If this flag is not set but the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag is set, a MAC is computed on the data.</span></span><br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <span data-ttu-id="97f4b-114"><dt>**WINBIO \_ \_Indicateur de \_ données**</dt> - <dt>0x20</dt> brut</span><span class="sxs-lookup"><span data-stu-id="97f4b-114"><dt>**WINBIO\_DATA\_FLAG\_RAW**</dt> <dt>0x20</dt></span></span> </dl>                                                   | <span data-ttu-id="97f4b-115">Les données sont au format avec lequel elles ont été capturées.</span><span class="sxs-lookup"><span data-stu-id="97f4b-115">The data is in the format with which it was captured.</span></span><br/>                                                                                                                                                  |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <span data-ttu-id="97f4b-116"><dt>**WINBIO \_ \_Indicateur de \_ données**</dt> - <dt>0x40</dt> intermédiaire</span><span class="sxs-lookup"><span data-stu-id="97f4b-116"><dt>**WINBIO\_DATA\_FLAG\_INTERMEDIATE**</dt> <dt>0x40</dt></span></span> </dl>                        | <span data-ttu-id="97f4b-117">Les données ne sont pas brutes, mais elles n’ont pas été complètement traitées.</span><span class="sxs-lookup"><span data-stu-id="97f4b-117">The data is not raw but has not been completely processed.</span></span><br/>                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <span data-ttu-id="97f4b-118"><dt>**WINBIO \_ Indicateur de données \_ \_ traité**</dt> à <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="97f4b-118"><dt>**WINBIO\_DATA\_FLAG\_PROCESSED**</dt> <dt>0x80</dt></span></span> </dl>                                 | <span data-ttu-id="97f4b-119">Les données ont été traitées.</span><span class="sxs-lookup"><span data-stu-id="97f4b-119">The data has been processed.</span></span><br/>                                                                                                                                                                           |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <span data-ttu-id="97f4b-120"><dt>**WINBIO \_ Masque d’option de l’indicateur de données \_ \_ \_ \_ actuel**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="97f4b-120"><dt>**WINBIO\_DATA\_FLAG\_OPTION\_MASK\_PRESENT**</dt> <dt>0x08</dt></span></span> </dl> | <span data-ttu-id="97f4b-121">Masque de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="97f4b-121">The flag mask.</span></span> <span data-ttu-id="97f4b-122">Cette valeur est toujours un (1).</span><span class="sxs-lookup"><span data-stu-id="97f4b-122">This value is always one (1).</span></span><br/>                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="97f4b-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97f4b-123">Requirements</span></span>



| <span data-ttu-id="97f4b-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97f4b-124">Requirement</span></span> | <span data-ttu-id="97f4b-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="97f4b-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97f4b-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97f4b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="97f4b-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97f4b-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="97f4b-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97f4b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="97f4b-129">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97f4b-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="97f4b-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="97f4b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="97f4b-131"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="97f4b-131"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97f4b-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97f4b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97f4b-133">Constantes d’application cliente</span><span class="sxs-lookup"><span data-stu-id="97f4b-133">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





