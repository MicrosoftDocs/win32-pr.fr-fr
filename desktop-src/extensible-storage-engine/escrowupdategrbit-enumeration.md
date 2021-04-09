---
description: 'En savoir plus sur : énumération EscrowUpdateGrbit'
title: Énumération EscrowUpdateGrbit
TOCTitle: EscrowUpdateGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.escrowupdategrbit(v=EXCHG.10)
ms:contentKeyID: 39514160
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.None
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.NoRollback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.None
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.NoRollback
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d301ef801a5685057a9e33beb794f3b6cf13e646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953031"
---
# <a name="escrowupdategrbit-enumeration"></a><span data-ttu-id="907b6-103">Énumération EscrowUpdateGrbit</span><span class="sxs-lookup"><span data-stu-id="907b6-103">EscrowUpdateGrbit enumeration</span></span>

<span data-ttu-id="907b6-104">Options pour JetEscrowUpdate.</span><span class="sxs-lookup"><span data-stu-id="907b6-104">Options for JetEscrowUpdate.</span></span>

<span data-ttu-id="907b6-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="907b6-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="907b6-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="907b6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="907b6-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="907b6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="907b6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="907b6-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EscrowUpdateGrbit
'Usage
Dim instance As EscrowUpdateGrbit
```

``` csharp
[FlagsAttribute]
public enum EscrowUpdateGrbit
```

## <a name="members"></a><span data-ttu-id="907b6-109">Membres</span><span class="sxs-lookup"><span data-stu-id="907b6-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="907b6-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="907b6-110">Member name</span></span></th>
<th><span data-ttu-id="907b6-111">Description</span><span class="sxs-lookup"><span data-stu-id="907b6-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="907b6-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="907b6-112">None</span></span></td>
<td><span data-ttu-id="907b6-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="907b6-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="907b6-114">Norollback</span><span class="sxs-lookup"><span data-stu-id="907b6-114">NoRollback</span></span></td>
<td><span data-ttu-id="907b6-115">Cette mise à jour ne sera pas annulée même si la session effectuant la mise à jour du tiers de confiance a été restaurée.</span><span class="sxs-lookup"><span data-stu-id="907b6-115">Even if the session performing the escrow update has its transaction rollback this update will not be undone.</span></span> <span data-ttu-id="907b6-116">Étant donné que les enregistrements du journal ne peuvent pas être vidés sur le disque, les mises à jour récentes des tiers de confiance effectuées avec cet indicateur peuvent être perdues en cas de panne.</span><span class="sxs-lookup"><span data-stu-id="907b6-116">As the log records may not be flushed to disk, recent escrow updates done with this flag may be lost if there is a crash.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="907b6-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="907b6-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="907b6-118">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="907b6-118">Reference</span></span>

[<span data-ttu-id="907b6-119">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="907b6-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
