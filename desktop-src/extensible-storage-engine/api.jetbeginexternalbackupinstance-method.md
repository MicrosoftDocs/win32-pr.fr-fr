---
description: 'En savoir plus sur : méthode API. JetBeginExternalBackupInstance'
title: API. JetBeginExternalBackupInstance, méthode
TOCTitle: 'JetBeginExternalBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginExternalBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.BeginExternalBackupGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbeginexternalbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55100659
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginExternalBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginExternalBackupInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b590ed0fb13c4540a4fad15eea1de5c4ad24e40611285d976ebf04b6269c6b6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983639"
---
# <a name="apijetbeginexternalbackupinstance-method"></a>API. JetBeginExternalBackupInstance, méthode

Lance une sauvegarde externe alors que le moteur et la base de données sont en ligne et actifs.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetBeginExternalBackupInstance ( _
    instance As JET_INSTANCE, _
    grbit As BeginExternalBackupGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As BeginExternalBackupGrbitApi.JetBeginExternalBackupInstance(instance, _
    grbit)
```

``` csharp
public static void JetBeginExternalBackupInstance(
    JET_INSTANCE instance,
    BeginExternalBackupGrbit grbit
)
```

#### <a name="parameters"></a>Paramètres

  - instance  
    Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    L’instance prépare la sauvegarde.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. BeginExternalBackupGrbit](./beginexternalbackupgrbit-enumeration.md)  
    
    Options de sauvegarde.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
