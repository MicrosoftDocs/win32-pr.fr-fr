---
title: RasAdminGetErrorString, fonction (rassapi. h)
description: La fonction RasAdminGetErrorString récupère une chaîne de message qui correspond à un code d’erreur RAS renvoyé par l’une des fonctions d’administration de serveur RAS (RasAdmin).
ms.assetid: b51bc1f9-fed7-43b6-9a07-f19ea4c0cd01
keywords:
- RasAdminGetErrorString fonction RAS
topic_type:
- apiref
api_name:
- RasAdminGetErrorString
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc239c5f26061b5234631079ba21ce0d24ad570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524005"
---
# <a name="rasadmingeterrorstring-function"></a><span data-ttu-id="b014c-104">RasAdminGetErrorString fonction)</span><span class="sxs-lookup"><span data-stu-id="b014c-104">RasAdminGetErrorString function</span></span>

<span data-ttu-id="b014c-105">\[Cette fonction est fournie uniquement pour la compatibilité descendante avec Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="b014c-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="b014c-106">Elle retourne un \_ appel \_ d’erreur non \_ implémenté sur Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b014c-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="b014c-107">Les applications doivent utiliser la fonction [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) .\]</span><span class="sxs-lookup"><span data-stu-id="b014c-107">Applications should use the [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring) function.\]</span></span>

<span data-ttu-id="b014c-108">La fonction **RasAdminGetErrorString** récupère une chaîne de message qui correspond à un code d’erreur RAS renvoyé par l’une des fonctions d’administration de serveur RAS (RasAdmin).</span><span class="sxs-lookup"><span data-stu-id="b014c-108">The **RasAdminGetErrorString** function retrieves a message string that corresponds to a RAS error code returned by one of the RAS server administration (RasAdmin) functions.</span></span> <span data-ttu-id="b014c-109">Ces chaînes de message sont extraites de la Rasmsg.dll installée dans le cadre du service RAS.</span><span class="sxs-lookup"><span data-stu-id="b014c-109">These message strings are retrieved from the Rasmsg.dll that is installed as part of RAS.</span></span>

## <a name="syntax"></a><span data-ttu-id="b014c-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b014c-110">Syntax</span></span>


```C++
DWORD RasAdminGetErrorString(
  _In_  UINT  ResourceId,
  _Out_ WCHAR *lpszString,
  _In_  DWORD InBufSize
);
```



## <a name="parameters"></a><span data-ttu-id="b014c-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b014c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b014c-112">*ResourceId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b014c-112">*ResourceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b014c-113">Spécifie un code d’erreur retourné par l’une des fonctions RasAdmin.</span><span class="sxs-lookup"><span data-stu-id="b014c-113">Specifies an error code returned by one of the RasAdmin functions.</span></span> <span data-ttu-id="b014c-114">Cette valeur doit être comprise dans la plage de codes d’erreur de RASBASE à RASBASEEND.</span><span class="sxs-lookup"><span data-stu-id="b014c-114">This value must be in the range of error codes from RASBASE to RASBASEEND.</span></span> <span data-ttu-id="b014c-115">Celles-ci sont définies dans Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="b014c-115">These are defined in Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="b014c-116">*lpszString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b014c-116">*lpszString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b014c-117">Pointeur vers une mémoire tampon qui reçoit le message d’erreur qui correspond au code d’erreur spécifié.</span><span class="sxs-lookup"><span data-stu-id="b014c-117">Pointer to a buffer that receives the error message that corresponds to the specified error code.</span></span>

</dd> <dt>

<span data-ttu-id="b014c-118">*InBufSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b014c-118">*InBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b014c-119">Spécifie la taille, en caractères, de la mémoire tampon *lpszString* .</span><span class="sxs-lookup"><span data-stu-id="b014c-119">Specifies the size, in characters, of the *lpszString* buffer.</span></span> <span data-ttu-id="b014c-120">Les messages d’erreur sont généralement de 80 caractères au maximum ; une taille de mémoire tampon de 512 caractères est toujours appropriée.</span><span class="sxs-lookup"><span data-stu-id="b014c-120">Error messages are typically 80 characters or less; a buffer size of 512 characters is always adequate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b014c-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b014c-121">Return value</span></span>

<span data-ttu-id="b014c-122">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="b014c-122">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="b014c-123">Si la fonction échoue, la valeur de retour est un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b014c-123">If the function fails, the return value is an error code.</span></span> <span data-ttu-id="b014c-124">Cette valeur peut être une dernière valeur d’erreur définie par les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc)ou [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) . Il peut s’agir de l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="b014c-124">This value can be a last error value set by the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc), or [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) functions; or it can be one of the following error codes.</span></span>



| <span data-ttu-id="b014c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="b014c-125">Value</span></span>                                                                                                      | <span data-ttu-id="b014c-126">Signification</span><span class="sxs-lookup"><span data-stu-id="b014c-126">Meaning</span></span>                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b014c-127"><dt>**paramètre d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b014c-127"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>   | <span data-ttu-id="b014c-128">Les paramètres *ResourceId* ou *lpszString* ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="b014c-128">The *ResourceId* or *lpszString* parameters are invalid.</span></span><br/>      |
| <dl> <span data-ttu-id="b014c-129"><dt>**ERREUR \_ de \_ mémoire tampon insuffisante**</dt></span><span class="sxs-lookup"><span data-stu-id="b014c-129"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="b014c-130">La taille spécifiée par le paramètre *InBufSize* est trop petite.</span><span class="sxs-lookup"><span data-stu-id="b014c-130">The size specified by the *InBufSize* parameter is too small.</span></span><br/> |



 

<span data-ttu-id="b014c-131">Il n’y a pas d’informations d’erreur étendues pour cette fonction. ne pas appeler [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="b014c-131">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="b014c-132">Notes</span><span class="sxs-lookup"><span data-stu-id="b014c-132">Remarks</span></span>

<span data-ttu-id="b014c-133">Les fonctions RasAdmin peuvent retourner des codes d’erreur qui ne sont pas dans la plage prise en charge par la fonction **RasAdminGetErrorString** .</span><span class="sxs-lookup"><span data-stu-id="b014c-133">The RasAdmin functions can return error codes that are not in the range supported by the **RasAdminGetErrorString** function.</span></span> <span data-ttu-id="b014c-134">Par exemple, les fonctions RasAdmin peuvent retourner des codes d’erreur définis dans Lmerr. h et winerror. h.</span><span class="sxs-lookup"><span data-stu-id="b014c-134">For example, the RasAdmin functions can return error codes that are defined in Lmerr.h and Winerror.h.</span></span> <span data-ttu-id="b014c-135">Avant d’appeler **RasAdminGetErrorString**, vérifiez que le code d’erreur se trouve dans la plage RASBASE à RASBASEEND, comme défini dans Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="b014c-135">Before calling **RasAdminGetErrorString**, verify that the error code is in the range RASBASE to RASBASEEND, as defined in Raserror.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="b014c-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b014c-136">Requirements</span></span>



| <span data-ttu-id="b014c-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b014c-137">Requirement</span></span> | <span data-ttu-id="b014c-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="b014c-138">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b014c-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b014c-139">End of client support</span></span><br/> | <span data-ttu-id="b014c-140">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="b014c-140">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="b014c-141">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="b014c-141">End of server support</span></span><br/> | <span data-ttu-id="b014c-142">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b014c-142">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="b014c-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="b014c-143">Header</span></span><br/>                | <dl> <span data-ttu-id="b014c-144"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b014c-144"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="b014c-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b014c-145">Library</span></span><br/>               | <dl> <span data-ttu-id="b014c-146"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b014c-146"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b014c-147">DLL</span><span class="sxs-lookup"><span data-stu-id="b014c-147">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b014c-148"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b014c-148"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b014c-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b014c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b014c-150">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="b014c-150">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="b014c-151">Fonctions d’administration du serveur RAS</span><span class="sxs-lookup"><span data-stu-id="b014c-151">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="b014c-152">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="b014c-152">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="b014c-153">**GlobalAlloc**</span><span class="sxs-lookup"><span data-stu-id="b014c-153">**GlobalAlloc**</span></span>](/windows/win32/api/winbase/nf-winbase-globalalloc)
</dt> <dt>

[<span data-ttu-id="b014c-154">**LoadString**</span><span class="sxs-lookup"><span data-stu-id="b014c-154">**LoadString**</span></span>](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> </dl>

 

