---
description: 'En savoir plus sur : méthode ColumnStream. Seek'
title: ColumnStream. Seek, méthode
TOCTitle: 'Seek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Seek(System.Int64,System.IO.SeekOrigin)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.seek(v=EXCHG.10)
ms:contentKeyID: 55100949
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5489bb0ee9a4a1550166e14a945a2a6d58c45af
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120301"
---
# <a name="columnstreamseek-method"></a>ColumnStream. Seek, méthode

Définit la position dans le flux actuel.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Overrides Function Seek ( _
    offset As Long, _
    origin As SeekOrigin _
) As Long
'Usage
Dim instance As ColumnStream
Dim offset As Long
Dim origin As SeekOrigin
Dim returnValue As Long

returnValue = instance.Seek(offset, origin)
```

``` csharp
public override long Seek(
    long offset,
    SeekOrigin origin
)
```

#### <a name="parameters"></a>Paramètres

  - offset  
    Type : [System. Int64](/dotnet/api/system.int64)  
    
    Décalage d’octet par rapport au paramètre Origin.

<!-- end list -->

  - origin  
    Type : [System. IO. SeekOrigin](/dotnet/api/system.io.seekorigin)  
    
    SeekOrigin indiquant le point de référence pour la nouvelle position.

#### <a name="return-value"></a>Valeur de retour

Type : [System. Int64](/dotnet/api/system.int64)  
Nouvelle position dans le flux actuel.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Référence

[ColumnStream, classe](./columnstream-class.md)

[Membres ColumnStream](./columnstream-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
