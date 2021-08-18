---
description: 'En savoir plus sur : classe EsentNTSystemCallFailedException'
title: EsentNTSystemCallFailedException, classe
TOCTitle: EsentNTSystemCallFailedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNTSystemCallFailedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentntsystemcallfailedexception(v=EXCHG.10)
ms:contentKeyID: 55102309
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNTSystemCallFailedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNTSystemCallFailedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 21d06fc3be6da5032fc68a90d6518ae92cdff7e8d8268d85d47df8f9ab027790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119040357"
---
# <a name="esentntsystemcallfailedexception-class"></a>EsentNTSystemCallFailedException, classe

Classe de base pour JET_err. Exceptions NTSystemCallFailed.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentOperationException](./esentoperationexception-class.md)  
          Microsoft. ISAM. esent. Interop. EsentNTSystemCallFailedException  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNTSystemCallFailedException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentNTSystemCallFailedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNTSystemCallFailedException : EsentOperationException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres EsentNTSystemCallFailedException](./esentntsystemcallfailedexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
