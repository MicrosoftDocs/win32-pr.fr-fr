---
title: Constantes WINBIO_BIR_QUALITY ( \_ types WINBIO. h)
description: Spécifiez la qualité relative des données biométriques dans le BIR si une valeur entière comprise entre 0 et 100 n’a pas été spécifiée.
ms.assetid: A42AA21B-9AA5-4DB6-B58F-0776BEC63E6C
topic_type:
- apiref
api_name:
- WINBIO_DATA_QUALITY_NOT_SET
- WINBIO_DATA_QUALITY_NOT_SUPPORTED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1eb0881672c9e3bf51214cff93cb3f68d802b04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106192"
---
# <a name="winbio_bir_quality-constants"></a><span data-ttu-id="f62e3-103">\_ \_ Constantes de qualité WINBIO Bir</span><span class="sxs-lookup"><span data-stu-id="f62e3-103">WINBIO\_BIR\_QUALITY Constants</span></span>

<span data-ttu-id="f62e3-104">Les indicateurs suivants sont utilisés par le membre **DataQuality** de la structure d' [**\_ \_ en-tête Bir WINBIO**](winbio-bir-header.md) pour spécifier la qualité relative des données biométriques dans le Bir si une valeur entière comprise entre 0 et 100 n’a pas été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f62e3-104">The following flags are used by the **DataQuality** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure to specify the relative quality of biometric data in the BIR if an integer value from 0 to 100 has not been specified.</span></span>



| <span data-ttu-id="f62e3-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="f62e3-105">Constant/value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="f62e3-106">Description</span><span class="sxs-lookup"><span data-stu-id="f62e3-106">Description</span></span>                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <span data-ttu-id="f62e3-107"><dt>**WINBIO \_ Qualité des données \_ \_ non \_ définie**</dt> <dt> 1</dt></span><span class="sxs-lookup"><span data-stu-id="f62e3-107"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SET**</dt> <dt> 1</dt></span></span> </dl>                   | <span data-ttu-id="f62e3-108">Les mesures de qualité sont prises en charge par le créateur BIR, mais aucune valeur n’est définie dans BIR.</span><span class="sxs-lookup"><span data-stu-id="f62e3-108">Quality measurements are supported by the BIR creator, but no value is set in the BIR.</span></span><br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <span data-ttu-id="f62e3-109"><dt>**WINBIO \_ Qualité des données \_ \_ non \_ prise en charge**</dt> <dt> 2</dt></span><span class="sxs-lookup"><span data-stu-id="f62e3-109"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SUPPORTED**</dt> <dt> 2</dt></span></span> </dl> | <span data-ttu-id="f62e3-110">Les mesures de qualité ne sont pas prises en charge par le créateur BIR.</span><span class="sxs-lookup"><span data-stu-id="f62e3-110">Quality measurements are not supported by the BIR creator.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="f62e3-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f62e3-111">Requirements</span></span>



| <span data-ttu-id="f62e3-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f62e3-112">Requirement</span></span> | <span data-ttu-id="f62e3-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="f62e3-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f62e3-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f62e3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f62e3-115">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f62e3-115">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="f62e3-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f62e3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f62e3-117">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f62e3-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f62e3-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f62e3-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f62e3-119"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f62e3-119"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f62e3-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f62e3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f62e3-121">Constantes d’application cliente</span><span class="sxs-lookup"><span data-stu-id="f62e3-121">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





