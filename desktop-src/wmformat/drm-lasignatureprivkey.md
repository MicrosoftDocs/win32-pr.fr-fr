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
ms.openlocfilehash: 9354cc652bfce22183370b1183062d6cf7f27ce60b3681862f150f565d444a6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704323"
---
# <a name="drm_lasignatureprivkey"></a>\_LASIGNATUREPRIVKEY DRM

La propriété **DRM \_ LASignaturePrivKey** contient la clé privée utilisée pour chiffrer l’en-tête DRM.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ LASignaturePrivKey

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Remarques

Cette propriété peut être générée à l’aide de la méthode [**IWMDRMWriter :: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) . Cette propriété doit rester un secret connu uniquement par le créateur du contenu. Cette propriété peut être définie à l’aide de la méthode [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) . Elle n’est pas accessible à l’objet lecteur.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




