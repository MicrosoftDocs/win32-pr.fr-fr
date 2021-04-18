---
title: RasAdminPortDisconnect, fonction (rassapi. h)
description: La fonction RasAdminPortDisconnect déconnecte un port en cours d’utilisation.
ms.assetid: 7ed3bc46-2d56-44c8-afd5-fcbdad0f7f3a
keywords:
- RasAdminPortDisconnect fonction RAS
topic_type:
- apiref
api_name:
- RasAdminPortDisconnect
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee05e7927bd6c9adb086a09f76b9022affd74792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533157"
---
# <a name="rasadminportdisconnect-function"></a><span data-ttu-id="67876-104">RasAdminPortDisconnect fonction)</span><span class="sxs-lookup"><span data-stu-id="67876-104">RasAdminPortDisconnect function</span></span>

<span data-ttu-id="67876-105">\[Cette fonction est fournie uniquement pour la compatibilité descendante avec Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="67876-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="67876-106">Elle retourne un \_ appel \_ d’erreur non \_ implémenté sur Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="67876-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="67876-107">Les applications doivent utiliser la fonction [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) .\]</span><span class="sxs-lookup"><span data-stu-id="67876-107">Applications should use the [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect) function.\]</span></span>

<span data-ttu-id="67876-108">La fonction **RasAdminPortDisconnect** déconnecte un port en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="67876-108">The **RasAdminPortDisconnect** function disconnects a port that is currently in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="67876-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67876-109">Syntax</span></span>


```C++
DWORD RasAdminPortDisconnect(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a><span data-ttu-id="67876-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67876-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67876-111">*lpszServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="67876-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67876-112">Pointeur vers une chaîne Unicode terminée par le caractère null qui spécifie le nom du serveur RAS Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="67876-112">Pointer to a null-terminated Unicode string that specifies the name of the Windows NT/Windows 2000 RAS server.</span></span> <span data-ttu-id="67876-113">Spécifiez le nom avec les \\ \\ caractères «» de début, sous la forme : \\ \\ *NomServeur*.</span><span class="sxs-lookup"><span data-stu-id="67876-113">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> <dt>

<span data-ttu-id="67876-114">*lpszPort* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="67876-114">*lpszPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67876-115">Pointeur vers une chaîne Unicode terminée par le caractère null qui spécifie le nom du port sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="67876-115">Pointer to a null-terminated Unicode string that specifies the name of the port on the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67876-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="67876-116">Return value</span></span>

<span data-ttu-id="67876-117">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="67876-117">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="67876-118">Si la fonction échoue, la valeur de retour peut être l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="67876-118">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="67876-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="67876-119">Value</span></span>                                                                                               | <span data-ttu-id="67876-120">Signification</span><span class="sxs-lookup"><span data-stu-id="67876-120">Meaning</span></span>                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="67876-121"><dt>**PORT d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="67876-121"><dt>**ERROR\_INVALID\_PORT**</dt></span></span> </dl> | <span data-ttu-id="67876-122">Le port spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="67876-122">The specified port is invalid.</span></span><br/>    |
| <dl> <span data-ttu-id="67876-123"><dt>**NERR \_ UserNotFound**</dt></span><span class="sxs-lookup"><span data-stu-id="67876-123"><dt>**NERR\_UserNotFound**</dt></span></span> </dl>   | <span data-ttu-id="67876-124">Le port n’est pas en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="67876-124">The port is not currently in use.</span></span><br/> |



 

<span data-ttu-id="67876-125">Il n’y a pas d’informations d’erreur étendues pour cette fonction. ne pas appeler [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="67876-125">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="67876-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67876-126">Requirements</span></span>



| <span data-ttu-id="67876-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67876-127">Requirement</span></span> | <span data-ttu-id="67876-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="67876-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67876-129">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="67876-129">End of client support</span></span><br/> | <span data-ttu-id="67876-130">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="67876-130">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="67876-131">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="67876-131">End of server support</span></span><br/> | <span data-ttu-id="67876-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="67876-132">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="67876-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="67876-133">Header</span></span><br/>                | <dl> <span data-ttu-id="67876-134"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="67876-134"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="67876-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="67876-135">Library</span></span><br/>               | <dl> <span data-ttu-id="67876-136"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67876-136"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="67876-137">DLL</span><span class="sxs-lookup"><span data-stu-id="67876-137">DLL</span></span><br/>                   | <dl> <span data-ttu-id="67876-138"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67876-138"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67876-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67876-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67876-140">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="67876-140">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="67876-141">Fonctions d’administration du serveur RAS</span><span class="sxs-lookup"><span data-stu-id="67876-141">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> </dl>

 

