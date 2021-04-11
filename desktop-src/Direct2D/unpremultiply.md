---
title: Effet Unpremultiply
description: Utilisez cet effet pour convertir une image de l’alpha prémultiplié en unpremultiplied alpha.
ms.assetid: A4FAF899-81DA-4BDA-98B4-DE63EC1664F5
keywords:
- effet unpremultiply
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5628ea646443a08abffa4549ad25147deb609acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385060"
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
| Client minimal pris en charge | Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\] |
| Serveur minimal pris en charge | Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\] |
| En-tête                   | d2d1effects. h                                                                      |
| Bibliothèque                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
