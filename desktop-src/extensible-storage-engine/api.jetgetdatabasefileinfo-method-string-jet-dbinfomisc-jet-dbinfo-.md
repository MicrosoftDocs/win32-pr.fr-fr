---
description: 'En savoir plus sur : méthode API. JetGetDatabaseFileInfo (String, JET_DBINFOMISC, JET_DbInfo)'
title: Méthode API. JetGetDatabaseFileInfo (String, JET_DBINFOMISC, JET_DbInfo)
TOCTitle: JetGetDatabaseFileInfo method (String, JET_DBINFOMISC, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo(System.String,Microsoft.Isam.Esent.Interop.JET_DBINFOMISC@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabasefileinfo(v=EXCHG.10)
ms:contentKeyID: 55100709
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d72711314312c843d9e456a5194cb6133b4f491f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112582"
---
# <a name="apijetgetdatabasefileinfo-method-string-jet_dbinfomisc-jet_dbinfo"></a>Méthode API. JetGetDatabaseFileInfo (String, JET_DBINFOMISC, JET_DbInfo)

Récupère certaines informations sur la base de données spécifiée.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetGetDatabaseFileInfo ( _
    databaseName As String, _
    <OutAttribute> ByRef dbinfomisc As JET_DBINFOMISC, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim databaseName As String
Dim dbinfomisc As JET_DBINFOMISC
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseFileInfo(databaseName, _
    dbinfomisc, infoLevel)
```

``` csharp
public static void JetGetDatabaseFileInfo(
    string databaseName,
    out JET_DBINFOMISC dbinfomisc,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a>Paramètres

  - databaseName  
    Type : [System. String](/dotnet/api/system.string)  
    
    Nom de fichier de la base de données.

<!-- end list -->

  - dbinfomisc  
    Type : [Microsoft.ISAM.esent.Interop.JET_DBINFOMISC](./jet-dbinfomisc-class.md)  
    
    Valeur à récupérer.

<!-- end list -->

  - infoLevel  
    Type : [Microsoft.ISAM.esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)  
    
    Données spécifiques à récupérer.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Surcharge JetGetDatabaseFileInfo](./api.jetgetdatabasefileinfo-method.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
