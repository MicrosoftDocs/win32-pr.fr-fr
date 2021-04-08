---
description: 'En savoir plus sur : JET_SESID'
title: JET_SESID
TOCTitle: JET_SESID
ms:assetid: 56b53532-e0a8-4255-8442-bb90184d91da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269253(v=EXCHG.10)
ms:contentKeyID: 32765555
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 542802c806bbea55aafb4fc1a0241a92b2842878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862209"
---
# <a name="jet_sesid"></a><span data-ttu-id="3edeb-103">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3edeb-103">JET_SESID</span></span>


<span data-ttu-id="3edeb-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="3edeb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_sesid"></a><span data-ttu-id="3edeb-105">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3edeb-105">JET_SESID</span></span>

<span data-ttu-id="3edeb-106">Le type de données **JET_SESID** contient un descripteur de la session à utiliser pour un appel à l’API jet.</span><span class="sxs-lookup"><span data-stu-id="3edeb-106">The **JET_SESID** data type contains a handle to the session to use for a call to the JET API.</span></span>

```cpp
    typedef JET_API_PTR JET_SESID;
```

### <a name="data-types"></a><span data-ttu-id="3edeb-107">Types de données</span><span class="sxs-lookup"><span data-stu-id="3edeb-107">Data Types</span></span>

<span data-ttu-id="3edeb-108">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="3edeb-108">JET_SESID</span></span>

<span data-ttu-id="3edeb-109">La **valeur null** ou [JET_sesidNil](./invalid-handle-constants.md) peut être utilisée pour indiquer un handle de session non valide.</span><span class="sxs-lookup"><span data-stu-id="3edeb-109">Either **NULL** or [JET_sesidNil](./invalid-handle-constants.md) can be used to indicate an invalid session handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="3edeb-110">Notes</span><span class="sxs-lookup"><span data-stu-id="3edeb-110">Remarks</span></span>

<span data-ttu-id="3edeb-111">Une session est le contexte de transaction du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="3edeb-111">A session is the transaction context of the database engine.</span></span> <span data-ttu-id="3edeb-112">Il peut être utilisé pour commencer, valider ou abandonner des transactions qui affectent la visibilité et la durabilité des modifications apportées par ce ou d’autres sessions.</span><span class="sxs-lookup"><span data-stu-id="3edeb-112">It can be used to begin, commit, or abort transactions that affect the visibility and durability of changes that are made by this or other sessions.</span></span>

<span data-ttu-id="3edeb-113">Une transaction peut être démarrée à l’aide de [JetBeginTransaction](./jetbegintransaction-function.md).</span><span class="sxs-lookup"><span data-stu-id="3edeb-113">A transaction can be started using [JetBeginTransaction](./jetbegintransaction-function.md).</span></span> <span data-ttu-id="3edeb-114">Une session peut être créée à l’aide de [JetBeginSession](./jetbeginsession-function.md).</span><span class="sxs-lookup"><span data-stu-id="3edeb-114">A session may be created using [JetBeginSession](./jetbeginsession-function.md).</span></span> <span data-ttu-id="3edeb-115">Le nombre maximal de sessions qui peuvent être créées à un moment donné est contrôlé par [JET_paramMaxSessions](./resource-parameters.md), ce qui peut être configuré au moyen de [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="3edeb-115">The maximum number of sessions that can be created at any one time is controlled by [JET_paramMaxSessions](./resource-parameters.md), which can be configured by means of [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="3edeb-116">Une session est explicitement terminée par un appel à [JetEndSession](./jetendsession-function.md) ou est terminée implicitement par un appel à [JetTerm](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="3edeb-116">A session is explicitly ended by a call to [JetEndSession](./jetendsession-function.md) or implicitly ended by a call to [JetTerm](./jetterm-function.md).</span></span>

<span data-ttu-id="3edeb-117">Chaque session ne peut être utilisée que par un seul thread à la fois.</span><span class="sxs-lookup"><span data-stu-id="3edeb-117">Each session can only be used by one thread at a time.</span></span> <span data-ttu-id="3edeb-118">En outre, le comportement par défaut du moteur consiste à limiter l’utilisation d’une session au même thread à partir du moment où le premier appel à [JetBeginTransaction](./jetbegintransaction-function.md) est effectué jusqu’au moment où l’appel correspondant à [JetCommitTransaction](./jetcommittransaction-function.md) ou [JetRollback](./jetrollback-function.md) est effectué.</span><span class="sxs-lookup"><span data-stu-id="3edeb-118">In addition, the default behavior of the engine is to restrict the use of a session to the same thread from the time the first call to [JetBeginTransaction](./jetbegintransaction-function.md) is made until the time when the matching call to [JetCommitTransaction](./jetcommittransaction-function.md) or [JetRollback](./jetrollback-function.md) is made.</span></span> <span data-ttu-id="3edeb-119">Ce comportement peut être modifié pour supprimer cette deuxième restriction en définissant un contexte de session personnalisé à l’aide de [JetSetSessionContext](./jetsetsessioncontext-function.md) et [JetResetSessionContext](./jetresetsessioncontext-function.md).</span><span class="sxs-lookup"><span data-stu-id="3edeb-119">This behavior can be changed to remove this second restriction by setting a custom session context using [JetSetSessionContext](./jetsetsessioncontext-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="3edeb-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3edeb-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3edeb-121"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="3edeb-121"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="3edeb-122">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="3edeb-122">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3edeb-123"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="3edeb-123"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="3edeb-124">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="3edeb-124">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3edeb-125"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="3edeb-125"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="3edeb-126">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="3edeb-126">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="3edeb-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3edeb-127">See Also</span></span>

[<span data-ttu-id="3edeb-128">JET_paramMaxSessions</span><span class="sxs-lookup"><span data-stu-id="3edeb-128">JET_paramMaxSessions</span></span>](./resource-parameters.md)  
[<span data-ttu-id="3edeb-129">JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="3edeb-129">JetBeginSession</span></span>](./jetbeginsession-function.md)  
[<span data-ttu-id="3edeb-130">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="3edeb-130">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="3edeb-131">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="3edeb-131">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="3edeb-132">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="3edeb-132">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="3edeb-133">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="3edeb-133">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="3edeb-134">JetRollback</span><span class="sxs-lookup"><span data-stu-id="3edeb-134">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="3edeb-135">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="3edeb-135">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="3edeb-136">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="3edeb-136">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="3edeb-137">JetTerm</span><span class="sxs-lookup"><span data-stu-id="3edeb-137">JetTerm</span></span>](./jetterm-function.md)
