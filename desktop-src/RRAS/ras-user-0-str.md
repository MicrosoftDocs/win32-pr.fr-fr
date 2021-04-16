---
title: Structure RAS_USER_0 (rassapi. h)
description: La structure de l' \_ utilisateur RAS \_ 0 est utilisée dans les fonctions RasAdminUserSetInfo et RasAdminUserGetInfo pour spécifier des informations sur un utilisateur.
ms.assetid: a2d4a935-f46d-4bc2-ada8-beaa3ac74834
keywords:
- RAS_USER_0 de la structure RAS
- Point d’accès RAS du pointeur de structure PRAS_USER_0
topic_type:
- apiref
api_name:
- RAS_USER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c79a6b946ed9d10cd2bfc989f8cde27fad2ffa92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508534"
---
# <a name="ras_user_0-structure"></a><span data-ttu-id="d02a4-105">Structure de l' \_ utilisateur RAS \_ 0</span><span class="sxs-lookup"><span data-stu-id="d02a4-105">RAS\_USER\_0 structure</span></span>

<span data-ttu-id="d02a4-106">\[Cette version de la structure de l' **\_ utilisateur RAS \_ 0** n’est pas prise en charge à partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d02a4-106">\[This version of the **RAS\_USER\_0** structure is not supported as of Windows Vista.</span></span> <span data-ttu-id="d02a4-107">Utilisez à la place l' [**\_ utilisateur RAS \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) plus récent défini dans mprapi. h.\]</span><span class="sxs-lookup"><span data-stu-id="d02a4-107">Use the newer [**RAS\_USER\_0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) defined in mprapi.h instead.\]</span></span>

<span data-ttu-id="d02a4-108">La structure de l' **\_ utilisateur RAS \_ 0** est utilisée dans les fonctions [**RasAdminUserSetInfo**](rasadminusersetinfo.md) et [**RasAdminUserGetInfo**](rasadminusergetinfo.md) pour spécifier des informations sur un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d02a4-108">The **RAS\_USER\_0** structure is used in the [**RasAdminUserSetInfo**](rasadminusersetinfo.md) and [**RasAdminUserGetInfo**](rasadminusergetinfo.md) functions to specify information about a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="d02a4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d02a4-109">Syntax</span></span>


```C++
typedef struct _RAS_USER_0 {
  BYTE  bfPrivilege;
  WCHAR szPhoneNumber[RASSAPI_MAX_PHONENUMBER_SIZE + 1];
} RAS_USER_0, *PRAS_USER_0;
```



## <a name="members"></a><span data-ttu-id="d02a4-110">Membres</span><span class="sxs-lookup"><span data-stu-id="d02a4-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="d02a4-111">**bfPrivilege**</span><span class="sxs-lookup"><span data-stu-id="d02a4-111">**bfPrivilege**</span></span>
</dt> <dd>

<span data-ttu-id="d02a4-112">Jeu d’indicateurs binaires qui spécifient les privilèges d’accès distant de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d02a4-112">A set of bit flags that specify the RAS privileges of the user.</span></span> <span data-ttu-id="d02a4-113">Ce membre peut être une combinaison de l' \_ indicateur RASPRIV DialinPrivilege et de l’un des indicateurs de rappel.</span><span class="sxs-lookup"><span data-stu-id="d02a4-113">This member can be a combination of the RASPRIV\_DialinPrivilege flag and one of the call-back flags.</span></span> <span data-ttu-id="d02a4-114">Utilisez le \_ masque RASPRIV CallbackType pour identifier le type de privilège de rappel fourni à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d02a4-114">Use the RASPRIV\_CallbackType mask to identify the type of call-back privilege provided to the user.</span></span> <span data-ttu-id="d02a4-115">Les indicateurs suivants sont définis.</span><span class="sxs-lookup"><span data-stu-id="d02a4-115">The following flags are defined.</span></span>



