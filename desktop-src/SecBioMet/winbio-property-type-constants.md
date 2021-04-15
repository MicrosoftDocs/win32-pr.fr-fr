---
title: Constantes WINBIO_PROPERTY_TYPE (WinBio. h)
description: Spécifiez la source des informations de propriété dans la fonction WinBioGetProperty.
ms.assetid: 82C54092-032B-4F32-820E-A1D4BB81ECCE
topic_type:
- apiref
api_name:
- WINBIO_PROPERTY_TYPE_SESSION
- WINBIO_PROPERTY_TYPE_TEMPLATE
- WINBIO_PROPERTY_TYPE_UNIT
- WINBIO_PROPERTY_TYPE_ACCOUNT
api_location:
- Winbio.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4a1420af18bfa4d2ba5d0457b22cd5f77e7b0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466998"
---
# <a name="winbio_property_type-constants"></a><span data-ttu-id="8cfd2-103">\_Constantes de type de propriété WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="8cfd2-103">WINBIO\_PROPERTY\_TYPE Constants</span></span>

<span data-ttu-id="8cfd2-104">Les constantes de **\_ \_ type de propriété WINBIO** suivantes peuvent être utilisées pour spécifier la source des informations de propriété dans la fonction [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty) .</span><span class="sxs-lookup"><span data-stu-id="8cfd2-104">The following **WINBIO\_PROPERTY\_TYPE** constants can be used to specify the source of the property information in the [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty) function.</span></span>

<dl> <dt>

<span data-ttu-id="8cfd2-105"><span id="WINBIO_PROPERTY_TYPE_SESSION"></span><span id="winbio_property_type_session"></span>**\_session de \_ type de propriété WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="8cfd2-105"><span id="WINBIO_PROPERTY_TYPE_SESSION"></span><span id="winbio_property_type_session"></span>**WINBIO\_PROPERTY\_TYPE\_SESSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cfd2-106">La propriété s’applique à une session biométrique spécifique.</span><span class="sxs-lookup"><span data-stu-id="8cfd2-106">The property applies to a specific biometric session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cfd2-107"><span id="WINBIO_PROPERTY_TYPE_TEMPLATE"></span><span id="winbio_property_type_template"></span>**\_modèle de \_ type de propriété WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="8cfd2-107"><span id="WINBIO_PROPERTY_TYPE_TEMPLATE"></span><span id="winbio_property_type_template"></span>**WINBIO\_PROPERTY\_TYPE\_TEMPLATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cfd2-108">La propriété s’applique à un modèle biométrique spécifique.</span><span class="sxs-lookup"><span data-stu-id="8cfd2-108">The property applies to a specific biometric template.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cfd2-109"><span id="WINBIO_PROPERTY_TYPE_UNIT"></span><span id="winbio_property_type_unit"></span>**\_unité de \_ type de propriété WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="8cfd2-109"><span id="WINBIO_PROPERTY_TYPE_UNIT"></span><span id="winbio_property_type_unit"></span>**WINBIO\_PROPERTY\_TYPE\_UNIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cfd2-110">La propriété s’applique à une unité biométrique spécifique.</span><span class="sxs-lookup"><span data-stu-id="8cfd2-110">The property applies to a specific biometric unit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8cfd2-111"><span id="WINBIO_PROPERTY_TYPE_ACCOUNT"></span><span id="winbio_property_type_account"></span>**\_type de propriété WINBIO \_ \_ compte**</span><span class="sxs-lookup"><span data-stu-id="8cfd2-111"><span id="WINBIO_PROPERTY_TYPE_ACCOUNT"></span><span id="winbio_property_type_account"></span>**WINBIO\_PROPERTY\_TYPE\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8cfd2-112">La propriété s’applique à un compte d’utilisateur spécifique qui a une inscription biométrique.</span><span class="sxs-lookup"><span data-stu-id="8cfd2-112">The property applies to a specific user account that has a biometric enrollment.</span></span> <span data-ttu-id="8cfd2-113">Cette valeur est prise en charge à partir de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8cfd2-113">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8cfd2-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8cfd2-114">Requirements</span></span>



| <span data-ttu-id="8cfd2-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8cfd2-115">Requirement</span></span> | <span data-ttu-id="8cfd2-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8cfd2-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cfd2-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8cfd2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8cfd2-118">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8cfd2-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="8cfd2-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8cfd2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8cfd2-120">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8cfd2-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8cfd2-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="8cfd2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cfd2-122"><dt>WinBio. h (inclure WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8cfd2-122"><dt>Winbio.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cfd2-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8cfd2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cfd2-124">Constantes d’application cliente</span><span class="sxs-lookup"><span data-stu-id="8cfd2-124">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="8cfd2-125">**WinBioGetProperty**</span><span class="sxs-lookup"><span data-stu-id="8cfd2-125">**WinBioGetProperty**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> </dl>

 

 





