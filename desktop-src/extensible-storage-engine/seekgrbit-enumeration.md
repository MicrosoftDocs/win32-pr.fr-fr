---
description: 'En savoir plus sur : énumération SeekGrbit'
title: Énumération SeekGrbit
TOCTitle: SeekGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SeekGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.seekgrbit(v=EXCHG.10)
ms:contentKeyID: 39515862
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e59072055710676f5f7647130f42ad5acf50527
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533920"
---
# <a name="seekgrbit-enumeration"></a><span data-ttu-id="b7d19-103">Énumération SeekGrbit</span><span class="sxs-lookup"><span data-stu-id="b7d19-103">SeekGrbit enumeration</span></span>

<span data-ttu-id="b7d19-104">Options pour JetSeek.</span><span class="sxs-lookup"><span data-stu-id="b7d19-104">Options for JetSeek.</span></span>

<span data-ttu-id="b7d19-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="b7d19-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="b7d19-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b7d19-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b7d19-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b7d19-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b7d19-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7d19-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SeekGrbit
'Usage
Dim instance As SeekGrbit
```

``` csharp
[FlagsAttribute]
public enum SeekGrbit
```

## <a name="members"></a><span data-ttu-id="b7d19-109">Membres</span><span class="sxs-lookup"><span data-stu-id="b7d19-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="b7d19-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="b7d19-110">Member name</span></span></th>
<th><span data-ttu-id="b7d19-111">Description</span><span class="sxs-lookup"><span data-stu-id="b7d19-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b7d19-112">SeekEQ</span><span class="sxs-lookup"><span data-stu-id="b7d19-112">SeekEQ</span></span></td>
<td><span data-ttu-id="b7d19-113">Le curseur est positionné à l’entrée d’index la plus proche du début de l’index qui correspond exactement à la clé de recherche.</span><span class="sxs-lookup"><span data-stu-id="b7d19-113">The cursor will be positioned at the index entry closest to the start of the index that exactly matches the search key.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="b7d19-114">SeekLT</span><span class="sxs-lookup"><span data-stu-id="b7d19-114">SeekLT</span></span></td>
<td><span data-ttu-id="b7d19-115">Le curseur est positionné à l’entrée d’index la plus proche de la fin de l’index qui est inférieure à une entrée d’index qui correspond exactement aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="b7d19-115">The cursor will be positioned at the index entry closest to the end of the index that is less than an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b7d19-116">SeekLE</span><span class="sxs-lookup"><span data-stu-id="b7d19-116">SeekLE</span></span></td>
<td><span data-ttu-id="b7d19-117">Le curseur est positionné à l’entrée d’index la plus proche de la fin de l’index qui est inférieure ou égale à une entrée d’index qui correspond exactement aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="b7d19-117">The cursor will be positioned at the index entry closest to the end of the index that is less than or equal to an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="b7d19-118">SeekGE</span><span class="sxs-lookup"><span data-stu-id="b7d19-118">SeekGE</span></span></td>
<td><span data-ttu-id="b7d19-119">Le curseur est positionné à l’entrée d’index la plus proche du début de l’index qui est supérieure ou égale à une entrée d’index qui correspond exactement aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="b7d19-119">The cursor will be positioned at the index entry closest to the start of the index that is greater than or equal to an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b7d19-120">SeekGT</span><span class="sxs-lookup"><span data-stu-id="b7d19-120">SeekGT</span></span></td>
<td><span data-ttu-id="b7d19-121">Le curseur est positionné à l’entrée d’index la plus proche du début de l’index qui est supérieure à une entrée d’index qui correspond exactement aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="b7d19-121">The cursor will be positioned at the index entry closest to the start of the index that is greater than an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="b7d19-122">SetIndexRange</span><span class="sxs-lookup"><span data-stu-id="b7d19-122">SetIndexRange</span></span></td>
<td><span data-ttu-id="b7d19-123">Une plage d’index sera automatiquement configurée pour toutes les clés qui correspondent exactement à la clé de recherche.</span><span class="sxs-lookup"><span data-stu-id="b7d19-123">An index range will automatically be setup for all keys that exactly match the search key.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="b7d19-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7d19-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b7d19-125">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="b7d19-125">Reference</span></span>

[<span data-ttu-id="b7d19-126">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b7d19-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
