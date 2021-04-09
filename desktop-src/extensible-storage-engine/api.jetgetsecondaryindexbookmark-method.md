---
description: 'En savoir plus sur : méthode API. JetGetSecondaryIndexBookmark'
title: API. JetGetSecondaryIndexBookmark, méthode
TOCTitle: 'JetGetSecondaryIndexBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.GetSecondaryIndexBookmarkGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetsecondaryindexbookmark(v=EXCHG.10)
ms:contentKeyID: 55100725
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b0a25e78ca291271a96d06e5c0bf61c691acd4de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033908"
---
# <a name="apijetgetsecondaryindexbookmark-method"></a>API. JetGetSecondaryIndexBookmark, méthode

Récupère un signet spécial pour l’entrée d’index secondaire à la position actuelle d’un curseur. Ce signet peut ensuite être utilisé pour repositionner efficacement ce curseur sur la même entrée d’index à l’aide de JetGotoSecondaryIndexBookmark. Cela est particulièrement utile lors du repositionnement sur un index secondaire qui contient des clés dupliquées ou qui contient plusieurs entrées d’index pour le même enregistrement.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetGetSecondaryIndexBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    secondaryKey As Byte(), _
    secondaryKeySize As Integer, _
    <OutAttribute> ByRef actualSecondaryKeySize As Integer, _
    primaryKey As Byte(), _
    primaryKeySize As Integer, _
    <OutAttribute> ByRef actualPrimaryKeySize As Integer, _
    grbit As GetSecondaryIndexBookmarkGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim secondaryKey As Byte()
Dim secondaryKeySize As Integer
Dim actualSecondaryKeySize As Integer
Dim primaryKey As Byte()
Dim primaryKeySize As Integer
Dim actualPrimaryKeySize As Integer
Dim grbit As GetSecondaryIndexBookmarkGrbitApi.JetGetSecondaryIndexBookmark(sesid, _
    tableid, secondaryKey, secondaryKeySize, _
    actualSecondaryKeySize, primaryKey, _
    primaryKeySize, actualPrimaryKeySize, _
    grbit)
```

``` csharp
public static void JetGetSecondaryIndexBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] secondaryKey,
    int secondaryKeySize,
    out int actualSecondaryKeySize,
    byte[] primaryKey,
    int primaryKeySize,
    out int actualPrimaryKeySize,
    GetSecondaryIndexBookmarkGrbit grbit
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - TableID  
    Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Curseur à partir duquel récupérer le signet.

<!-- end list -->

  - secondaryKey  
    Entrer \[\]  
    
    Mémoire tampon de sortie pour la clé secondaire.

<!-- end list -->

  - secondaryKeySize  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Taille de la mémoire tampon de la clé secondaire.

<!-- end list -->

  - actualSecondaryKeySize  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Retourne la taille de la clé secondaire.

<!-- end list -->

  - primaryKey  
    Entrer \[\]  
    
    Mémoire tampon de sortie pour la clé primaire.

<!-- end list -->

  - primaryKeySize  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Taille de la mémoire tampon de clé primaire.

<!-- end list -->

  - actualPrimaryKeySize  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Retourne la taille de la clé primaire.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. GetSecondaryIndexBookmarkGrbit](./getsecondaryindexbookmarkgrbit-enumeration.md)  
    
    Options pour l’appel.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
