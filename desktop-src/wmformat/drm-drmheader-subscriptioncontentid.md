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
# <a name="drm_drmheader_subscriptioncontentid"></a>\_DRMHEADER DRM \_ SubscriptionContentID

L’attribut **DRM \_ DRMHeader \_ SUBSCRIPTIONCONTENTID** contient l’ID de contenu de l’abonnement.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Notes

Cet attribut est présent uniquement avec le contenu DRM version 7. L’ID de contenu de l’abonnement est facultatif et est déterminé uniquement par le créateur du contenu. L’objet enregistreur n’a aucun effet avec cet attribut. Il peut être défini à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) et il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




