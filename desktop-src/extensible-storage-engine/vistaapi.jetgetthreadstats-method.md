---
description: 'En savoir plus sur : méthode VistaApi. JetGetThreadStats'
title: Méthode VistaApi. JetGetThreadStats (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'JetGetThreadStats method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetthreadstats(v=EXCHG.10)
ms:contentKeyID: 55104192
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 92572fd538f0c6c2643e7b40a07ac168ae6980d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524966"
---
# <a name="vistaapijetgetthreadstats-method"></a><span data-ttu-id="d1cdb-103">Méthode VistaApi. JetGetThreadStats</span><span class="sxs-lookup"><span data-stu-id="d1cdb-103">VistaApi.JetGetThreadStats method</span></span>

<span data-ttu-id="d1cdb-104">Récupère les informations de performance du moteur de base de données pour le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="d1cdb-104">Retrieves performance information from the database engine for the current thread.</span></span> <span data-ttu-id="d1cdb-105">Plusieurs appels peuvent être utilisés pour collecter des statistiques qui reflètent l’activité du moteur de base de données sur ce thread entre ces appels.</span><span class="sxs-lookup"><span data-stu-id="d1cdb-105">Multiple calls can be used to collect statistics that reflect the activity of the database engine on this thread between those calls.</span></span>

<span data-ttu-id="d1cdb-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d1cdb-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="d1cdb-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d1cdb-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d1cdb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1cdb-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetThreadStats ( _
    <OutAttribute> ByRef threadstats As JET_THREADSTATS _
)
'Usage
Dim threadstats As JET_THREADSTATSVistaApi.JetGetThreadStats(threadstats)
```

``` csharp
public static void JetGetThreadStats(
    out JET_THREADSTATS threadstats
)
```

#### <a name="parameters"></a><span data-ttu-id="d1cdb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1cdb-109">Parameters</span></span>

  - <span data-ttu-id="d1cdb-110">threadstats</span><span class="sxs-lookup"><span data-stu-id="d1cdb-110">threadstats</span></span>  
    <span data-ttu-id="d1cdb-111">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="d1cdb-111">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="d1cdb-112">Retourne les données de statistiques de thread.</span><span class="sxs-lookup"><span data-stu-id="d1cdb-112">Returns the thread statistics data.</span></span>

## <a name="see-also"></a><span data-ttu-id="d1cdb-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1cdb-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d1cdb-114">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="d1cdb-114">Reference</span></span>

[<span data-ttu-id="d1cdb-115">VistaApi, classe</span><span class="sxs-lookup"><span data-stu-id="d1cdb-115">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="d1cdb-116">Membres VistaApi</span><span class="sxs-lookup"><span data-stu-id="d1cdb-116">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="d1cdb-117">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="d1cdb-117">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
