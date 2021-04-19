---
description: Handle vers une mémoire tampon de chaîne mutable que vous pouvez utiliser pour créer un HSTRING.
ms.assetid: D173CE70-ABF3-4703-A229-0753F2AF6F70
title: HSTRING_BUFFER (hstring. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d70b961d442739e084e3b17d5666653c103cc35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514022"
---
# <a name="hstring_buffer"></a>\_mémoire tampon HSTRING

Handle vers une mémoire tampon de chaîne mutable que vous pouvez utiliser pour créer un [**HSTRING**](hstring.md).


```C++
typedef HANDLE HSTRING_BUFFER;
```



## <a name="remarks"></a>Notes

**HSTRING \_ BUFFER** représente une mémoire tampon de chaîne que vous pouvez modifier avant de la convertir en [**HSTRING**](hstring.md)immuable.

Appelez la fonction [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) pour créer une **\_ mémoire tampon HSTRING**. Appelez [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) pour convertir une **\_ mémoire tampon HSTRING** en un [**HSTRING**](hstring.md)immuable.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>Hstring. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>


</dt> <dt>

[**HSTRING**](hstring.md)
</dt> <dt>

[**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> <dt>

[**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer)
</dt> </dl>

 

 
