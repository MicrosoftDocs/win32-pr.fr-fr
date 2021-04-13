---
title: DRM_ActionAllowed_CollaborativePlay
description: L' \_ attribut DRM ActionAllowed \_ CollaborativePlay indique si la licence permet de lire le contenu en collaboration.
ms.assetid: 111e8fa7-ef5a-483a-b930-8a8e5b4d120a
keywords:
- Format Windows Media DRM_ActionAllowed_CollaborativePlay
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CollaborativePlay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0268c9c3d70a8f51db390544bf854e5acd5b9e88
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381549"
---
# <a name="drm_actionallowed_collaborativeplay"></a>\_ACTIONALLOWED DRM \_ CollaborativePlay

L’attribut **DRM \_ ActionAllowed \_ CollaborativePlay** indique si la licence permet de lire le contenu en collaboration.

## <a name="global-constant"></a>Constante globale

g \_ wszWMDRM \_ ActionAllowed \_ CollaborativePlay

## <a name="data-type"></a>Type de données

**\_type WMT \_ bool**

## <a name="remarks"></a>Notes

Le droit de travail collaboratif s’applique à la lecture de contenu protégé dans le cadre d’une session de collaboration utilisant des services d’égal à égal. Par exemple, les utilisateurs de MSN Messenger 2004 peuvent lire du contenu protégé dans une session MusicMix. Ce droit ne peut être utilisé que pour fournir un fichier protégé à une seule session à la fois et tous les utilisateurs participant à la session doivent être en ligne pour afficher le contenu.

Il s’agit d’une propriété en lecture seule qui est récupérée à l’aide de [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés DRM**](drm-properties.md)
</dt> </dl>

 

 




