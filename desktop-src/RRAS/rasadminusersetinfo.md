---
title: RasAdminUserSetInfo, fonction (rassapi. h)
description: La fonction RasAdminUserSetInfo définit les autorisations RAS et le numéro de téléphone de rappel pour un utilisateur spécifié.
ms.assetid: 5b049dfd-ecc8-47e4-82cc-71a875752714
keywords:
- RasAdminUserSetInfo fonction RAS
topic_type:
- apiref
api_name:
- RasAdminUserSetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16d35f62713a3f4669db191891d2fb6b1694cabe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535988"
---
# <a name="rasadminusersetinfo-function"></a><span data-ttu-id="9ced3-104">RasAdminUserSetInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="9ced3-104">RasAdminUserSetInfo function</span></span>

<span data-ttu-id="9ced3-105">\[Cette fonction est fournie uniquement pour la compatibilité descendante avec Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="9ced3-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="9ced3-106">Elle retourne un \_ appel \_ d’erreur non \_ implémenté sur Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9ced3-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="9ced3-107">Les applications doivent utiliser la fonction [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) .\]</span><span class="sxs-lookup"><span data-stu-id="9ced3-107">Applications should use the [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) function.\]</span></span>

<span data-ttu-id="9ced3-108">La fonction **RasAdminUserSetInfo** définit les autorisations RAS et le numéro de téléphone de rappel pour un utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="9ced3-108">The **RasAdminUserSetInfo** function sets the RAS permissions and call-back phone number for a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ced3-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ced3-109">Syntax</span></span>


```C++
DWORD RasAdminUserSetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
  _In_ const PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a><span data-ttu-id="9ced3-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ced3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ced3-111">*lpszUserAccountServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9ced3-111">*lpszUserAccountServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ced3-112">Pointeur vers une chaîne Unicode terminée par le caractère null qui spécifie le nom du contrôleur de domaine principal ou secondaire qui possède la base de données de comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9ced3-112">Pointer to a null-terminated Unicode string that specifies the name of the primary or backup domain controller that has the user account database.</span></span> <span data-ttu-id="9ced3-113">Utilisez la fonction [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) pour récupérer ce nom de serveur.</span><span class="sxs-lookup"><span data-stu-id="9ced3-113">Use the [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) function to get this server name.</span></span>

</dd> <dt>

<span data-ttu-id="9ced3-114">*lpszUser* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9ced3-114">*lpszUser* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ced3-115">Pointeur vers une chaîne Unicode terminée par le caractère null qui spécifie le nom de l’utilisateur pour lequel les informations RAS doivent être définies.</span><span class="sxs-lookup"><span data-stu-id="9ced3-115">Pointer to a null-terminated Unicode string that specifies the name of the user for whom RAS information is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="9ced3-116">*pRasUser0* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9ced3-116">*pRasUser0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ced3-117">Pointeur vers la structure d' [**\_ utilisateur RAS \_ 0**](ras-user-0-str.md) qui spécifie les nouvelles données RAS pour l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="9ced3-117">Pointer to the [**RAS\_USER\_0**](ras-user-0-str.md) structure that specifies the new RAS data for the specified user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ced3-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9ced3-118">Return value</span></span>

<span data-ttu-id="9ced3-119">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="9ced3-119">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="9ced3-120">Si la fonction échoue, la valeur de retour peut être l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="9ced3-120">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="9ced3-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ced3-121">Value</span></span>                                                                                                           | <span data-ttu-id="9ced3-122">Description</span><span class="sxs-lookup"><span data-stu-id="9ced3-122">Description</span></span>                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9ced3-123"><dt>**ERREUR de \_ données non valides \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9ced3-123"><dt>**ERROR\_INVALID\_DATA**</dt></span></span> </dl>             | <span data-ttu-id="9ced3-124">La mémoire tampon *pRasUser0* contient des données non valides.</span><span class="sxs-lookup"><span data-stu-id="9ced3-124">The *pRasUser0* buffer contains invalid data.</span></span><br/>                                        |
| <dl> <span data-ttu-id="9ced3-125"><dt>**ERREUR \_ \_ numéro de rappel non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9ced3-125"><dt>**ERROR\_INVALID\_CALLBACK\_NUMBER**</dt></span></span> </dl> | <span data-ttu-id="9ced3-126">Le numéro de rappel spécifié dans la mémoire tampon *pRasUser0* contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="9ced3-126">The callback number specified in the *pRasUser0* buffer contains invalid characters.</span></span><br/> |
| <dl> <span data-ttu-id="9ced3-127"><dt>**NERR \_ BufTooSmall**</dt></span><span class="sxs-lookup"><span data-stu-id="9ced3-127"><dt>**NERR\_BufTooSmall** </dt></span></span> </dl>               | <span data-ttu-id="9ced3-128">Mémoire insuffisante pour exécuter cette fonction.</span><span class="sxs-lookup"><span data-stu-id="9ced3-128">Insufficient memory to perform this function.</span></span><br/>                                        |



 

<span data-ttu-id="9ced3-129">Il n’y a pas d’informations d’erreur étendues pour cette fonction. ne pas appeler [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="9ced3-129">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="9ced3-130">Notes</span><span class="sxs-lookup"><span data-stu-id="9ced3-130">Remarks</span></span>

<span data-ttu-id="9ced3-131">Lors de la définition des autorisations RAS pour un utilisateur, le membre **bfPrivilege** de la structure de l' [**\_ utilisateur RAS \_ 0**](ras-user-0-str.md) doit spécifier au moins l’un des indicateurs de rappel.</span><span class="sxs-lookup"><span data-stu-id="9ced3-131">When setting the RAS permissions for a user, the **bfPrivilege** member of the [**RAS\_USER\_0**](ras-user-0-str.md) structure must specify at least one of the call-back flags.</span></span> <span data-ttu-id="9ced3-132">Par exemple, pour définir les privilèges d’un utilisateur afin d’autoriser les droits d’accès à distance, mais aucun privilège de rappel, définissez **bfPrivilege** sur RASPRIV \_ DialinPrivilege \| RASPRIV \_ nocallback.</span><span class="sxs-lookup"><span data-stu-id="9ced3-132">For example, to set a user's privileges to allow dial-in privilege but no call-back privilege, set **bfPrivilege** to RASPRIV\_DialinPrivilege \| RASPRIV\_NoCallback.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ced3-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ced3-133">Requirements</span></span>



| <span data-ttu-id="9ced3-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ced3-134">Requirement</span></span> | <span data-ttu-id="9ced3-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ced3-135">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ced3-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="9ced3-136">End of client support</span></span><br/> | <span data-ttu-id="9ced3-137">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="9ced3-137">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="9ced3-138">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="9ced3-138">End of server support</span></span><br/> | <span data-ttu-id="9ced3-139">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9ced3-139">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="9ced3-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ced3-140">Header</span></span><br/>                | <dl> <span data-ttu-id="9ced3-141"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ced3-141"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ced3-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9ced3-142">Library</span></span><br/>               | <dl> <span data-ttu-id="9ced3-143"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ced3-143"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="9ced3-144">DLL</span><span class="sxs-lookup"><span data-stu-id="9ced3-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9ced3-145"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ced3-145"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ced3-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ced3-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ced3-147">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="9ced3-147">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="9ced3-148">Fonctions d’administration du serveur RAS</span><span class="sxs-lookup"><span data-stu-id="9ced3-148">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="9ced3-149">**\_Utilisateur RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="9ced3-149">**RAS\_USER\_0**</span></span>](ras-user-0-str.md)
</dt> <dt>

[<span data-ttu-id="9ced3-150">**RasAdminGetUserAccountServer**</span><span class="sxs-lookup"><span data-stu-id="9ced3-150">**RasAdminGetUserAccountServer**</span></span>](rasadmingetuseraccountserver.md)
</dt> <dt>

[<span data-ttu-id="9ced3-151">**RasAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="9ced3-151">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)
</dt> </dl>

 

