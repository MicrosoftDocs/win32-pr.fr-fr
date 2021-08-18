---
description: 'En savoir plus sur : classe EsentIOException'
title: Classe EsentIOException
TOCTitle: EsentIOException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentIOException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentioexception(v=EXCHG.10)
ms:contentKeyID: 55102033
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentIOException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentIOException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82c10cc71e7621aa5fb338acc8964a3e221af3cc068eafb1d32aab6273182501
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119115949"
---
# <a name="esentioexception-class"></a>Classe EsentIOException

Classe de base pour les exceptions d’e/s.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentOperationException](./esentoperationexception-class.md)  
          Microsoft. ISAM. esent. Interop. EsentIOException  
            [Microsoft. ISAM. esent. Interop. EsentDeleteBackupFileFailException](./esentdeletebackupfilefailexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentDiskIOException](./esentdiskioexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentFileAccessDeniedException](./esentfileaccessdeniedexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentLogWriteFailException](./esentlogwritefailexception-class.md)  
            [Microsoft. ISAM. esent. Interop. EsentMakeBackupDirectoryFailException](./esentmakebackupdirectoryfailexception-class.md)  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentIOException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentIOException
```

``` csharp
[SerializableAttribute]
public abstract class EsentIOException : EsentOperationException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentIOException](./esentioexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
