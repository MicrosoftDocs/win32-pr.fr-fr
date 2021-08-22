---
description: 'En savoir plus sur : classe EsentCannotNestDDLException'
title: EsentCannotNestDDLException, classe
TOCTitle: EsentCannotNestDDLException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCannotNestDDLException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcannotnestddlexception(v=EXCHG.10)
ms:contentKeyID: 55101267
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCannotNestDDLException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCannotNestDDLException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ca852d4ebf90b133a8475b5ff14a32f5b4002b8f509d60bf68cafbce318ae403
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119365719"
---
# <a name="esentcannotnestddlexception-class"></a>EsentCannotNestDDLException, classe

Classe de base pour JET_err. Exceptions CannotNestDDL.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentCannotNestDDLException  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCannotNestDDLException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentCannotNestDDLException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCannotNestDDLException : EsentUsageException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentCannotNestDDLException](./esentcannotnestddlexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
