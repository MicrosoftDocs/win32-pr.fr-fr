---
description: 'En savoir plus sur : énumération RetrieveColumnGrbit'
title: Énumération RetrieveColumnGrbit
TOCTitle: RetrieveColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.retrievecolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39511391
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a223a288b8ad2d2e976be3bb9f2f524f78b9a8fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106517887"
---
# <a name="retrievecolumngrbit-enumeration"></a><span data-ttu-id="69cf4-103">Énumération RetrieveColumnGrbit</span><span class="sxs-lookup"><span data-stu-id="69cf4-103">RetrieveColumnGrbit enumeration</span></span>

<span data-ttu-id="69cf4-104">Options pour JetRetrieveColumn.</span><span class="sxs-lookup"><span data-stu-id="69cf4-104">Options for JetRetrieveColumn.</span></span>

<span data-ttu-id="69cf4-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="69cf4-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="69cf4-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="69cf4-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="69cf4-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="69cf4-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="69cf4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69cf4-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration RetrieveColumnGrbit
'Usage
Dim instance As RetrieveColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum RetrieveColumnGrbit
```

## <a name="members"></a><span data-ttu-id="69cf4-109">Membres</span><span class="sxs-lookup"><span data-stu-id="69cf4-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="69cf4-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="69cf4-110">Member name</span></span></th>
<th><span data-ttu-id="69cf4-111">Description</span><span class="sxs-lookup"><span data-stu-id="69cf4-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="69cf4-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="69cf4-112">None</span></span></td>
<td><span data-ttu-id="69cf4-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="69cf4-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="69cf4-114">RetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="69cf4-114">RetrieveCopy</span></span></td>
<td><span data-ttu-id="69cf4-115">Cet indicateur force la récupération de la colonne à récupérer la valeur modifiée au lieu de la valeur d’origine.</span><span class="sxs-lookup"><span data-stu-id="69cf4-115">This flag causes retrieve column to retrieve the modified value instead of the original value.</span></span> <span data-ttu-id="69cf4-116">Si la valeur n’a pas été modifiée, la valeur d’origine est récupérée.</span><span class="sxs-lookup"><span data-stu-id="69cf4-116">If the value has not been modified, then the original value is retrieved.</span></span> <span data-ttu-id="69cf4-117">De cette façon, une valeur qui n’a pas encore été insérée ou mise à jour peut être récupérée pendant l’opération d’insertion ou de mise à jour d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="69cf4-117">In this way, a value that has not yet been inserted or updated may be retrieved during the operation of inserting or updating a record.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="69cf4-118">RetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="69cf4-118">RetrieveFromIndex</span></span></td>
<td><span data-ttu-id="69cf4-119">Cette option permet de récupérer des valeurs de colonne à partir de l’index, si possible, sans accéder à l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="69cf4-119">This option is used to retrieve column values from the index, if possible, without accessing the record.</span></span> <span data-ttu-id="69cf4-120">De cette façon, le chargement inutile d’enregistrements peut être évité lorsque les données nécessaires sont disponibles à partir d’entrées d’index.</span><span class="sxs-lookup"><span data-stu-id="69cf4-120">In this way, unnecessary loading of records can be avoided when needed data is available from index entries themselves.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="69cf4-121">RetrieveFromPrimaryBookmark</span><span class="sxs-lookup"><span data-stu-id="69cf4-121">RetrieveFromPrimaryBookmark</span></span></td>
<td><span data-ttu-id="69cf4-122">Cette option est utilisée pour extraire des valeurs de colonne du signet d’index et peut différer de la valeur d’index lorsqu’une colonne apparaît à la fois dans l’index primaire et dans l’index actuel.</span><span class="sxs-lookup"><span data-stu-id="69cf4-122">This option is used to retrieve column values from the index bookmark, and may differ from the index value when a column appears both in the primary index and the current index.</span></span> <span data-ttu-id="69cf4-123">Cette option ne doit pas être spécifiée si l’index actuel est l’index cluster ou principal.</span><span class="sxs-lookup"><span data-stu-id="69cf4-123">This option should not be specified if the current index is the clustered, or primary, index.</span></span> <span data-ttu-id="69cf4-124">Ce bit ne peut pas être défini si RetrieveFromIndex est également défini.</span><span class="sxs-lookup"><span data-stu-id="69cf4-124">This bit cannot be set if RetrieveFromIndex is also set.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="69cf4-125">RetrieveTag</span><span class="sxs-lookup"><span data-stu-id="69cf4-125">RetrieveTag</span></span></td>
<td><span data-ttu-id="69cf4-126">Cette option permet de récupérer le numéro de séquence d’une valeur de colonne à valeurs multiples dans JET_RETINFO. itagSequence.</span><span class="sxs-lookup"><span data-stu-id="69cf4-126">This option is used to retrieve the sequence number of a multi-valued column value in JET_RETINFO.itagSequence.</span></span> <span data-ttu-id="69cf4-127">La récupération du numéro de séquence peut être une opération coûteuse et ne doit être effectuée que si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="69cf4-127">Retrieving the sequence number can be a costly operation and should only be done if necessary.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="69cf4-128">RetrieveNull</span><span class="sxs-lookup"><span data-stu-id="69cf4-128">RetrieveNull</span></span></td>
<td><span data-ttu-id="69cf4-129">Cette option permet de récupérer des valeurs NULL de colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="69cf4-129">This option is used to retrieve multi-valued column NULL values.</span></span> <span data-ttu-id="69cf4-130">Si cette option n’est pas spécifiée, les valeurs NULL de la colonne à valeurs multiples sont automatiquement ignorées.</span><span class="sxs-lookup"><span data-stu-id="69cf4-130">If this option is not specified, multi-valued column NULL values will automatically be skipped.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="69cf4-131">RetrieveIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="69cf4-131">RetrieveIgnoreDefault</span></span></td>
<td><span data-ttu-id="69cf4-132">Cette option affecte uniquement les colonnes à valeurs multiples et entraîne le renvoi d’une valeur NULL lorsque le numéro de séquence demandé est 1 et qu’il n’existe aucune valeur définie pour la colonne dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="69cf4-132">This option affects only multi-valued columns and causes a NULL value to be returned when the requested sequence number is 1 and there are no set values for the column in the record.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="69cf4-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69cf4-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="69cf4-134">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="69cf4-134">Reference</span></span>

[<span data-ttu-id="69cf4-135">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="69cf4-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
