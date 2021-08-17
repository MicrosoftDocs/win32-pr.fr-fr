---
description: 'En savoir plus sur : classe EsentDatabaseFileReadOnlyException'
title: EsentDatabaseFileReadOnlyException, classe
TOCTitle: EsentDatabaseFileReadOnlyException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseFileReadOnlyException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasefilereadonlyexception(v=EXCHG.10)
ms:contentKeyID: 55101357
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseFileReadOnlyException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseFileReadOnlyException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ec4c7d29b19e1c3e58561836e2ce9d5dfcf547e3b9a9082e2021ab5ce3cb2fa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118781240"
---
# <a name="esentdatabasefilereadonlyexception-class"></a>EsentDatabaseFileReadOnlyException, classe

Classe de base pour JET_err. Exceptions DatabaseFileReadOnly.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentDatabaseFileReadOnlyException  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseFileReadOnlyException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseFileReadOnlyException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseFileReadOnlyException : EsentUsageException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentDatabaseFileReadOnlyException](./esentdatabasefilereadonlyexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
