---
description: 'En savoir plus sur : énumération JET_SNP'
title: Énumération JET_SNP
TOCTitle: JET_SNP enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SNP
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_snp(v=EXCHG.10)
ms:contentKeyID: 39511218
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SNP.Backup
- Microsoft.Isam.Esent.Interop.JET_SNP.Repair
- Microsoft.Isam.Esent.Interop.JET_SNP.Compact
- Microsoft.Isam.Esent.Interop.JET_SNP.Scrub
- Microsoft.Isam.Esent.Interop.JET_SNP
- Microsoft.Isam.Esent.Interop.JET_SNP.Restore
- Microsoft.Isam.Esent.Interop.JET_SNP.UpgradeRecordFormat
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SNP.Scrub
- Microsoft.Isam.Esent.Interop.JET_SNP
- Microsoft.Isam.Esent.Interop.JET_SNP.Backup
- Microsoft.Isam.Esent.Interop.JET_SNP.Restore
- Microsoft.Isam.Esent.Interop.JET_SNP.UpgradeRecordFormat
- Microsoft.Isam.Esent.Interop.JET_SNP.Compact
- Microsoft.Isam.Esent.Interop.JET_SNP.Repair
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10061d0c00d90aa5ca4e0778cba046d2e6f62f4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519248"
---
# <a name="jet_snp-enumeration"></a><span data-ttu-id="7b84d-103">Énumération JET_SNP</span><span class="sxs-lookup"><span data-stu-id="7b84d-103">JET_SNP enumeration</span></span>

<span data-ttu-id="7b84d-104">Type d’opération pour lequel la progression est signalée.</span><span class="sxs-lookup"><span data-stu-id="7b84d-104">The type of operation that progress is being reported for.</span></span>

<span data-ttu-id="7b84d-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7b84d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7b84d-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7b84d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7b84d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b84d-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_SNP
'Usage
Dim instance As JET_SNP
```

``` csharp
public enum JET_SNP
```

## <a name="members"></a><span data-ttu-id="7b84d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7b84d-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="7b84d-109">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="7b84d-109">Member name</span></span></th>
<th><span data-ttu-id="7b84d-110">Description</span><span class="sxs-lookup"><span data-stu-id="7b84d-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7b84d-111">Réparation</span><span class="sxs-lookup"><span data-stu-id="7b84d-111">Repair</span></span></td>
<td><span data-ttu-id="7b84d-112">Le rappel est destiné à une option de réparation.</span><span class="sxs-lookup"><span data-stu-id="7b84d-112">Callback is for a repair option.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="7b84d-113">Compact</span><span class="sxs-lookup"><span data-stu-id="7b84d-113">Compact</span></span></td>
<td><span data-ttu-id="7b84d-114">Le rappel est destiné à la défragmentation de la base de données.</span><span class="sxs-lookup"><span data-stu-id="7b84d-114">Callback is for database defragmentation.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7b84d-115">Restaurer</span><span class="sxs-lookup"><span data-stu-id="7b84d-115">Restore</span></span></td>
<td><span data-ttu-id="7b84d-116">Le rappel concerne les options de restauration.</span><span class="sxs-lookup"><span data-stu-id="7b84d-116">Callback is for a restore options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="7b84d-117">Sauvegarde</span><span class="sxs-lookup"><span data-stu-id="7b84d-117">Backup</span></span></td>
<td><span data-ttu-id="7b84d-118">Le rappel est destiné aux options de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="7b84d-118">Callback is for a backup options.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7b84d-119">Balay</span><span class="sxs-lookup"><span data-stu-id="7b84d-119">Scrub</span></span></td>
<td><span data-ttu-id="7b84d-120">Le rappel est destiné à la mise en zéro de la base de données.</span><span class="sxs-lookup"><span data-stu-id="7b84d-120">Callback is for database zeroing.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="7b84d-121">UpgradeRecordFormat</span><span class="sxs-lookup"><span data-stu-id="7b84d-121">UpgradeRecordFormat</span></span></td>
<td><span data-ttu-id="7b84d-122">Le rappel est destiné au processus de mise à niveau du format d’enregistrement de toutes les pages de la base de données.</span><span class="sxs-lookup"><span data-stu-id="7b84d-122">Callback is for the process of upgrading the record format of all database pages.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="7b84d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b84d-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7b84d-124">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="7b84d-124">Reference</span></span>

[<span data-ttu-id="7b84d-125">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7b84d-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
