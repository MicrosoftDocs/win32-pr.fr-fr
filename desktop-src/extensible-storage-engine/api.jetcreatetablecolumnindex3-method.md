---
description: 'En savoir plus sur : méthode API. JetCreateTableColumnIndex3'
title: API. JetCreateTableColumnIndex3, méthode
TOCTitle: 'JetCreateTableColumnIndex3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateTableColumnIndex3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_TABLECREATE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatetablecolumnindex3(v=EXCHG.10)
ms:contentKeyID: 55100678
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTableColumnIndex3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTableColumnIndex3
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ea254a4affde3ad6b2252f4ebe2f4b59137570066cc4ecc38c2e75d22e52b2ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117719237"
---
# <a name="apijetcreatetablecolumnindex3-method"></a>API. JetCreateTableColumnIndex3, méthode

Crée une table, ajoute des colonnes et des index sur cette table.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetCreateTableColumnIndex3 ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablecreate As JET_TABLECREATE _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablecreate As JET_TABLECREATEApi.JetCreateTableColumnIndex3(sesid, _
    dbid, tablecreate)
```

``` csharp
public static void JetCreateTableColumnIndex3(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_TABLECREATE tablecreate
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - dbid  
    Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Base de données à laquelle ajouter la nouvelle table.

<!-- end list -->

  - tablecreate  
    Type : [Microsoft.ISAM.esent.Interop.JET_TABLECREATE](./jet-tablecreate-class.md)  
    
    Objet décrivant la table à créer.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
