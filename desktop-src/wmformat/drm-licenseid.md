---
title: DRM_LicenseID
description: La \_ propriété DRM LicenseID contient une chaîne extraite de la licence associée au fichier actuellement ouvert qui identifie de façon unique cette licence.
ms.assetid: d5967f5b-99b6-41ea-8494-ac4a7331bbfe
keywords:
- Format Windows Media DRM_LicenseID
topic_type:
- apiref
api_name:
- DRM_LicenseID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d9174e364e186056e63375b8ed322875dfb868
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295923"
---
# <a name="drm_licenseid"></a>\_LICENSEID DRM

La propriété **DRM \_ LicenseID** contient une chaîne extraite de la licence associée au fichier actuellement ouvert qui identifie de façon unique cette licence.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ LicenseID

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Notes

Cet attribut est présent uniquement avec le contenu DRM version 7. Il peut être défini à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) et il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

L’ID de licence est stocké dans une licence, et non dans un fichier ASF. Chaque licence a un ID unique affecté par le générateur de licences au moment de la création de la licence. Par exemple, si vous obtenez deux licences pour le même contenu, chacune d’entre elles aura un attribut LicenseID différent. En règle générale, les applications n’ont pas besoin de récupérer cette valeur.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




