---
title: RasAdminFreeBuffer, fonction (rassapi. h)
description: La fonction RasAdminFreeBuffer libère de la mémoire qui a été allouée par RAS pour le compte de l’appelant.
ms.assetid: 6dfbba22-3af1-4771-8c22-506996f30c6b
keywords:
- RasAdminFreeBuffer fonction RAS
topic_type:
- apiref
api_name:
- RasAdminFreeBuffer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf86a3005a2b865b2096eddc5ffa9c0c33f848a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535426"
---
# <a name="rasadminfreebuffer-function"></a><span data-ttu-id="b5b8d-104">RasAdminFreeBuffer fonction)</span><span class="sxs-lookup"><span data-stu-id="b5b8d-104">RasAdminFreeBuffer function</span></span>

<span data-ttu-id="b5b8d-105">\[Cette fonction est fournie uniquement pour la compatibilité descendante avec Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="b5b8d-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="b5b8d-106">Elle retourne un \_ appel \_ d’erreur non \_ implémenté sur Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b5b8d-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="b5b8d-107">Les applications doivent utiliser la fonction [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) .\]</span><span class="sxs-lookup"><span data-stu-id="b5b8d-107">Applications should use the [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree) function.\]</span></span>

<span data-ttu-id="b5b8d-108">La fonction **RasAdminFreeBuffer** libère de la mémoire qui a été allouée par RAS pour le compte de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="b5b8d-108">The **RasAdminFreeBuffer** function frees memory that was allocated by RAS on behalf of the caller.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5b8d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5b8d-109">Syntax</span></span>


```C++
DWORD RasAdminFreeBuffer(
  _In_ PVOID Pointer
);
```



## <a name="parameters"></a><span data-ttu-id="b5b8d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b5b8d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5b8d-111">*Pointeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b5b8d-111">*Pointer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5b8d-112">Pointeur vers la mémoire tampon à libérer.</span><span class="sxs-lookup"><span data-stu-id="b5b8d-112">Pointer to the buffer to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5b8d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b5b8d-113">Return value</span></span>

<span data-ttu-id="b5b8d-114">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="b5b8d-114">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="b5b8d-115">Si la fonction échoue, la valeur de retour peut être le code d’erreur suivant.</span><span class="sxs-lookup"><span data-stu-id="b5b8d-115">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="b5b8d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5b8d-116">Value</span></span>                                                                                                    | <span data-ttu-id="b5b8d-117">Signification</span><span class="sxs-lookup"><span data-stu-id="b5b8d-117">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="b5b8d-118"><dt>**paramètre d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5b8d-118"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="b5b8d-119">Le paramètre de *pointeur* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="b5b8d-119">The *Pointer* parameter is invalid.</span></span><br/> |



 

<span data-ttu-id="b5b8d-120">Il n’y a pas d’informations d’erreur étendues pour cette fonction. ne pas appeler [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="b5b8d-120">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="b5b8d-121">Notes</span><span class="sxs-lookup"><span data-stu-id="b5b8d-121">Remarks</span></span>

<span data-ttu-id="b5b8d-122">Utilisez la fonction **RasAdminFreeBuffer** pour libérer les tampons alloués par les fonctions [**RasAdminPortEnum**](rasadminportenum.md) et [**RasAdminPortGetInfo**](rasadminportgetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="b5b8d-122">Use the **RasAdminFreeBuffer** function to free the buffers allocated by the [**RasAdminPortEnum**](rasadminportenum.md) and [**RasAdminPortGetInfo**](rasadminportgetinfo.md) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5b8d-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5b8d-123">Requirements</span></span>



| <span data-ttu-id="b5b8d-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5b8d-124">Requirement</span></span> | <span data-ttu-id="b5b8d-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5b8d-125">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5b8d-126">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b5b8d-126">End of client support</span></span><br/> | <span data-ttu-id="b5b8d-127">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="b5b8d-127">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="b5b8d-128">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="b5b8d-128">End of server support</span></span><br/> | <span data-ttu-id="b5b8d-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b5b8d-129">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="b5b8d-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5b8d-130">Header</span></span><br/>                | <dl> <span data-ttu-id="b5b8d-131"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5b8d-131"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5b8d-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b5b8d-132">Library</span></span><br/>               | <dl> <span data-ttu-id="b5b8d-133"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5b8d-133"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b5b8d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b5b8d-134">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b5b8d-135"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5b8d-135"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5b8d-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5b8d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5b8d-137">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="b5b8d-137">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="b5b8d-138">Fonctions d’administration du serveur RAS</span><span class="sxs-lookup"><span data-stu-id="b5b8d-138">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="b5b8d-139">**RasAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="b5b8d-139">**RasAdminPortEnum**</span></span>](rasadminportenum.md)
</dt> <dt>

[<span data-ttu-id="b5b8d-140">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="b5b8d-140">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

