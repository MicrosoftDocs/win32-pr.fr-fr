---
description: 'En savoir plus sur : JET_LS'
title: JET_LS
TOCTitle: JET_LS
ms:assetid: 8e4e7902-84b1-404b-8654-bb430a0952aa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269336(v=EXCHG.10)
ms:contentKeyID: 32765625
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
ms.openlocfilehash: 3300fd88c0dd1e1fca55722bf58350e28f3c3b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522106"
---
# <a name="jet_ls"></a><span data-ttu-id="b5930-103">JET_LS</span><span class="sxs-lookup"><span data-stu-id="b5930-103">JET_LS</span></span>


<span data-ttu-id="b5930-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="b5930-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_ls"></a><span data-ttu-id="b5930-105">JET_LS</span><span class="sxs-lookup"><span data-stu-id="b5930-105">JET_LS</span></span>

<span data-ttu-id="b5930-106">Le type de données **JET_LS** contient un descripteur de contexte pour le stockage local (LS). Ce handle peut être associé à un curseur ou à une table et peut faire référence à des ressources allouées dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="b5930-106">The **JET_LS** data type contains a context handle to local storage (LS).This handle might be associated with a cursor or a table and might refer to dynamically allocated resources.</span></span>

<span data-ttu-id="b5930-107">**Windows XP : JET_LS** est introduite dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b5930-107">**Windows XP:  JET_LS** is introduced in Windows XP.</span></span>

```cpp
    typedef JET_API_PTR JET_LS;
```

### <a name="data-types"></a><span data-ttu-id="b5930-108">Types de données</span><span class="sxs-lookup"><span data-stu-id="b5930-108">Data Types</span></span>

<span data-ttu-id="b5930-109">JET_LS</span><span class="sxs-lookup"><span data-stu-id="b5930-109">JET_LS</span></span>

<span data-ttu-id="b5930-110">La valeur JET_LSNil indique un handle de contexte non valide.</span><span class="sxs-lookup"><span data-stu-id="b5930-110">A value of JET_LSNil indicates an invalid context handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="b5930-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b5930-111">Remarks</span></span>

<span data-ttu-id="b5930-112">Un descripteur de contexte est initialement associé à l' **JET_LS** type de données, à l’aide de [JetSetLS](./jetsetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="b5930-112">A context handle is initially associated with the **JET_LS** data type, using [JetSetLS](./jetsetls-function.md).</span></span> <span data-ttu-id="b5930-113">Le descripteur de contexte peut être récupéré à partir du type de données **JET_LS** à l’aide de [JetGetLS](./jetgetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="b5930-113">The context handle can be retrieved from the **JET_LS** data type, using [JetGetLS](./jetgetls-function.md).</span></span>

<span data-ttu-id="b5930-114">Le descripteur de contexte peut être explicitement dissocié du type de données **JET_LS** à l’aide de [JetGetLS](./jetgetls-function.md) avec JET_bitLSReset.</span><span class="sxs-lookup"><span data-stu-id="b5930-114">The context handle can be explicitly disassociated from the **JET_LS** data type using [JetGetLS](./jetgetls-function.md) with JET_bitLSReset.</span></span> <span data-ttu-id="b5930-115">Le handle de contexte peut également être dissocié implicitement du type de données **JET_LS** lorsque l’objet sous-jacent est libéré par le moteur de base de données à la suite d’une action directe ou indirecte de l’application.</span><span class="sxs-lookup"><span data-stu-id="b5930-115">Alternatively, the context handle can be implicitly disassociated from the **JET_LS** data type when the underlying object is released by the database engine as a result of direct or indirect action by the application.</span></span> <span data-ttu-id="b5930-116">Dans le cas implicite, un rappel d’exécution est émis pour l’application afin qu’elle puisse nettoyer le handle de contexte.</span><span class="sxs-lookup"><span data-stu-id="b5930-116">In the implicit case, a runtime callback is issued to the application so that it can clean up the context handle.</span></span> <span data-ttu-id="b5930-117">Pour plus d’informations sur la dissociation implicite du type de données **JET_LS** , consultez [JetSetLS](./jetsetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="b5930-117">For more information on implicitly disassociating from the **JET_LS** data type, see [JetSetLS](./jetsetls-function.md).</span></span>

<span data-ttu-id="b5930-118">Les indicateurs suivants sont associés au type de données JET_LS.</span><span class="sxs-lookup"><span data-stu-id="b5930-118">The following flags are associated with the JET_LS data type.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b5930-119">Terme</span><span class="sxs-lookup"><span data-stu-id="b5930-119">Term</span></span></p></th>
<th><p><span data-ttu-id="b5930-120">Description</span><span class="sxs-lookup"><span data-stu-id="b5930-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5930-121">JET_bitLSReset</span><span class="sxs-lookup"><span data-stu-id="b5930-121">JET_bitLSReset</span></span></p></td>
<td><p><span data-ttu-id="b5930-122">Le handle de contexte est dissocié de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b5930-122">The context handle is disassociated from the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5930-123">JET_bitLSCursor</span><span class="sxs-lookup"><span data-stu-id="b5930-123">JET_bitLSCursor</span></span></p></td>
<td><p><span data-ttu-id="b5930-124">Définissez ou récupérez le stockage local associé à un curseur de table.</span><span class="sxs-lookup"><span data-stu-id="b5930-124">Set or retrieve the local storage associated with a table cursor.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5930-125">JET_bitLSTable</span><span class="sxs-lookup"><span data-stu-id="b5930-125">JET_bitLSTable</span></span></p></td>
<td><p><span data-ttu-id="b5930-126">Définissez ou récupérez le stockage local associé à une table.</span><span class="sxs-lookup"><span data-stu-id="b5930-126">Set or retrieve the local storage associated with a table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5930-127">JET_LSNil</span><span class="sxs-lookup"><span data-stu-id="b5930-127">JET_LSNil</span></span></p></td>
<td><p><span data-ttu-id="b5930-128">Le descripteur de contexte n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="b5930-128">The context handle is invalid.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="b5930-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5930-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5930-130"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b5930-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b5930-131">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b5930-131">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5930-132"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="b5930-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b5930-133">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b5930-133">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5930-134"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="b5930-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b5930-135">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="b5930-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="b5930-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5930-136">See Also</span></span>

[<span data-ttu-id="b5930-137">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="b5930-137">JetSetLS</span></span>](./jetsetls-function.md)  
[<span data-ttu-id="b5930-138">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="b5930-138">JetGetLS</span></span>](./jetgetls-function.md)
