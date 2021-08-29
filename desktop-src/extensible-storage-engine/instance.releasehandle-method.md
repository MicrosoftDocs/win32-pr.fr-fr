---
description: 'En savoir plus sur : méthode instance. ReleaseHandle'
title: Méthode instance. ReleaseHandle
TOCTitle: 'ReleaseHandle method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.ReleaseHandle
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.releasehandle(v=EXCHG.10)
ms:contentKeyID: 55103298
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance.ReleaseHandle
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance.ReleaseHandle
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c3d5b614bdf2b00f7b47b8d9fc2f6c5e2edec2e71960bf0b480024ec65de5540
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112568"
---
# <a name="instancereleasehandle-method"></a>Méthode instance. ReleaseHandle

Libère le handle pour cette instance.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Protected Overrides Function ReleaseHandle As Boolean
'Usage
Dim returnValue As Boolean

returnValue = Me.ReleaseHandle()
```

``` csharp
protected override bool ReleaseHandle()
```

#### <a name="return-value"></a>Valeur de retour

Type : [System. Boolean](/dotnet/api/system.boolean)  
True si le handle peut être relâché.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’instance](./instance-class.md)

[Membres d’instance](./instance-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