| <span data-ttu-id="d02a4-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d02a4-116">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="d02a4-117">Signification</span><span class="sxs-lookup"><span data-stu-id="d02a4-117">Meaning</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="RASPRIV_NoCallback"></span><span id="raspriv_nocallback"></span><span id="RASPRIV_NOCALLBACK"></span><dl> <span data-ttu-id="d02a4-118"><dt>**RASPRIV \_ Nocallback**</dt></span><span class="sxs-lookup"><span data-stu-id="d02a4-118"><dt>**RASPRIV\_NoCallback**</dt></span></span> </dl>                             | <span data-ttu-id="d02a4-119">L’utilisateur n’a pas de privilège de rappel.</span><span class="sxs-lookup"><span data-stu-id="d02a4-119">The user has no call-back privilege.</span></span><br/>                                               |
| <span id="RASPRIV_AdminSetCallback"></span><span id="raspriv_adminsetcallback"></span><span id="RASPRIV_ADMINSETCALLBACK"></span><dl> <span data-ttu-id="d02a4-120"><dt>**RASPRIV \_ AdminSetCallback**</dt></span><span class="sxs-lookup"><span data-stu-id="d02a4-120"><dt>**RASPRIV\_AdminSetCallback**</dt></span></span> </dl>     | <span data-ttu-id="d02a4-121">Le compte d’utilisateur est configuré pour demander à l’administrateur de définir le numéro de rappel.</span><span class="sxs-lookup"><span data-stu-id="d02a4-121">The user account is configured to have the administrator set the call-back number.</span></span><br/> |
| <span id="RASPRIV_CallerSetCallback"></span><span id="raspriv_callersetcallback"></span><span id="RASPRIV_CALLERSETCALLBACK"></span><dl> <span data-ttu-id="d02a4-122"><dt>**RASPRIV \_ CallerSetCallback**</dt></span><span class="sxs-lookup"><span data-stu-id="d02a4-122"><dt>**RASPRIV\_CallerSetCallback**</dt></span></span> </dl> | <span data-ttu-id="d02a4-123">L’utilisateur distant peut spécifier un numéro de téléphone de rappel lors de la numérotation.</span><span class="sxs-lookup"><span data-stu-id="d02a4-123">The remote user can specify a call-back phone number when dialing in.</span></span><br/>              |
| <span id="RASPRIV_DialinPrivilege"></span><span id="raspriv_dialinprivilege"></span><span id="RASPRIV_DIALINPRIVILEGE"></span><dl> <span data-ttu-id="d02a4-124"><dt>**RASPRIV \_ DialinPrivilege**</dt></span><span class="sxs-lookup"><span data-stu-id="d02a4-124"><dt>**RASPRIV\_DialinPrivilege**</dt></span></span> </dl>         | <span data-ttu-id="d02a4-125">L’utilisateur a l’autorisation de se connecter à ce serveur.</span><span class="sxs-lookup"><span data-stu-id="d02a4-125">The user has permission to dial in to this server.</span></span><br/>                                 |



 

<span data-ttu-id="d02a4-126">Spécifiez l’un des indicateurs de rappel dans l’appel à la fonction [**RasAdminUserSetInfo**](rasadminusersetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="d02a4-126">Specify one of the call-back flags in the call to the [**RasAdminUserSetInfo**](rasadminusersetinfo.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d02a4-127">**szPhoneNumber**</span><span class="sxs-lookup"><span data-stu-id="d02a4-127">**szPhoneNumber**</span></span>
</dt> <dd>

<span data-ttu-id="d02a4-128">Chaîne Unicode se terminant par un caractère null qui spécifie le numéro de téléphone de rappel de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d02a4-128">A null-terminated Unicode string that specifies the call-back phone number for the user.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d02a4-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d02a4-129">Requirements</span></span>



| <span data-ttu-id="d02a4-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d02a4-130">Requirement</span></span> | <span data-ttu-id="d02a4-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="d02a4-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d02a4-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d02a4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d02a4-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d02a4-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d02a4-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d02a4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d02a4-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d02a4-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d02a4-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d02a4-136">End of client support</span></span><br/>    | <span data-ttu-id="d02a4-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d02a4-137">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="d02a4-138">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="d02a4-138">End of server support</span></span><br/>    | <span data-ttu-id="d02a4-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d02a4-139">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="d02a4-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="d02a4-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d02a4-141"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d02a4-141"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d02a4-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d02a4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d02a4-143">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="d02a4-143">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="d02a4-144">Structures d’administration de serveur RAS</span><span class="sxs-lookup"><span data-stu-id="d02a4-144">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="d02a4-145">**RasAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="d02a4-145">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)
</dt> <dt>

[<span data-ttu-id="d02a4-146">**RasAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="d02a4-146">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)
</dt> </dl>

 

 





