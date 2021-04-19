---
description: 'En savoir plus sur : classe EsentCheckpointCorruptException'
title: EsentCheckpointCorruptException, classe
TOCTitle: EsentCheckpointCorruptException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCheckpointCorruptException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcheckpointcorruptexception(v=EXCHG.10)
ms:contentKeyID: 55101237
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCheckpointCorruptException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCheckpointCorruptException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d0654ff85fa74cca8435ca6366e301bc3c70fc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534166"
---
# <a name="esentcheckpointcorruptexception-class"></a>EsentCheckpointCorruptException, classe

Classe de base pour JET_err. Exceptions CheckpointCorrupt.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentDataException](./esentdataexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentCorruptionException](./esentcorruptionexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentCheckpointCorruptException  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCheckpointCorruptException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentCheckpointCorruptException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCheckpointCorruptException : EsentCorruptionException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentCheckpointCorruptException](./esentcheckpointcorruptexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
