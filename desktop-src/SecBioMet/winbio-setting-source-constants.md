---
title: Constantes WINBIO_SETTING_SOURCE ( \_ types WINBIO. h)
description: Déterminez si la Windows Biometric Framework est actuellement activée.
ms.assetid: d95aa6cc-ddff-40fb-ab82-eac78dc0cb6b
topic_type:
- apiref
api_name:
- WINBIO_SETTING_SOURCE_INVALID
- WINBIO_SETTING_SOURCE_DEFAULT
- WINBIO_SETTING_SOURCE_POLICY
- WINBIO_SETTING_SOURCE_LOCAL
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54723612c7e0948e09baddf22ad4f4703ca5c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942816"
---
# <a name="winbio_setting_source-constants"></a><span data-ttu-id="f916d-103">\_Constantes de la source de paramètre WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="f916d-103">WINBIO\_SETTING\_SOURCE Constants</span></span>

<span data-ttu-id="f916d-104">Les constantes suivantes sont utilisées par la fonction [**WinBioGetEnabledSetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting) pour déterminer si la Windows Biometric Framework est actuellement activée.</span><span class="sxs-lookup"><span data-stu-id="f916d-104">The following constants are used by the [**WinBioGetEnabledSetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting) function to determine whether the Windows Biometric Framework is currently enabled.</span></span> <span data-ttu-id="f916d-105">Les constantes spécifient l’origine du paramètre.</span><span class="sxs-lookup"><span data-stu-id="f916d-105">The constants specify where the setting originated.</span></span>



| <span data-ttu-id="f916d-106">Constante</span><span class="sxs-lookup"><span data-stu-id="f916d-106">Constant</span></span>                                                                                                                                                                                                        | <span data-ttu-id="f916d-107">Description</span><span class="sxs-lookup"><span data-stu-id="f916d-107">Description</span></span>                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| <span id="WINBIO_SETTING_SOURCE_INVALID"></span><span id="winbio_setting_source_invalid"></span><dl> <span data-ttu-id="f916d-108"><dt>**\_source du paramètre WINBIO \_ \_ non valide**</dt></span><span class="sxs-lookup"><span data-stu-id="f916d-108"><dt>**WINBIO\_SETTING\_SOURCE\_INVALID**</dt></span></span> </dl> | <span data-ttu-id="f916d-109">Le paramètre n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f916d-109">The setting is not valid.</span></span><br/>                              |
| <span id="WINBIO_SETTING_SOURCE_DEFAULT"></span><span id="winbio_setting_source_default"></span><dl> <span data-ttu-id="f916d-110"><dt>**\_ \_ \_ valeur par défaut de la source du paramètre WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="f916d-110"><dt>**WINBIO\_SETTING\_SOURCE\_DEFAULT**</dt></span></span> </dl> | <span data-ttu-id="f916d-111">Le paramètre provient de la stratégie intégrée.</span><span class="sxs-lookup"><span data-stu-id="f916d-111">The setting originated from built-in policy.</span></span><br/>           |
| <span id="WINBIO_SETTING_SOURCE_POLICY"></span><span id="winbio_setting_source_policy"></span><dl> <span data-ttu-id="f916d-112"><dt>**\_stratégie de \_ source du paramètre WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f916d-112"><dt>**WINBIO\_SETTING\_SOURCE\_POLICY**</dt></span></span> </dl>    | <span data-ttu-id="f916d-113">Le paramètre provient du registre de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="f916d-113">The setting originated in the local computer registry.</span></span><br/> |
| <span id="WINBIO_SETTING_SOURCE_LOCAL"></span><span id="winbio_setting_source_local"></span><dl> <span data-ttu-id="f916d-114"><dt>**\_ \_ source locale du paramètre WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f916d-114"><dt>**WINBIO\_SETTING\_SOURCE\_LOCAL**</dt></span></span> </dl>       | <span data-ttu-id="f916d-115">Le paramètre a été créé par stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="f916d-115">The setting was created by Group Policy</span></span><br/>                |



## <a name="requirements"></a><span data-ttu-id="f916d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f916d-116">Requirements</span></span>



| <span data-ttu-id="f916d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f916d-117">Requirement</span></span> | <span data-ttu-id="f916d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f916d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f916d-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f916d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f916d-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f916d-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="f916d-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f916d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f916d-122">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f916d-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f916d-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="f916d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f916d-124"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f916d-124"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f916d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f916d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f916d-126">Constantes d’application cliente</span><span class="sxs-lookup"><span data-stu-id="f916d-126">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





