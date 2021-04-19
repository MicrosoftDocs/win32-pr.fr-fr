---
description: 'En savoir plus sur : méthode API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)'
title: Méthode API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
TOCTitle: JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100790
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d417e188c72914f871df4b46dede204f6633a8b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514157"
---
# <a name="apijetretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-int32-retrievecolumngrbit-jet_retinfo"></a>Méthode API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)

Récupère une valeur de colonne unique à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur. Cette fonction peut également récupérer une colonne d’un enregistrement en cours de création dans le tampon de copie de curseur. Cette fonction peut également récupérer des données de colonne à partir d’une entrée d’index qui fait référence à l’enregistrement actif. En plus de récupérer la valeur réelle de la colonne, JetRetrieveColumn peut également être utilisé pour récupérer la taille d’une colonne, avant de récupérer les données de la colonne elle-même afin que les tampons d’application puissent être dimensionnés de manière appropriée.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Function JetRetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    <OutAttribute> ByRef actualDataSize As Integer, _
    grbit As RetrieveColumnGrbit, _
    retinfo As JET_RETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumn(sesid, _
    tableid, columnid, data, dataSize, _
    actualDataSize, grbit, retinfo)
```

``` csharp
public static JET_wrn JetRetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    out int actualDataSize,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - TableID  
    Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Curseur à partir duquel récupérer la colonne.

<!-- end list -->

  - columnid  
    Type : [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    ColumnID à récupérer.

<!-- end list -->

  - data  
    Entrer \[\]  
    
    Mémoire tampon de données à récupérer dans.

<!-- end list -->

  - dataSize  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Taille de la mémoire tampon de données.

<!-- end list -->

  - actualDataSize  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Retourne la taille réelle de la mémoire tampon de données.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)  
    
    Récupérez les options de colonne.

<!-- end list -->

  - retinfo  
    Type : [Microsoft.ISAM.esent.Interop.JET_RETINFO](./jet-retinfo-class.md)  
    
    Si pretinfo a la valeur NULL, la fonction se comporte comme si un itagSequence de 1 et un ibLongValue de 0 (zéro) ont été donnés. Ainsi, la récupération de colonne récupère la première valeur d’une colonne à valeurs multiples et récupère les données de type long à l’offset 0 (zéro).

#### <a name="return-value"></a>Valeur retournée

Type : [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Code d’avertissement ESENT.  

## <a name="remarks"></a>Notes

Les fonctions RetrieveColumnAs fournissent des fonctions de récupération spécifiques au type de données.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Surcharge JetRetrieveColumn](./api.jetretrievecolumn-method.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
