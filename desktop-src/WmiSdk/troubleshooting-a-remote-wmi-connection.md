---
description: Les sections suivantes décrivent les problèmes courants que les développeurs peuvent rencontrer avec la création d’une connexion WMI à distance.
ms.assetid: 328e420b-a859-4ce9-8a31-67150eb0a78f
ms.tgt_platform: multiple
title: Résolution des problèmes d’une connexion WMI à distance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae475f91836b9e99b1c7faaf149c452e00a66722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521486"
---
# <a name="troubleshooting-a-remote-wmi-connection"></a><span data-ttu-id="45030-103">Résolution des problèmes d’une connexion WMI à distance</span><span class="sxs-lookup"><span data-stu-id="45030-103">Troubleshooting a Remote WMI Connection</span></span>

<span data-ttu-id="45030-104">Les sections suivantes décrivent les problèmes courants que les développeurs peuvent rencontrer avec la création d’une connexion WMI à distance.</span><span class="sxs-lookup"><span data-stu-id="45030-104">The following sections describe common issues developers may have with creating a remote WMI connection.</span></span>

<span data-ttu-id="45030-105">Les sections suivantes sont présentées dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="45030-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="45030-106">Accès DCOM refusé</span><span class="sxs-lookup"><span data-stu-id="45030-106">DCOM Access Denied</span></span>](#dcom-access-denied)
-   [<span data-ttu-id="45030-107">Échec de la connexion</span><span class="sxs-lookup"><span data-stu-id="45030-107">Failure to Connect</span></span>](#failure-to-connect)
-   [<span data-ttu-id="45030-108">Expiration de la connexion WMI</span><span class="sxs-lookup"><span data-stu-id="45030-108">WMI Connection Timed Out</span></span>](#wmi-connection-timed-out)
-   [<span data-ttu-id="45030-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="45030-109">Related topics</span></span>](#related-topics)

## <a name="dcom-access-denied"></a><span data-ttu-id="45030-110">Accès DCOM refusé</span><span class="sxs-lookup"><span data-stu-id="45030-110">DCOM Access Denied</span></span>

<dl> <dt>

<span data-ttu-id="45030-111"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Indice</span><span class="sxs-lookup"><span data-stu-id="45030-111"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span></span>
</dt> <dd>

<span data-ttu-id="45030-112">votre connexion a échoué avec l’erreur « accès DCOM refusé », ainsi que la valeur décimale-2147024891 ou Hex value0x80070005.</span><span class="sxs-lookup"><span data-stu-id="45030-112">your connection failed with the error "DCOM Access Denied", along with the decimal value -2147024891 or hex value0x80070005.</span></span>

</dd> <dt>

<span data-ttu-id="45030-113"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Problématique</span><span class="sxs-lookup"><span data-stu-id="45030-113"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span></span>
</dt> <dd>

<span data-ttu-id="45030-114">DCOM n’est peut-être pas configuré pour autoriser une connexion WMI.</span><span class="sxs-lookup"><span data-stu-id="45030-114">DCOM may not be configured to allow a WMI connection.</span></span>

</dd> <dt>

<span data-ttu-id="45030-115"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>768</span><span class="sxs-lookup"><span data-stu-id="45030-115"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolution</span></span>
</dt> <dd>

<span data-ttu-id="45030-116">Vous pouvez configurer les paramètres DCOM pour WMI à l’aide de l’utilitaire de configuration DCOM (**DCOMCnfg.exe**) disponible dans **Outils d’administration** dans le **panneau** de configuration.</span><span class="sxs-lookup"><span data-stu-id="45030-116">You can configure DCOM settings for WMI using the DCOM Config utility (**DCOMCnfg.exe**) found in **Administrative Tools** in **Control Panel**.</span></span> <span data-ttu-id="45030-117">Cet utilitaire expose les paramètres qui permettent à certains utilisateurs de se connecter à l’ordinateur à distance via DCOM.</span><span class="sxs-lookup"><span data-stu-id="45030-117">This utility exposes the settings that enable certain users to connect to the computer remotely through DCOM.</span></span> <span data-ttu-id="45030-118">Les membres du groupe administrateurs sont autorisés à se connecter à distance à l’ordinateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="45030-118">Members of the Administrators group are allowed to remotely connect to the computer by default.</span></span> <span data-ttu-id="45030-119">Avec cet utilitaire, vous pouvez définir la sécurité pour démarrer, accéder et configurer le service WMI.</span><span class="sxs-lookup"><span data-stu-id="45030-119">With this utility you can set the security to start, access, and configure the WMI service.</span></span>

<span data-ttu-id="45030-120">Pour plus d’informations, consultez [sécurisation d’une connexion WMI à distance](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="45030-120">For more information, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span>

</dd> </dl>

## <a name="failure-to-connect"></a><span data-ttu-id="45030-121">Échec de la connexion</span><span class="sxs-lookup"><span data-stu-id="45030-121">Failure to Connect</span></span>

<dl> <dt>

<span data-ttu-id="45030-122"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Indice</span><span class="sxs-lookup"><span data-stu-id="45030-122"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span></span>
</dt> <dd>

<span data-ttu-id="45030-123">Vous ne pouvez pas vous connecter à WMI sur un système distant.</span><span class="sxs-lookup"><span data-stu-id="45030-123">You cannot connect to WMI on a remote system.</span></span>

</dd> <dt>

<span data-ttu-id="45030-124"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Problématique</span><span class="sxs-lookup"><span data-stu-id="45030-124"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span></span>
</dt> <dd>

<span data-ttu-id="45030-125">Vous essayez peut-être de vous connecter à un système qui ne prend pas en charge WMI.</span><span class="sxs-lookup"><span data-stu-id="45030-125">You may be trying to connect to a system that does not support WMI.</span></span> <span data-ttu-id="45030-126">Les connexions suivantes entre les versions de système d’exploitation ne sont pas prises en charge :</span><span class="sxs-lookup"><span data-stu-id="45030-126">The following connections between operating system versions are not supported:</span></span>

-   <span data-ttu-id="45030-127">Vous ne pouvez pas vous connecter à un ordinateur qui exécute une édition Starter, de base ou personnelle.</span><span class="sxs-lookup"><span data-stu-id="45030-127">You cannot connect to a computer that is running a Starter, Basic, or Home edition.</span></span>

<span data-ttu-id="45030-128">Vous pouvez également essayer de vous connecter à un espace de noms qui nécessite une connexion chiffrée, qui requiert un niveau d’authentification `pktPrivacy` , **WbemAuthenticationLevelPktPrivacy** ou une déclaration de **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC C**.</span><span class="sxs-lookup"><span data-stu-id="45030-128">Alternately, you may be trying to connect to a namespace which requires an encrypted connection, one that requires an authentication level of `pktPrivacy`, **WbemAuthenticationLevelPktPrivacy**, or **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>

</dd> <dt>

<span data-ttu-id="45030-129"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>768</span><span class="sxs-lookup"><span data-stu-id="45030-129"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolution</span></span>
</dt> <dd>

<span data-ttu-id="45030-130">Pour plus d’informations, consultez [sécurisation des espaces de noms WMI](securing-wmi-namespaces.md), [sécurisation des clients et fournisseurs C++](securing-c---clients-and-providers.md), ou [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="45030-130">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md), [Securing C++ Clients and Providers](securing-c---clients-and-providers.md), or [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

</dd> </dl>

## <a name="wmi-connection-timed-out"></a><span data-ttu-id="45030-131">Expiration de la connexion WMI</span><span class="sxs-lookup"><span data-stu-id="45030-131">WMI Connection Timed Out</span></span>

<dl> <dt>

<span data-ttu-id="45030-132"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Indice</span><span class="sxs-lookup"><span data-stu-id="45030-132"><span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Symptom</span></span>
</dt> <dd>

<span data-ttu-id="45030-133">Votre connexion WMI expire.</span><span class="sxs-lookup"><span data-stu-id="45030-133">Your WMI connection times out.</span></span>

</dd> <dt>

<span data-ttu-id="45030-134"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Problématique</span><span class="sxs-lookup"><span data-stu-id="45030-134"><span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Issue</span></span>
</dt> <dd>

<span data-ttu-id="45030-135">En raison de problèmes de latence du réseau, l’ordinateur ne peut tout simplement pas répondre dans le temps.</span><span class="sxs-lookup"><span data-stu-id="45030-135">Due to network lag issues, the computer is simply not able to respond in time.</span></span>

</dd> <dt>

<span data-ttu-id="45030-136"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>768</span><span class="sxs-lookup"><span data-stu-id="45030-136"><span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>Resolution</span></span>
</dt> <dd>

<span data-ttu-id="45030-137">Lors de la connexion à WMI via un appel à [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) ou [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), vous pouvez définir l’indicateur **wbemConnectFlagUseMaxWait** (script) ou la valeur de l' **\_ indicateur WBEM \_ Connect \_ use \_ Max \_ Wait** en C++ sur 128 (0x80) pour imposer un délai de deux (2) minutes sur l’appel.</span><span class="sxs-lookup"><span data-stu-id="45030-137">When connecting to WMI through a call to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) or [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), you can set the **wbemConnectFlagUseMaxWait** flag (scripting) or the **WBEM\_FLAG\_CONNECT\_USE\_MAX\_WAIT** in C++ value to 128 (0x80) to impose a two (2) minute time-out on the call.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="45030-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="45030-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45030-139">Connexion à WMI sur un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="45030-139">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 



