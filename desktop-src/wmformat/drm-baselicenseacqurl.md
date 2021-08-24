---
title: DRM_BaseLicenseAcqURL
description: L' \_ attribut DRM BaseLicenseAcqURL contient une URL de base partielle à laquelle une application de joueur doit accéder pour obtenir une licence pour le contenu.
ms.assetid: 9acaac44-81b2-467c-9510-023fbb47dd04
keywords:
- Format Windows Media DRM_BaseLicenseAcqURL
topic_type:
- apiref
api_name:
- DRM_BaseLicenseAcqURL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77827068ee8a491cd732b28e5b8d60e1868ec66c04c72156f08358dd7d3751d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658999"
---
# <a name="drm_baselicenseacqurl"></a>\_BASELICENSEACQURL DRM

L’attribut **DRM \_ BaseLicenseAcqURL** contient une URL de base partielle à laquelle une application de joueur doit accéder pour obtenir une licence pour le contenu.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ BaseLicenseAcqURL

## <a name="data-type"></a>Type de données

**\_chaîne de type WMT \_**

## <a name="remarks"></a>Remarques

Il s’agit d’une propriété en lecture-écriture facultative qui est définie et récupérée à l’aide de [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty). Il est fourni pour permettre aux systèmes de distribution de licences d’utiliser des chemins d’accès relatifs dans les propriétés de l’URL d’acquisition de licence.

Après avoir défini cette propriété, toutes les URL d’acquisition de licence partielles dans les en-têtes de contenu auront l’URL de base ajoutée au début de l’URL partielle pour former une URL complète pour l’application de lecteur à laquelle naviguer. L’appel de **IWMDRMReader :: GetDRMProperty** pour **DRM \_ BaseLicenseAcqURL** ne fonctionne que dans la même session que celle qui a été définie. La propriété n’est pas stockée dans l’en-tête de contenu ; Il est dynamique, et seule l’URL relative est stockée dans le contenu.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés DRM**](drm-properties.md)
</dt> </dl>

 

 




