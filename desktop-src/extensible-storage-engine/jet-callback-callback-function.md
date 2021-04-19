---
description: 'En savoir plus sur : fonction de rappel JET_CALLBACK'
title: JET_CALLBACK fonction de rappel
TOCTitle: JET_CALLBACK Callback Function
ms:assetid: d15d4f84-8378-4b4b-9b8b-e89a56be5ead
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294098(v=EXCHG.10)
ms:contentKeyID: 32765713
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
ms.openlocfilehash: 5e6d26bd5e347757fce270d5f2c78ab471755c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519773"
---
# <a name="jet_callback-callback-function"></a><span data-ttu-id="465dd-103">JET_CALLBACK fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="465dd-103">JET_CALLBACK Callback Function</span></span>


<span data-ttu-id="465dd-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="465dd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_callback-callback-function"></a><span data-ttu-id="465dd-105">JET_CALLBACK fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="465dd-105">JET_CALLBACK Callback Function</span></span>

<span data-ttu-id="465dd-106">La fonction **JET_CALLBACK** est une fonction de rappel polyvalente utilisée par le moteur de base de données pour informer l’application d’un événement impliquant la défragmentation en ligne et les notifications de l’état du curseur.</span><span class="sxs-lookup"><span data-stu-id="465dd-106">The **JET_CALLBACK** function is a multi-purpose callback function used by the database engine to inform the application of an event involving online defragmentation and cursor state notifications.</span></span>

<span data-ttu-id="465dd-107">Consultez [JET_CBTYP](./jet-cbtyp.md) pour connaître les paramètres spécifiques à utiliser pour les paramètres de cette fonction, car ces paramètres diffèrent en fonction de l’option **JET_CBTYP** sélectionnée pour être utilisée dans le paramètre *CBTYP* .</span><span class="sxs-lookup"><span data-stu-id="465dd-107">See [JET_CBTYP](./jet-cbtyp.md) for specific settings to use for the parameters of this function, as these settings will differ depending upon the **JET_CBTYP** option that is selected for use in the *cbtyp* parameter.</span></span>

```cpp
    JET_ERR JET_API* JET_CALLBACK(
      [in]                 JET_SESID sesid,
      [in]                 JET_DBID dbid,
      [in]                 JET_TABLEID tableid,
      [in]                 JET_CBTYP cbtyp,
      [in, out]            void* pvArg1,
      [in, out]            void* pvArg2,
      [in]                 void* pvContext,
      [in]                 JET_API_PTR ulUnused
    );
```

### <a name="parameters"></a><span data-ttu-id="465dd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="465dd-108">Parameters</span></span>

<span data-ttu-id="465dd-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="465dd-109">*sesid*</span></span>

<span data-ttu-id="465dd-110">Session pour laquelle le rappel est effectué.</span><span class="sxs-lookup"><span data-stu-id="465dd-110">The session for which the callback is being made.</span></span>

<span data-ttu-id="465dd-111">*dbid*</span><span class="sxs-lookup"><span data-stu-id="465dd-111">*dbid*</span></span>

<span data-ttu-id="465dd-112">Base de données pour laquelle le rappel est effectué.</span><span class="sxs-lookup"><span data-stu-id="465dd-112">The database for which the callback is being made.</span></span>

<span data-ttu-id="465dd-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="465dd-113">*tableid*</span></span>

<span data-ttu-id="465dd-114">Curseur pour lequel le rappel est effectué.</span><span class="sxs-lookup"><span data-stu-id="465dd-114">The cursor for which the callback is being made.</span></span>

<span data-ttu-id="465dd-115">*cbtyp*</span><span class="sxs-lookup"><span data-stu-id="465dd-115">*cbtyp*</span></span>

