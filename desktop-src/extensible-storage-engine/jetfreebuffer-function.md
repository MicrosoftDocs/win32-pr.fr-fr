---
description: 'En savoir plus sur : fonction JetFreeBuffer'
title: JetFreeBuffer fonction)
TOCTitle: JetFreeBuffer Function
ms:assetid: f37d35f6-4bea-46ba-a334-7b8ad7a1568c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294134(v=EXCHG.10)
ms:contentKeyID: 32765748
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetFreeBuffer
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe638e2aab1d37324a6fd6bf477a578f02b9ac58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523389"
---
# <a name="jetfreebuffer-function"></a><span data-ttu-id="6c55f-103">JetFreeBuffer fonction)</span><span class="sxs-lookup"><span data-stu-id="6c55f-103">JetFreeBuffer Function</span></span>


<span data-ttu-id="6c55f-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="6c55f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetfreebuffer-function"></a><span data-ttu-id="6c55f-105">JetFreeBuffer fonction)</span><span class="sxs-lookup"><span data-stu-id="6c55f-105">JetFreeBuffer Function</span></span>

<span data-ttu-id="6c55f-106">La fonction **JetFreeBuffer** libère de la mémoire qui a été allouée par un appel du moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="6c55f-106">The **JetFreeBuffer** function frees memory that was allocated by a database engine call.</span></span>

<span data-ttu-id="6c55f-107">**Windows XP : JetFreeBuffer** est introduit dans Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6c55f-107">**Windows XP:  JetFreeBuffer** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetFreeBuffer(
      __in          char* pbBuf
    );
```

### <a name="parameters"></a><span data-ttu-id="6c55f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c55f-108">Parameters</span></span>

<span data-ttu-id="6c55f-109">*pbBuf*</span><span class="sxs-lookup"><span data-stu-id="6c55f-109">*pbBuf*</span></span>

<span data-ttu-id="6c55f-110">Pointeur vers une zone de mémoire précédemment allouée par un appel au moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="6c55f-110">Pointer to a region of memory that was previously allocated by a call to the database engine.</span></span> <span data-ttu-id="6c55f-111">**Null** est acceptable et sera ignoré.</span><span class="sxs-lookup"><span data-stu-id="6c55f-111">**NULL** is acceptable, and will be ignored.</span></span>

### <a name="return-value"></a><span data-ttu-id="6c55f-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6c55f-112">Return Value</span></span>

<span data-ttu-id="6c55f-113">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="6c55f-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6c55f-114">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6c55f-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c55f-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6c55f-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="6c55f-116">Description</span><span class="sxs-lookup"><span data-stu-id="6c55f-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c55f-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6c55f-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6c55f-118">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="6c55f-118">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="6c55f-119">Notes</span><span class="sxs-lookup"><span data-stu-id="6c55f-119">Remarks</span></span>

<span data-ttu-id="6c55f-120">Il s’agit d’un comportement indéfini pour passer de la mémoire qui n’a pas été allouée par le moteur de base de données dans à *pbBuf*.</span><span class="sxs-lookup"><span data-stu-id="6c55f-120">It is undefined behavior to pass memory that was not allocated by the database engine in to *pbBuf*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="6c55f-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c55f-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c55f-122"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="6c55f-122"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6c55f-123">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6c55f-123">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c55f-124"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="6c55f-124"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6c55f-125">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6c55f-125">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c55f-126"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="6c55f-126"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6c55f-127">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="6c55f-127">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c55f-128"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="6c55f-128"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6c55f-129">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6c55f-129">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c55f-130"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6c55f-130"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6c55f-131">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6c55f-131">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6c55f-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c55f-132">See Also</span></span>

[<span data-ttu-id="6c55f-133">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6c55f-133">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6c55f-134">JetGetInstanceInfo</span><span class="sxs-lookup"><span data-stu-id="6c55f-134">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)
