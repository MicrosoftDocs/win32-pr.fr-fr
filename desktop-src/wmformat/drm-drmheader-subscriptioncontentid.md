---
title: DRM_DRMHeader_SubscriptionContentID
description: L' \_ attribut DRM DRMHeader \_ SubscriptionContentID contient l’ID de contenu de l’abonnement.
ms.assetid: e582d841-4865-40d3-889e-847d3aac0a7c
keywords:
- Format Windows Media DRM_DRMHeader_SubscriptionContentID
topic_type:
- apiref
api_name:
- DRM_DRMHeader_SubscriptionContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 151665777aa6b68078361eb6e063e374a52f30bf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103940680"
---
# <a name="drm_drmheader_subscriptioncontentid"></a><span data-ttu-id="d4263-104">\_DRMHEADER DRM \_ SubscriptionContentID</span><span class="sxs-lookup"><span data-stu-id="d4263-104">DRM\_DRMHeader\_SubscriptionContentID</span></span>

<span data-ttu-id="d4263-105">L’attribut **DRM \_ DRMHeader \_ SUBSCRIPTIONCONTENTID** contient l’ID de contenu de l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="d4263-105">The **DRM\_DRMHeader\_SubscriptionContentID** attribute contains the subscription content ID.</span></span>

## <a name="global-constant"></a><span data-ttu-id="d4263-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="d4263-106">Global Constant</span></span>

<span data-ttu-id="d4263-107">g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID</span><span class="sxs-lookup"><span data-stu-id="d4263-107">g\_wszWMDRM\_DRMHeader\_SubscriptionContentID</span></span>

## <a name="data-type"></a><span data-ttu-id="d4263-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="d4263-108">Data Type</span></span>

<span data-ttu-id="d4263-109">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d4263-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="d4263-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d4263-110">Remarks</span></span>

<span data-ttu-id="d4263-111">Cet attribut est présent uniquement avec le contenu DRM version 7.</span><span class="sxs-lookup"><span data-stu-id="d4263-111">This attribute is present with DRM Version 7 content only.</span></span> <span data-ttu-id="d4263-112">L’ID de contenu de l’abonnement est facultatif et est déterminé uniquement par le créateur du contenu.</span><span class="sxs-lookup"><span data-stu-id="d4263-112">The subscription content ID is optional and is determined solely by the content creator.</span></span> <span data-ttu-id="d4263-113">L’objet enregistreur n’a aucun effet avec cet attribut.</span><span class="sxs-lookup"><span data-stu-id="d4263-113">The writer object does nothing with this attribute.</span></span> <span data-ttu-id="d4263-114">Il peut être défini à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) et il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="d4263-114">It can be set using [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and it can be retrieved with [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="d4263-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4263-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4263-116">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="d4263-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




