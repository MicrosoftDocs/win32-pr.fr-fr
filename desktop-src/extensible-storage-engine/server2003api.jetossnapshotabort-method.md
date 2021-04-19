---
description: 'En savoir plus sur : méthode Server2003Api. JetOSSnapshotAbort'
title: Méthode Server2003Api. JetOSSnapshotAbort (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: 'JetOSSnapshotAbort method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Server2003.SnapshotAbortGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003api.jetossnapshotabort(v=EXCHG.10)
ms:contentKeyID: 55104209
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 44ee61a7c6cff7fe90a77fdaced786532457c132
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545803"
---
# <a name="server2003apijetossnapshotabort-method"></a><span data-ttu-id="622ba-103">Méthode Server2003Api. JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="622ba-103">Server2003Api.JetOSSnapshotAbort method</span></span>

<span data-ttu-id="622ba-104">Notifie le moteur qu’il peut reprendre des opérations d’e/s normales après la fin d’une période de blocage avec un instantané ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="622ba-104">Notifies the engine that it can resume normal IO operations after a freeze period ended with a failed snapshot.</span></span>

<span data-ttu-id="622ba-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="622ba-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="622ba-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="622ba-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="622ba-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="622ba-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotAbort ( _
    snapid As JET_OSSNAPID, _
    grbit As SnapshotAbortGrbit _
)
'Usage
Dim snapid As JET_OSSNAPID
Dim grbit As SnapshotAbortGrbitServer2003Api.JetOSSnapshotAbort(snapid, _
    grbit)
```

``` csharp
public static void JetOSSnapshotAbort(
    JET_OSSNAPID snapid,
    SnapshotAbortGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="622ba-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="622ba-108">Parameters</span></span>

  - <span data-ttu-id="622ba-109">snapid</span><span class="sxs-lookup"><span data-stu-id="622ba-109">snapid</span></span>  
    <span data-ttu-id="622ba-110">Type : [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="622ba-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="622ba-111">Identificateur de la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="622ba-111">Identifier of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="622ba-112">grbit</span><span class="sxs-lookup"><span data-stu-id="622ba-112">grbit</span></span>  
    <span data-ttu-id="622ba-113">Type : [Microsoft. ISAM. esent. Interop. Server2003. SnapshotAbortGrbit](./snapshotabortgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="622ba-113">Type: [Microsoft.Isam.Esent.Interop.Server2003.SnapshotAbortGrbit](./snapshotabortgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="622ba-114">Options pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="622ba-114">Options for this call.</span></span>

## <a name="see-also"></a><span data-ttu-id="622ba-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="622ba-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="622ba-116">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="622ba-116">Reference</span></span>

[<span data-ttu-id="622ba-117">Server2003Api, classe</span><span class="sxs-lookup"><span data-stu-id="622ba-117">Server2003Api class</span></span>](./server2003api-class.md)

[<span data-ttu-id="622ba-118">Membres Server2003Api</span><span class="sxs-lookup"><span data-stu-id="622ba-118">Server2003Api members</span></span>](./server2003api-members.md)

[<span data-ttu-id="622ba-119">Espace de noms Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="622ba-119">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
