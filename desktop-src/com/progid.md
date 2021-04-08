---
title: ProgID
description: Associe un ProgID à un CLSID.
ms.assetid: 89060943-7007-418b-a544-effbad548e87
keywords:
- ProgID de la clé de registre COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feec17db2cf16425968c64ef25759f284341bdb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673098"
---
# <a name="progid"></a>ProgID

Associe un ProgID à un CLSID.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      ProgID = value
```

## <a name="remarks"></a>Notes

Chaque classe d’objet qui peut être insérée a un ProgID. Pour plus d’informations sur la création d’un ProgID, consultez la [ <ProgID> clé](-progid--key.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[<ProgID> essentiel](-progid--key.md)
</dt> <dt>

[**VersionIndependentProgID**](versionindependentprogid.md)
</dt> </dl>

 

 




