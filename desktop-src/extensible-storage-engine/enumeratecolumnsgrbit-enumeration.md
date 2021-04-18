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
ms.openlocfilehash: 5e27e6810b37b513d550bbafce509b2815ccea2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526308"
---
# <a name="enumeratecolumnsgrbit-enumeration"></a><span data-ttu-id="58114-103">Énumération EnumerateColumnsGrbit</span><span class="sxs-lookup"><span data-stu-id="58114-103">EnumerateColumnsGrbit enumeration</span></span>

<span data-ttu-id="58114-104">Options pour JetEnumerateColumns.</span><span class="sxs-lookup"><span data-stu-id="58114-104">Options for JetEnumerateColumns.</span></span>

<span data-ttu-id="58114-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="58114-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="58114-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="58114-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="58114-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="58114-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="58114-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58114-108">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="58114-109">Membres</span><span class="sxs-lookup"><span data-stu-id="58114-109">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="58114-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="58114-110">Member name</span></span></th>
<th><span data-ttu-id="58114-111">Description</span><span class="sxs-lookup"><span data-stu-id="58114-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="58114-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="58114-112">None</span></span></td>
<td><span data-ttu-id="58114-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="58114-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="58114-114">EnumerateCompressOutput</span><span class="sxs-lookup"><span data-stu-id="58114-114">EnumerateCompressOutput</span></span></td>
<td><span data-ttu-id="58114-115">Lors de l’énumération des valeurs de colonne, toutes les colonnes pour lesquelles nous récupérons toutes les valeurs et qui ont une seule valeur de colonne non NULL peuvent être retournées dans un format compressé.</span><span class="sxs-lookup"><span data-stu-id="58114-115">When enumerating column values, all columns for which we are retrieving all values and that have only one non-NULL column value may be returned in a compressed format.</span></span> <span data-ttu-id="58114-116">L’état de ces colonnes est défini sur <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> et la taille de la valeur de colonne et la mémoire contenant la valeur de colonne sont retournées directement dans la structure <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> .</span><span class="sxs-lookup"><span data-stu-id="58114-116">The status for such columns will be set to <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> and the size of the column value and the memory containing the column value will be returned directly in the <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> structure.</span></span> <span data-ttu-id="58114-117">Il n’est pas garanti que toutes les colonnes admissibles soient compressées de cette manière.</span><span class="sxs-lookup"><span data-stu-id="58114-117">It is not guaranteed that all eligible columns are compressed in this manner.</span></span> <span data-ttu-id="58114-118">Pour plus d’informations, consultez <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> .</span><span class="sxs-lookup"><span data-stu-id="58114-118">See <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> for more information.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="58114-119">EnumerateCopy</span><span class="sxs-lookup"><span data-stu-id="58114-119">EnumerateCopy</span></span></td>
<td><span data-ttu-id="58114-120">Cette option indique que les valeurs de colonne modifiées de l’enregistrement doivent être énumérées au lieu des valeurs de colonne d’origine.</span><span class="sxs-lookup"><span data-stu-id="58114-120">This option indicates that the modified column values of the record should be enumerated rather than the original column values.</span></span> <span data-ttu-id="58114-121">Si une valeur de colonne n’a pas été modifiée, la valeur de colonne d’origine est énumérée.</span><span class="sxs-lookup"><span data-stu-id="58114-121">If a column value has not been modified, the original column value is enumerated.</span></span> <span data-ttu-id="58114-122">De cette façon, une valeur de colonne qui n’a pas encore été insérée ou mise à jour peut être énumérée lors de l’insertion ou de la mise à jour d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="58114-122">In this way, a column value that has not yet been inserted or updated may be enumerated when inserting or updating a record.</span></span>
<p><span data-ttu-id="58114-123">Cette option est identique à <a href="hh578120(v=exchg.10).md">RetrieveCopy</a>.</span><span class="sxs-lookup"><span data-stu-id="58114-123">This option is identical to <a href="hh578120(v=exchg.10).md">RetrieveCopy</a>.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="58114-124">EnumerateIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="58114-124">EnumerateIgnoreDefault</span></span></td>
<td><span data-ttu-id="58114-125">Si une colonne donnée n’est pas présente dans l’enregistrement, aucune valeur de colonne n’est retournée.</span><span class="sxs-lookup"><span data-stu-id="58114-125">If a given column is not present in the record then no column value will be returned.</span></span> <span data-ttu-id="58114-126">En règle générale, la valeur par défaut de la colonne, le cas échéant, est retournée dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="58114-126">Ordinarily, the default value for the column, if any, would be returned in this case.</span></span> <span data-ttu-id="58114-127">Il est garanti que si la colonne est définie sur une valeur différente de la valeur par défaut, cette valeur différente sera retournée (autrement dit, si une colonne avec une valeur par défaut est explicitement définie sur NULL, une valeur NULL est retournée en tant que valeur pour cette colonne).</span><span class="sxs-lookup"><span data-stu-id="58114-127">It is guaranteed that if the column is set to a value different than the default value then that different value will be returned (that is, if a column with a default value is explicitly set to NULL then a NULL will be returned as the value for that column).</span></span> <span data-ttu-id="58114-128">Même si cette option est demandée, il est toujours possible de voir une valeur de colonne qui se trouve être égale à la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="58114-128">Even if this option is requested, it is still possible to see a column value that happens to be equal to the default value.</span></span> <span data-ttu-id="58114-129">Aucun effort n’est apporté pour supprimer des valeurs de colonne qui correspondent à leurs valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="58114-129">No effort is made to remove column values that match their default values.</span></span> <span data-ttu-id="58114-130">Il est important de se souvenir que cette option affecte la sortie de <a href="dn292148(v=exchg.10).md">JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a> quand elle est utilisée avec EnumeratePresenceOnly ou EnumerateTaggedOnly.</span><span class="sxs-lookup"><span data-stu-id="58114-130">It is important to remember that this option affects the output of <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a> when used with EnumeratePresenceOnly or EnumerateTaggedOnly.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="58114-131">EnumeratePresenceOnly</span><span class="sxs-lookup"><span data-stu-id="58114-131">EnumeratePresenceOnly</span></span></td>
<td><span data-ttu-id="58114-132">Si une valeur non NULL existe pour la colonne ou la valeur de colonne demandée, les données associées ne sont pas retournées.</span><span class="sxs-lookup"><span data-stu-id="58114-132">If a non-NULL value exists for the requested column or column value then the associated data is not returned.</span></span> <span data-ttu-id="58114-133">Au lieu de cela, l’état associé à la colonne ou à la valeur de cette colonne sera défini sur <a href="hh557250(v=exchg.10).md">ColumnPresent</a>.</span><span class="sxs-lookup"><span data-stu-id="58114-133">Instead, the associated status for that column or column value will be set to <a href="hh557250(v=exchg.10).md">ColumnPresent</a>.</span></span> <span data-ttu-id="58114-134">Si la colonne ou la valeur de colonne est NULL, <a href="hh557250(v=exchg.10).md">ColumnNull</a> est retourné comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="58114-134">If the column or column value is NULL then <a href="hh557250(v=exchg.10).md">ColumnNull</a> will be returned as usual.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="58114-135">EnumerateTaggedOnly</span><span class="sxs-lookup"><span data-stu-id="58114-135">EnumerateTaggedOnly</span></span></td>
<td><span data-ttu-id="58114-136">Lors de l’énumération de toutes les valeurs de colonne dans l’enregistrement (par exemple, lorsque numColumnids est égal à zéro), seules les valeurs de colonne avec balises sont retournées.</span><span class="sxs-lookup"><span data-stu-id="58114-136">When enumerating all column values in the record (for example,that is when numColumnids is zero), only tagged column values will be returned.</span></span> <span data-ttu-id="58114-137">Cette option n’est pas autorisée lors de l’énumération d’un tableau spécifique d’ID de colonne.</span><span class="sxs-lookup"><span data-stu-id="58114-137">This option is not allowed when enumerating a specific array of column IDs.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="58114-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58114-138">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="58114-139">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="58114-139">Reference</span></span>

[<span data-ttu-id="58114-140">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="58114-140">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="58114-141">EnumerateIgnoreUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="58114-141">EnumerateIgnoreUserDefinedDefault</span></span>](./server2003grbits.enumerateignoreuserdefineddefault-field.md)

[<span data-ttu-id="58114-142">EnumerateInRecordOnly</span><span class="sxs-lookup"><span data-stu-id="58114-142">EnumerateInRecordOnly</span></span>](./windows7grbits.enumerateinrecordonly-field.md)
