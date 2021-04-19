---
description: 'En savoir plus sur : énumération SetIndexRangeGrbit'
title: Énumération SetIndexRangeGrbit
TOCTitle: SetIndexRangeGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setindexrangegrbit(v=EXCHG.10)
ms:contentKeyID: 39515181
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.None
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInclusive
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInstantDuration
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeRemove
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeUpperLimit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInstantDuration
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeUpperLimit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.None
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInclusive
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeRemove
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6cda73597f88d2c8fca911ebb96d7a3c6399ed9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514651"
---
# <a name="setindexrangegrbit-enumeration"></a><span data-ttu-id="f5c20-103">Énumération SetIndexRangeGrbit</span><span class="sxs-lookup"><span data-stu-id="f5c20-103">SetIndexRangeGrbit enumeration</span></span>

<span data-ttu-id="f5c20-104">Options pour JetSetIndexRange.</span><span class="sxs-lookup"><span data-stu-id="f5c20-104">Options for JetSetIndexRange.</span></span>

<span data-ttu-id="f5c20-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="f5c20-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="f5c20-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f5c20-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f5c20-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f5c20-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f5c20-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5c20-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetIndexRangeGrbit
'Usage
Dim instance As SetIndexRangeGrbit
```

``` csharp
[FlagsAttribute]
public enum SetIndexRangeGrbit
```

## <a name="members"></a><span data-ttu-id="f5c20-109">Membres</span><span class="sxs-lookup"><span data-stu-id="f5c20-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f5c20-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="f5c20-110">Member name</span></span></th>
<th><span data-ttu-id="f5c20-111">Description</span><span class="sxs-lookup"><span data-stu-id="f5c20-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f5c20-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="f5c20-112">None</span></span></td>
<td><span data-ttu-id="f5c20-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="f5c20-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f5c20-114">RangeInclusive</span><span class="sxs-lookup"><span data-stu-id="f5c20-114">RangeInclusive</span></span></td>
<td><span data-ttu-id="f5c20-115">Cette option indique que la limite de la plage d’index est comprise.</span><span class="sxs-lookup"><span data-stu-id="f5c20-115">This option indicates that the limit of the index range is inclusive.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f5c20-116">RangeUpperLimit</span><span class="sxs-lookup"><span data-stu-id="f5c20-116">RangeUpperLimit</span></span></td>
<td><span data-ttu-id="f5c20-117">La clé de recherche dans le curseur représente les critères de recherche pour l’entrée d’index la plus proche de la fin de l’index qui correspondra à la plage d’index.</span><span class="sxs-lookup"><span data-stu-id="f5c20-117">The search key in the cursor represents the search criteria for the index entry closest to the end of the index that will match the index range.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f5c20-118">RangeInstantDuration</span><span class="sxs-lookup"><span data-stu-id="f5c20-118">RangeInstantDuration</span></span></td>
<td><span data-ttu-id="f5c20-119">La plage d’index doit être supprimée dès qu’elle a été établie.</span><span class="sxs-lookup"><span data-stu-id="f5c20-119">The index range should be removed as soon as it has been established.</span></span> <span data-ttu-id="f5c20-120">Cela est utile pour tester l’existence d’entrées d’index qui correspondent aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="f5c20-120">This is useful for testing for the existence of index entries that match the search criteria.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f5c20-121">RangeRemove</span><span class="sxs-lookup"><span data-stu-id="f5c20-121">RangeRemove</span></span></td>
<td><span data-ttu-id="f5c20-122">Annuler et plage d’index existante.</span><span class="sxs-lookup"><span data-stu-id="f5c20-122">Cancel and existing index range.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="f5c20-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5c20-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f5c20-124">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="f5c20-124">Reference</span></span>

[<span data-ttu-id="f5c20-125">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f5c20-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
