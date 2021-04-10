---
description: 'En savoir plus sur : méthode VistaApi. JetOSSnapshotPrepareInstance'
title: Méthode VistaApi. JetOSSnapshotPrepareInstance (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'JetOSSnapshotPrepareInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotPrepareInstance(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Vista.SnapshotPrepareInstanceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshotprepareinstance(v=EXCHG.10)
ms:contentKeyID: 55104304
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotPrepareInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotPrepareInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46151e2b11c669ac9635ce5974757999a8636b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115639"
---
# <a name="vistaapijetossnapshotprepareinstance-method"></a><span data-ttu-id="a8dd7-103">Méthode VistaApi. JetOSSnapshotPrepareInstance</span><span class="sxs-lookup"><span data-stu-id="a8dd7-103">VistaApi.JetOSSnapshotPrepareInstance method</span></span>

<span data-ttu-id="a8dd7-104">Sélectionne une instance spécifique pour faire partie de la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="a8dd7-104">Selects a specific instance to be part of the snapshot session.</span></span>

<span data-ttu-id="a8dd7-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a8dd7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="a8dd7-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a8dd7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a8dd7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8dd7-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotPrepareInstance ( _
    snapshot As JET_OSSNAPID, _
    instance As JET_INSTANCE, _
    grbit As SnapshotPrepareInstanceGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim instance As JET_INSTANCE
Dim grbit As SnapshotPrepareInstanceGrbitVistaApi.JetOSSnapshotPrepareInstance(snapshot, _
    instance, grbit)
```

``` csharp
public static void JetOSSnapshotPrepareInstance(
    JET_OSSNAPID snapshot,
    JET_INSTANCE instance,
    SnapshotPrepareInstanceGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="a8dd7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8dd7-108">Parameters</span></span>

  - <span data-ttu-id="a8dd7-109">instantané</span><span class="sxs-lookup"><span data-stu-id="a8dd7-109">snapshot</span></span>  
    <span data-ttu-id="a8dd7-110">Type : [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a8dd7-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="a8dd7-111">Identificateur de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="a8dd7-111">The snapshot identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="a8dd7-112">instance</span><span class="sxs-lookup"><span data-stu-id="a8dd7-112">instance</span></span>  
    <span data-ttu-id="a8dd7-113">Type : [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a8dd7-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="a8dd7-114">Instance à ajouter à l’instantané.</span><span class="sxs-lookup"><span data-stu-id="a8dd7-114">The instance to add to the snapshot.</span></span>

<!-- end list -->

  - <span data-ttu-id="a8dd7-115">grbit</span><span class="sxs-lookup"><span data-stu-id="a8dd7-115">grbit</span></span>  
    <span data-ttu-id="a8dd7-116">Type : [Microsoft. ISAM. esent. Interop. Vista. SnapshotPrepareInstanceGrbit](./snapshotprepareinstancegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a8dd7-116">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotPrepareInstanceGrbit](./snapshotprepareinstancegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="a8dd7-117">Options pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="a8dd7-117">Options for this call.</span></span>

## <a name="see-also"></a><span data-ttu-id="a8dd7-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8dd7-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a8dd7-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="a8dd7-119">Reference</span></span>

[<span data-ttu-id="a8dd7-120">VistaApi, classe</span><span class="sxs-lookup"><span data-stu-id="a8dd7-120">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="a8dd7-121">Membres VistaApi</span><span class="sxs-lookup"><span data-stu-id="a8dd7-121">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="a8dd7-122">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="a8dd7-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
