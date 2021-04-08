---
title: Type de confidentialité (Wininet. h)
description: Spécifie que les paramètres de confidentialité sont pour les cookies internes ou tiers.
ms.assetid: 7d0846d4-fd81-4af9-b7e6-05c4c1438770
topic_type:
- apiref
api_name:
- PRIVACY_TYPE_FIRST_PARTY
- PRIVACY_TYPE_THIRD_PARTY
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38583d5f0c5cee148353f98f5d2be2d4f1a50216
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844374"
---
# <a name="privacy-type"></a><span data-ttu-id="8f5d7-103">Type de confidentialité</span><span class="sxs-lookup"><span data-stu-id="8f5d7-103">Privacy Type</span></span>

<span data-ttu-id="8f5d7-104">Spécifie que les paramètres de confidentialité sont pour les cookies internes ou tiers.</span><span class="sxs-lookup"><span data-stu-id="8f5d7-104">Specifies that privacy settings are for either first-party or third-party cookies.</span></span>

<dl> <dt>

<span data-ttu-id="8f5d7-105"><span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**TYPE de confidentialité \_ \_ premier \_ tiers**</span><span class="sxs-lookup"><span data-stu-id="8f5d7-105"><span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**PRIVACY\_TYPE\_FIRST\_PARTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f5d7-106">0</span><span class="sxs-lookup"><span data-stu-id="8f5d7-106">0</span></span>
</dt> <dt>



<span data-ttu-id="8f5d7-107">Fait référence aux paramètres de confidentialité pour les cookies de premier tiers.</span><span class="sxs-lookup"><span data-stu-id="8f5d7-107">Refers to privacy settings for first party cookies.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8f5d7-108"><span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**TYPE de confidentialité \_ \_ tiers \_**</span><span class="sxs-lookup"><span data-stu-id="8f5d7-108"><span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**PRIVACY\_TYPE\_THIRD\_PARTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f5d7-109">1</span><span class="sxs-lookup"><span data-stu-id="8f5d7-109">1</span></span>
</dt> <dt>



<span data-ttu-id="8f5d7-110">Fait référence aux paramètres de confidentialité pour les cookies tiers.</span><span class="sxs-lookup"><span data-stu-id="8f5d7-110">Refers to privacy settings for third party cookies.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f5d7-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8f5d7-111">Remarks</span></span>

<span data-ttu-id="8f5d7-112">Les cookies sont catégorisés comme premier tiers et tiers.</span><span class="sxs-lookup"><span data-stu-id="8f5d7-112">Cookies are categorized as first-party and third-party.</span></span> <span data-ttu-id="8f5d7-113">Un cookie interne est un cookie qui provient du domaine hôte.</span><span class="sxs-lookup"><span data-stu-id="8f5d7-113">A first-party cookie is one that originates from the host domain.</span></span> <span data-ttu-id="8f5d7-114">Si « https://www.blueyonderairlines.com » se trouve dans la barre d’adresses Microsoft Internet Explorer, « www.blueyonderairlines.com » est le domaine hôte.</span><span class="sxs-lookup"><span data-stu-id="8f5d7-114">If "https://www.blueyonderairlines.com" is found in the Microsoft Internet Explorer address bar, "www.blueyonderairlines.com" is the host domain.</span></span> <span data-ttu-id="8f5d7-115">En visitant cette page, si un cookie est défini à partir d’un domaine autre que « www.blueyonderairlines.com », tel que « www.fourthcoffee.com », ce cookie est considéré comme un cookie tiers.</span><span class="sxs-lookup"><span data-stu-id="8f5d7-115">While visiting this page, if a cookie is set from a domain other than "www.blueyonderairlines.com", such as "www.fourthcoffee.com", this cookie is considered a third-party cookie.</span></span>

> [!Note]  
> <span data-ttu-id="8f5d7-116">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="8f5d7-116">WinINet does not support server implementations.</span></span> <span data-ttu-id="8f5d7-117">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="8f5d7-117">In addition, it should not be used from a service.</span></span> <span data-ttu-id="8f5d7-118">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="8f5d7-118">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8f5d7-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f5d7-119">Requirements</span></span>



| <span data-ttu-id="8f5d7-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f5d7-120">Requirement</span></span> | <span data-ttu-id="8f5d7-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f5d7-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8f5d7-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f5d7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8f5d7-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f5d7-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8f5d7-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f5d7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8f5d7-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f5d7-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8f5d7-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="8f5d7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f5d7-127"><dt>Wininet. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f5d7-127"><dt>Wininet.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f5d7-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f5d7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f5d7-129">**PrivacyGetZonePreferenceW**</span><span class="sxs-lookup"><span data-stu-id="8f5d7-129">**PrivacyGetZonePreferenceW**</span></span>](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[<span data-ttu-id="8f5d7-130">**PrivacySetZonePreferenceW**</span><span class="sxs-lookup"><span data-stu-id="8f5d7-130">**PrivacySetZonePreferenceW**</span></span>](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

