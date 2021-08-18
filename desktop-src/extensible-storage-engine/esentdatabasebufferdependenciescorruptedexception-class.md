---
description: 'En savoir plus sur : classe EsentDatabaseBufferDependenciesCorruptedException'
title: EsentDatabaseBufferDependenciesCorruptedException, classe
TOCTitle: EsentDatabaseBufferDependenciesCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseBufferDependenciesCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasebufferdependenciescorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55101428
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseBufferDependenciesCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseBufferDependenciesCorruptedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b0474689e5e7535c3b2ab3027451edf7ffa5bd0e4588ea4a4309a4b86d015640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118781476"
---
# <a name="esentdatabasebufferdependenciescorruptedexception-class"></a>EsentDatabaseBufferDependenciesCorruptedException, classe

Classe de base pour JET_err. Exceptions DatabaseBufferDependenciesCorrupted.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentDataException](./esentdataexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentCorruptionException](./esentcorruptionexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentDatabaseBufferDependenciesCorruptedException  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseBufferDependenciesCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentDatabaseBufferDependenciesCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseBufferDependenciesCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentDatabaseBufferDependenciesCorruptedException](./esentdatabasebufferdependenciescorruptedexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
