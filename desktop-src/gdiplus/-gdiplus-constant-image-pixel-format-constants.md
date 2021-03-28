---
description: Les constantes suivantes, définies dans Gdipluspixelformats. h, spécifient différents formats de pixel utilisés dans les bitmaps.
ms.assetid: 362204c5-5dd7-461a-b90b-15826c025689
title: Constantes de format de pixel d’image (Gdipluspixelformats. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b62abc8b0ed606b958764e27171f8b45e619d23b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982882"
---
# <a name="image-pixel-format-constants"></a>Constantes de format de pixel d’image

Les constantes suivantes, définies dans Gdipluspixelformats. h, spécifient différents formats de pixel utilisés dans les bitmaps.



| Constante                                                                                                                                                                                                                                     | Description                                                                                                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PixelFormat1bppIndexed"></span><span id="pixelformat1bppindexed"></span><span id="PIXELFORMAT1BPPINDEXED"></span><dl> <dt>**PixelFormat1bppIndexed**</dt> </dl>             | Spécifie que le format est 1 bit par pixel, indexé.<br/>                                                                                                                                                         |
| <span id="PixelFormat4bppIndexed"></span><span id="pixelformat4bppindexed"></span><span id="PIXELFORMAT4BPPINDEXED"></span><dl> <dt>**PixelFormat4bppIndexed**</dt> </dl>             | Spécifie que le format est 4 bits par pixel, indexés.<br/>                                                                                                                                                        |
| <span id="PixelFormat8bppIndexed"></span><span id="pixelformat8bppindexed"></span><span id="PIXELFORMAT8BPPINDEXED"></span><dl> <dt>**PixelFormat8bppIndexed**</dt> </dl>             | Spécifie que le format est 8 bits par pixel, indexés.<br/>                                                                                                                                                        |
| <span id="PixelFormat16bppARGB1555"></span><span id="pixelformat16bppargb1555"></span><span id="PIXELFORMAT16BPPARGB1555"></span><dl> <dt>**PixelFormat16bppARGB1555**</dt> </dl>     | Spécifie que le format est 16 bits par pixel ; 1 bit est utilisé pour le composant alpha et 5 bits sont utilisés pour les composants rouge, vert et bleu.<br/>                                                       |
| <span id="PixelFormat16bppGrayScale"></span><span id="pixelformat16bppgrayscale"></span><span id="PIXELFORMAT16BPPGRAYSCALE"></span><dl> <dt>**PixelFormat16bppGrayScale**</dt> </dl> | Spécifie que le format est 16 bits par pixel, en nuances de gris.<br/>                                                                                                                                                     |
| <span id="PixelFormat16bppRGB555"></span><span id="pixelformat16bpprgb555"></span><span id="PIXELFORMAT16BPPRGB555"></span><dl> <dt>**PixelFormat16bppRGB555**</dt> </dl>             | Spécifie que le format est 16 bits par pixel, dont 5 bits sont utilisés pour chaque composant rouge, vert et bleu. Le bit restant n'est pas utilisé.<br/>                                                                   |
| <span id="PixelFormat16bppRGB565"></span><span id="pixelformat16bpprgb565"></span><span id="PIXELFORMAT16BPPRGB565"></span><dl> <dt>**PixelFormat16bppRGB565**</dt> </dl>             | Spécifie que le format est 16 bits par pixel ; 5 bits sont utilisés pour le composant rouge, 6 bits pour le composant vert et 5 bits pour le composant bleu.<br/>                                    |
| <span id="PixelFormat24bppRGB"></span><span id="pixelformat24bpprgb"></span><span id="PIXELFORMAT24BPPRGB"></span><dl> <dt>**PixelFormat24bppRGB**</dt> </dl>                         | Spécifie que le format est 24 bits par pixel, dont 8 bits sont utilisés pour chaque composant rouge, vert et bleu.<br/>                                                                                                  |
| <span id="PixelFormat32bppARGB"></span><span id="pixelformat32bppargb"></span><span id="PIXELFORMAT32BPPARGB"></span><dl> <dt>**PixelFormat32bppARGB**</dt> </dl>                     | Spécifie que le format est 32 bits par pixel ; 8 bits sont utilisés pour chaque composant alpha, rouge, vert et bleu.<br/>                                                                                           |
| <span id="PixelFormat32bppPARGB"></span><span id="pixelformat32bpppargb"></span><span id="PIXELFORMAT32BPPPARGB"></span><dl> <dt>**PixelFormat32bppPARGB**</dt> </dl>                 | Spécifie que le format est 32 bits par pixel ; 8 bits sont utilisés pour chaque composant alpha, rouge, vert et bleu. Les composants rouges, verts et bleus sont prémultipliés en fonction du composant alpha.<br/>   |
| <span id="PixelFormat32bppRGB"></span><span id="pixelformat32bpprgb"></span><span id="PIXELFORMAT32BPPRGB"></span><dl> <dt>**PixelFormat32bppRGB**</dt> </dl>                         | Spécifie que le format est 32 bits par pixel, dont 8 bits sont utilisés pour chaque composant rouge, vert et bleu. Les 8 bits restants ne sont pas utilisés.<br/>                                                               |
| <span id="PixelFormat48bppRGB"></span><span id="pixelformat48bpprgb"></span><span id="PIXELFORMAT48BPPRGB"></span><dl> <dt>**PixelFormat48bppRGB**</dt> </dl>                         | Spécifie que le format est 48 bits par pixel, dont 16 bits sont utilisés pour chaque composant rouge, vert et bleu.<br/>                                                                                                 |
| <span id="PixelFormat64bppARGB"></span><span id="pixelformat64bppargb"></span><span id="PIXELFORMAT64BPPARGB"></span><dl> <dt>**PixelFormat64bppARGB**</dt> </dl>                     | Spécifie que le format est 64 bits par pixel, dont 16 bits sont utilisés pour chaque composant alpha, rouge, vert et bleu.<br/>                                                                                          |
| <span id="PixelFormat64bppPARGB"></span><span id="pixelformat64bpppargb"></span><span id="PIXELFORMAT64BPPPARGB"></span><dl> <dt>**PixelFormat64bppPARGB**</dt> </dl>                 | Spécifie que le format est 64 bits par pixel, dont 16 bits sont utilisés pour chaque composant alpha, rouge, vert et bleu. Les composants rouges, verts et bleus sont prémultipliés en fonction du composant alpha. <br/> |



## <a name="remarks"></a>Notes

**PixelFormat48bppRGB**, **PixelFormat64bppARGB** et **PixelFormat64bppPARGB** utilisent 16 bits par composant de couleur (canal). Windows GDI+ version 1,0 peut lire des images de 16 bits par canal, mais ces images sont converties en un format de 8 bits par canal pour le traitement, l’affichage et l’enregistrement.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Gdipluspixelformats. h</dt> </dl> |



 

 




