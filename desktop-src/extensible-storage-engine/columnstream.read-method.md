---
description: 'En savoir plus sur : méthode ColumnStream. Read'
title: ColumnStream. Read, méthode
TOCTitle: 'Read method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Read(System.Byte[],System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.read(v=EXCHG.10)
ms:contentKeyID: 55100988
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e407a9069807d10eaabf4f7ac3fce3919576bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536412"
---
# <a name="columnstreamread-method"></a>ColumnStream. Read, méthode

Lit une séquence d'octets dans le flux actuel et avance la position dans le flux du nombre d'octets lus.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Overrides Function Read ( _
    buffer As Byte(), _
    offset As Integer, _
    count As Integer _
) As Integer
'Usage
Dim instance As ColumnStream
Dim buffer As Byte()
Dim offset As Integer
Dim count As Integer
Dim returnValue As Integer

returnValue = instance.Read(buffer, offset, _
    count)
```

``` csharp
public override int Read(
    byte[] buffer,
    int offset,
    int count
)
```

#### <a name="parameters"></a>Paramètres

  - buffer  
    Entrer \[\]  
    
    Mémoire tampon à lire.

<!-- end list -->

  - offset  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Offset dans la mémoire tampon à lire.

<!-- end list -->

  - count  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Nombre d'octets à lire.

#### <a name="return-value"></a>Valeur retournée

Type : [System. Int32](/dotnet/api/system.int32)  
Nombre d’octets lus dans la mémoire tampon.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[ColumnStream, classe](./columnstream-class.md)

[Membres ColumnStream](./columnstream-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
