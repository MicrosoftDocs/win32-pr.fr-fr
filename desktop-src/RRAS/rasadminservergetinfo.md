---
title: RasAdminServerGetInfo, fonction (rassapi. h)
description: La fonction RasAdminServerGetInfo obtient la configuration du serveur d’un serveur RAS.
ms.assetid: a1c371fd-462c-443c-8016-592efb2f0b1a
keywords:
- RasAdminServerGetInfo fonction RAS
topic_type:
- apiref
api_name:
- RasAdminServerGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115a2421db5efbafb72d73952684ff7758c6995b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542678"
---
# <a name="rasadminservergetinfo-function"></a><span data-ttu-id="57be2-104">RasAdminServerGetInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="57be2-104">RasAdminServerGetInfo function</span></span>

<span data-ttu-id="57be2-105">\[Cette fonction est fournie uniquement pour la compatibilité descendante avec Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="57be2-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="57be2-106">Elle retourne un \_ appel \_ d’erreur non \_ implémenté sur Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="57be2-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="57be2-107">Les applications doivent utiliser la fonction [**MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) .\]</span><span class="sxs-lookup"><span data-stu-id="57be2-107">Applications should use the [**MprAdminServerGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminservergetinfo) function.\]</span></span>

<span data-ttu-id="57be2-108">La fonction **RasAdminServerGetInfo** obtient la configuration du serveur d’un serveur RAS.</span><span class="sxs-lookup"><span data-stu-id="57be2-108">The **RasAdminServerGetInfo** function gets the server configuration of a RAS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="57be2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57be2-109">Syntax</span></span>


```C++
DWORD RasAdminServerGetInfo(
  _In_  const WCHAR         *lpszServer,
  _Out_       PRAS_SERVER_0 pRasServer0
);
```



## <a name="parameters"></a><span data-ttu-id="57be2-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57be2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57be2-111">*lpszServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="57be2-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57be2-112">Pointeur vers une chaîne Unicode terminée par le caractère **null** qui spécifie le nom du serveur RAS Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="57be2-112">Pointer to a **null**-terminated Unicode string that specifies the name of the Windows NT/Windows 2000 RAS server.</span></span> <span data-ttu-id="57be2-113">Si ce paramètre a la **valeur null**, la fonction retourne des informations sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="57be2-113">If this parameter is **NULL**, the function returns information about the local computer.</span></span> <span data-ttu-id="57be2-114">Spécifiez le nom avec les \\ \\ caractères «» de début, sous la forme : \\ \\ *NomServeur*.</span><span class="sxs-lookup"><span data-stu-id="57be2-114">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="57be2-115">*pRasServer0* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="57be2-115">*pRasServer0* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57be2-116">Pointeur vers la structure du [**\_ serveur RAS \_ 0**](ras-server-0-str.md) qui reçoit le nombre de ports configurés sur le serveur, le nombre de ports en cours d’utilisation et le numéro de version du serveur.</span><span class="sxs-lookup"><span data-stu-id="57be2-116">Pointer to the [**RAS\_SERVER\_0**](ras-server-0-str.md) structure that receives the number of ports configured on the server, the number of ports currently in use, and the server version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57be2-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="57be2-117">Return value</span></span>

<span data-ttu-id="57be2-118">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="57be2-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="57be2-119">Si la fonction échoue, la valeur de retour est un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="57be2-119">If the function fails, the return value is an error code.</span></span> <span data-ttu-id="57be2-120">Les codes d’erreur possibles incluent ceux retournés par [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour la fonction [**CallNamedPipe**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) .</span><span class="sxs-lookup"><span data-stu-id="57be2-120">Possible error codes include those returned by [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) for the [**CallNamedPipe**](/windows/desktop/api/winbase/nf-winbase-callnamedpipea) function.</span></span> <span data-ttu-id="57be2-121">Il n’y a pas d’informations d’erreur étendues pour cette fonction. ne pas appeler **GetLastError**.</span><span class="sxs-lookup"><span data-stu-id="57be2-121">There is no extended error information for this function; do not call **GetLastError**.</span></span>

## <a name="remarks"></a><span data-ttu-id="57be2-122">Notes</span><span class="sxs-lookup"><span data-stu-id="57be2-122">Remarks</span></span>

<span data-ttu-id="57be2-123">Pour énumérer tous les serveurs RAS dans un domaine, appelez la fonction [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) et spécifiez la \_ \_ numérotation de type SV pour le paramètre *ServerType* .</span><span class="sxs-lookup"><span data-stu-id="57be2-123">To enumerate all RAS servers in a domain, call the [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) function and specify SV\_TYPE\_DIALIN for the *servertype* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="57be2-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57be2-124">Requirements</span></span>



| <span data-ttu-id="57be2-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57be2-125">Requirement</span></span> | <span data-ttu-id="57be2-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="57be2-126">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57be2-127">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="57be2-127">End of client support</span></span><br/> | <span data-ttu-id="57be2-128">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="57be2-128">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="57be2-129">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="57be2-129">End of server support</span></span><br/> | <span data-ttu-id="57be2-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="57be2-130">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="57be2-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="57be2-131">Header</span></span><br/>                | <dl> <span data-ttu-id="57be2-132"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="57be2-132"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="57be2-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="57be2-133">Library</span></span><br/>               | <dl> <span data-ttu-id="57be2-134"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57be2-134"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="57be2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="57be2-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="57be2-136"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57be2-136"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57be2-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57be2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57be2-138">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="57be2-138">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="57be2-139">Fonctions d’administration du serveur RAS</span><span class="sxs-lookup"><span data-stu-id="57be2-139">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="57be2-140">**NetServerEnum**</span><span class="sxs-lookup"><span data-stu-id="57be2-140">**NetServerEnum**</span></span>](/windows/win32/api/lmserver/nf-lmserver-netserverenum)
</dt> <dt>

[<span data-ttu-id="57be2-141">**\_Serveur RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="57be2-141">**RAS\_SERVER\_0**</span></span>](ras-server-0-str.md)
</dt> </dl>

 

