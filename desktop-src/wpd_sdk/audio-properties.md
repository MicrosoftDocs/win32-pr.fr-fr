---
description: Windows Les appareils mobiles prennent en charge les propriétés audio suivantes.
ms.assetid: 5d6c6a95-abb7-4191-a961-bcb30ca96bb6
title: Propriétés audio (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Audio
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 93ddbee0eb078c1b9d5a1e7c64288e95b47e2bdb0363bf8b7b19cb773129d0ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590409"
---
# <a name="audio-properties"></a>Propriétés audio

Windows Les appareils mobiles prennent en charge les propriétés audio suivantes.



| Propriété                         | VarType     | Description                                                                                                                                                                                                        |
|----------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_profondeur de \_ bits \_ audio wpd**       | **VT \_ UI4** | Profondeur du bit de l’audio.                                                                                                                                                                                        |
| **\_ \_ débit binaire wpd**          | **VT \_ UI4** | Vitesse de transmission de l’audio, en bits par seconde.                                                                                                                                                                     |
| **\_alignement des \_ blocs \_ audio wpd** | **VT \_ UI4** | Alignement de bloc du fichier audio, en octets.                                                                                                                                                                   |
| **\_nombre de \_ canaux \_ audio wpd**   | **VT \_ R4**  | Nombre de canaux dans ce fichier audio, par exemple 1, 2 ou 5,1.                                                                                                                                              |
| **\_Code de \_ format \_ audio wpd**     | **VT \_ UI4** | Numéro de code du format WAVE enregistré. Pour obtenir la liste des formats WAVE inscrits, consultez l’article sur les [codes FourCC et les formats Wave inscrits](https://msdn2.microsoft.com/library/ms867195.aspx) sur le site Web MSDN. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés et attributs WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




