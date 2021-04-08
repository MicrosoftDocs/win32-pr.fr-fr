---
title: DRM_HeaderSignPrivKey
description: La \_ propriété DRM HeaderSignPrivKey contient la clé privée utilisée pour signer l’en-tête ASF.
ms.assetid: 0f32e63d-d416-4a1d-b10c-2534b747adf3
keywords:
- Format Windows Media DRM_HeaderSignPrivKey
topic_type:
- apiref
api_name:
- DRM_HeaderSignPrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af73ea90acca6c20817f35a035f8f297aa56e90b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723490"
---
# <a name="drm_headersignprivkey"></a>\_HEADERSIGNPRIVKEY DRM

La propriété **DRM \_ HeaderSignPrivKey** contient la clé privée utilisée pour signer l’en-tête ASF.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ HeaderSignPrivKey

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Notes

Cette propriété est générée à l’aide de [**IWMDRMWriter :: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair). Conservez ce secret clé et partagez la clé publique uniquement avec le service de licence. Une fois que vous avez défini cette clé, le composant DRM l’utilise pour signer l’en-tête de fichier ASF (pas l’en-tête DRM qui est signé avec les valeurs d’objet de signature numérique comme DRM \_ LASignaturePrivKey). Évidemment, **DRM \_ HeaderSignPrivKey** n’est pas inclus dans l’en-tête de fichier.

Cette propriété n’est pas accessible à partir de l’objet lecteur. Il peut être défini à partir de l’objet Writer à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés DRM**](drm-properties.md)
</dt> </dl>

 

 




