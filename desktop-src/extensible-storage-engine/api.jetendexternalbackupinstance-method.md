---
description: 'En savoir plus sur : méthode API. JetEndExternalBackupInstance'
title: API. JetEndExternalBackupInstance, méthode
TOCTitle: 'JetEndExternalBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetendexternalbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55100691
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4611962006d4edc70eb558ad84b6ee47e6fd290a4ed301794695efe9ce513f2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042697"
---
# <a name="apijetendexternalbackupinstance-method"></a>API. JetEndExternalBackupInstance, méthode

Met fin à une session de sauvegarde externe. Cette API est la dernière API d’une série d’API qui doivent être appelées pour exécuter une sauvegarde en ligne réussie (non basée sur VSS).

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetEndExternalBackupInstance ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetEndExternalBackupInstance(instance)
```

``` csharp
public static void JetEndExternalBackupInstance(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a>Paramètres

  - instance  
    Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Instance pour laquelle terminer la sauvegarde.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
