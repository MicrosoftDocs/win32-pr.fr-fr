---
title: DRM_DRMHeader_ContentDistributor
description: L' \_ attribut DRM DRMHeader \_ ContentDistributor contient une chaîne identifiying le serveur de distribution de contenu.
ms.assetid: ea9ae7ba-35cc-4e86-995c-9abcdae48f9c
keywords:
- Format Windows Media DRM_DRMHeader_ContentDistributor
topic_type:
- apiref
api_name:
- DRM_DRMHeader_ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a82e570c43acbe065ec20e1d7296cff701853591759e9187e2b9329ffed8efe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586459"
---
# <a name="drm_drmheader_contentdistributor"></a>\_DRMHEADER DRM \_ ContentDistributor

L’attribut **DRM \_ DRMHeader \_ ContentDistributor** contient une chaîne identifiying le serveur de distribution de contenu.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ DRMHeader \_ ContentDistributor

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Remarques

L’ID de contenu est facultatif et est déterminé uniquement par le créateur du contenu. L’objet enregistreur n’a aucun effet avec cet attribut. Cet attribut est présent uniquement avec le contenu DRM version 7. Il peut être défini à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) et il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




