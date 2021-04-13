---
title: Structure RAS_PORT_0 (rassapi. h)
description: La \_ structure du port RAS \_ 0 contient des informations qui décrivent un port RAS.
ms.assetid: 750fc705-0770-427b-b7d6-7876b8b9118a
keywords:
- RAS_PORT_0 de la structure RAS
- Point d’accès RAS du pointeur de structure PRAS_PORT_0
topic_type:
- apiref
api_name:
- RAS_PORT_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80d66725415d86aea44138f23fb3748e3187820f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508645"
---
# <a name="ras_port_0-structure"></a><span data-ttu-id="b93a0-105">\_Structure du port RAS \_ 0</span><span class="sxs-lookup"><span data-stu-id="b93a0-105">RAS\_PORT\_0 structure</span></span>

<span data-ttu-id="b93a0-106">\[Cette version de la structure du **\_ port RAS \_ 0** n’est pas prise en charge à partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b93a0-106">\[This version of the **RAS\_PORT\_0** structure is not supported as of Windows Vista.</span></span> <span data-ttu-id="b93a0-107">Utilisez à la place le [**\_ port RAS \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) plus récent défini dans mprapi. h.\]</span><span class="sxs-lookup"><span data-stu-id="b93a0-107">Use the newer [**RAS\_PORT\_0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) defined in mprapi.h instead.\]</span></span>

<span data-ttu-id="b93a0-108">La structure du **\_ port RAS \_ 0** contient des informations qui décrivent un port RAS.</span><span class="sxs-lookup"><span data-stu-id="b93a0-108">The **RAS\_PORT\_0** structure contains information that describes a RAS port.</span></span>

## <a name="syntax"></a><span data-ttu-id="b93a0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b93a0-109">Syntax</span></span>


```C++
typedef struct _RAS_PORT_0 {
  WCHAR wszPortName[RASSAPI_MAX_PORT_NAME];
  WCHAR wszDeviceType[RASSAPI_MAX_DEVICETYPE_NAME];
  WCHAR wszDeviceName[RASSAPI_MAX_DEVICE_NAME];
  WCHAR wszMediaName[RASSAPI_MAX_MEDIA_NAME];
  DWORD reserved;
  DWORD Flags;
  WCHAR wszUserName[UNLEN + 1];
  WCHAR wszComputer[NETBIOS_NAME_LEN];
  DWORD dwStartSessionTime;
  WCHAR wszLogonDomain[DNLEN + 1];
  BOOL  fAdvancedServer;
} RAS_PORT_0, *PRAS_PORT_0;
```



## <a name="members"></a><span data-ttu-id="b93a0-110">Membres</span><span class="sxs-lookup"><span data-stu-id="b93a0-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="b93a0-111">**wszPortName**</span><span class="sxs-lookup"><span data-stu-id="b93a0-111">**wszPortName**</span></span>
</dt> <dd>

<span data-ttu-id="b93a0-112">Chaîne Unicode terminée par le caractère null qui spécifie le nom du port, par exemple « COM1 ».</span><span class="sxs-lookup"><span data-stu-id="b93a0-112">A null-terminated Unicode string that specifies the name of the port, such as "COM1".</span></span>

</dd> <dt>

<span data-ttu-id="b93a0-113">**wszDeviceType**</span><span class="sxs-lookup"><span data-stu-id="b93a0-113">**wszDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="b93a0-114">Chaîne Unicode terminée par le caractère null qui spécifie le type de l’appareil sur lequel la connexion a été établie, par exemple modem ou RNIS.</span><span class="sxs-lookup"><span data-stu-id="b93a0-114">A null-terminated Unicode string that specifies the type of the device on which the connection was made, such as Modem or ISDN.</span></span> <span data-ttu-id="b93a0-115">La liste des types d’appareils qui peuvent être spécifiés dans ce membre inclut tous les types d’appareils installés sur le serveur, y compris les périphériques tiers.</span><span class="sxs-lookup"><span data-stu-id="b93a0-115">The list of device types that might be specified in this member includes all the device types installed on the server, including third-party devices.</span></span>

</dd> <dt>

<span data-ttu-id="b93a0-116">**wszDeviceName**</span><span class="sxs-lookup"><span data-stu-id="b93a0-116">**wszDeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="b93a0-117">Chaîne Unicode terminée par le caractère null qui spécifie le nom de l’appareil sur lequel la connexion a été établie, par exemple « Hayes 9600 » ou « PCIMACISDN1 ».</span><span class="sxs-lookup"><span data-stu-id="b93a0-117">A null-terminated Unicode string that specifies the name of the device on which the connection was made, such as "Hayes 9600" or "PCIMACISDN1".</span></span>

</dd> <dt>

<span data-ttu-id="b93a0-118">**wszMediaName**</span><span class="sxs-lookup"><span data-stu-id="b93a0-118">**wszMediaName**</span></span>
</dt> <dd>

<span data-ttu-id="b93a0-119">Spécifie une chaîne Unicode terminée par le caractère null qui spécifie le nom du média utilisé pour la connexion, par exemple *rasser* ou *rastapi*.</span><span class="sxs-lookup"><span data-stu-id="b93a0-119">Specifies a null-terminated Unicode string that specifies the name of the media used for the connection, such as *rasser* or *rastapi*.</span></span>

</dd> <dt>

<span data-ttu-id="b93a0-120">**réservé**</span><span class="sxs-lookup"><span data-stu-id="b93a0-120">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="b93a0-121">Réservé.</span><span class="sxs-lookup"><span data-stu-id="b93a0-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="b93a0-122">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="b93a0-122">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="b93a0-123">Spécifie un jeu d’indicateurs binaires qui spécifient la nature de la connexion établie sur ce port.</span><span class="sxs-lookup"><span data-stu-id="b93a0-123">Specifies a set of bit flags that specify the nature of the connection made on this port.</span></span> <span data-ttu-id="b93a0-124">Ce membre peut être une combinaison des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="b93a0-124">This member can be a combination of the following flags.</span></span>



| <span data-ttu-id="b93a0-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="b93a0-125">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="b93a0-126">Signification</span><span class="sxs-lookup"><span data-stu-id="b93a0-126">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GATEWAY_ACTIVE"></span><span id="gateway_active"></span><dl> <span data-ttu-id="b93a0-127"><dt>**PASSERELLE \_ active**</dt></span><span class="sxs-lookup"><span data-stu-id="b93a0-127"><dt>**GATEWAY\_ACTIVE**</dt></span></span> </dl>             | <span data-ttu-id="b93a0-128">Si cet indicateur est défini, la passerelle NetBIOS est active sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="b93a0-128">If this flag is set, the NetBIOS gateway is active on the server.</span></span><br/>                                                                                                                                                                                                                                                                                                               |
| <span id="MESSENGER_PRESENT"></span><span id="messenger_present"></span><dl> <span data-ttu-id="b93a0-129"><dt>**MESSENGER \_ présent**</dt></span><span class="sxs-lookup"><span data-stu-id="b93a0-129"><dt>**MESSENGER\_PRESENT**</dt></span></span> </dl>    | <span data-ttu-id="b93a0-130">Si cet indicateur est défini, le service Messenger s’exécute sur le client distant.</span><span class="sxs-lookup"><span data-stu-id="b93a0-130">If this flag is set, the messenger service is running on the remote client.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="PORT_MULTILINKED"></span><span id="port_multilinked"></span><dl> <span data-ttu-id="b93a0-131"><dt>**PORT à \_ liaisons multiples**</dt></span><span class="sxs-lookup"><span data-stu-id="b93a0-131"><dt>**PORT\_MULTILINKED**</dt></span></span> </dl>       | <span data-ttu-id="b93a0-132">Si cet indicateur est défini, le port est lié à des liaisons multiples avec d’autres ports.</span><span class="sxs-lookup"><span data-stu-id="b93a0-132">If this flag is set, the port is multilinked with other ports.</span></span> <span data-ttu-id="b93a0-133">Utilisez ces informations pour afficher l’état de la connexion en tant que port à liaisons multiples.</span><span class="sxs-lookup"><span data-stu-id="b93a0-133">Use this information to display the connection status as a multilinked port.</span></span> <br/> <span data-ttu-id="b93a0-134">Pour un port à liaisons multiples, la structure des [**\_ \_ statistiques du port RAS**](ras-port-statistics-str.md) contient deux ensembles de statistiques : un pour le port seul et un autre pour les ports combinés dans la connexion à liaisons multiples.</span><span class="sxs-lookup"><span data-stu-id="b93a0-134">For a multilinked port, the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure contains two sets of statistics: one for the port alone, and another for the combined ports in the multilink connection.</span></span><br/> |
| <span id="PPP_CLIENT"></span><span id="ppp_client"></span><dl> <span data-ttu-id="b93a0-135"><dt>**\_client PPP**</dt></span><span class="sxs-lookup"><span data-stu-id="b93a0-135"><dt>**PPP\_CLIENT**</dt></span></span> </dl>                         | <span data-ttu-id="b93a0-136">Si cet indicateur est défini, le client distant s’est connecté à l’aide de PPP.</span><span class="sxs-lookup"><span data-stu-id="b93a0-136">If this flag is set, the remote client connected using PPP.</span></span> <span data-ttu-id="b93a0-137">Si cet indicateur n’est pas défini, le client distant s’est connecté à l’aide du protocole AMB.</span><span class="sxs-lookup"><span data-stu-id="b93a0-137">If this flag is not set, the remote client connected using the AMB protocol.</span></span><br/>                                                                                                                                                                                                                                        |
| <span id="REMOTE_LISTEN"></span><span id="remote_listen"></span><dl> <span data-ttu-id="b93a0-138"><dt>**écoute à distance \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b93a0-138"><dt>**REMOTE\_LISTEN**</dt></span></span> </dl>                | <span data-ttu-id="b93a0-139">Si cet indicateur est défini, le paramètre RemoteListen de la passerelle NetBIOS est défini sur 1 sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="b93a0-139">If this flag is set, the RemoteListen parameter of the NetBIOS gateway is set to 1 on the server.</span></span><br/>                                                                                                                                                                                                                                                                               |
| <span id="USER_AUTHENTICATED"></span><span id="user_authenticated"></span><dl> <span data-ttu-id="b93a0-140"><dt>**UTILISATEUR \_ authentifié**</dt></span><span class="sxs-lookup"><span data-stu-id="b93a0-140"><dt>**USER\_AUTHENTICATED**</dt></span></span> </dl> | <span data-ttu-id="b93a0-141">Si cet indicateur est défini, un client distant est connecté au serveur et l’utilisateur a été authentifié.</span><span class="sxs-lookup"><span data-stu-id="b93a0-141">If this flag is set, a remote client is connected to the server and the user has been authenticated.</span></span> <span data-ttu-id="b93a0-142">Cochez cet indicateur pour vous assurer qu’un client est réellement connecté à un port.</span><span class="sxs-lookup"><span data-stu-id="b93a0-142">Check this flag to ensure that a client is actually connected to a port.</span></span><br/>                                                                                                                                                                                                   |



 

<span data-ttu-id="b93a0-143">Si les \_ indicateurs Messenger présent, passerelle \_ active et écoute distante \_ sont définis, utilisez le service Messenger pour envoyer un message administratif au client distant.</span><span class="sxs-lookup"><span data-stu-id="b93a0-143">If the MESSENGER\_PRESENT, GATEWAY\_ACTIVE, and REMOTE\_LISTEN flags are set, use the messenger service to send an administrative message to the remote client.</span></span> <span data-ttu-id="b93a0-144">Si MESSENGER \_ est présent et que \_ l’écoute à distance est définie, mais \_ que la passerelle est active, n’envoyez des messages au client qu’à partir du serveur RAS auquel le client est connecté.</span><span class="sxs-lookup"><span data-stu-id="b93a0-144">If MESSENGER\_PRESENT and REMOTE\_LISTEN are set, but GATEWAY\_ACTIVE is not, send messages to the client only from the RAS server to which the client is connected.</span></span>

</dd> <dt>

<span data-ttu-id="b93a0-145">**wszUserName**</span><span class="sxs-lookup"><span data-stu-id="b93a0-145">**wszUserName**</span></span>
</dt> <dd>

<span data-ttu-id="b93a0-146">Chaîne Unicode terminée par le caractère null qui spécifie le nom de l’utilisateur distant connecté à ce port.</span><span class="sxs-lookup"><span data-stu-id="b93a0-146">A null-terminated Unicode string that specifies the name of the remote user connected to this port.</span></span>

</dd> <dt>

<span data-ttu-id="b93a0-147">**wszComputer**</span><span class="sxs-lookup"><span data-stu-id="b93a0-147">**wszComputer**</span></span>
</dt> <dd>

<span data-ttu-id="b93a0-148">Chaîne Unicode terminée par le caractère null qui spécifie le nom de l’ordinateur client distant.</span><span class="sxs-lookup"><span data-stu-id="b93a0-148">A null-terminated Unicode string that specifies the name of the remote client computer.</span></span>

</dd> <dt>

<span data-ttu-id="b93a0-149">**dwStartSessionTime**</span><span class="sxs-lookup"><span data-stu-id="b93a0-149">**dwStartSessionTime**</span></span>
</dt> <dd>

<span data-ttu-id="b93a0-150">Spécifie la durée, en secondes, à partir du 1er janvier 1970, que le client s’est connecté au serveur RAS sur ce port.</span><span class="sxs-lookup"><span data-stu-id="b93a0-150">Specifies the time, in seconds from January 1, 1970, that the client connected to the RAS server on this port.</span></span> <span data-ttu-id="b93a0-151">Utilisez les fonctions d’heure standard pour mettre en forme cette valeur pour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="b93a0-151">Use the standard time functions to format this value for display.</span></span>

</dd> <dt>

<span data-ttu-id="b93a0-152">**wszLogonDomain**</span><span class="sxs-lookup"><span data-stu-id="b93a0-152">**wszLogonDomain**</span></span>
</dt> <dd>

<span data-ttu-id="b93a0-153">Spécifie une chaîne Unicode terminée par le caractère null qui spécifie le nom du domaine sur lequel l’utilisateur distant a été authentifié.</span><span class="sxs-lookup"><span data-stu-id="b93a0-153">Specifies a null-terminated Unicode string that specifies the name of the domain on which the remote user was authenticated.</span></span> <span data-ttu-id="b93a0-154">Cette chaîne est le nom de domaine uniquement, sans \\ \\ préfixe «».</span><span class="sxs-lookup"><span data-stu-id="b93a0-154">This string is the domain name only, with no "\\\\" prefix.</span></span>

</dd> <dt>

<span data-ttu-id="b93a0-155">**fAdvancedServer**</span><span class="sxs-lookup"><span data-stu-id="b93a0-155">**fAdvancedServer**</span></span>
</dt> <dd>

<span data-ttu-id="b93a0-156">Spécifie un indicateur différent de zéro si le serveur RAS associé à ce port est un serveur avancé tel que Windows 2000 Advanced Server.</span><span class="sxs-lookup"><span data-stu-id="b93a0-156">Specifies a flag that is nonzero if the RAS server associated with this port is an advanced server such as Windows 2000 Advanced Server.</span></span> <span data-ttu-id="b93a0-157">Utilisez ces informations pour déterminer le nom du serveur qui contient la base de données de comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b93a0-157">Use this information to determine the name of the server that has the user account database.</span></span> <span data-ttu-id="b93a0-158">Si le serveur RAS est un serveur avancé, récupérez le nom du serveur de comptes d’utilisateur en concaténant le préfixe « \\ \\ » au nom renvoyé dans le membre **wszLogonDomain** .</span><span class="sxs-lookup"><span data-stu-id="b93a0-158">If the RAS server is an advanced server, get the name of the user account server by concatenating the prefix "\\\\" to the name returned in the **wszLogonDomain** member.</span></span> <span data-ttu-id="b93a0-159">En effet, pour un serveur avancé, le nom de domaine d’ouverture de session locale est le même que le nom du serveur.</span><span class="sxs-lookup"><span data-stu-id="b93a0-159">This is because for an advanced server the local logon domain name is the same as the server name.</span></span> <span data-ttu-id="b93a0-160">Si le serveur RAS est une station de travail, utilisez la fonction [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) pour obtenir le nom du serveur de compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b93a0-160">If the RAS server is a workstation, use the [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) function to get the name of the user account server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b93a0-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b93a0-161">Requirements</span></span>



| <span data-ttu-id="b93a0-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b93a0-162">Requirement</span></span> | <span data-ttu-id="b93a0-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="b93a0-163">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b93a0-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b93a0-164">Minimum supported client</span></span><br/> | <span data-ttu-id="b93a0-165">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b93a0-165">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b93a0-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b93a0-166">Minimum supported server</span></span><br/> | <span data-ttu-id="b93a0-167">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b93a0-167">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b93a0-168">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b93a0-168">End of client support</span></span><br/>    | <span data-ttu-id="b93a0-169">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b93a0-169">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="b93a0-170">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="b93a0-170">End of server support</span></span><br/>    | <span data-ttu-id="b93a0-171">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b93a0-171">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="b93a0-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="b93a0-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="b93a0-173"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b93a0-173"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b93a0-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b93a0-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b93a0-175">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="b93a0-175">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="b93a0-176">Structures d’administration de serveur RAS</span><span class="sxs-lookup"><span data-stu-id="b93a0-176">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="b93a0-177">**\_Port RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="b93a0-177">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="b93a0-178">**\_statistiques du port RAS \_**</span><span class="sxs-lookup"><span data-stu-id="b93a0-178">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="b93a0-179">**RasAdminGetUserAccountServer**</span><span class="sxs-lookup"><span data-stu-id="b93a0-179">**RasAdminGetUserAccountServer**</span></span>](rasadmingetuseraccountserver.md)
</dt> <dt>

[<span data-ttu-id="b93a0-180">**RasAdminPortEnum**</span><span class="sxs-lookup"><span data-stu-id="b93a0-180">**RasAdminPortEnum**</span></span>](rasadminportenum.md)
</dt> </dl>

 

 





