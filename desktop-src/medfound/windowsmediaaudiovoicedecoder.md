---
description: Le décodeur vocal Windows Media Audio décode les flux qui ont été encodés par l’encodeur vocal Windows Media Audio.
ms.assetid: 8bb5c8bd-949f-4faa-b679-8854f78076a4
title: Windows Media Audio le décodeur vocal (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4565a511f2816d2914ec96f3ae89f3af5dd19016
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532828"
---
# <a name="windows-media-audio-voice-decoder"></a>Décodeur vocal Windows Media Audio

Le décodeur vocal Windows Media Audio décode les flux qui ont été encodés par l’encodeur [**vocal Windows Media Audio**](windowsmediaaudiovoiceencoder.md).

## <a name="class-identifier"></a>Identificateur de classe

L’identificateur de classe (CLSID) du décodeur Windows Media Audio Voice est représenté par la constante **CLSID \_ CWMSPDecMediaObject**. Vous pouvez créer une instance du décodeur vocal en appelant **CoCreateInstance**.

## <a name="input-formats"></a>Formats d’entrée

Windows Media Audio contenu encodé en voix est identifié par la balise de format 0x00A.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista ou Windows 7<br/>                                       |
| En-tête<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmspdmod.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets codec](codecobjects.md)
</dt> <dt>

[Utilisation du codec Windows Media Audio Voice](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[Encodeur vocal Windows Media Audio](windowsmediaaudiovoiceencoder.md)
</dt> </dl>

 

 




