---
title: RasAdminGetUserAccountServer, fonction (rassapi. h)
description: La fonction RasAdminGetUserAccountServer récupère le nom du serveur qui contient la base de données de comptes d’utilisateur. Utilisez le nom de serveur renvoyé dans les fonctions RasAdminUserGetInfo et RasAdminUserSetInfo pour obtenir ou définir des informations sur un utilisateur spécifié.
ms.assetid: db91aa48-32af-49ac-87ed-8c484926ca15
keywords:
- RasAdminGetUserAccountServer fonction RAS
topic_type:
- apiref
api_name:
- RasAdminGetUserAccountServer
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c506287d94c5ec64445c74d8364a04db98100751
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528122"
---
# <a name="rasadmingetuseraccountserver-function"></a><span data-ttu-id="6b594-105">RasAdminGetUserAccountServer fonction)</span><span class="sxs-lookup"><span data-stu-id="6b594-105">RasAdminGetUserAccountServer function</span></span>

<span data-ttu-id="6b594-106">\[Cette fonction est fournie uniquement pour la compatibilité descendante avec Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="6b594-106">\[This function is provided only for backward compatibility with Windows NT Server 4.0.</span></span> <span data-ttu-id="6b594-107">Elle retourne un \_ appel \_ d’erreur non \_ implémenté sur Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6b594-107">It returns ERROR\_CALL\_NOT\_IMPLEMENTED on Windows Server 2003.</span></span> <span data-ttu-id="6b594-108">Les applications doivent utiliser la fonction [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) .\]</span><span class="sxs-lookup"><span data-stu-id="6b594-108">Applications should use the [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) function.\]</span></span>

<span data-ttu-id="6b594-109">La fonction **RasAdminGetUserAccountServer** récupère le nom du serveur qui contient la base de données de comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6b594-109">The **RasAdminGetUserAccountServer** function retrieves the name of the server that has the user account database.</span></span> <span data-ttu-id="6b594-110">Utilisez le nom de serveur renvoyé dans les fonctions [**RasAdminUserGetInfo**](rasadminusergetinfo.md) et [**RasAdminUserSetInfo**](rasadminusersetinfo.md) pour obtenir ou définir des informations sur un utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="6b594-110">Use the returned server name in the [**RasAdminUserGetInfo**](rasadminusergetinfo.md) and [**RasAdminUserSetInfo**](rasadminusersetinfo.md) functions to get or set information about a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b594-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b594-111">Syntax</span></span>


```C++
DWORD RasAdminGetUserAccountServer(
  _In_  const WCHAR  *lpszDomain,
  _In_  const WCHAR  *lpszServer,
  _Out_       LPWSTR lpszUserAccountServer
);
```



## <a name="parameters"></a><span data-ttu-id="6b594-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b594-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b594-113">*lpszDomain* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b594-113">*lpszDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b594-114">Pointeur vers une chaîne Unicode terminée par le caractère **null** qui spécifie le nom du domaine auquel le serveur RAS appartient.</span><span class="sxs-lookup"><span data-stu-id="6b594-114">Pointer to a **null**-terminated Unicode string that specifies the name of the domain to which the RAS server belongs.</span></span> <span data-ttu-id="6b594-115">Ce paramètre a la **valeur null** pour les applications d’administration RAS qui s’exécutent sur des stations de travail ou des serveurs qui ne sont pas membres d’un domaine.</span><span class="sxs-lookup"><span data-stu-id="6b594-115">This parameter is **NULL** for the RAS administration applications running on workstations or servers that are not members of a domain.</span></span> <span data-ttu-id="6b594-116">Si ce paramètre a la **valeur null**, le paramètre *lpszServer* doit être non **null**.</span><span class="sxs-lookup"><span data-stu-id="6b594-116">If this parameter is **NULL**, the *lpszServer* parameter must be non-**NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6b594-117">*lpszServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b594-117">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b594-118">Pointeur vers une chaîne Unicode terminée par le caractère **null** qui spécifie le nom du serveur RAS.</span><span class="sxs-lookup"><span data-stu-id="6b594-118">Pointer to a **null**-terminated Unicode string that specifies the name of the RAS server.</span></span> <span data-ttu-id="6b594-119">Spécifiez le nom avec les \\ \\ caractères «» de début, sous la forme : \\ \\ *NomServeur*.</span><span class="sxs-lookup"><span data-stu-id="6b594-119">Specify the name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span> <span data-ttu-id="6b594-120">Ce paramètre peut avoir la **valeur null** si le paramètre *lpszDomain* n’a pas la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="6b594-120">This parameter can be **NULL** if the *lpszDomain* parameter is not **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6b594-121">*lpszUserAccountServer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6b594-121">*lpszUserAccountServer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b594-122">Pointeur vers une mémoire tampon qui reçoit une chaîne Unicode terminée par le caractère **null** qui spécifie le nom d’un contrôleur de domaine qui possède la base de données de compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6b594-122">Pointer to a buffer that receives a **null**-terminated Unicode string that specifies the name of a domain controller that has the user account database.</span></span> <span data-ttu-id="6b594-123">La mémoire tampon doit être suffisamment grande pour contenir le nom du serveur (ONCLEn + 1).</span><span class="sxs-lookup"><span data-stu-id="6b594-123">The buffer should be big enough to hold the server name (UNCLEN +1).</span></span> <span data-ttu-id="6b594-124">La fonction préfixe le nom du serveur retourné avec les \\ \\ caractères «» de début, sous la forme : \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="6b594-124">The function prefixes the returned server name with leading "\\\\" characters, in the form: \\\\*servername*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b594-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6b594-125">Return value</span></span>

<span data-ttu-id="6b594-126">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="6b594-126">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="6b594-127">Si la fonction échoue, la valeur de retour peut être le code d’erreur suivant.</span><span class="sxs-lookup"><span data-stu-id="6b594-127">If the function fails, the return value can be the following error code.</span></span>



| <span data-ttu-id="6b594-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b594-128">Value</span></span>                                                                                                    | <span data-ttu-id="6b594-129">Signification</span><span class="sxs-lookup"><span data-stu-id="6b594-129">Meaning</span></span>                                                     |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="6b594-130"><dt>**paramètre d’erreur \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6b594-130"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="6b594-131">*LpszDomain* et *lpszServer* sont tous deux **null**.</span><span class="sxs-lookup"><span data-stu-id="6b594-131">Both *lpszDomain* and *lpszServer* are **NULL**.</span></span><br/> |



 

<span data-ttu-id="6b594-132">Il n’y a pas d’informations d’erreur étendues pour cette fonction. ne pas appeler [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="6b594-132">There is no extended error information for this function; do not call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="6b594-133">Notes</span><span class="sxs-lookup"><span data-stu-id="6b594-133">Remarks</span></span>

<span data-ttu-id="6b594-134">La fonction **RasAdminGetUserAccountServer** obtient le nom du serveur avec la base de données des comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6b594-134">The **RasAdminGetUserAccountServer** function obtains the name of the server with the user accounts database.</span></span> <span data-ttu-id="6b594-135">Cette fonction requiert le nom du serveur RAS ou le nom du domaine dans lequel réside le serveur RAS.</span><span class="sxs-lookup"><span data-stu-id="6b594-135">This function requires the name of the RAS server or the name of the domain in which the RAS server resides.</span></span>

<span data-ttu-id="6b594-136">Le paramètre *lpszDomain* doit spécifier un nom de domaine valide.</span><span class="sxs-lookup"><span data-stu-id="6b594-136">The *lpszDomain* parameter should specify a valid domain name.</span></span> <span data-ttu-id="6b594-137">Ce paramètre a la **valeur null** pour les applications d’administration RAS s’exécutant sur des serveurs qui ne sont pas membres d’un domaine (par exemple, le serveur est dans son propre groupe de travail).</span><span class="sxs-lookup"><span data-stu-id="6b594-137">This parameter is **NULL** for RAS administration applications running on servers that are not members of a domain (for example, the server is in its own workgroup).</span></span> <span data-ttu-id="6b594-138">Dans ce cas, le paramètre *lpszServer* doit spécifier le nom du serveur.</span><span class="sxs-lookup"><span data-stu-id="6b594-138">In this case, the *lpszServer* parameter must specify the server name.</span></span> <span data-ttu-id="6b594-139">Pour récupérer le nom du serveur, appelez la fonction [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) .</span><span class="sxs-lookup"><span data-stu-id="6b594-139">To get the server name, call the [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea) function.</span></span> <span data-ttu-id="6b594-140">Veillez à faire précéder le nom du serveur de \\ \\ caractères «».</span><span class="sxs-lookup"><span data-stu-id="6b594-140">Be sure to prefix the server name with the "\\\\" characters.</span></span>

<span data-ttu-id="6b594-141">Si le nom du serveur spécifié par *lpszServer* est un serveur autonome (autrement dit, si le serveur ou la station de travail n’est pas membre d’un domaine), le nom du serveur lui-même est retourné dans la mémoire tampon *lpszUserAccountServer* .</span><span class="sxs-lookup"><span data-stu-id="6b594-141">If the server name specified by *lpszServer* is a stand-alone server (that is, the server or workstation is not a member of a domain), then the server name itself is returned in the *lpszUserAccountServer* buffer.</span></span>

<span data-ttu-id="6b594-142">Utilisez ensuite le nom du serveur de compte d’utilisateur dans un appel à la fonction [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) pour énumérer les utilisateurs de la base de données des comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6b594-142">Then use the name of the user account server in a call to the [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) function to enumerate the users in the user account database.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b594-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b594-143">Requirements</span></span>



| <span data-ttu-id="6b594-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b594-144">Requirement</span></span> | <span data-ttu-id="6b594-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b594-145">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b594-146">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="6b594-146">End of client support</span></span><br/> | <span data-ttu-id="6b594-147">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="6b594-147">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="6b594-148">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="6b594-148">End of server support</span></span><br/> | <span data-ttu-id="6b594-149">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6b594-149">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="6b594-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="6b594-150">Header</span></span><br/>                | <dl> <span data-ttu-id="6b594-151"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b594-151"><dt>Rassapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="6b594-152">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6b594-152">Library</span></span><br/>               | <dl> <span data-ttu-id="6b594-153"><dt>Rassapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b594-153"><dt>Rassapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="6b594-154">DLL</span><span class="sxs-lookup"><span data-stu-id="6b594-154">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6b594-155"><dt>Rassapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b594-155"><dt>Rassapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b594-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b594-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b594-157">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="6b594-157">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="6b594-158">Fonctions d’administration du serveur RAS</span><span class="sxs-lookup"><span data-stu-id="6b594-158">RAS Server Administration Functions</span></span>](ras-server-administration-functions.md)
</dt> <dt>

[<span data-ttu-id="6b594-159">**GetComputerName**</span><span class="sxs-lookup"><span data-stu-id="6b594-159">**GetComputerName**</span></span>](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> <dt>

[<span data-ttu-id="6b594-160">**RasAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="6b594-160">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)
</dt> <dt>

[<span data-ttu-id="6b594-161">**RasAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="6b594-161">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)
</dt> </dl>

 

