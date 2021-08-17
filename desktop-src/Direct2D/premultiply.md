---
title: Effet prémultiplier
description: Utilisez cet effet pour convertir une image de unpremultiplied alpha en valeur alpha prémultipliée.
ms.assetid: 8A5F55C6-3AC7-48B4-87D8-C19D8B4EA0DD
keywords:
- effet prémultiplier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af158ab8f885c51d2dce15d5bfbc5c24f34f6a980ebc8e8f4631617d31a2a48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075023"
---
# <a name="premultiply-effect"></a>Effet prémultiplier

Utilisez cet effet pour convertir une image de unpremultiplied alpha en valeur alpha prémultipliée. L’effet remplace chaque pixel d’entrée `P = {R, G, B, A}` par `P' = {R*A, G*A, B*A, A}` dans la sortie.

Cet effet n’a pas de propriétés.

Le CLSID de cet effet est CLSID \_ D2D1Premultiply.

## <a name="output-bitmap"></a>Bitmap de sortie

La taille de la bitmap de sortie est la même que la taille de la bitmap d’entrée.

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

 

 
