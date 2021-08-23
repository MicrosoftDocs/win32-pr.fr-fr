---
description: 'En savoir plus sur : méthode API. JetCreateIndex'
title: API. JetCreateIndex, méthode
TOCTitle: 'JetCreateIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.CreateIndexGrbit,System.String,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateindex(v=EXCHG.10)
ms:contentKeyID: 55100693
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df24e16252ec3aa837b9232859bf56726ee54b09448a57572281fab97a28c5c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670549"
---
# <a name="apijetcreateindex-method"></a>API. JetCreateIndex, méthode

Crée un index sur les données d’une base de données ESE. Un index peut être utilisé pour localiser rapidement des données spécifiques.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetCreateIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexName As String, _
    grbit As CreateIndexGrbit, _
    keyDescription As String, _
    keyDescriptionLength As Integer, _
    density As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexName As String
Dim grbit As CreateIndexGrbit
Dim keyDescription As String
Dim keyDescriptionLength As Integer
Dim density As IntegerApi.JetCreateIndex(sesid, tableid, _
    indexName, grbit, keyDescription, _
    keyDescriptionLength, density)
```

``` csharp
public static void JetCreateIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexName,
    CreateIndexGrbit grbit,
    string keyDescription,
    int keyDescriptionLength,
    int density
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - TableID  
    Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Table sur laquelle créer l’index.

<!-- end list -->

  - indexName  
    Type : [System. String](/dotnet/api/system.string)  
    
    Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’index à créer.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. CreateIndexGrbit](./createindexgrbit-enumeration.md)  
    
    Options de création d’index.

<!-- end list -->

  - keydescription  
    Type : [System. String](/dotnet/api/system.string)  
    
    Pointeur vers une chaîne double terminée par un caractère null des jetons délimités par des valeurs NULL.

<!-- end list -->

  - keyDescriptionLength  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Longueur, en caractères, de szKey, y compris les deux valeurs null de fin.

<!-- end list -->

  - masse  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Densité initiale B + arborescence.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
