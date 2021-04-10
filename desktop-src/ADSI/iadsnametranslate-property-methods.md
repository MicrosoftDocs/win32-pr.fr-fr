---
title: Méthodes de propriété IADsNameTranslate (IADs. h)
description: Définit la propriété ChaseReferral.
ms.assetid: 7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsNameTranslate ADSI
topic_type:
- apiref
api_name:
- IADsNameTranslate Property Methods
- IADsNameTranslate.ChaseReferral
- IADsNameTranslate.put_ChaseReferral
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b90d068da3b8dca1bbcae361d1dbacafcf44464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942567"
---
# <a name="iadsnametranslate-property-methods"></a><span data-ttu-id="d1798-104">Méthodes de propriété IADsNameTranslate</span><span class="sxs-lookup"><span data-stu-id="d1798-104">IADsNameTranslate Property Methods</span></span>

<span data-ttu-id="d1798-105">La méthode Property de l’interface [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) définit la propriété **ChaseReferral** .</span><span class="sxs-lookup"><span data-stu-id="d1798-105">The property method of the [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) interface sets the **ChaseReferral** property.</span></span> <span data-ttu-id="d1798-106">Pour plus d’informations, consultez [méthodes de propriété d’interface](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="d1798-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="d1798-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d1798-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="d1798-108">**ChaseReferral**</span><span class="sxs-lookup"><span data-stu-id="d1798-108">**ChaseReferral**</span></span>
<span data-ttu-id="d1798-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d1798-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="d1798-110">Options de repérage de références telles qu’elles sont définies dans l' [**\_ \_ \_ énumération des références de la Chase ADS**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum).</span><span class="sxs-lookup"><span data-stu-id="d1798-110">Options of referral chasing as defined in [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum).</span></span> <span data-ttu-id="d1798-111">Lorsque le repérage de références est défini, la traduction de nom est effectuée sur les objets qui n’appartiennent pas à ce répertoire et les références retournées par le repérage de références.</span><span class="sxs-lookup"><span data-stu-id="d1798-111">When referral chasing is set, the name translation is performed on objects that do not belong to this directory and are the referrals returned from referral chasing.</span></span>

<dt>

<span data-ttu-id="d1798-112">Type d’accès : écriture seule</span><span class="sxs-lookup"><span data-stu-id="d1798-112">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="d1798-113">Type de données de script : **long**</span><span class="sxs-lookup"><span data-stu-id="d1798-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT put_ChaseReferral(
  [in] LONG lnChaseReferral
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="d1798-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d1798-114">Remarks</span></span>

<span data-ttu-id="d1798-115">Les options de repérage de références s’appliquent uniquement lorsque vous utilisez [**IADsNameTranslate :: Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) et [**IADsNameTranslate :: obten**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get).</span><span class="sxs-lookup"><span data-stu-id="d1798-115">The referral chasing options apply only when you use [**IADsNameTranslate::Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) and [**IADsNameTranslate::Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get).</span></span> <span data-ttu-id="d1798-116">La fonctionnalité n’est pas disponible avec [**IADsNameTranslate :: SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex) ou [**IADsNameTranslate :: GETEX**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex).</span><span class="sxs-lookup"><span data-stu-id="d1798-116">The feature is not available with [**IADsNameTranslate::SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex) or [**IADsNameTranslate::GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex).</span></span>

<span data-ttu-id="d1798-117">L’interface [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) a une implémentation partielle de [**l' \_ \_ \_ énumération de références de la Chase ADS**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) par le biais de la propriété **ChaseReferral** .</span><span class="sxs-lookup"><span data-stu-id="d1798-117">The [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) interface has a partial implementation of [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) through the **ChaseReferral** property.</span></span> <span data-ttu-id="d1798-118">Si la propriété **ChaseReferral** a la valeur zéro (0), elle est identique à la spécification des références de la **Chase des publicités \_ \_ \_ jamais** (0).</span><span class="sxs-lookup"><span data-stu-id="d1798-118">If the **ChaseReferral** property is set to zero (0), it is the same as specifying **ADS\_CHASE\_REFERRALS\_NEVER** (0).</span></span> <span data-ttu-id="d1798-119">Si une valeur différente de zéro est utilisée, elle est identique à la spécification des références de la **Chase des publicités \_ \_ \_ Always** (0x60).</span><span class="sxs-lookup"><span data-stu-id="d1798-119">If a nonzero value is used, it is the same as specifying **ADS\_CHASE\_REFERRALS\_ALWAYS** (0x60).</span></span> <span data-ttu-id="d1798-120">**IADsNameTranslate** n’implémente pas les options de **\_ références de poursuites ad \_ \_ subordonnées** (0x20) ou de références de la **\_ Chase ADS \_ \_ externes** (0x40).</span><span class="sxs-lookup"><span data-stu-id="d1798-120">**IADsNameTranslate** does not implement the **ADS\_CHASE\_REFERRALS\_SUBORDINATE** (0x20) or **ADS\_CHASE\_REFERRALS\_EXTERNAL** (0x40) options.</span></span>

<span data-ttu-id="d1798-121">Le paramètre par défaut pour le repérage de références est activé (les références de la **poursuite ADS sont \_ \_ \_ toujours**).</span><span class="sxs-lookup"><span data-stu-id="d1798-121">The default setting for referral chasing is enabled (**ADS\_CHASE\_REFERRALS\_ALWAYS**).</span></span> <span data-ttu-id="d1798-122">Sans le repérage de références, vous pouvez faire en sorte que la traduction de noms soit effectuée sur les objets résidant uniquement sur le serveur d’annuaire connecté.</span><span class="sxs-lookup"><span data-stu-id="d1798-122">Without referral chasing, you can have name translation performed on those objects residing on the connected directory server only.</span></span> <span data-ttu-id="d1798-123">Si vous n’êtes pas certain que l’objet concerné se trouve sur le serveur spécifié, vous devez définir cette propriété sur les références de la **\_ Chase ADS \_ \_ Always**.</span><span class="sxs-lookup"><span data-stu-id="d1798-123">If you are uncertain whether the object of interest is on the specified server, you should set this property to be **ADS\_CHASE\_REFERRALS\_ALWAYS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1798-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1798-124">Requirements</span></span>



| <span data-ttu-id="d1798-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1798-125">Requirement</span></span> | <span data-ttu-id="d1798-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1798-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1798-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1798-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d1798-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1798-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1798-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1798-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d1798-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1798-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1798-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1798-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1798-132"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1798-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="d1798-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d1798-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1798-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1798-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="d1798-135">IID</span><span class="sxs-lookup"><span data-stu-id="d1798-135">IID</span></span><br/>                      | <span data-ttu-id="d1798-136">IID \_ IADsNameTranslate est défini en tant que B1B272A3-3625-11D1-A3A4-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="d1798-136">IID\_IADsNameTranslate is defined as B1B272A3-3625-11D1-A3A4-00C04FB950DC</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="d1798-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1798-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1798-138">**\_ \_ énumérations de références de Chase ADS \_**</span><span class="sxs-lookup"><span data-stu-id="d1798-138">**ADS\_CHASE\_REFERRALS\_ENUM**</span></span>](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)
</dt> <dt>

[<span data-ttu-id="d1798-139">**IADsNameTranslate**</span><span class="sxs-lookup"><span data-stu-id="d1798-139">**IADsNameTranslate**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)
</dt> <dt>

[<span data-ttu-id="d1798-140">**IADsNameTranslate :: obtient**</span><span class="sxs-lookup"><span data-stu-id="d1798-140">**IADsNameTranslate::Get**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get)
</dt> <dt>

[<span data-ttu-id="d1798-141">**IADsNameTranslate::GetEx**</span><span class="sxs-lookup"><span data-stu-id="d1798-141">**IADsNameTranslate::GetEx**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex)
</dt> <dt>

[<span data-ttu-id="d1798-142">**IADsNameTranslate :: Set**</span><span class="sxs-lookup"><span data-stu-id="d1798-142">**IADsNameTranslate::Set**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set)
</dt> <dt>

[<span data-ttu-id="d1798-143">**IADsNameTranslate::SetEx**</span><span class="sxs-lookup"><span data-stu-id="d1798-143">**IADsNameTranslate::SetEx**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex)
</dt> <dt>

[<span data-ttu-id="d1798-144">Méthodes de propriété d’interface</span><span class="sxs-lookup"><span data-stu-id="d1798-144">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





