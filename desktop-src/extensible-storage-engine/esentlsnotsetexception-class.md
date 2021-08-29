---
description: 'En savoir plus sur : classe EsentLSNotSetException'
title: EsentLSNotSetException, classe
TOCTitle: EsentLSNotSetException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLSNotSetException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlsnotsetexception(v=EXCHG.10)
ms:contentKeyID: 55102236
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLSNotSetException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLSNotSetException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0d7446b9589c6c8f8c0ec3e0b654b304bab80917da55e2dba42c4a90ae56c5f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019239"
---
# <a name="esentlsnotsetexception-class"></a>EsentLSNotSetException, classe

Classe de base pour JET_err. Exceptions LSNotSet.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentStateException](./esentstateexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentLSNotSetException  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLSNotSetException _
    Inherits EsentStateException
'Usage
Dim instance As EsentLSNotSetException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLSNotSetException : EsentStateException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentLSNotSetException](./esentlsnotsetexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
