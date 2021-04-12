---
description: 'En savoir plus sur : énumération CrashDumpGrbit'
title: Énumération CrashDumpGrbit (Microsoft. ISAM. esent. Interop. d’un)
TOCTitle: CrashDumpGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.crashdumpgrbit(v=EXCHG.10)
ms:contentKeyID: 39515535
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCachedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMinimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Maximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCorruptedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMaximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeDirtyPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Minimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeDirtyPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMaximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMinimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCachedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCorruptedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Minimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Maximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3108190143115b1e6be5b7e0981d49c4bd9d4afa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318673"
---
# <a name="crashdumpgrbit-enumeration"></a><span data-ttu-id="f7439-103">Énumération CrashDumpGrbit</span><span class="sxs-lookup"><span data-stu-id="f7439-103">CrashDumpGrbit enumeration</span></span>

<span data-ttu-id="f7439-104">Options pour JetConfigureProcessForCrashDump.</span><span class="sxs-lookup"><span data-stu-id="f7439-104">Options for JetConfigureProcessForCrashDump.</span></span>

<span data-ttu-id="f7439-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="f7439-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="f7439-106">**Espace de noms :**[Microsoft. ISAM. esent. Interop.](./microsoft.isam.esent.interop.windows7-namespace.md) une  </span><span class="sxs-lookup"><span data-stu-id="f7439-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)</span></span>  
<span data-ttu-id="f7439-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f7439-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f7439-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7439-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CrashDumpGrbit
'Usage
Dim instance As CrashDumpGrbit
```

``` csharp
[FlagsAttribute]
public enum CrashDumpGrbit
```

## <a name="members"></a><span data-ttu-id="f7439-109">Membres</span><span class="sxs-lookup"><span data-stu-id="f7439-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f7439-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="f7439-110">Member name</span></span></th>
<th><span data-ttu-id="f7439-111">Description</span><span class="sxs-lookup"><span data-stu-id="f7439-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f7439-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="f7439-112">None</span></span></td>
<td><span data-ttu-id="f7439-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="f7439-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f7439-114">Minimum</span><span class="sxs-lookup"><span data-stu-id="f7439-114">Minimum</span></span></td>
<td><span data-ttu-id="f7439-115">Le vidage minimal comprend CacheMinimum.</span><span class="sxs-lookup"><span data-stu-id="f7439-115">Dump minimum includes CacheMinimum.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f7439-116">Maximale</span><span class="sxs-lookup"><span data-stu-id="f7439-116">Maximum</span></span></td>
<td><span data-ttu-id="f7439-117">Le nombre maximal de dumps comprend CacheMaximum.</span><span class="sxs-lookup"><span data-stu-id="f7439-117">Dump maximum includes CacheMaximum.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f7439-118">CacheMinimum</span><span class="sxs-lookup"><span data-stu-id="f7439-118">CacheMinimum</span></span></td>
<td><span data-ttu-id="f7439-119">CacheMinimum comprend les pages verrouillées.</span><span class="sxs-lookup"><span data-stu-id="f7439-119">CacheMinimum includes pages that are latched.</span></span> <span data-ttu-id="f7439-120">CacheMinimum comprend les pages utilisées pour la mémoire.</span><span class="sxs-lookup"><span data-stu-id="f7439-120">CacheMinimum includes pages that are used for memory.</span></span> <span data-ttu-id="f7439-121">CacheMinimum comprend des pages qui sont marquées avec des erreurs.</span><span class="sxs-lookup"><span data-stu-id="f7439-121">CacheMinimum includes pages that are flagged with errors.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f7439-122">CacheMaximum</span><span class="sxs-lookup"><span data-stu-id="f7439-122">CacheMaximum</span></span></td>
<td><span data-ttu-id="f7439-123">Le cache maximal comprend le cache minimal.</span><span class="sxs-lookup"><span data-stu-id="f7439-123">Cache maximum includes cache minimum.</span></span> <span data-ttu-id="f7439-124">Le cache maximal comprend la totalité de l’image du cache.</span><span class="sxs-lookup"><span data-stu-id="f7439-124">Cache maximum includes the entire cache image.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f7439-125">CacheIncludeDirtyPages</span><span class="sxs-lookup"><span data-stu-id="f7439-125">CacheIncludeDirtyPages</span></span></td>
<td><span data-ttu-id="f7439-126">Le vidage comprend des pages qui sont modifiées.</span><span class="sxs-lookup"><span data-stu-id="f7439-126">Dump includes pages that are modified.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="f7439-127">CacheIncludeCachedPages</span><span class="sxs-lookup"><span data-stu-id="f7439-127">CacheIncludeCachedPages</span></span></td>
<td><span data-ttu-id="f7439-128">Le vidage comprend des pages qui contiennent des données valides.</span><span class="sxs-lookup"><span data-stu-id="f7439-128">Dump includes pages that contain valid data.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="f7439-129">CacheIncludeCorruptedPages</span><span class="sxs-lookup"><span data-stu-id="f7439-129">CacheIncludeCorruptedPages</span></span></td>
<td><span data-ttu-id="f7439-130">Le vidage comprend des pages endommagées (coûteuses à calculer).</span><span class="sxs-lookup"><span data-stu-id="f7439-130">Dump includes pages that are corrupted (expensive to compute).</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="f7439-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7439-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f7439-132">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="f7439-132">Reference</span></span>

[<span data-ttu-id="f7439-133">Espace de noms Microsoft. ISAM. esent. Interop. les</span><span class="sxs-lookup"><span data-stu-id="f7439-133">Microsoft.Isam.Esent.Interop.Windows7 namespace</span></span>](./microsoft.isam.esent.interop.windows7-namespace.md)
