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
ms.openlocfilehash: ab7f8cc90e509294d9de9d3577ad5a2d56b61eb3a471f9b493e555c0f1ecf824
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547609"
---
# <a name="drm_headersignprivkey"></a>\_HEADERSIGNPRIVKEY DRM

La propriété **DRM \_ HeaderSignPrivKey** contient la clé privée utilisée pour signer l’en-tête ASF.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ HeaderSignPrivKey

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Remarques

Cette propriété est générée à l’aide de [**IWMDRMWriter :: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair). Conservez ce secret clé et partagez la clé publique uniquement avec le service de licence. Une fois que vous avez défini cette clé, le composant DRM l’utilise pour signer l’en-tête de fichier ASF (pas l’en-tête DRM qui est signé avec les valeurs d’objet de signature numérique comme DRM \_ LASignaturePrivKey). Évidemment, **DRM \_ HeaderSignPrivKey** n’est pas inclus dans l’en-tête de fichier.

Cette propriété n’est pas accessible à partir de l’objet lecteur. Il peut être défini à partir de l’objet Writer à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés DRM**](drm-properties.md)
</dt> </dl>

 

 




