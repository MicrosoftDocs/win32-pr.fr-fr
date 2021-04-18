---
title: Structure RAS_SERVER_0 (rassapi. h)
description: La \_ structure du serveur RAS \_ 0 est utilisée par la fonction RasAdminServerGetInfo pour retourner des informations sur les ports configurés sur un serveur RAS.
ms.assetid: 8818ad68-b528-45fe-9ff4-eea194259f25
keywords:
- RAS_SERVER_0 de la structure RAS
- Point d’accès RAS du pointeur de structure PRAS_SERVER_0
topic_type:
- apiref
api_name:
- RAS_SERVER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16f910fdfe53221daf8227d9f3e594133548fee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509124"
---
# <a name="ras_server_0-structure"></a><span data-ttu-id="7779a-105">\_Structure du serveur RAS \_ 0</span><span class="sxs-lookup"><span data-stu-id="7779a-105">RAS\_SERVER\_0 structure</span></span>

<span data-ttu-id="7779a-106">\[La structure du **\_ serveur RAS \_ 0** n’est pas prise en charge à partir de Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="7779a-106">\[The **RAS\_SERVER\_0** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="7779a-107">La structure du **\_ serveur RAS \_ 0** est utilisée par la fonction [**RasAdminServerGetInfo**](rasadminservergetinfo.md) pour retourner des informations sur les ports configurés sur un serveur RAS.</span><span class="sxs-lookup"><span data-stu-id="7779a-107">The **RAS\_SERVER\_0** structure is used by the [**RasAdminServerGetInfo**](rasadminservergetinfo.md) function to return information about the ports configured on a RAS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="7779a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7779a-108">Syntax</span></span>


```C++
typedef struct _RAS_SERVER_0 {
  WORD  TotalPorts;
  WORD  PortsInUse;
  DWORD RasVersion;
} RAS_SERVER_0, *PRAS_SERVER_0;
```



## <a name="members"></a><span data-ttu-id="7779a-109">Membres</span><span class="sxs-lookup"><span data-stu-id="7779a-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="7779a-110">**TotalPorts**</span><span class="sxs-lookup"><span data-stu-id="7779a-110">**TotalPorts**</span></span>
</dt> <dd>

<span data-ttu-id="7779a-111">Spécifie le nombre total de ports configurés sur le serveur RAS et disponibles pour la connexion des clients distants.</span><span class="sxs-lookup"><span data-stu-id="7779a-111">Specifies the total number of ports configured on the RAS server that are available for remote clients to connect to.</span></span> <span data-ttu-id="7779a-112">Par exemple, si le nombre total de ports configurés pour la connexion à un serveur est de quatre, mais que l’un des ports est actuellement utilisé pour la numérotation, **TotalPorts** est trois.</span><span class="sxs-lookup"><span data-stu-id="7779a-112">For example, if the total number of ports configured for dialing in to a server is four, but one of the ports is currently in use for dialing out, **TotalPorts** is three.</span></span>

</dd> <dt>

<span data-ttu-id="7779a-113">**PortsInUse**</span><span class="sxs-lookup"><span data-stu-id="7779a-113">**PortsInUse**</span></span>
</dt> <dd>

<span data-ttu-id="7779a-114">Spécifie le nombre de ports actuellement utilisés par les clients distants.</span><span class="sxs-lookup"><span data-stu-id="7779a-114">Specifies the number of ports currently in use by remote clients.</span></span>

</dd> <dt>

<span data-ttu-id="7779a-115">**RasVersion**</span><span class="sxs-lookup"><span data-stu-id="7779a-115">**RasVersion**</span></span>
</dt> <dd>

<span data-ttu-id="7779a-116">Spécifie la version du serveur RAS.</span><span class="sxs-lookup"><span data-stu-id="7779a-116">Specifies the version of the RAS server.</span></span> <span data-ttu-id="7779a-117">Utilisez ces informations pour prendre une mesure propre à la version.</span><span class="sxs-lookup"><span data-stu-id="7779a-117">Use this information to take version-specific action.</span></span> <span data-ttu-id="7779a-118">Ce membre est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7779a-118">This member is one of the following values.</span></span>



| <span data-ttu-id="7779a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7779a-119">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="7779a-120">Signification</span><span class="sxs-lookup"><span data-stu-id="7779a-120">Meaning</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="RASDOWNLEVEL"></span><span id="rasdownlevel"></span><dl> <span data-ttu-id="7779a-121"><dt>**RASDOWNLEVEL**</dt></span><span class="sxs-lookup"><span data-stu-id="7779a-121"><dt>**RASDOWNLEVEL**</dt></span></span> </dl>              | <span data-ttu-id="7779a-122">Indique un serveur RAS LAN Manager version 1,0.</span><span class="sxs-lookup"><span data-stu-id="7779a-122">Indicates a LAN Manager version 1.0 RAS server.</span></span><br/>                      |
| <span id="RASADMIN_35"></span><span id="rasadmin_35"></span><dl> <span data-ttu-id="7779a-123"><dt>**RASADMIN \_ 35**</dt></span><span class="sxs-lookup"><span data-stu-id="7779a-123"><dt>**RASADMIN\_35**</dt></span></span> </dl>                | <span data-ttu-id="7779a-124">Indique un serveur ou un client RAS Windows NT Server 3,51 et antérieur.</span><span class="sxs-lookup"><span data-stu-id="7779a-124">Indicates a Windows NT Server 3.51 and earlier RAS server or client.</span></span><br/> |
| <span id="RASADMIN_CURRENT"></span><span id="rasadmin_current"></span><dl> <span data-ttu-id="7779a-125"><dt>**RASADMIN \_ actuel**</dt></span><span class="sxs-lookup"><span data-stu-id="7779a-125"><dt>**RASADMIN\_CURRENT**</dt></span></span> </dl> | <span data-ttu-id="7779a-126">Indique un client ou un serveur RAS Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="7779a-126">Indicates a Windows NT 4.0 RAS server or client.</span></span><br/>                     |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7779a-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7779a-127">Requirements</span></span>



| <span data-ttu-id="7779a-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7779a-128">Requirement</span></span> | <span data-ttu-id="7779a-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="7779a-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7779a-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7779a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7779a-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7779a-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7779a-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7779a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7779a-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7779a-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7779a-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7779a-134">End of client support</span></span><br/>    | <span data-ttu-id="7779a-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7779a-135">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="7779a-136">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="7779a-136">End of server support</span></span><br/>    | <span data-ttu-id="7779a-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7779a-137">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="7779a-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="7779a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="7779a-139"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7779a-139"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7779a-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7779a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7779a-141">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="7779a-141">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="7779a-142">Structures d’administration de serveur RAS</span><span class="sxs-lookup"><span data-stu-id="7779a-142">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="7779a-143">**RasAdminServerGetInfo**</span><span class="sxs-lookup"><span data-stu-id="7779a-143">**RasAdminServerGetInfo**</span></span>](rasadminservergetinfo.md)
</dt> </dl>

 

 





