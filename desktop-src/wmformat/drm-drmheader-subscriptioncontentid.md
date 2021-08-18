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
ms.openlocfilehash: a2b273cf95d2bbb271b055eeff3da80a788a38c88bb2e87db37f5a73e6e918e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086149"
---
# <a name="drm_drmheader_subscriptioncontentid"></a>\_DRMHEADER DRM \_ SubscriptionContentID

L’attribut **DRM \_ DRMHeader \_ SUBSCRIPTIONCONTENTID** contient l’ID de contenu de l’abonnement.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Remarques

Cet attribut est présent uniquement avec le contenu DRM version 7. L’ID de contenu de l’abonnement est facultatif et est déterminé uniquement par le créateur du contenu. L’objet enregistreur n’a aucun effet avec cet attribut. Il peut être défini à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) et il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




