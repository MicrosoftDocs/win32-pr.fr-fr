---
title: Constantes WINBIO_POOL ( \_ types WINBIO. h)
description: Spécifiez le type de pool d’unités biométriques à utiliser dans la session.
ms.assetid: e6e49b95-981a-477d-9889-ea132db5b387
topic_type:
- apiref
api_name:
- WINBIO_POOL_UNKNOWN
- WINBIO_POOL_SYSTEM
- WINBIO_POOL_PRIVATE
- WINBIO_POOL_UNASSIGNED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7af1ec8d5692a390bb91ecb63736bd94efb2e85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509406"
---
# <a name="winbio_pool-constants"></a><span data-ttu-id="e344c-103">\_Constantes de pool WINBIO</span><span class="sxs-lookup"><span data-stu-id="e344c-103">WINBIO\_POOL Constants</span></span>

<span data-ttu-id="e344c-104">Les constantes suivantes peuvent être utilisées dans la fonction [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) pour spécifier le type de pool d’unités biométriques à utiliser dans la session.</span><span class="sxs-lookup"><span data-stu-id="e344c-104">The following constants can be used in the [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) function to specify the type of biometric unit pool to be used in the session.</span></span>



| <span data-ttu-id="e344c-105">Constante</span><span class="sxs-lookup"><span data-stu-id="e344c-105">Constant</span></span>                                                                                                                                                                                  | <span data-ttu-id="e344c-106">Description</span><span class="sxs-lookup"><span data-stu-id="e344c-106">Description</span></span>                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <span data-ttu-id="e344c-107"><dt>**\_pool WINBIO \_ inconnu**</dt></span><span class="sxs-lookup"><span data-stu-id="e344c-107"><dt>**WINBIO\_POOL\_UNKNOWN**</dt></span></span> </dl>          | <span data-ttu-id="e344c-108">Le type de pool est inconnu.</span><span class="sxs-lookup"><span data-stu-id="e344c-108">The pool type is unknown.</span></span><br/>                                                         |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <span data-ttu-id="e344c-109"><dt>**\_système de pool WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e344c-109"><dt>**WINBIO\_POOL\_SYSTEM**</dt></span></span> </dl>             | <span data-ttu-id="e344c-110">Spécifie une collection partagée d’unités biométriques gérées par le fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="e344c-110">Specifies a shared collection of biometric units managed by the service provider.</span></span><br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <span data-ttu-id="e344c-111"><dt>**\_pool WINBIO \_ privé**</dt></span><span class="sxs-lookup"><span data-stu-id="e344c-111"><dt>**WINBIO\_POOL\_PRIVATE**</dt></span></span> </dl>          | <span data-ttu-id="e344c-112">Spécifie une collection d’unités biométriques gérées par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e344c-112">Specifies a collection of biometric units that are managed by the caller.</span></span><br/>         |
| <span id="WINBIO_POOL_UNASSIGNED"></span><span id="winbio_pool_unassigned"></span><dl> <span data-ttu-id="e344c-113"><dt>**\_pool WINBIO \_ non assigné**</dt></span><span class="sxs-lookup"><span data-stu-id="e344c-113"><dt>**WINBIO\_POOL\_UNASSIGNED**</dt></span></span> </dl> | <span data-ttu-id="e344c-114">Réservé.</span><span class="sxs-lookup"><span data-stu-id="e344c-114">Reserved.</span></span><br/>                                                                         |



## <a name="requirements"></a><span data-ttu-id="e344c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e344c-115">Requirements</span></span>



| <span data-ttu-id="e344c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e344c-116">Requirement</span></span> | <span data-ttu-id="e344c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e344c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e344c-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e344c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e344c-119">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e344c-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="e344c-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e344c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e344c-121">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e344c-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e344c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e344c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e344c-123"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e344c-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e344c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e344c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e344c-125">Constantes d’application cliente</span><span class="sxs-lookup"><span data-stu-id="e344c-125">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





