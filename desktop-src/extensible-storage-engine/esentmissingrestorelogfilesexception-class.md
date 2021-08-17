---
description: 'En savoir plus sur : classe EsentMissingRestoreLogFilesException'
title: EsentMissingRestoreLogFilesException, classe
TOCTitle: EsentMissingRestoreLogFilesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMissingRestoreLogFilesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmissingrestorelogfilesexception(v=EXCHG.10)
ms:contentKeyID: 55102315
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMissingRestoreLogFilesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMissingRestoreLogFilesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7bce3b7a1323b90650efee124bd9a267831edc35e594d8e3bc32436bf1d2b1bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119115429"
---
# <a name="esentmissingrestorelogfilesexception-class"></a>EsentMissingRestoreLogFilesException, classe

Classe de base pour JET_err. Exceptions MissingRestoreLogFiles.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentDataException](./esentdataexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentMissingRestoreLogFilesException  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMissingRestoreLogFilesException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentMissingRestoreLogFilesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMissingRestoreLogFilesException : EsentInconsistentException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentMissingRestoreLogFilesException](./esentmissingrestorelogfilesexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
