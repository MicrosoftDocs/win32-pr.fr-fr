---
description: 'En savoir plus sur : énumération IdleGrbit'
title: Énumération IdleGrbit
TOCTitle: IdleGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.IdleGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.idlegrbit(v=EXCHG.10)
ms:contentKeyID: 39514282
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IdleGrbit
- Microsoft.Isam.Esent.Interop.IdleGrbit.Compact
- Microsoft.Isam.Esent.Interop.IdleGrbit.FlushBuffers
- Microsoft.Isam.Esent.Interop.IdleGrbit.GetStatus
- Microsoft.Isam.Esent.Interop.IdleGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IdleGrbit.Compact
- Microsoft.Isam.Esent.Interop.IdleGrbit.FlushBuffers
- Microsoft.Isam.Esent.Interop.IdleGrbit
- Microsoft.Isam.Esent.Interop.IdleGrbit.None
- Microsoft.Isam.Esent.Interop.IdleGrbit.GetStatus
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f02937241066762b6d711d89e62e67cfed9f41f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201894"
---
# <a name="idlegrbit-enumeration"></a><span data-ttu-id="aeee0-103">Énumération IdleGrbit</span><span class="sxs-lookup"><span data-stu-id="aeee0-103">IdleGrbit enumeration</span></span>

<span data-ttu-id="aeee0-104">Options pour [JetIdle (JET_SESID, IdleGrbit)](./api.jetidle-method.md).</span><span class="sxs-lookup"><span data-stu-id="aeee0-104">Options for [JetIdle(JET_SESID, IdleGrbit)](./api.jetidle-method.md).</span></span>

<span data-ttu-id="aeee0-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="aeee0-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="aeee0-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aeee0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="aeee0-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="aeee0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="aeee0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aeee0-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration IdleGrbit
'Usage
Dim instance As IdleGrbit
```

``` csharp
[FlagsAttribute]
public enum IdleGrbit
```

## <a name="members"></a><span data-ttu-id="aeee0-109">Membres</span><span class="sxs-lookup"><span data-stu-id="aeee0-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="aeee0-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="aeee0-110">Member name</span></span></th>
<th><span data-ttu-id="aeee0-111">Description</span><span class="sxs-lookup"><span data-stu-id="aeee0-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="aeee0-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="aeee0-112">None</span></span></td>
<td><span data-ttu-id="aeee0-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="aeee0-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="aeee0-114">FlushBuffers</span><span class="sxs-lookup"><span data-stu-id="aeee0-114">FlushBuffers</span></span></td>
<td><span data-ttu-id="aeee0-115">Déclenche le nettoyage de la Banque des versions.</span><span class="sxs-lookup"><span data-stu-id="aeee0-115">Triggers cleanup of the version store.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="aeee0-116">Compact</span><span class="sxs-lookup"><span data-stu-id="aeee0-116">Compact</span></span></td>
<td><span data-ttu-id="aeee0-117">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="aeee0-117">Reserved for future use.</span></span> <span data-ttu-id="aeee0-118">Si cet indicateur est spécifié, l’API retourne <a href="hh564840(v=exchg.10).md">InvalidGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="aeee0-118">If this flag is specified, the API will return <a href="hh564840(v=exchg.10).md">InvalidGrbit</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="aeee0-119">GetStatus</span><span class="sxs-lookup"><span data-stu-id="aeee0-119">GetStatus</span></span></td>
<td><span data-ttu-id="aeee0-120">Retourne <a href="hh557250(v=exchg.10).md">IdleFull</a> si la Banque des versions est supérieure à la moitié complète.</span><span class="sxs-lookup"><span data-stu-id="aeee0-120">Returns <a href="hh557250(v=exchg.10).md">IdleFull</a> if version store is more than half full.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="aeee0-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aeee0-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="aeee0-122">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="aeee0-122">Reference</span></span>

[<span data-ttu-id="aeee0-123">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="aeee0-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
