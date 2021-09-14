---
description: 'En savoir plus sur : méthode API. JetEnumerateColumns'
title: API. JetEnumerateColumns, méthode
TOCTitle: 'JetEnumerateColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID[],System.Int32@,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN[]@,Microsoft.Isam.Esent.Interop.JET_PFNREALLOC,System.IntPtr,System.Int32,Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetenumeratecolumns(v=EXCHG.10)
ms:contentKeyID: 55100695
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c9a9848d4470d54cc2a146098343b664c9bd3419
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126854758"
---
# <a name="apijetenumeratecolumns-method"></a>API. JetEnumerateColumns, méthode

Récupère efficacement un ensemble de colonnes et leurs valeurs à partir de l’enregistrement actuel d’un curseur ou de la mémoire tampon de copie de ce curseur. Les colonnes et les valeurs récupérées peuvent être restreintes par une liste d’ID de colonne, de nombres itagSequence et d’autres caractéristiques. Cette API de récupération de colonne est unique dans la mesure où elle retourne des informations dans la mémoire allouée dynamiquement obtenue à l’aide d’un rappel compatible réalloué fourni par l’utilisateur. Cette nouvelle flexibilité permet une récupération efficace des données de colonne avec des caractéristiques spécifiques (telles que la taille et la multiplicité) qui sont inconnues pour l’appelant. Cela élimine le besoin d’utiliser les modes de découverte de JetRetrieveColumn pour déterminer ces caractéristiques afin de configurer un dernier appel à JetRetrieveColumn qui récupérera correctement les données souhaitées.

Cette API n’est pas conforme CLS. 

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function JetEnumerateColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numColumnids As Integer, _
    columnids As JET_ENUMCOLUMNID(), _
    <OutAttribute> ByRef numColumnValues As Integer, _
    <OutAttribute> ByRef columnValues As JET_ENUMCOLUMN(), _
    allocator As JET_PFNREALLOC, _
    allocatorContext As IntPtr, _
    maxDataSize As Integer, _
    grbit As EnumerateColumnsGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numColumnids As Integer
Dim columnids As JET_ENUMCOLUMNID()
Dim numColumnValues As Integer
Dim columnValues As JET_ENUMCOLUMN()
Dim allocator As JET_PFNREALLOC
Dim allocatorContext As IntPtr
Dim maxDataSize As Integer
Dim grbit As EnumerateColumnsGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetEnumerateColumns(sesid, _
    tableid, numColumnids, columnids, _
    numColumnValues, columnValues, allocator, _
    allocatorContext, maxDataSize, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static JET_wrn JetEnumerateColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    int numColumnids,
    JET_ENUMCOLUMNID[] columnids,
    out int numColumnValues,
    out JET_ENUMCOLUMN[] columnValues,
    JET_PFNREALLOC allocator,
    IntPtr allocatorContext,
    int maxDataSize,
    EnumerateColumnsGrbit grbit
)
```

#### <a name="parameters"></a>Paramètres

  - sesid  
    Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Session à utiliser.

<!-- end list -->

  - TableID  
    Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Curseur à partir duquel récupérer des données.

<!-- end list -->

  - numColumnids  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Nombre de JET_ENUMCOLUMNIDS.

<!-- end list -->

  - columnids  
    Entrer \[\]  
    
    Tableau facultatif d’ID de colonne, chacun avec un tableau facultatif de nombres itagSequence à énumérer.

<!-- end list -->

  - numColumnValues  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Retourne le nombre de valeurs de colonne récupérées.

<!-- end list -->

  - columnValues  
    Entrer \[\]  
    
    Retourne les valeurs de la colonne énumérée.

<!-- end list -->

  - allocator  
    Type : [Microsoft.ISAM.esent.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)  
    
    Rappel utilisé pour allouer de la mémoire.

<!-- end list -->

  - allocatorContext  
    Type : [System. IntPtr](/dotnet/api/system.intptr)  
    
    Contexte du rappel d’allocation.

<!-- end list -->

  - maxDataSize  
    Type : [System. Int32](/dotnet/api/system.int32)  
    
    Définit une limite sur la quantité de données à retourner à partir d’une colonne de texte long ou d’une colonne binaire longue. Ce paramètre peut être utilisé pour empêcher l’énumération d’une valeur de colonne extrêmement volumineuse.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. EnumerateColumnsGrbit](./enumeratecolumnsgrbit-enumeration.md)  
    
    Récupérez les options.

#### <a name="return-value"></a>Valeur de retour

Type : [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Avertissement ou réussite.  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
