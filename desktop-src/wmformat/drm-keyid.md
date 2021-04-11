---
title: DRM_KeyID
description: L' \_ attribut DRM KeyId contient l’identificateur de clé.
ms.assetid: 90406809-76d9-4559-afe8-6812efbc1477
keywords:
- Format Windows Media DRM_KeyID
topic_type:
- apiref
api_name:
- DRM_KeyID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97a60afa330a7cf967b42a4d06009d9c921d8f56
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030836"
---
# <a name="drm_keyid"></a>\_KEYID DRM

L’attribut **DRM \_ KeyId** contient l’identificateur de clé.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ KeyId

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Notes

Cet attribut est présent uniquement pour le contenu DRM version 7. Il peut être défini à l’aide de [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) et il peut être récupéré avec [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Le même attribut de fichier peut être récupéré à l’aide de [**DRM \_ DRMHeader \_ KeyId**](drm-drmheader-keyid.md).

L’ID de clé est utilisé conjointement avec la valeur initiale de la clé pour créer la clé de contenu qui est utilisée pour chiffrer et déchiffrer le fichier. L’application Writer utilise l’ID de clé pour chiffrer le fichier, puis stocke l’ID de clé dans l’en-tête de fichier. Quand une application de lecteur demande une licence pour un fichier, le composant DRM envoie l’ID de clé (ainsi que le reste de l’en-tête DRM) au serveur de licences. Le serveur de licences, qui a la valeur initiale de clé secrète, l’utilise et l’ID de clé pour créer une clé pour le fichier, qu’il insère ensuite dans une licence avec les différents droits qui seront appliqués au fichier.

En règle générale, une valeur initiale de clé est utilisée avec de nombreux ID de clé. L’amorce de clé est un secret partagé uniquement par le créateur de contenu et le serveur de distribution de licences. L’ID de clé est utilisé par les applications clientes DRM et est stocké dans l’en-tête DRM en clair.

Cet attribut est identique à [**DRM \_ DRMHeader \_ KeyId**](drm-drmheader-keyid.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




