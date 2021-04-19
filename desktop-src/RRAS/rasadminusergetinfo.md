---
title: RasAdminUserGetInfo, fonction (rassapi. h)
description: La fonction RasAdminUserGetInfo obtient les informations d’autorisation RAS et le numéro de téléphone de rappel pour un utilisateur spécifié.
ms.assetid: 178ff775-9cd2-43f0-9a9a-dbae337c5fe8
keywords:
- RasAdminUserGetInfo fonction RAS
topic_type:
- apiref
api_name:
- RasAdminUserGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89fe08a918a958ffb5a656ce2c76cecec31cbb61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533057"
---
# <a name="rasadminusergetinfo-function"></a><span data-ttu-id="3a26a-104">RasAdminUserGetInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="3a26a-104">RasAdminUserGetInfo function</span></span>

<span data-ttu-id="3a26a-105">\[Cette fonction est fournie uniquement pour la compatibilité descendante avec Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="3a26a-105">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="3a26a-106">Elle retourne un \_ appel \_ d’erreur non \_ implémenté sur Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3a26a-106">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="3a26a-107">Les applications doivent utiliser la fonction [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) .\]</span><span class="sxs-lookup"><span data-stu-id="3a26a-107">Applications should use the [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) function.\]</span></span>

<span data-ttu-id="3a26a-108">La fonction **RasAdminUserGetInfo** obtient les informations d’autorisation RAS et le numéro de téléphone de rappel pour un utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="3a26a-108">The **RasAdminUserGetInfo** function gets the RAS permissions and callback phone number information for a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a26a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a26a-109">Syntax</span></span>


```C++
DWORD RasAdminUserGetInfo(
  _In_ const WCHAR       *lpszUserAccountServer,
  _In_ const WCHAR       *lpszUser,
             PRAS_USER_0 pRasUser0
);
```



## <a name="parameters"></a><span data-ttu-id="3a26a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a26a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a26a-111">*lpszUserAccountServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3a26a-111">*lpszUserAccountServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a26a-112">Pointeur vers une chaîne Unicode terminée par le caractère null qui spécifie le nom du contrôleur de domaine principal ou secondaire qui possède la base de données de comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3a26a-112">Pointer to a null-terminated Unicode string that specifies the name of the primary or backup domain controller that has the user account database.</span></span> <span data-ttu-id="3a26a-113">Utilisez la fonction [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) pour récupérer ce nom de serveur.</span><span class="sxs-lookup"><span data-stu-id="3a26a-113">Use the [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) function to get this server name.</span></span>

</dd> <dt>

<span data-ttu-id="3a26a-114">*lpszUser* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3a26a-114">*lpszUser* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a26a-115">Pointeur vers une chaîne Unicode terminée par le caractère null qui spécifie le nom de l’utilisateur pour lequel obtenir des informations RAS.</span><span class="sxs-lookup"><span data-stu-id="3a26a-115">Pointer to a null-terminated Unicode string that specifies the name of the user for whom to get RAS information.</span></span>

</dd> <dt>

<span data-ttu-id="3a26a-116">*pRasUser0*</span><span class="sxs-lookup"><span data-stu-id="3a26a-116">*pRasUser0*</span></span> 
</dt> <dd>

<span data-ttu-id="3a26a-117">Pointeur vers la structure d' [**\_ utilisateur RAS \_ 0**](ras-user-0-str.md) qui reçoit les données RAS pour l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="3a26a-117">Pointer to the [**RAS\_USER\_0**](ras-user-0-str.md) structure that receives the RAS data for the specified user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a26a-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3a26a-118">Return value</span></span>

<span data-ttu-id="3a26a-119">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="3a26a-119">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="3a26a-120">Si la fonction échoue, la valeur de retour peut être le code d’erreur suivant.</span><span class="sxs-lookup"><span data-stu-id="3a26a-120">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="3a26a-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a26a-121">Value</span></span>                                                                                            | <span data-ttu-id="3a26a-122">Signification</span><span class="sxs-lookup"><span data-stu-id="3a26a-122">Meaning</span></span>                                                  |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="3a26a-123"><dt>**NERR \_ BufTooSmall**</dt></span><span class="sxs-lookup"><span data-stu-id="3a26a-123"><dt>**NERR\_BufTooSmall**</dt></span></span> </dl> | <span data-ttu-id="3a26a-124">Mémoire insuffisante pour exécuter cette fonction.</span><span class="sxs-lookup"><span data-stu-id="3a26a-124">Insufficient memory to perform this function.</span></span><br/> |



 

<span data-ttu-id="3a26a-125">Il n’y a pas d’informations d’erreur étendues pour cette fonction. ne pas appeler [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="3a26a-125">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a26a-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a26a-126">Requirements</span></span>



| <span data-ttu-id="3a26a-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a26a-127">Requirement</span></span> | <span data-ttu-id="3a26a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a26a-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a26a-129">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="3a26a-129">End of client support</span></span><br/> | <span data-ttu-id="3a26a-130">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="3a26a-130">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="3a26a-131">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="3a26a-131">End of server support</span></span><br/> | <span data-ttu-id="3a26a-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3a26a-132">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="3a26a-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="3a26a-133">Header</span></span><br/>                | <dl> <span data-ttu-id="3a26a-134"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a26a-134"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a26a-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3a26a-135">Library</span></span><br/>               | <dl> <span data-ttu-id="3a26a-136"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a26a-136"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="3a26a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3a26a-137">DLL</span></span><br/>                   | <dl> <span data-ttu-id="3a26a-138"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a26a-138"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a26a-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a26a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a26a-140">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="3a26a-140">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="3a26a-141">Fonctions d’administration du serveur RAS</span><span class="sxs-lookup"><span data-stu-id="3a26a-141">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="3a26a-142">**\_Utilisateur RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="3a26a-142">**RAS\_USER\_0**</span></span>](ras-user-0-str.md)
</dt> <dt>

[<span data-ttu-id="3a26a-143">**RasAdminGetUserAccountServer**</span><span class="sxs-lookup"><span data-stu-id="3a26a-143">**RasAdminGetUserAccountServer**</span></span>](rasadmingetuseraccountserver.md)
</dt> <dt>

[<span data-ttu-id="3a26a-144">**RasAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="3a26a-144">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)
</dt> </dl>

 

