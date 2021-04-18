---
description: 'En savoir plus sur : méthode API. JetOpenTempTable'
title: API. JetOpenTempTable, méthode
TOCTitle: 'JetOpenTempTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable(v=EXCHG.10)
ms:contentKeyID: 55100773
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa41ce62b8bc2d7f2429acb5de809ad0be44a609
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526945"
---
# <a name="apijetopentemptable-method"></a>API. JetOpenTempTable, méthode

Crée une table temporaire avec un index unique. Une table temporaire stocke et récupère des enregistrements comme une table ordinaire créée à l’aide de JetCreateTableColumnIndex. Toutefois, les tables temporaires sont beaucoup plus rapides que les tables ordinaires en raison de leur nature volatile. Ils peuvent également être utilisés pour trier et effectuer très rapidement la suppression des doublons sur les jeux d’enregistrements lorsque vous y accédez de manière purement séquentielle. Consultez également [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md). [JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetOpenTempTable ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable(sesid, columns, _
    numColumns, grbit, tableid, columnids)
```

``` csharp
public static void JetOpenTempTable(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - colonnes  
    Entrer \[\]  
    
    Définitions de colonne pour les colonnes créées dans la table temporaire.

<!-- end list -->

  - numColumns  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Nombre de définitions de colonne.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. TempTableGrbit](./temptablegrbit-enumeration.md)  
    
    Options de création de table.

<!-- end list -->

  - TableID  
    Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Retourne l’TableID de la table temporaire. La fermeture de ce TableID avec [JetCloseTable (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) libère les ressources associées à la table temporaire.

<!-- end list -->

  - columnids  
    Entrer \[\]  
    
    Mémoire tampon de sortie qui reçoit le tableau d’ID de colonne générés au cours de la création de la table temporaire. Les ID de colonne dans ce tableau correspondent exactement au tableau d’entrée des définitions de colonne. Par conséquent, la taille de cette mémoire tampon doit correspondre à la taille du tableau d’entrée.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
