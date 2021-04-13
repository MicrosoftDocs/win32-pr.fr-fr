---
description: 'En savoir plus sur : méthode API. JetComputeStats'
title: API. JetComputeStats, méthode
TOCTitle: 'JetComputeStats method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetComputeStats(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcomputestats(v=EXCHG.10)
ms:contentKeyID: 55100667
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetComputeStats
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetComputeStats
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b102aca5971656232fae02684aeab30322d208b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201198"
---
# <a name="apijetcomputestats-method"></a><span data-ttu-id="3eb2e-103">API. JetComputeStats, méthode</span><span class="sxs-lookup"><span data-stu-id="3eb2e-103">Api.JetComputeStats method</span></span>

<span data-ttu-id="3eb2e-104">Parcourt chaque index d’une table pour calculer exactement le nombre d’entrées dans un index et le nombre de clés distinctes dans un index.</span><span class="sxs-lookup"><span data-stu-id="3eb2e-104">Walks each index of a table to exactly compute the number of entries in an index, and the number of distinct keys in an index.</span></span> <span data-ttu-id="3eb2e-105">Ces informations, ainsi que le nombre de pages de base de données allouées pour un index et l’heure actuelle du calcul, sont stockées dans les métadonnées d’index dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="3eb2e-105">This information, together with the number of database pages allocated for an index and the current time of the computation is stored in index metadata in the database.</span></span> <span data-ttu-id="3eb2e-106">Ces données peuvent être récupérées par la suite avec les opérations d’informations.</span><span class="sxs-lookup"><span data-stu-id="3eb2e-106">This data can be subsequently retrieved with information operations.</span></span>

<span data-ttu-id="3eb2e-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3eb2e-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3eb2e-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3eb2e-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3eb2e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3eb2e-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetComputeStats ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetComputeStats(sesid, tableid)
```

``` csharp
public static void JetComputeStats(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="3eb2e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3eb2e-110">Parameters</span></span>

  - <span data-ttu-id="3eb2e-111">sesid</span><span class="sxs-lookup"><span data-stu-id="3eb2e-111">sesid</span></span>  
    <span data-ttu-id="3eb2e-112">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3eb2e-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3eb2e-113">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="3eb2e-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3eb2e-114">TableID</span><span class="sxs-lookup"><span data-stu-id="3eb2e-114">tableid</span></span>  
    <span data-ttu-id="3eb2e-115">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3eb2e-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="3eb2e-116">Table sur laquelle les statistiques seront calculées.</span><span class="sxs-lookup"><span data-stu-id="3eb2e-116">The table that the statistics will be computed on.</span></span>

## <a name="see-also"></a><span data-ttu-id="3eb2e-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3eb2e-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3eb2e-118">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="3eb2e-118">Reference</span></span>

[<span data-ttu-id="3eb2e-119">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="3eb2e-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3eb2e-120">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="3eb2e-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3eb2e-121">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3eb2e-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
