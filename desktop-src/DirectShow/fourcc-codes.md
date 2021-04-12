---
description: Codes FOURCC
ms.assetid: 7627b580-4119-48e2-88b7-51b714b5d5b2
title: Codes FOURCC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb789bc16a1643ee737c1c1a63bdbc5704567931
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108546"
---
# <a name="fourcc-codes"></a>Codes FOURCC

De nombreux formats multimédias numériques ont des Codes FOURCC qui leur sont affectés. Un code FOURCC est un entier non signé 32 bits créé par la concaténation de quatre caractères ASCII. Par exemple, le code FOURCC pour la vidéo YUY2 est « YUY2 ». Pour les formats vidéo compressés et les formats vidéo non RVB (tels que YUV), le membre de la **compression** de la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) doit être défini sur le code FourCC.

Il existe plusieurs macros C/C++ qui facilitent la déclaration de valeurs FOURCC dans le code source. Par exemple, la macro **MAKEFOURCC** est déclarée dans Mmsystem. h, et la macro **FCC** est déclarée dans Aviriff. h. Utilisez-les comme suit :


```C++
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```



Vous pouvez également déclarer directement un code FOURCC en tant que littéral de chaîne en inversant l’ordre des caractères. Par exemple :


```C++
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```



L’inversion de l’ordre est nécessaire, car le système d’exploitation Microsoft Windows utilise une architecture Little endian. 'Y' = 0x59, 'U' = 0x55, et' 2 ' = 0x32, donc' 2YUY’est 0x32595559.

### <a name="converting-fourcc-codes-to-subtype-guids"></a>Conversion de codes FOURCC en GUID de sous-type

Une plage de 2 \* 32 GUID est réservée à la représentation de FOURCCs. Ces GUID se présentent sous la forme `XXXXXXXX-0000-0010-8000-00AA00389B71` `XXXXXXXX` du code FourCC. Ainsi, le GUID de sous-type pour YUY2 est `32595559-0000-0010-8000-00AA00389B71` .

Un grand nombre de ces GUID sont déjà définis dans le fichier d’en-tête UUID. h. Par exemple, le sous-type YUY2 est défini en tant que MEDIASUBTYPE \_ YUY2. La bibliothèque de classes de base DirectShow fournit également une classe d’assistance, [**FOURCCMap**](fourccmap.md), qui peut être utilisée pour convertir les codes FourCC en valeurs GUID. Le constructeur **FOURCCMap** prend un code FourCC comme paramètre d’entrée. Vous pouvez ensuite effectuer un cast de l’objet **FOURCCMap** vers le GUID correspondant :


```C++
FOURCCMap fccMap(FCC('YUY2'));
GUID g1 = (GUID)fccMap;

// Equivalent:
GUID g2 = (GUID)FOURCCMap(FCC('YUY2'));
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Sous-types audio**](audio-subtypes.md)
</dt> <dt>

[Sous-types de vidéos](video-subtypes.md)
</dt> <dt>

[Utilisation des codecs](working-with-codecs.md)
</dt> </dl>

 

 



