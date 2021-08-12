---
description: 'En savoir plus sur : méthode API. JetDefragment'
title: API. JetDefragment, méthode
TOCTitle: 'JetDefragment method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDefragment(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32@,System.Int32@,Microsoft.Isam.Esent.Interop.DefragGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdefragment(v=EXCHG.10)
ms:contentKeyID: 55100679
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9761782e2c6522752d6a05f69005a4db6844542c700cbc5c942ea80d96bf4c2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118272653"
---
# <a name="apijetdefragment-method"></a>API. JetDefragment, méthode

Démarre et arrête les tâches de défragmentation de base de données qui améliorent l’Organisation des données dans une base de données.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Function JetDefragment ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    ByRef passes As Integer, _
    ByRef seconds As Integer, _
    grbit As DefragGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim passes As Integer
Dim seconds As Integer
Dim grbit As DefragGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetDefragment(sesid, _
    dbid, tableName, passes, seconds, _
    grbit)
```

``` csharp
public static JET_wrn JetDefragment(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    ref int passes,
    ref int seconds,
    DefragGrbit grbit
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser pour l’appel.

<!-- end list -->

  - dbid  
    Type : [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Base de données à défragmenter.

<!-- end list -->

  - tableName  
    Type : [System. String](/dotnet/api/system.string)  
    
    Paramètre inutilisé. La défragmentation est effectuée pour l’ensemble de la base de données décrite par l’ID de base de données spécifié.

<!-- end list -->

  - mettent  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Lors du démarrage d’une tâche de défragmentation en ligne, ce paramètre définit le nombre maximal de passes de défragmentation. Lors de l’arrêt d’une tâche de défragmentation en ligne, ce paramètre est défini sur le nombre de passes effectuées.

<!-- end list -->

  - secondes  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Lors du démarrage d’une tâche de défragmentation en ligne, ce paramètre définit la durée maximale de la défragmentation. Lors de l’arrêt d’une tâche de défragmentation en ligne, cette mémoire tampon de sortie est définie sur la durée utilisée pour la défragmentation.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. DefragGrbit](./defraggrbit-enumeration.md)  
    
    Options de défragmentation.

#### <a name="return-value"></a>Valeur renvoyée

Type : [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Code d’avertissement.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
