---
description: 'En savoir plus sur : méthode VistaApi. JetGetRecordSize'
title: Méthode VistaApi. JetGetRecordSize (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'JetGetRecordSize method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetRecordSize(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE@,Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetrecordsize(v=EXCHG.10)
ms:contentKeyID: 55104285
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetRecordSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetRecordSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37576e39d83270dcac3333e4d1f78fce32bb2669
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514206"
---
# <a name="vistaapijetgetrecordsize-method"></a><span data-ttu-id="b5a00-103">Méthode VistaApi. JetGetRecordSize</span><span class="sxs-lookup"><span data-stu-id="b5a00-103">VistaApi.JetGetRecordSize method</span></span>

<span data-ttu-id="b5a00-104">Récupère des informations sur la taille des enregistrements à partir de l’emplacement souhaité.</span><span class="sxs-lookup"><span data-stu-id="b5a00-104">Retrieves record size information from the desired location.</span></span>

<span data-ttu-id="b5a00-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b5a00-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="b5a00-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b5a00-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b5a00-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5a00-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetRecordSize ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ByRef recsize As JET_RECSIZE, _
    grbit As GetRecordSizeGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim recsize As JET_RECSIZE
Dim grbit As GetRecordSizeGrbitVistaApi.JetGetRecordSize(sesid, tableid, _
    recsize, grbit)
```

``` csharp
public static void JetGetRecordSize(
    JET_SESID sesid,
    JET_TABLEID tableid,
    ref JET_RECSIZE recsize,
    GetRecordSizeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="b5a00-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5a00-108">Parameters</span></span>

  - <span data-ttu-id="b5a00-109">sesid</span><span class="sxs-lookup"><span data-stu-id="b5a00-109">sesid</span></span>  
    <span data-ttu-id="b5a00-110">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b5a00-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b5a00-111">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b5a00-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b5a00-112">TableID</span><span class="sxs-lookup"><span data-stu-id="b5a00-112">tableid</span></span>  
    <span data-ttu-id="b5a00-113">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b5a00-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b5a00-114">Curseur qui sera utilisé pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="b5a00-114">The cursor that will be used for the API call.</span></span> <span data-ttu-id="b5a00-115">Le curseur doit être positionné sur un enregistrement ou avoir une mise à jour préparée.</span><span class="sxs-lookup"><span data-stu-id="b5a00-115">The cursor must be positioned on a record, or have an update prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="b5a00-116">recsize</span><span class="sxs-lookup"><span data-stu-id="b5a00-116">recsize</span></span>  
    <span data-ttu-id="b5a00-117">Type : [Microsoft.ISAM.esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="b5a00-117">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="b5a00-118">Retourne la taille de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b5a00-118">Returns the size of the record.</span></span>

<!-- end list -->

  - <span data-ttu-id="b5a00-119">grbit</span><span class="sxs-lookup"><span data-stu-id="b5a00-119">grbit</span></span>  
    <span data-ttu-id="b5a00-120">Type : [Microsoft. ISAM. esent. Interop. GetRecordSizeGrbit](./getrecordsizegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b5a00-120">Type: [Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit](./getrecordsizegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b5a00-121">Options d’appel.</span><span class="sxs-lookup"><span data-stu-id="b5a00-121">Call options.</span></span>

## <a name="see-also"></a><span data-ttu-id="b5a00-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5a00-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b5a00-123">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="b5a00-123">Reference</span></span>

[<span data-ttu-id="b5a00-124">VistaApi, classe</span><span class="sxs-lookup"><span data-stu-id="b5a00-124">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="b5a00-125">Membres VistaApi</span><span class="sxs-lookup"><span data-stu-id="b5a00-125">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="b5a00-126">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="b5a00-126">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
