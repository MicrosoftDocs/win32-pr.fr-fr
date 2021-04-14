---
title: DRM_LASignaturePrivKey
description: La \_ propriété DRM LASignaturePrivKey contient la clé privée utilisée pour chiffrer l’en-tête DRM.
ms.assetid: b7083237-da11-4f31-a143-c0278a54b5a6
keywords:
- Format Windows Media DRM_LASignaturePrivKey
topic_type:
- apiref
api_name:
- DRM_LASignaturePrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdb22f3abc57fc2331ff87bd05bc05d580d607c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381551"
---
# <a name="drm_lasignatureprivkey"></a>\_LASIGNATUREPRIVKEY DRM

La propriété **DRM \_ LASignaturePrivKey** contient la clé privée utilisée pour chiffrer l’en-tête DRM.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ LASignaturePrivKey

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Notes

Cette propriété peut être générée à l’aide de la méthode [**IWMDRMWriter :: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) . Cette propriété doit rester un secret connu uniquement par le créateur du contenu. Cette propriété peut être définie à l’aide de la méthode [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) . Elle n’est pas accessible à l’objet lecteur.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




