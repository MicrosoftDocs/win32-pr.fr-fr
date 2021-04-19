---
title: Structure RAS_PORT_1 (rassapi. h)
description: La \_ structure du port \_ 1 RAS contient des informations sur un port RAS.
ms.assetid: f226ef16-feb4-41e0-ba60-ddb2f0acd305
keywords:
- RAS_PORT_1 de la structure RAS
- Point d’accès RAS du pointeur de structure PRAS_PORT_1
topic_type:
- apiref
api_name:
- RAS_PORT_1
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73fe450e5ea5f8ceee48436dbbe05570d0d818a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512580"
---
# <a name="ras_port_1-structure"></a><span data-ttu-id="e8290-105">\_Structure du port RAS \_ 1</span><span class="sxs-lookup"><span data-stu-id="e8290-105">RAS\_PORT\_1 structure</span></span>

<span data-ttu-id="e8290-106">\[Cette version de la structure du **\_ port \_ 1 RAS** n’est pas prise en charge à partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e8290-106">\[This version of the **RAS\_PORT\_1** structure is not supported as of Windows Vista.</span></span> <span data-ttu-id="e8290-107">Utilisez à la place le [**\_ port RAS \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) plus récent défini dans mprapi. h.\]</span><span class="sxs-lookup"><span data-stu-id="e8290-107">Use the newer [**RAS\_PORT\_1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) defined in mprapi.h instead.\]</span></span>

<span data-ttu-id="e8290-108">La structure du **\_ port \_ 1 RAS** contient des informations sur un port RAS.</span><span class="sxs-lookup"><span data-stu-id="e8290-108">The **RAS\_PORT\_1** structure contains information about a RAS port.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8290-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8290-109">Syntax</span></span>


```C++
typedef struct _RAS_PORT_1 {
  RAS_PORT_0                rasport0;
  DWORD                     LineCondition;
  DWORD                     HardwareCondition;
  DWORD                     LineSpeed;
  WORD                      NumStatistics;
  WORD                      NumMediaParms;
  DWORD                     SizeMediaParms;
  RAS_PPP_PROJECTION_RESULT ProjResult;
} RAS_PORT_1, *PRAS_PORT_1;
```



## <a name="members"></a><span data-ttu-id="e8290-110">Membres</span><span class="sxs-lookup"><span data-stu-id="e8290-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="e8290-111">**rasport0**</span><span class="sxs-lookup"><span data-stu-id="e8290-111">**rasport0**</span></span>
</dt> <dd>

<span data-ttu-id="e8290-112">Spécifie une structure de [**\_ port RAS \_ 0**](ras-port-0-str.md) qui contient des informations sur le port, telles que le nom du port, le nom de l’utilisateur distant connecté au port, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="e8290-112">Specifies a [**RAS\_PORT\_0**](ras-port-0-str.md) structure that contains information about the port, such as the name of the port, the name of the remote user connected to the port, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="e8290-113">**LineCondition**</span><span class="sxs-lookup"><span data-stu-id="e8290-113">**LineCondition**</span></span>
</dt> <dd>

<span data-ttu-id="e8290-114">Spécifie l’état du port.</span><span class="sxs-lookup"><span data-stu-id="e8290-114">Specifies the state of the port.</span></span> <span data-ttu-id="e8290-115">Ce membre peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e8290-115">This member can be one of the following values.</span></span>



| <span data-ttu-id="e8290-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8290-116">Value</span></span>                                                                                                                                                                                            | <span data-ttu-id="e8290-117">Signification</span><span class="sxs-lookup"><span data-stu-id="e8290-117">Meaning</span></span>                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RAS_PORT_NON_OPERATIONAL"></span><span id="ras_port_non_operational"></span><dl> <span data-ttu-id="e8290-118"><dt>**\_port RAS \_ non \_ opérationnel**</dt></span><span class="sxs-lookup"><span data-stu-id="e8290-118"><dt>**RAS\_PORT\_NON\_OPERATIONAL**</dt></span></span> </dl> | <span data-ttu-id="e8290-119">Le port n’est pas opérationnel.</span><span class="sxs-lookup"><span data-stu-id="e8290-119">The port is not operational.</span></span> <span data-ttu-id="e8290-120">Recherchez dans le journal des événements les erreurs signalées par le serveur.</span><span class="sxs-lookup"><span data-stu-id="e8290-120">Check the event log for errors reported by the server.</span></span><br/>                                                                         |
| <span id="RAS_PORT_DISCONNECTED"></span><span id="ras_port_disconnected"></span><dl> <span data-ttu-id="e8290-121"><dt>**\_port RAS \_ déconnecté**</dt></span><span class="sxs-lookup"><span data-stu-id="e8290-121"><dt>**RAS\_PORT\_DISCONNECTED**</dt></span></span> </dl>           | <span data-ttu-id="e8290-122">Le port est actuellement déconnecté.</span><span class="sxs-lookup"><span data-stu-id="e8290-122">The port is currently disconnected.</span></span><br/>                                                                                                                         |
| <span id="RAS_PORT_CALLING_BACK"></span><span id="ras_port_calling_back"></span><dl> <span data-ttu-id="e8290-123"><dt>**\_port RAS \_ rappelé \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e8290-123"><dt>**RAS\_PORT\_CALLING\_BACK**</dt></span></span> </dl>          | <span data-ttu-id="e8290-124">Le serveur RAS rappelle le client RAS.</span><span class="sxs-lookup"><span data-stu-id="e8290-124">The RAS server is calling back the RAS client.</span></span><br/>                                                                                                              |
| <span id="RAS_PORT_LISTENING"></span><span id="ras_port_listening"></span><dl> <span data-ttu-id="e8290-125"><dt>**\_écoute du port RAS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e8290-125"><dt>**RAS\_PORT\_LISTENING**</dt></span></span> </dl>                    | <span data-ttu-id="e8290-126">Le port attend qu’un client appelle dans.</span><span class="sxs-lookup"><span data-stu-id="e8290-126">The port is waiting for a client to call in.</span></span><br/>                                                                                                                |
| <span id="RAS_PORT_AUTHENTICATING"></span><span id="ras_port_authenticating"></span><dl> <span data-ttu-id="e8290-127"><dt>**PORT RAS d' \_ \_ authentification**</dt></span><span class="sxs-lookup"><span data-stu-id="e8290-127"><dt>**RAS\_PORT\_AUTHENTICATING**</dt></span></span> </dl>     | <span data-ttu-id="e8290-128">Le serveur est en cours d’authentification du client distant.</span><span class="sxs-lookup"><span data-stu-id="e8290-128">The server is in the process of authenticating the remote client.</span></span><br/>                                                                                           |
| <span id="RAS_PORT_AUTHENTICATED"></span><span id="ras_port_authenticated"></span><dl> <span data-ttu-id="e8290-129"><dt>**\_port RAS \_ authentifié**</dt></span><span class="sxs-lookup"><span data-stu-id="e8290-129"><dt>**RAS\_PORT\_AUTHENTICATED**</dt></span></span> </dl>        | <span data-ttu-id="e8290-130">Le client distant est à présent authentifié.</span><span class="sxs-lookup"><span data-stu-id="e8290-130">The remote client is now authenticated.</span></span><br/>                                                                                                                     |
| <span id="RAS_PORT_INITIALIZING"></span><span id="ras_port_initializing"></span><dl> <span data-ttu-id="e8290-131"><dt>**\_ \_ initialisation du port RAS**</dt></span><span class="sxs-lookup"><span data-stu-id="e8290-131"><dt>**RAS\_PORT\_INITIALIZING**</dt></span></span> </dl>           | <span data-ttu-id="e8290-132">L’appareil attaché au port est en cours d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="e8290-132">The device attached to the port is being initialized.</span></span> <span data-ttu-id="e8290-133">L’état du port passe à l’écoute du \_ port RAS \_ lorsque l’initialisation est terminée.</span><span class="sxs-lookup"><span data-stu-id="e8290-133">The state of the port will change to RAS\_PORT\_LISTENING when the initialization has been completed.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e8290-134">**HardwareCondition**</span><span class="sxs-lookup"><span data-stu-id="e8290-134">**HardwareCondition**</span></span>
</dt> <dd>

<span data-ttu-id="e8290-135">Spécifie l’une des valeurs suivantes pour indiquer l’état de l’appareil attaché au port.</span><span class="sxs-lookup"><span data-stu-id="e8290-135">Specifies one of the following values to indicate the state of the device attached to the port.</span></span>



| <span data-ttu-id="e8290-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8290-136">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="e8290-137">Signification</span><span class="sxs-lookup"><span data-stu-id="e8290-137">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="RAS_MODEM_OPERATIONAL"></span><span id="ras_modem_operational"></span><dl> <span data-ttu-id="e8290-138"><dt>**\_modem RAS \_ opérationnel**</dt></span><span class="sxs-lookup"><span data-stu-id="e8290-138"><dt>**RAS\_MODEM\_OPERATIONAL**</dt></span></span> </dl>                 | <span data-ttu-id="e8290-139">Le modem attaché à ce port est opérationnel et est prêt à recevoir les appels des clients.</span><span class="sxs-lookup"><span data-stu-id="e8290-139">The modem attached to this port is operational and is ready to receive client calls.</span></span><br/> |
| <span id="RAS_MODEM_HARDWARE_FAILURE"></span><span id="ras_modem_hardware_failure"></span><dl> <span data-ttu-id="e8290-140"><dt>**\_ \_ défaillance matérielle du modem RAS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e8290-140"><dt>**RAS\_MODEM\_HARDWARE\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="e8290-141">Le modem attaché à ce port présente un problème matériel.</span><span class="sxs-lookup"><span data-stu-id="e8290-141">The modem attached to this port has a hardware problem.</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="e8290-142">**LineSpeed**</span><span class="sxs-lookup"><span data-stu-id="e8290-142">**LineSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="e8290-143">Spécifie la vitesse, en bits par seconde, avec laquelle l’ordinateur peut communiquer avec le port.</span><span class="sxs-lookup"><span data-stu-id="e8290-143">Specifies the speed, in bits per second, with which the computer can communicate with the port.</span></span>

</dd> <dt>

<span data-ttu-id="e8290-144">**NumStatistics**</span><span class="sxs-lookup"><span data-stu-id="e8290-144">**NumStatistics**</span></span>
</dt> <dd>

<span data-ttu-id="e8290-145">Ce membre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="e8290-145">This member is not used.</span></span> <span data-ttu-id="e8290-146">Les fonctions d’administration RAS, telles que la fonction [**RasAdminPortGetInfo**](rasadminportgetinfo.md) , utilisent la structure des [**\_ \_ statistiques du port RAS**](ras-port-statistics-str.md) pour retourner les statistiques des ports.</span><span class="sxs-lookup"><span data-stu-id="e8290-146">The RAS administration functions, such as the [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function, use the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure to return port statistics.</span></span>

</dd> <dt>

<span data-ttu-id="e8290-147">**NumMediaParms**</span><span class="sxs-lookup"><span data-stu-id="e8290-147">**NumMediaParms**</span></span>
</dt> <dd>

<span data-ttu-id="e8290-148">Spécifie le nombre de paramètres spécifiques au média pour ce port.</span><span class="sxs-lookup"><span data-stu-id="e8290-148">Specifies the number of media-specific parameters for this port.</span></span> <span data-ttu-id="e8290-149">Pour les supports série, il s’agit généralement du nombre de valeurs qui apparaissent dans le fichier SERIAL.INI.</span><span class="sxs-lookup"><span data-stu-id="e8290-149">For serial media this is typically the number of values that appear in the SERIAL.INI file.</span></span>

</dd> <dt>

<span data-ttu-id="e8290-150">**SizeMediaParms**</span><span class="sxs-lookup"><span data-stu-id="e8290-150">**SizeMediaParms**</span></span>
</dt> <dd>

<span data-ttu-id="e8290-151">Spécifie la taille, en octets, de la mémoire tampon requise pour tous les paramètres spécifiques au média.</span><span class="sxs-lookup"><span data-stu-id="e8290-151">Specifies the size, in bytes, of the buffer required for all media-specific parameters.</span></span> <span data-ttu-id="e8290-152">La fonction [**RasAdminPortGetInfo**](rasadminportgetinfo.md) retourne une mémoire tampon qui contient un tableau de structures de [**\_ paramètres RAS**](ras-parameters-str.md) avec les paramètres et les valeurs de média pour le port.</span><span class="sxs-lookup"><span data-stu-id="e8290-152">The [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function returns a buffer that contains an array of [**RAS\_PARAMETERS**](ras-parameters-str.md) structures with the media parameters and values for the port.</span></span>

</dd> <dt>

<span data-ttu-id="e8290-153">**ProjResult**</span><span class="sxs-lookup"><span data-stu-id="e8290-153">**ProjResult**</span></span>
</dt> <dd>

<span data-ttu-id="e8290-154">Structure [**de \_ \_ \_ résultat de projection PPP RAS**](ras-ppp-projection-result-str.md) qui spécifie les informations de projection PPP pour ce port.</span><span class="sxs-lookup"><span data-stu-id="e8290-154">A [**RAS\_PPP\_PROJECTION\_RESULT**](ras-ppp-projection-result-str.md) structure that specifies the PPP projection information for this port.</span></span> <span data-ttu-id="e8290-155">Cette structure fournit des informations pour chaque protocole négocié lorsqu’un client RAS se connecte à un serveur.</span><span class="sxs-lookup"><span data-stu-id="e8290-155">This structure provides information for each protocol that is negotiated when a RAS client connects to a server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8290-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8290-156">Requirements</span></span>



| <span data-ttu-id="e8290-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8290-157">Requirement</span></span> | <span data-ttu-id="e8290-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8290-158">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e8290-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8290-159">Minimum supported client</span></span><br/> | <span data-ttu-id="e8290-160">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8290-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e8290-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e8290-161">Minimum supported server</span></span><br/> | <span data-ttu-id="e8290-162">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e8290-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e8290-163">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e8290-163">End of client support</span></span><br/>    | <span data-ttu-id="e8290-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e8290-164">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="e8290-165">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="e8290-165">End of server support</span></span><br/>    | <span data-ttu-id="e8290-166">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e8290-166">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="e8290-167">En-tête</span><span class="sxs-lookup"><span data-stu-id="e8290-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8290-168"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8290-168"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8290-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8290-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8290-170">Vue d’ensemble du service d’accès à distance (RAS)</span><span class="sxs-lookup"><span data-stu-id="e8290-170">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="e8290-171">Structures d’administration de serveur RAS</span><span class="sxs-lookup"><span data-stu-id="e8290-171">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="e8290-172">**\_paramètres RAS**</span><span class="sxs-lookup"><span data-stu-id="e8290-172">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> <dt>

[<span data-ttu-id="e8290-173">**\_Port RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="e8290-173">**RAS\_PORT\_0**</span></span>](ras-port-0-str.md)
</dt> <dt>

[<span data-ttu-id="e8290-174">**\_statistiques du port RAS \_**</span><span class="sxs-lookup"><span data-stu-id="e8290-174">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="e8290-175">**résultat de la \_ projection PPP RAS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e8290-175">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="e8290-176">**RasAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="e8290-176">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)
</dt> <dt>

[<span data-ttu-id="e8290-177">**RasAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="e8290-177">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md)
</dt> <dt>

[<span data-ttu-id="e8290-178">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="e8290-178">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





