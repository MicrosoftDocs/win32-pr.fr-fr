---
description: 'En savoir plus sur : énumération EnumerateColumnsGrbit'
title: Énumération EnumerateColumnsGrbit
TOCTitle: EnumerateColumnsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.enumeratecolumnsgrbit(v=EXCHG.10)
ms:contentKeyID: 39516754
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c1e6f768d2f8a837416540bcd3ca31f8984e55ad
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466806"
---
# <a name="enumeratecolumnsgrbit-enumeration"></a>Énumération EnumerateColumnsGrbit

Options pour JetEnumerateColumns.

Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EnumerateColumnsGrbit
'Usage
Dim instance As EnumerateColumnsGrbit
```

``` csharp
[FlagsAttribute]
public enum EnumerateColumnsGrbit
```

## <a name="members"></a>Membres


|  | Nom du membre | Description | 
|--|-------------|-------------|
|  | None | Options par défaut. | 
|  | EnumerateCompressOutput | Lors de l’énumération des valeurs de colonne, toutes les colonnes pour lesquelles nous récupérons toutes les valeurs et qui ont une seule valeur de colonne non NULL peuvent être retournées dans un format compressé. L’état de ces colonnes est défini sur <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> et la taille de la valeur de colonne et la mémoire contenant la valeur de colonne sont retournées directement dans la structure <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> . Il n’est pas garanti que toutes les colonnes admissibles soient compressées de cette manière. Pour plus d’informations, consultez <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> . | 
|  | EnumerateCopy | Cette option indique que les valeurs de colonne modifiées de l’enregistrement doivent être énumérées au lieu des valeurs de colonne d’origine. Si une valeur de colonne n’a pas été modifiée, la valeur de colonne d’origine est énumérée. De cette façon, une valeur de colonne qui n’a pas encore été insérée ou mise à jour peut être énumérée lors de l’insertion ou de la mise à jour d’un enregistrement.<p>Cette option est identique à <a href="hh578120(v=exchg.10).md">RetrieveCopy</a>.</p> | 
|  | EnumerateIgnoreDefault | Si une colonne donnée n’est pas présente dans l’enregistrement, aucune valeur de colonne n’est retournée. En règle générale, la valeur par défaut de la colonne, le cas échéant, est retournée dans ce cas. Il est garanti que si la colonne est définie sur une valeur différente de la valeur par défaut, cette valeur différente sera retournée (autrement dit, si une colonne avec une valeur par défaut est explicitement définie sur NULL, une valeur NULL est retournée en tant que valeur pour cette colonne). Même si cette option est demandée, il est toujours possible de voir une valeur de colonne qui se trouve être égale à la valeur par défaut. Aucun effort n’est apporté pour supprimer des valeurs de colonne qui correspondent à leurs valeurs par défaut. Il est important de se souvenir que cette option affecte la sortie de <a href="dn292148(v=exchg.10).md">JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a> quand elle est utilisée avec EnumeratePresenceOnly ou EnumerateTaggedOnly. | 
|  | EnumeratePresenceOnly | Si une valeur non NULL existe pour la colonne ou la valeur de colonne demandée, les données associées ne sont pas retournées. Au lieu de cela, l’état associé à la colonne ou à la valeur de cette colonne sera défini sur <a href="hh557250(v=exchg.10).md">ColumnPresent</a>. Si la colonne ou la valeur de colonne est NULL, <a href="hh557250(v=exchg.10).md">ColumnNull</a> est retourné comme d’habitude. | 
|  | EnumerateTaggedOnly | Lors de l’énumération de toutes les valeurs de colonne dans l’enregistrement (par exemple, lorsque numColumnids est égal à zéro), seules les valeurs de colonne avec balises sont retournées. Cette option n’est pas autorisée lors de l’énumération d’un tableau spécifique d’ID de colonne. | 



## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Référence

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

[EnumerateIgnoreUserDefinedDefault](./server2003grbits.enumerateignoreuserdefineddefault-field.md)

[EnumerateInRecordOnly](./windows7grbits.enumerateinrecordonly-field.md)
