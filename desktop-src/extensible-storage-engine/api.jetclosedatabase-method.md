---
description: 'En savoir plus sur : méthode API. JetCloseDatabase'
title: API. JetCloseDatabase, méthode
TOCTitle: 'JetCloseDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCloseDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.CloseDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetclosedatabase(v=EXCHG.10)
ms:contentKeyID: 55100662
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCloseDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCloseDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f5a213cb824e1eb1b29a9648caf06670f99de7c0008048ff5969c009609142b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983509"
---
# <a name="apijetclosedatabase-method"></a>API. JetCloseDatabase, méthode

Ferme un fichier de base de données qui a été ouvert précédemment avec [JetOpenDatabase (JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md) ou créé avec [JetCreateDatabase (JET_SESID, String, String, JET_DBID, CreateDatabaseGrbit)](./api.jetcreatedatabase-method.md).

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetCloseDatabase ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    grbit As CloseDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim grbit As CloseDatabaseGrbitApi.JetCloseDatabase(sesid, dbid, _
    grbit)
```

``` csharp
public static void JetCloseDatabase(
    JET_SESID sesid,
    JET_DBID dbid,
    CloseDatabaseGrbit grbit
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - dbid  
    Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Base de données à fermer.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. CloseDatabaseGrbit](./closedatabasegrbit-enumeration.md)  
    
    Options de fermeture.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
