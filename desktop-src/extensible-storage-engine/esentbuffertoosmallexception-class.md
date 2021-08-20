---
description: 'En savoir plus sur : classe EsentBufferTooSmallException'
title: EsentBufferTooSmallException, classe
TOCTitle: EsentBufferTooSmallException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBufferTooSmallException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbuffertoosmallexception(v=EXCHG.10)
ms:contentKeyID: 55101109
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBufferTooSmallException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBufferTooSmallException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f024ab7e3808ff00b2d53483b1a96b18ba7a758f72d44b14147a4786dc49897d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118082579"
---
# <a name="esentbuffertoosmallexception-class"></a>EsentBufferTooSmallException, classe

Classe de base pour JET_err. Exceptions BufferTooSmall.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentStateException](./esentstateexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentBufferTooSmallException  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBufferTooSmallException _
    Inherits EsentStateException
'Usage
Dim instance As EsentBufferTooSmallException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBufferTooSmallException : EsentStateException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentBufferTooSmallException](./esentbuffertoosmallexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
