---
title: Effet de métadonnées d’opacité
description: Vous pouvez utiliser cet effet pour marquer une zone d’une image d’entrée comme opaque, afin que les optimisations de rendu internes au graphique soient possibles.
ms.assetid: 25B34A31-8533-4339-BBF7-2D7E5488E301
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be14699214337dc3f8c6e9e525f128a382c14ee479af08b99ea1f9eadd00041d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118665319"
---
# <a name="opacity-metadata-effect"></a>Effet de métadonnées d’opacité

Vous pouvez utiliser cet effet pour marquer une zone d’une image d’entrée comme opaque, afin que les optimisations de rendu internes au graphique soient possibles.

> [!Note]  
> Cet effet ne modifie pas l’image elle-même pour qu’elle soit opaque. Il modifie les données associées à l’image afin que le convertisseur suppose que la région spécifiée est opaque.

 

Le CLSID de cet effet est CLSID \_ D2D1OpacityMetadata.

## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                                                 | Type et valeur par défaut                                                             | Description                                                                                       |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| OutputRect<br/> D2D1 \_ OPACITYMETADATA \_ prop \_ , \_ rectangle opaque d’entrée \_ <br/> | D2D1 \_ vecteur \_ 4F<br/> (-FLT \_ MAX,-FLT \_ Max, FLT Max, \_ flt \_ Max.) <br/> | Partie de l’image source qui est opaque. La valeur par défaut est la totalité de l’image d’entrée.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge | mise à jour Windows 8 et de plateforme pour les applications de bureau Windows 7 Windows les applications du windows \[ \| Store\] |
| Serveur minimal pris en charge | mise à jour Windows 8 et de plateforme pour les applications de bureau Windows 7 Windows les applications du windows \[ \| Store\] |
| En-tête                   | d2d1effects. h                                                                      |
| Bibliothèque                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

