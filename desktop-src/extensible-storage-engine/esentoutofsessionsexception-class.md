---
description: 'En savoir plus sur : classe EsentOutOfSessionsException'
title: EsentOutOfSessionsException, classe
TOCTitle: EsentOutOfSessionsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofsessionsexception(v=EXCHG.10)
ms:contentKeyID: 55102494
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 70b3c466586551f67f451d8ecc6ad108da52089a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126854662"
---
# <a name="esentoutofsessionsexception-class"></a>EsentOutOfSessionsException, classe

Classe de base pour JET_err. Exceptions OutOfSessions.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentResourceException](./esentresourceexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentMemoryException](./esentmemoryexception-class.md)  
              Microsoft. ISAM. esent. Interop. EsentOutOfSessionsException  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfSessionsException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentOutOfSessionsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfSessionsException : EsentMemoryException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentOutOfSessionsException](./esentoutofsessionsexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
