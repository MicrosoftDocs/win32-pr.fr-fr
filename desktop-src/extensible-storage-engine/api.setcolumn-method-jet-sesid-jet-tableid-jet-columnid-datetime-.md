---
description: 'En savoir plus sur : méthode API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)'
title: Méthode API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.DateTime)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100875
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e43864a1b632adbc4ecf84d4963e7f87ea799283
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127216316"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-datetime"></a>Méthode API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)

Modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou pour mettre à jour l’enregistrement en cours.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As DateTime _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As DateTimeApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    DateTime data
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - TableID  
    Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Curseur à mettre à jour. Une mise à jour doit être préparée.

<!-- end list -->

  - columnid  
    Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    ColumnID à définir.

<!-- end list -->

  - data  
    Type : [System. DateTime](/dotnet/api/system.datetime)  
    
    Données à définir.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Surcharge SetColumn](./api.setcolumn-method.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