<span data-ttu-id="465dd-116">Point de l’opération au niveau duquel le rappel est effectué.</span><span class="sxs-lookup"><span data-stu-id="465dd-116">The point in the operation at which the callback is being made.</span></span> <span data-ttu-id="465dd-117">Consultez [JET_CBTYP](./jet-cbtyp.md) pour obtenir la liste des valeurs et la signification des paramètres suivants dans chaque cas.</span><span class="sxs-lookup"><span data-stu-id="465dd-117">See [JET_CBTYP](./jet-cbtyp.md) for a list of values and the meaning of the following parameters in each case.</span></span>

<span data-ttu-id="465dd-118">*pvArg1*</span><span class="sxs-lookup"><span data-stu-id="465dd-118">*pvArg1*</span></span>

<span data-ttu-id="465dd-119">Paramètre utilisé pour communiquer avec l’application à l’aide du rappel.</span><span class="sxs-lookup"><span data-stu-id="465dd-119">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="465dd-120">Consultez [JET_CBTYP](./jet-cbtyp.md) pour plus d’informations sur l’utilisation de ce paramètre pour chaque rappel pris en charge par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="465dd-120">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

<span data-ttu-id="465dd-121">*pvArg2*</span><span class="sxs-lookup"><span data-stu-id="465dd-121">*pvArg2*</span></span>

<span data-ttu-id="465dd-122">Paramètre utilisé pour communiquer avec l’application à l’aide du rappel.</span><span class="sxs-lookup"><span data-stu-id="465dd-122">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="465dd-123">Consultez [JET_CBTYP](./jet-cbtyp.md) pour plus d’informations sur l’utilisation de ce paramètre pour chaque rappel pris en charge par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="465dd-123">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

<span data-ttu-id="465dd-124">*pvContext*</span><span class="sxs-lookup"><span data-stu-id="465dd-124">*pvContext*</span></span>

<span data-ttu-id="465dd-125">Paramètre utilisé pour communiquer avec l’application à l’aide du rappel.</span><span class="sxs-lookup"><span data-stu-id="465dd-125">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="465dd-126">Consultez [JET_CBTYP](./jet-cbtyp.md) pour plus d’informations sur l’utilisation de ce paramètre pour chaque rappel pris en charge par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="465dd-126">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

<span data-ttu-id="465dd-127">*ulUnused*</span><span class="sxs-lookup"><span data-stu-id="465dd-127">*ulUnused*</span></span>

<span data-ttu-id="465dd-128">Paramètre utilisé pour communiquer avec l’application à l’aide du rappel.</span><span class="sxs-lookup"><span data-stu-id="465dd-128">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="465dd-129">Consultez [JET_CBTYP](./jet-cbtyp.md) pour plus d’informations sur l’utilisation de ce paramètre pour chaque rappel pris en charge par le moteur de base de données.</span><span class="sxs-lookup"><span data-stu-id="465dd-129">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

#### <a name="return-value"></a><span data-ttu-id="465dd-130">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="465dd-130">Return Value</span></span>

