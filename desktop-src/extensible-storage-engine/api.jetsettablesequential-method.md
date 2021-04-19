---
description: 'En savoir plus sur : méthode API. JetSetTableSequential'
title: API. JetSetTableSequential, méthode
TOCTitle: 'JetSetTableSequential method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SetTableSequentialGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsettablesequential(v=EXCHG.10)
ms:contentKeyID: 55100810
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 879eca53c4867bb41ee0a231bff9adce39aa58a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523682"
---
# <a name="apijetsettablesequential-method"></a><span data-ttu-id="dbcf5-103">API. JetSetTableSequential, méthode</span><span class="sxs-lookup"><span data-stu-id="dbcf5-103">Api.JetSetTableSequential method</span></span>

<span data-ttu-id="dbcf5-104">Notifie le moteur de base de données que l’application analyse la totalité de l’index sur lequel le curseur est positionné.</span><span class="sxs-lookup"><span data-stu-id="dbcf5-104">Notifies the database engine that the application is scanning the entire index that the cursor is positioned on.</span></span> <span data-ttu-id="dbcf5-105">Par conséquent, les méthodes utilisées pour accéder aux données d’index seront paramétrées pour rendre ce scénario aussi rapide que possible.</span><span class="sxs-lookup"><span data-stu-id="dbcf5-105">Consequently, the methods that are used to access the index data will be tuned to make this scenario as fast as possible.</span></span> <span data-ttu-id="dbcf5-106">Consultez également [JetResetTableSequential (JET_SESID, JET_TABLEID, ResetTableSequentialGrbit)](./api.jetresettablesequential-method.md).</span><span class="sxs-lookup"><span data-stu-id="dbcf5-106">Also see [JetResetTableSequential(JET_SESID, JET_TABLEID, ResetTableSequentialGrbit)](./api.jetresettablesequential-method.md).</span></span>

<span data-ttu-id="dbcf5-107">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dbcf5-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dbcf5-108">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dbcf5-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dbcf5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbcf5-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetTableSequential ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SetTableSequentialGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SetTableSequentialGrbitApi.JetSetTableSequential(sesid, _
    tableid, grbit)
```

``` csharp
public static void JetSetTableSequential(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SetTableSequentialGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="dbcf5-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbcf5-110">Parameters</span></span>

  - <span data-ttu-id="dbcf5-111">sesid</span><span class="sxs-lookup"><span data-stu-id="dbcf5-111">sesid</span></span>  
    <span data-ttu-id="dbcf5-112">Type : [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dbcf5-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="dbcf5-113">Session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="dbcf5-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="dbcf5-114">TableID</span><span class="sxs-lookup"><span data-stu-id="dbcf5-114">tableid</span></span>  
    <span data-ttu-id="dbcf5-115">Type : [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dbcf5-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="dbcf5-116">Curseur qui accède aux données.</span><span class="sxs-lookup"><span data-stu-id="dbcf5-116">The cursor that will be accessing the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="dbcf5-117">grbit</span><span class="sxs-lookup"><span data-stu-id="dbcf5-117">grbit</span></span>  
    <span data-ttu-id="dbcf5-118">Type : [Microsoft. ISAM. esent. Interop. SetTableSequentialGrbit](./settablesequentialgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="dbcf5-118">Type: [Microsoft.Isam.Esent.Interop.SetTableSequentialGrbit](./settablesequentialgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="dbcf5-119">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="dbcf5-119">Reserved for future use.</span></span>

## <a name="see-also"></a><span data-ttu-id="dbcf5-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbcf5-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dbcf5-121">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="dbcf5-121">Reference</span></span>

[<span data-ttu-id="dbcf5-122">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="dbcf5-122">Api class</span></span>](./api-class.md)

[<span data-ttu-id="dbcf5-123">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="dbcf5-123">Api members</span></span>](./api-members.md)

[<span data-ttu-id="dbcf5-124">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="dbcf5-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
