---
title: WS_XML_BUFFER (WebServices. h)
description: Type opaque utilisé pour une référence à une mémoire tampon XML.
ms.assetid: 75f1df70-4dc9-4365-9005-5eaca6688f16
keywords:
- WS_XML_BUFFER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22f84bc755d24d07e8e2ed9bacf91b644c883871
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234359"
---
# <a name="ws_xml_buffer"></a>\_ \_ mémoire tampon XML WS

Type opaque utilisé pour une référence à une [mémoire tampon XML](xml-buffer.md).


```C++
typedef struct _WS_XML_BUFFER WS_XML_BUFFER;
```



## <a name="remarks"></a>Notes

Cet objet n’est pas thread-safe. Pour plus d’informations, consultez [sécurité des threads](thread-safety.md).

## <a name="requirements"></a>Spécifications



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

 

 





