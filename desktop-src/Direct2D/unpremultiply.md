---
title: Effet Unpremultiply
description: Utilisez cet effet pour convertir une image de l’alpha prémultiplié en unpremultiplied alpha.
ms.assetid: A4FAF899-81DA-4BDA-98B4-DE63EC1664F5
keywords:
- effet unpremultiply
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a152803956b9839b881404be013c521dc0f5bfc764b2f07a8462275b523ba762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664877"
---
# <a name="unpremultiply-effect"></a>Effet Unpremultiply

Utilisez cet effet pour convertir une image de l’alpha prémultiplié en unpremultiplied alpha. L’effet remplace chaque pixel d’entrée `P = {R, G, B, A}` par `P' = {R/A, G/A, B/A, A}` dans la sortie.

Cet effet n’a pas de propriétés.

Le CLSID de cet effet est CLSID \_ D2D1Unpremultiply.

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

 

 