<span data-ttu-id="465dd-131">La fonction retourne l’un des [codes d’erreur du moteur de stockage extensible](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="465dd-131">The function returns one of the [Extensible Storage Engine error codes](./extensible-storage-engine-error-codes.md).</span></span> <span data-ttu-id="465dd-132">Pour plus d’informations sur la façon de renvoyer ces codes en tant que HRESULT, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md).</span><span class="sxs-lookup"><span data-stu-id="465dd-132">For information about how to return these codes as HRESULTs, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span></span> <span data-ttu-id="465dd-133">En cas de réussite, l’opération qui a émis le rappel peut se poursuivre normalement.</span><span class="sxs-lookup"><span data-stu-id="465dd-133">On success, the operation that issued the callback can proceed normally.</span></span> <span data-ttu-id="465dd-134">Dans certains cas, le rappel peut retourner un avertissement qui influence cette opération.</span><span class="sxs-lookup"><span data-stu-id="465dd-134">In some cases, the callback may return a warning that influences that operation.</span></span> <span data-ttu-id="465dd-135">Pour plus d’informations sur l’utilisation de ces avertissements par l’opération, consultez [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="465dd-135">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of these warnings by the operation.</span></span>

<span data-ttu-id="465dd-136">En cas d’échec, l’opération qui a émis le rappel peut se poursuivre normalement ou échouer.</span><span class="sxs-lookup"><span data-stu-id="465dd-136">On failure, the operation that issued the callback may proceed normally or may fail.</span></span> <span data-ttu-id="465dd-137">Pour plus d’informations sur l’utilisation du code d’erreur par l’opération, consultez [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="465dd-137">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of the error code by the operation.</span></span>

#### <a name="remarks"></a><span data-ttu-id="465dd-138">Notes</span><span class="sxs-lookup"><span data-stu-id="465dd-138">Remarks</span></span>

<span data-ttu-id="465dd-139">Si le rappel passe un curseur à l’application, il est important de savoir que ce curseur est intentionnellement limité à un ensemble de fonctionnalités plus réduit pour éviter la récursivité et d’autres ugliness.</span><span class="sxs-lookup"><span data-stu-id="465dd-139">If the callback passes a cursor to the application then it is important to know that this cursor is intentionally limited to a smaller set of functionality to avoid recursion and other ugliness.</span></span> <span data-ttu-id="465dd-140">Les opérations suivantes sont autorisées :</span><span class="sxs-lookup"><span data-stu-id="465dd-140">The following operations are allowed:</span></span>

  - [<span data-ttu-id="465dd-141">JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="465dd-141">JetDupCursor</span></span>](./jetdupcursor-function.md)

  - [<span data-ttu-id="465dd-142">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="465dd-142">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="465dd-143">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="465dd-143">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="465dd-144">JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="465dd-144">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)

  - [<span data-ttu-id="465dd-145">JetGetCursorInfo</span><span class="sxs-lookup"><span data-stu-id="465dd-145">JetGetCursorInfo</span></span>](./jetgetcursorinfo-function.md)

  - [<span data-ttu-id="465dd-146">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="465dd-146">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="465dd-147">JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="465dd-147">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)

  - [<span data-ttu-id="465dd-148">JetGetSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="465dd-148">JetGetSecondaryIndexBookmark</span></span>](./jetgetsecondaryindexbookmark-function.md)

  - [<span data-ttu-id="465dd-149">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="465dd-149">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)

  - [<span data-ttu-id="465dd-150">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="465dd-150">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)

  - [<span data-ttu-id="465dd-151">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="465dd-151">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="465dd-152">JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="465dd-152">JetRegisterCallback</span></span>](./jetregistercallback-function.md)

  - [<span data-ttu-id="465dd-153">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="465dd-153">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="465dd-154">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="465dd-154">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="465dd-155">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="465dd-155">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="465dd-156">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="465dd-156">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="465dd-157">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="465dd-157">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="465dd-158">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="465dd-158">JetSetLS</span></span>](./jetsetls-function.md)

  - [<span data-ttu-id="465dd-159">JetUnregisterCallback</span><span class="sxs-lookup"><span data-stu-id="465dd-159">JetUnregisterCallback</span></span>](./jetunregistercallback-function.md)

<span data-ttu-id="465dd-160">Lorsque vous concevez votre rappel, prenez en compte le fait que même avec ces restrictions, il est toujours possible que le rappel échoue.</span><span class="sxs-lookup"><span data-stu-id="465dd-160">When you design your callback, take into account that even with these restrictions, it is still possible for the callback to fail.</span></span>

#### <a name="requirements"></a><span data-ttu-id="465dd-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="465dd-161">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="465dd-162"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="465dd-162"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="465dd-163">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="465dd-163">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="465dd-164"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="465dd-164"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="465dd-165">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="465dd-165">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="465dd-166"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="465dd-166"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="465dd-167">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="465dd-167">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="465dd-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="465dd-168">See Also</span></span>

[<span data-ttu-id="465dd-169">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="465dd-169">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="465dd-170">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="465dd-170">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="465dd-171">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="465dd-171">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="465dd-172">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="465dd-172">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="465dd-173">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="465dd-173">JET_CBTYP</span></span>](./jet-cbtyp.md)
