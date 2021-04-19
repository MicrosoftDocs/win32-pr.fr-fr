---
description: 'En savoir plus sur : classe EsentBackupAbortByServerException'
title: EsentBackupAbortByServerException, classe
TOCTitle: EsentBackupAbortByServerException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBackupAbortByServerException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbackupabortbyserverexception(v=EXCHG.10)
ms:contentKeyID: 55101070
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBackupAbortByServerException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBackupAbortByServerException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be5f1fca4cfdbfe880288b66d3d6c8a439666384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530711"
---
# <a name="esentbackupabortbyserverexception-class"></a>EsentBackupAbortByServerException, classe

Classe de base pour JET_err. Exceptions BackupAbortByServer.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentOperationException](./esentoperationexception-class.md)  
          Microsoft. ISAM. esent. Interop. EsentBackupAbortByServerException  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBackupAbortByServerException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentBackupAbortByServerException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBackupAbortByServerException : EsentOperationException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentBackupAbortByServerException](./esentbackupabortbyserverexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
