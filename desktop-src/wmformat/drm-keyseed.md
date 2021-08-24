---
title: DRM_KeySeed
description: La \_ propriété DRM keyseed contient la valeur de départ de clé qui sera utilisée conjointement avec le KeyId pour créer la clé.
ms.assetid: 38613d50-89c2-4422-9265-5e89de030ae9
keywords:
- Format Windows Media DRM_KeySeed
topic_type:
- apiref
api_name:
- DRM_KeySeed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46766dc5754bde33c00af250f03a54caf3c12c607ec14da858ac638a70f79baf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658969"
---
# <a name="drm_keyseed"></a>Keyseed DRM \_

La propriété **DRM \_ keyseed** contient la valeur de départ de clé qui sera utilisée conjointement avec le KeyId pour créer la clé.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ keyseed

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Remarques

Cette propriété peut être définie à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute). Elle n’est pas accessible par l’objet lecteur.

Un Seed de clé est généralement utilisé pour protéger plusieurs fichiers ou ensembles de fichiers, par exemple tous les fichiers émis par un serveur de licences, ou peut-être tous les fichiers par un artiste particulier. Le KeyID, toutefois, est unique pour chaque fichier.

La valeur initiale de la clé doit rester un secret partagé uniquement entre le créateur du contenu et le serveur de distribution de licences. Cette valeur n’est pas stockée dans l’en-tête DRM et n’est ni nécessaire ni accessible aux applications de lecteur DRM.

Une nouvelle valeur initiale de clé peut être générée à l’aide de la méthode [**IWMDRMWriter :: GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed) ou par tout autre moyen approprié.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés DRM**](drm-properties.md)
</dt> </dl>

 

 




