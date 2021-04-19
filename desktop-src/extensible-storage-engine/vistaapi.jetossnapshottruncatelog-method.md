---
description: 'En savoir plus sur : méthode VistaApi. JetOSSnapshotTruncateLog'
title: Méthode VistaApi. JetOSSnapshotTruncateLog (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'JetOSSnapshotTruncateLog method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshottruncatelog(v=EXCHG.10)
ms:contentKeyID: 55104308
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0af8054bc414ea5dbd6c7225fa9e2cd7117c74c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514560"
---
# <a name="vistaapijetossnapshottruncatelog-method"></a><span data-ttu-id="adc2e-103">Méthode VistaApi. JetOSSnapshotTruncateLog</span><span class="sxs-lookup"><span data-stu-id="adc2e-103">VistaApi.JetOSSnapshotTruncateLog method</span></span>

<span data-ttu-id="adc2e-104">Active la troncation du journal pour toutes les instances qui font partie de la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="adc2e-104">Enables log truncation for all instances that are part of the snapshot session.</span></span>

<span data-ttu-id="adc2e-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="adc2e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="adc2e-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="adc2e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="adc2e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="adc2e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotTruncateLog ( _
    snapshot As JET_OSSNAPID, _
    grbit As SnapshotTruncateLogGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotTruncateLogGrbitVistaApi.JetOSSnapshotTruncateLog(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotTruncateLog(
    JET_OSSNAPID snapshot,
    SnapshotTruncateLogGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="adc2e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="adc2e-108">Parameters</span></span>

  - <span data-ttu-id="adc2e-109">instantané</span><span class="sxs-lookup"><span data-stu-id="adc2e-109">snapshot</span></span>  
    <span data-ttu-id="adc2e-110">Type : [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="adc2e-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="adc2e-111">Identificateur de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="adc2e-111">The snapshot identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="adc2e-112">grbit</span><span class="sxs-lookup"><span data-stu-id="adc2e-112">grbit</span></span>  
    <span data-ttu-id="adc2e-113">Type : [Microsoft. ISAM. esent. Interop. Vista. SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="adc2e-113">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="adc2e-114">Options pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="adc2e-114">Options for this call.</span></span>

## <a name="remarks"></a><span data-ttu-id="adc2e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="adc2e-115">Remarks</span></span>

<span data-ttu-id="adc2e-116">Cette fonction doit être appelée uniquement si l’instantané a été créé avec l’option [ContinueAfterThaw](./vistagrbits.continueafterthaw-field.md) .</span><span class="sxs-lookup"><span data-stu-id="adc2e-116">This function should be called only if the snapshot was created with the [ContinueAfterThaw](./vistagrbits.continueafterthaw-field.md) option.</span></span> <span data-ttu-id="adc2e-117">Dans le cas contraire, la session d’instantané se termine après l’appel à [JetOSSnapshotThaw (JET_OSSNAPID, SnapshotThawGrbit)](./api.jetossnapshotthaw-method.md).</span><span class="sxs-lookup"><span data-stu-id="adc2e-117">Otherwise, the snapshot session ends after the call to [JetOSSnapshotThaw(JET_OSSNAPID, SnapshotThawGrbit)](./api.jetossnapshotthaw-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="adc2e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adc2e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="adc2e-119">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="adc2e-119">Reference</span></span>

[<span data-ttu-id="adc2e-120">VistaApi, classe</span><span class="sxs-lookup"><span data-stu-id="adc2e-120">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="adc2e-121">Membres VistaApi</span><span class="sxs-lookup"><span data-stu-id="adc2e-121">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="adc2e-122">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="adc2e-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
