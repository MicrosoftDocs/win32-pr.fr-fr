---
description: 'En savoir plus sur : méthode API. JetOSSnapshotFreeze'
title: API. JetOSSnapshotFreeze, méthode
TOCTitle: 'JetOSSnapshotFreeze method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotFreeze(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,System.Int32@,Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO[]@,Microsoft.Isam.Esent.Interop.SnapshotFreezeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetossnapshotfreeze(v=EXCHG.10)
ms:contentKeyID: 55100793
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotFreeze
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotFreeze
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7434cb79e90f99ab946c86a97559079352956fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210527"
---
# <a name="apijetossnapshotfreeze-method"></a><span data-ttu-id="2c380-103">API. JetOSSnapshotFreeze, méthode</span><span class="sxs-lookup"><span data-stu-id="2c380-103">Api.JetOSSnapshotFreeze method</span></span>

<span data-ttu-id="2c380-104">Démarre un instantané.</span><span class="sxs-lookup"><span data-stu-id="2c380-104">Starts a snapshot.</span></span> <span data-ttu-id="2c380-105">Pendant que l’instantané est en cours, aucune activité d’écriture sur le disque par le moteur ne peut avoir lieu.</span><span class="sxs-lookup"><span data-stu-id="2c380-105">While the snapshot is in progress, no write-to-disk activity by the engine can take place.</span></span>

<span data-ttu-id="2c380-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2c380-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2c380-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2c380-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2c380-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c380-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotFreeze ( _
    snapshot As JET_OSSNAPID, _
    <OutAttribute> ByRef numInstances As Integer, _
    <OutAttribute> ByRef instances As JET_INSTANCE_INFO(), _
    grbit As SnapshotFreezeGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim numInstances As Integer
Dim instances As JET_INSTANCE_INFO()
Dim grbit As SnapshotFreezeGrbitApi.JetOSSnapshotFreeze(snapshot, _
    numInstances, instances, grbit)
```

``` csharp
public static void JetOSSnapshotFreeze(
    JET_OSSNAPID snapshot,
    out int numInstances,
    out JET_INSTANCE_INFO[] instances,
    SnapshotFreezeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="2c380-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c380-109">Parameters</span></span>

  - <span data-ttu-id="2c380-110">instantané</span><span class="sxs-lookup"><span data-stu-id="2c380-110">snapshot</span></span>  
    <span data-ttu-id="2c380-111">Type : [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2c380-111">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="2c380-112">Session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="2c380-112">The snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="2c380-113">numInstances</span><span class="sxs-lookup"><span data-stu-id="2c380-113">numInstances</span></span>  
    <span data-ttu-id="2c380-114">Type : [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2c380-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="2c380-115">Retourne le nombre d’instances qui font partie de la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="2c380-115">Returns the number of instances that are part of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="2c380-116">instances</span><span class="sxs-lookup"><span data-stu-id="2c380-116">instances</span></span>  
    <span data-ttu-id="2c380-117">Entrer \[\]</span><span class="sxs-lookup"><span data-stu-id="2c380-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="2c380-118">Retourne des informations sur les instances qui font partie de la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="2c380-118">Returns information about the instances that are part of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="2c380-119">grbit</span><span class="sxs-lookup"><span data-stu-id="2c380-119">grbit</span></span>  
    <span data-ttu-id="2c380-120">Type : [Microsoft. ISAM. esent. Interop. SnapshotFreezeGrbit](./snapshotfreezegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="2c380-120">Type: [Microsoft.Isam.Esent.Interop.SnapshotFreezeGrbit](./snapshotfreezegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="2c380-121">Options de blocage d’instantané.</span><span class="sxs-lookup"><span data-stu-id="2c380-121">Snapshot freeze options.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c380-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c380-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2c380-123">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="2c380-123">Reference</span></span>

[<span data-ttu-id="2c380-124">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="2c380-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="2c380-125">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="2c380-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="2c380-126">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2c380-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
