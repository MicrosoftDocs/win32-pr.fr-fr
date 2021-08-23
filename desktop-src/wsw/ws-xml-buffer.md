---
title: WS_XML_BUFFER (WebServices. h)
description: Type opaque utilisé pour une référence à une mémoire tampon XML.
ms.assetid: 75f1df70-4dc9-4365-9005-5eaca6688f16
keywords:
- WS_XML_BUFFER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 576c901434bb1d05aecbadc52ce51b163023b99e3c7c8959f0169e2e9b0badad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962758"
---
# <a name="ws_xml_buffer"></a>\_ \_ mémoire tampon XML WS

Type opaque utilisé pour une référence à une [mémoire tampon XML](xml-buffer.md).


```C++
typedef struct _WS_XML_BUFFER WS_XML_BUFFER;
```



## <a name="remarks"></a>Remarques

Cet objet n’est pas thread-safe. Pour plus d’informations, consultez [sécurité des threads](thread-safety.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>WebServices. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Mémoire tampon XML](xml-buffer.md)
</dt> <dt>

[Cohérence de thread](thread-safety.md)
</dt> </dl>

 

 





