---
description: 'En savoir plus sur : classe EsentBadLogVersionException'
title: EsentBadLogVersionException, classe
TOCTitle: EsentBadLogVersionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadLogVersionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbadlogversionexception(v=EXCHG.10)
ms:contentKeyID: 55101079
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadLogVersionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadLogVersionException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b146c79545cd2f3777f25037139bb182beca2c495901bbaa1e50ab2371b858f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042007"
---
# <a name="esentbadlogversionexception-class"></a>EsentBadLogVersionException, classe

Classe de base pour JET_err. Exceptions BadLogVersion.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentDataException](./esentdataexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentBadLogVersionException  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadLogVersionException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentBadLogVersionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadLogVersionException : EsentInconsistentException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentBadLogVersionException](./esentbadlogversionexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
