---
description: 'En savoir plus sur : méthode API. JetSetTableSequential'
title: API. JetSetTableSequential, méthode
TOCTitle: 'JetSetTableSequential method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SetTableSequentialGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsettablesequential(v=EXCHG.10)
ms:contentKeyID: 55100810
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 879eca53c4867bb41ee0a231bff9adce39aa58a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921099"
---
# <a name="apijetsettablesequential-method"></a>API. JetSetTableSequential, méthode

Notifie le moteur de base de données que l’application analyse la totalité de l’index sur lequel le curseur est positionné. Par conséquent, les méthodes utilisées pour accéder aux données d’index seront paramétrées pour rendre ce scénario aussi rapide que possible. Consultez également [JetResetTableSequential (JET_SESID, JET_TABLEID, ResetTableSequentialGrbit)](./api.jetresettablesequential-method.md).

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetSetTableSequential ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SetTableSequentialGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SetTableSequentialGrbitApi.JetSetTableSequential(sesid, _
    tableid, grbit)
```

``` csharp
public static void JetSetTableSequential(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SetTableSequentialGrbit grbit
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - TableID  
    Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Curseur qui accède aux données.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. SetTableSequentialGrbit](./settablesequentialgrbit-enumeration.md)  
    
    Réservé pour un usage futur.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
