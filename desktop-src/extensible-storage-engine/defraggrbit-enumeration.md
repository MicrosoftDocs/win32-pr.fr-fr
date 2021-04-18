---
description: 'En savoir plus sur : énumération DefragGrbit'
title: Énumération DefragGrbit
TOCTitle: DefragGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DefragGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.defraggrbit(v=EXCHG.10)
ms:contentKeyID: 39516122
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DefragGrbit
- Microsoft.Isam.Esent.Interop.DefragGrbit.AvailSpaceTreesOnly
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStart
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStop
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DefragGrbit
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStart
- Microsoft.Isam.Esent.Interop.DefragGrbit.AvailSpaceTreesOnly
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStop
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5da047fbdad20ac40d780dc5b0bba9e986e7672
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536220"
---
# <a name="defraggrbit-enumeration"></a><span data-ttu-id="69183-103">Énumération DefragGrbit</span><span class="sxs-lookup"><span data-stu-id="69183-103">DefragGrbit enumeration</span></span>

<span data-ttu-id="69183-104">Options pour [JetDefragment (JET_SESID, JET_DBID, String, Int32, Int32, DefragGrbit)](./api.jetdefragment-method.md).</span><span class="sxs-lookup"><span data-stu-id="69183-104">Options for [JetDefragment(JET_SESID, JET_DBID, String, Int32, Int32, DefragGrbit)](./api.jetdefragment-method.md).</span></span>

<span data-ttu-id="69183-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="69183-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="69183-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="69183-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="69183-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="69183-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="69183-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69183-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DefragGrbit
'Usage
Dim instance As DefragGrbit
```

``` csharp
[FlagsAttribute]
public enum DefragGrbit
```

## <a name="members"></a><span data-ttu-id="69183-109">Membres</span><span class="sxs-lookup"><span data-stu-id="69183-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="69183-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="69183-110">Member name</span></span></th>
<th><span data-ttu-id="69183-111">Description</span><span class="sxs-lookup"><span data-stu-id="69183-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="69183-112">AvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="69183-112">AvailSpaceTreesOnly</span></span></td>
<td><span data-ttu-id="69183-113">Défragmente la partie d’espace disponible de l’allocation de l’espace de la base de données ESE.</span><span class="sxs-lookup"><span data-stu-id="69183-113">Defragments the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="69183-114">L’espace de la base de données est divisé en deux types, l’espace détenu et l’espace disponible.</span><span class="sxs-lookup"><span data-stu-id="69183-114">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="69183-115">L’espace détenu est alloué à une table ou à un index, alors que l’espace disponible est prêt à être utilisé dans la table ou l’index, respectivement.</span><span class="sxs-lookup"><span data-stu-id="69183-115">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="69183-116">L’espace disponible est bien plus dynamique dans le comportement et nécessite une défragmentation en ligne plus qu’un espace détenu ou des données de table ou d’index.</span><span class="sxs-lookup"><span data-stu-id="69183-116">Available space is much more dynamic in behavior and requires on-line defragmentation more so than owned space or table or index data.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="69183-117">BatchStart</span><span class="sxs-lookup"><span data-stu-id="69183-117">BatchStart</span></span></td>
<td><span data-ttu-id="69183-118">Démarre une nouvelle tâche de défragmentation.</span><span class="sxs-lookup"><span data-stu-id="69183-118">Starts a new defragmentation task.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="69183-119">BatchStop</span><span class="sxs-lookup"><span data-stu-id="69183-119">BatchStop</span></span></td>
<td><span data-ttu-id="69183-120">Arrête une tâche de défragmentation.</span><span class="sxs-lookup"><span data-stu-id="69183-120">Stops a defragmentation task.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="69183-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69183-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="69183-122">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="69183-122">Reference</span></span>

[<span data-ttu-id="69183-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="69183-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
