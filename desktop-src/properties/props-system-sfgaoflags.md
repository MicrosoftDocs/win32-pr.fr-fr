---
description: 'Valeurs SFGAO telles qu’elles sont utilisées dans IShellFolder :: GetAttributesOf.'
ms.assetid: 0a63e019-a03c-43c2-b2dc-20ef7c37e0d3
title: System. SFGAOFlags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f494215f2302f2a33551ab73adf60d61d7176e2d4caf75215456b731b9aa57e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118464789"
---
# <a name="systemsfgaoflags"></a>System. SFGAOFlags

Valeurs [**SFGAO**](../shell/sfgao.md) telles qu’elles sont utilisées dans [**IShellFolder :: GetAttributesOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof).

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.SFGAOFlags
   shellPKey = PKEY_SFGAOFlags
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 25
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.SFGAOFlags
   shellPKey = PKEY_SFGAOFlags
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 25
   SearchInfo
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="remarks"></a>Remarques

Les valeurs de la valeur de l’une sont définies dans propKey. h.

Certaines valeurs de [**SFGAO**](../shell/sfgao.md) qui sont considérées comme provoquant des calculs lents ou qui manquent de contexte sont exclues ici par l’application du masque * * * [* SFGAO \_ PKEYSFGAOMASK * *](../shell/sfgao.md) * *.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
