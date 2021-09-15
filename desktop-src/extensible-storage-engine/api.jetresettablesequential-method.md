---
description: 'En savoir plus sur : méthode API. JetResetTableSequential'
title: API. JetResetTableSequential, méthode
TOCTitle: 'JetResetTableSequential method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.ResetTableSequentialGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetresettablesequential(v=EXCHG.10)
ms:contentKeyID: 55100789
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b45ca118894015df7cda56201733cdaad9b88d69
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404024"
---
# <a name="apijetresettablesequential-method"></a>API. JetResetTableSequential, méthode

Notifie le moteur de base de données que l’application n’analyse plus la totalité de l’index sur lequel le curseur est positionné. Cet appel inverse une notification envoyée par [JetSetTableSequential (JET_SESID, JET_TABLEID, SetTableSequentialGrbit)](./api.jetsettablesequential-method.md).

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetResetTableSequential ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As ResetTableSequentialGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As ResetTableSequentialGrbitApi.JetResetTableSequential(sesid, _
    tableid, grbit)
```

``` csharp
public static void JetResetTableSequential(
    JET_SESID sesid,
    JET_TABLEID tableid,
    ResetTableSequentialGrbit grbit
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - TableID  
    Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Curseur qui a accès aux données.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. ResetTableSequentialGrbit](./resettablesequentialgrbit-enumeration.md)  
    
    Réservé pour un usage futur.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
