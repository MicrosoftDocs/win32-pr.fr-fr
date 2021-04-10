---
description: 'En savoir plus sur : méthode API. JetOSSnapshotPrepare'
title: API. JetOSSnapshotPrepare, méthode
TOCTitle: 'JetOSSnapshotPrepare method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare(Microsoft.Isam.Esent.Interop.JET_OSSNAPID@,Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetossnapshotprepare(v=EXCHG.10)
ms:contentKeyID: 55100779
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0ac304cf522e7c99a2495925da8571b2139c0a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210526"
---
# <a name="apijetossnapshotprepare-method"></a><span data-ttu-id="6a3ce-103">API. JetOSSnapshotPrepare, méthode</span><span class="sxs-lookup"><span data-stu-id="6a3ce-103">Api.JetOSSnapshotPrepare method</span></span>

<span data-ttu-id="6a3ce-104">Commence les préparations pour une session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="6a3ce-104">Begins the preparations for a snapshot session.</span></span> <span data-ttu-id="6a3ce-105">Une session d’instantané est un intervalle de temps dans lequel le moteur n’émet pas d’e/s d’écriture sur le disque, de sorte que le moteur peut participer à une session d’instantané de volume (lorsqu’il est piloté par un enregistreur d’instantané).</span><span class="sxs-lookup"><span data-stu-id="6a3ce-105">A snapshot session is a short time interval in which the engine does not issue any write IOs to disk, so that the engine can participate in a volume snapshot session (when driven by a snapshot writer).</span></span>

<span data-ttu-id="6a3ce-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6a3ce-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6a3ce-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6a3ce-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6a3ce-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a3ce-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotPrepare ( _
    <OutAttribute> ByRef snapshot As JET_OSSNAPID, _
    grbit As SnapshotPrepareGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotPrepareGrbitApi.JetOSSnapshotPrepare(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotPrepare(
    out JET_OSSNAPID snapshot,
    SnapshotPrepareGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="6a3ce-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a3ce-109">Parameters</span></span>

  - <span data-ttu-id="6a3ce-110">instantané</span><span class="sxs-lookup"><span data-stu-id="6a3ce-110">snapshot</span></span>  
    <span data-ttu-id="6a3ce-111">Type : [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6a3ce-111">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="6a3ce-112">Retourne l’ID de la session d’instantané.</span><span class="sxs-lookup"><span data-stu-id="6a3ce-112">Returns the ID of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="6a3ce-113">grbit</span><span class="sxs-lookup"><span data-stu-id="6a3ce-113">grbit</span></span>  
    <span data-ttu-id="6a3ce-114">Type : [Microsoft. ISAM. esent. Interop. SnapshotPrepareGrbit](./snapshotpreparegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6a3ce-114">Type: [Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit](./snapshotpreparegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="6a3ce-115">Options d’instantané.</span><span class="sxs-lookup"><span data-stu-id="6a3ce-115">Snapshot options.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a3ce-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a3ce-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6a3ce-117">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="6a3ce-117">Reference</span></span>

[<span data-ttu-id="6a3ce-118">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="6a3ce-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6a3ce-119">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="6a3ce-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6a3ce-120">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6a3ce-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
