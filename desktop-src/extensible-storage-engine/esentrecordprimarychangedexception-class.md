---
description: 'En savoir plus sur : classe EsentRecordPrimaryChangedException'
title: EsentRecordPrimaryChangedException, classe
TOCTitle: EsentRecordPrimaryChangedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordPrimaryChangedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecordprimarychangedexception(v=EXCHG.10)
ms:contentKeyID: 55102532
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordPrimaryChangedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordPrimaryChangedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 06fe56bb34c20ce45c99999526a3db279f72f085
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530924"
---
# <a name="esentrecordprimarychangedexception-class"></a>EsentRecordPrimaryChangedException, classe

Classe de base pour JET_err. Exceptions RecordPrimaryChanged.

## <a name="inheritance-hierarchy"></a>Hiérarchie d’héritage

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. esent. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. esent. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. esent. Interop. EsentApiException](./esentapiexception-class.md)  
          [Microsoft. ISAM. esent. Interop. EsentUsageException](./esentusageexception-class.md)  
            Microsoft. ISAM. esent. Interop. EsentRecordPrimaryChangedException  

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordPrimaryChangedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentRecordPrimaryChangedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordPrimaryChangedException : EsentUsageException
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Référence

[Membres EsentRecordPrimaryChangedException](./esentrecordprimarychangedexception-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
