---
description: 'En savoir plus sur : méthode API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)'
title: Méthode API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100770
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2320b72a90ff97326c027b00cfeb5bf38453f68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515421"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-jet_indexlist"></a>Méthode API. JetGetIndexInfo (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)

**Remarque : cette API est désormais obsolète.**

Récupère des informations sur les index d’une table.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")> _
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    ignored As String, _
    <OutAttribute> ByRef indexlist As JET_INDEXLIST _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim ignored As String
Dim indexlist As JET_INDEXLISTApi.JetGetIndexInfo(sesid, dbid, _
    tablename, ignored, indexlist)
```

``` csharp
[ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")]
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string ignored,
    out JET_INDEXLIST indexlist
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - dbid  
    Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Base de données à utiliser.

<!-- end list -->

  - tablename  
    Type : [System. String](/dotnet/api/system.string)  
    
    Nom de la table sur laquelle récupérer les informations d’index.

<!-- end list -->

  - ignoré  
    Type : [System. String](/dotnet/api/system.string)  
    
    Ce paramètre est ignoré.

<!-- end list -->

  - indexlist  
    Type : [Microsoft.ISAM.esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)  
    
    Renseigné avec des informations sur les index de la table.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Surcharge JetGetIndexInfo](./api.jetgetindexinfo-method.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
