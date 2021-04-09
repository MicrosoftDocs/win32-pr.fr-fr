---
description: 'En savoir plus sur : énumération MoveGrbit'
title: Énumération MoveGrbit
TOCTitle: MoveGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.MoveGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.movegrbit(v=EXCHG.10)
ms:contentKeyID: 39513771
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.MoveGrbit
- Microsoft.Isam.Esent.Interop.MoveGrbit.MoveKeyNE
- Microsoft.Isam.Esent.Interop.MoveGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.MoveGrbit
- Microsoft.Isam.Esent.Interop.MoveGrbit.None
- Microsoft.Isam.Esent.Interop.MoveGrbit.MoveKeyNE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81f047cd69bca668a5eae2b5147d8c0a137011e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034603"
---
# <a name="movegrbit-enumeration"></a><span data-ttu-id="0b5a8-103">Énumération MoveGrbit</span><span class="sxs-lookup"><span data-stu-id="0b5a8-103">MoveGrbit enumeration</span></span>

<span data-ttu-id="0b5a8-104">Options pour JetMove.</span><span class="sxs-lookup"><span data-stu-id="0b5a8-104">Options for JetMove.</span></span>

<span data-ttu-id="0b5a8-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="0b5a8-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="0b5a8-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0b5a8-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0b5a8-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0b5a8-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0b5a8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b5a8-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration MoveGrbit
'Usage
Dim instance As MoveGrbit
```

``` csharp
[FlagsAttribute]
public enum MoveGrbit
```

## <a name="members"></a><span data-ttu-id="0b5a8-109">Membres</span><span class="sxs-lookup"><span data-stu-id="0b5a8-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="0b5a8-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="0b5a8-110">Member name</span></span></th>
<th><span data-ttu-id="0b5a8-111">Description</span><span class="sxs-lookup"><span data-stu-id="0b5a8-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0b5a8-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="0b5a8-112">None</span></span></td>
<td><span data-ttu-id="0b5a8-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="0b5a8-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0b5a8-114">MoveKeyNE</span><span class="sxs-lookup"><span data-stu-id="0b5a8-114">MoveKeyNE</span></span></td>
<td><span data-ttu-id="0b5a8-115">Déplace le curseur vers l’avant ou vers l’arrière selon le nombre d’entrées d’index requises pour ignorer le nombre demandé de valeurs de clé d’index rencontrées dans l’index.</span><span class="sxs-lookup"><span data-stu-id="0b5a8-115">Moves the cursor forward or backward by the number of index entries required to skip the requested number of index key values encountered in the index.</span></span> <span data-ttu-id="0b5a8-116">Cela a pour effet de réduire les entrées d’index avec des valeurs de clé en double dans une entrée d’index unique.</span><span class="sxs-lookup"><span data-stu-id="0b5a8-116">This has the effect of collapsing index entries with duplicate key values into a single index entry.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="0b5a8-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b5a8-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0b5a8-118">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="0b5a8-118">Reference</span></span>

[<span data-ttu-id="0b5a8-119">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0b5a8-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
