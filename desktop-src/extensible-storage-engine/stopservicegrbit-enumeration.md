---
description: 'En savoir plus sur : énumération StopServiceGrbit'
title: Énumération StopServiceGrbit (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: StopServiceGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.stopservicegrbit(v=EXCHG.10)
ms:contentKeyID: 55104330
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 54e54576dfb1023ec4e3bc55ddd198a77f0ddf25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524898"
---
# <a name="stopservicegrbit-enumeration"></a><span data-ttu-id="07073-103">Énumération StopServiceGrbit</span><span class="sxs-lookup"><span data-stu-id="07073-103">StopServiceGrbit enumeration</span></span>

<span data-ttu-id="07073-104">Options pour [JetStopServiceInstance2 (JET_INSTANCE, StopServiceGrbit)](./windows8api.jetstopserviceinstance2-method.md).</span><span class="sxs-lookup"><span data-stu-id="07073-104">Options for [JetStopServiceInstance2(JET_INSTANCE, StopServiceGrbit)](./windows8api.jetstopserviceinstance2-method.md).</span></span>

<span data-ttu-id="07073-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="07073-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="07073-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="07073-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="07073-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="07073-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="07073-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07073-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration StopServiceGrbit
'Usage
Dim instance As StopServiceGrbit
```

``` csharp
[FlagsAttribute]
public enum StopServiceGrbit
```

## <a name="members"></a><span data-ttu-id="07073-109">Membres</span><span class="sxs-lookup"><span data-stu-id="07073-109">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="07073-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="07073-110">Member name</span></span></th>
<th><span data-ttu-id="07073-111">Description</span><span class="sxs-lookup"><span data-stu-id="07073-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="07073-112">Tous</span><span class="sxs-lookup"><span data-stu-id="07073-112">All</span></span></td>
<td><span data-ttu-id="07073-113">Arrête tous les services ESE pour l’instance spécifiée.</span><span class="sxs-lookup"><span data-stu-id="07073-113">Stops all ESE services for the specified instance.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="07073-114">BackgroundUserTasks</span><span class="sxs-lookup"><span data-stu-id="07073-114">BackgroundUserTasks</span></span></td>
<td><span data-ttu-id="07073-115">Arrête les tâches de maintenance en arrière-plan spécifiques au client redémarrables (arbre B + arborescence).</span><span class="sxs-lookup"><span data-stu-id="07073-115">Stops restartable client specificed background maintenance tasks (B+ Tree Defrag).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="07073-116">QuiesceCaches</span><span class="sxs-lookup"><span data-stu-id="07073-116">QuiesceCaches</span></span></td>
<td><span data-ttu-id="07073-117">Quiesces tous les caches modifiés sur le disque.</span><span class="sxs-lookup"><span data-stu-id="07073-117">Quiesces all dirty caches to disk.</span></span> <span data-ttu-id="07073-118">Asynchrone.</span><span class="sxs-lookup"><span data-stu-id="07073-118">Asynchronous.</span></span> <span data-ttu-id="07073-119">La suspension est annulée si le bit de reprise est appelé par la suite.</span><span class="sxs-lookup"><span data-stu-id="07073-119">Quiescing is cancelled if the Resume bit is called subsequently.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="07073-120">Reprendre</span><span class="sxs-lookup"><span data-stu-id="07073-120">Resume</span></span></td>
<td><span data-ttu-id="07073-121">Reprend les opérations StopService précédemment émises, c.-à-d. &quot; redémarre le service &quot; .</span><span class="sxs-lookup"><span data-stu-id="07073-121">Resumes previously issued StopService operations, i.e. &quot;restarts service&quot;.</span></span> <span data-ttu-id="07073-122">Peut être combiné avec les grbits ci-dessus pour reprendre des services spécifiques, ou avec 0x0 pour reprendre tous les services arrêtés précédemment.</span><span class="sxs-lookup"><span data-stu-id="07073-122">Can be combined with above grbits to Resume specific services, or with 0x0 Resumes all previous stopped services.</span></span>
<p><span data-ttu-id="07073-123">AVERTISSEMENT : ce bit ne peut être utilisé que pour reprendre JET_bitStopServiceBackground et JET_bitStopServiceQuiesceCaches, si vous avez effectué une JET_bitStopServiceAll ou une JET_bitStopServiceAPI, toute tentative d’utilisation de JET_bitStopServiceResume échouera.</span><span class="sxs-lookup"><span data-stu-id="07073-123">Warning: This bit can only be used to resume JET_bitStopServiceBackground and JET_bitStopServiceQuiesceCaches, if you did a JET_bitStopServiceAll or JET_bitStopServiceAPI, attempting to use JET_bitStopServiceResume will fail.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="07073-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07073-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="07073-125">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="07073-125">Reference</span></span>

[<span data-ttu-id="07073-126">Espace de noms Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="07073-126">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
