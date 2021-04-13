---
title: Constantes d’authentification (WSManDisp. h)
description: Spécifiez la méthode d’authentification et la manière de gérer les serveurs de certificats pour le transport HTTPs des demandes.
ms.assetid: adfefbc9-c386-48db-a0c2-145aa4f91bfa
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagCredUsernamePassword
- WSManFlagSkipCACheck
- WSManFlagSkipCNCheck
- WSManFlagUseNoAuthentication
- WSManFlagUseDigest
- WSManFlagUseNegotiate
- WSManFlagUseBasic
- WSManFlagUseKerberos
- WSManFlagNoEncryption
- WSManFlagUseClientCertificate
- WSManFlagUseCredSsp
- WSManFlagSkipRevocationCheck
- WSManFlagAllowNegotiateImplicitCredentials
- WSManFlagUseSsl
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce45d1474cf6c925149c05ae348231333c3356e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509238"
---
# <a name="authentication-constants"></a><span data-ttu-id="c21b1-103">Constantes d’authentification</span><span class="sxs-lookup"><span data-stu-id="c21b1-103">Authentication Constants</span></span>

<span data-ttu-id="c21b1-104">Les constantes d’authentification sont des constantes de l’énumération **\_ \_ WSManSessionFlags** qui spécifient la méthode d’authentification et comment gérer les serveurs de certificats pour le transport HTTPS des requêtes.</span><span class="sxs-lookup"><span data-stu-id="c21b1-104">Authentication constants are constants in the **\_\_WSManSessionFlags** enumeration that specify the authentication method and how to handle certificate servers for HTTPS transport of requests.</span></span>

<span data-ttu-id="c21b1-105">Une ou plusieurs des constantes répertoriées dans la liste suivante sont requises dans le paramètre *Flags* dans les appels à [**WSMan. CreateSession**](wsman-createsession.md) ou dans les appels [**IWSMan :: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) qui se connectent à un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="c21b1-105">One or more of the constants listed in the following list are required in the *flags* parameter in calls to [**WSMan.CreateSession**](wsman-createsession.md) or in [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) calls that connect to a remote computer.</span></span>

<dl> <dt>

<span data-ttu-id="c21b1-106"><span id="WSManFlagCredUsernamePassword"></span><span id="wsmanflagcredusernamepassword"></span><span id="WSMANFLAGCREDUSERNAMEPASSWORD"></span>**WSManFlagCredUsernamePassword**</span><span class="sxs-lookup"><span data-stu-id="c21b1-106"><span id="WSManFlagCredUsernamePassword"></span><span id="wsmanflagcredusernamepassword"></span><span id="WSMANFLAGCREDUSERNAMEPASSWORD"></span>**WSManFlagCredUsernamePassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c21b1-107">4096 (0x1000)</span><span class="sxs-lookup"><span data-stu-id="c21b1-107">4096 (0x1000)</span></span>
</dt> <dt>



<span data-ttu-id="c21b1-108">Utilisez le nom d’utilisateur et le mot de passe comme informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="c21b1-108">Use the user name and password as the credentials.</span></span> <span data-ttu-id="c21b1-109">Définissez cet indicateur lorsque vous créez un objet [**ConnectionOptions**](connectionoptions.md) et fournissez le [**nom d’utilisateur**](connectionoptions-username.md) et le [**mot de passe**](connectionoptions-password.md).</span><span class="sxs-lookup"><span data-stu-id="c21b1-109">Set this flag when you create a [**ConnectionOptions**](connectionoptions.md) object and supply [**Username**](connectionoptions-username.md) and [**Password**](connectionoptions-password.md).</span></span> <span data-ttu-id="c21b1-110">Les informations d’identification peuvent être un compte de domaine ou un compte sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="c21b1-110">The credentials can be a domain account or an account on the local computer.</span></span> <span data-ttu-id="c21b1-111">Par défaut, le compte doit être membre du groupe Administrateurs local sur l’ordinateur local ou distant.</span><span class="sxs-lookup"><span data-stu-id="c21b1-111">By default, the account must be a member of the local Administrators group on the local or remote computer.</span></span> <span data-ttu-id="c21b1-112">Toutefois, le service WinRM peut être configuré pour autoriser d’autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c21b1-112">However, the WinRM service can be configured to allow other users.</span></span> <span data-ttu-id="c21b1-113">Pour plus d’informations, consultez [installation et configuration de Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="c21b1-113">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span> <span data-ttu-id="c21b1-114">Vous pouvez définir cet indicateur lorsque vous spécifiez des informations d’identification pour l’authentification par négociation (également appelée [*authentification intégrée Windows*](windows-remote-management-glossary.md)) ou pour [*l’authentification de base*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="c21b1-114">You can set this flag when you specify credentials for Negotiate authentication (also known as [*Windows Integrated Authentication*](windows-remote-management-glossary.md)) or for [*Basic authentication*](windows-remote-management-glossary.md).</span></span>

<span data-ttu-id="c21b1-115">La méthode de script associée est [**WSMan. SessionFlagCredUsernamePassword**](wsman-sessionflagcredusernamepassword.md), et la méthode C++ est [**IWSManEx. SessionFlagCredUsernamePassword**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword).</span><span class="sxs-lookup"><span data-stu-id="c21b1-115">The associated scripting method is [**WSMan.SessionFlagCredUsernamePassword**](wsman-sessionflagcredusernamepassword.md), and the C++ method is [**IWSManEx.SessionFlagCredUsernamePassword**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c21b1-116"><span id="WSManFlagSkipCACheck"></span><span id="wsmanflagskipcacheck"></span><span id="WSMANFLAGSKIPCACHECK"></span>**WSManFlagSkipCACheck**</span><span class="sxs-lookup"><span data-stu-id="c21b1-116"><span id="WSManFlagSkipCACheck"></span><span id="wsmanflagskipcacheck"></span><span id="WSMANFLAGSKIPCACHECK"></span>**WSManFlagSkipCACheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c21b1-117">8192 (0x2000)</span><span class="sxs-lookup"><span data-stu-id="c21b1-117">8192 (0x2000)</span></span>
</dt> <dt>



<span data-ttu-id="c21b1-118">Lors de la connexion via HTTPs, le client ne valide pas que le certificat de serveur est signé par une autorité de certification approuvée.</span><span class="sxs-lookup"><span data-stu-id="c21b1-118">When connecting over HTTPS, the client does not validate that the server certificate is signed by a trusted certification authority (CA).</span></span> <span data-ttu-id="c21b1-119">Utilisez cette valeur uniquement lorsque l’ordinateur distant est approuvé par d’autres moyens, par exemple, si l’ordinateur distant fait partie d’un réseau qui est physiquement sécurisé et isolé ou que l’ordinateur distant est listé comme un hôte approuvé dans la configuration WinRM.</span><span class="sxs-lookup"><span data-stu-id="c21b1-119">Use this value only when the remote computer is trusted by other means, for example, if the remote computer is part of a network that is physically secure and isolated or the remote computer is listed as a trusted host in the WinRM configuration.</span></span>

<span data-ttu-id="c21b1-120">La méthode de script associée est [**WSMan. SessionFlagSkipCACheck**](wsman-sessionflagskipcacheck.md), et la méthode C++ est [**IWSManEx. SessionFlagSkipCACheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck).</span><span class="sxs-lookup"><span data-stu-id="c21b1-120">The associated scripting method is [**WSMan.SessionFlagSkipCACheck**](wsman-sessionflagskipcacheck.md), and the C++ method is [**IWSManEx.SessionFlagSkipCACheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c21b1-121"><span id="WSManFlagSkipCNCheck"></span><span id="wsmanflagskipcncheck"></span><span id="WSMANFLAGSKIPCNCHECK"></span>**WSManFlagSkipCNCheck**</span><span class="sxs-lookup"><span data-stu-id="c21b1-121"><span id="WSManFlagSkipCNCheck"></span><span id="wsmanflagskipcncheck"></span><span id="WSMANFLAGSKIPCNCHECK"></span>**WSManFlagSkipCNCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c21b1-122">16384 (0x4000)</span><span class="sxs-lookup"><span data-stu-id="c21b1-122">16384 (0x4000)</span></span>
</dt> <dt>



<span data-ttu-id="c21b1-123">Lors de la connexion via HTTPs, le client ne valide pas que le nom commun (CN) dans le certificat de serveur correspond au nom de l’ordinateur dans la chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="c21b1-123">When connecting over HTTPS, the client will not validate that the common name (CN) in the server certificate matches the computer name in the connection string.</span></span> <span data-ttu-id="c21b1-124">À utiliser uniquement lorsque l’ordinateur distant est approuvé par d’autres moyens, par exemple, si l’ordinateur distant fait partie d’un réseau qui est physiquement sécurisé et isolé ou que l’ordinateur distant est listé comme un hôte approuvé dans la configuration WinRM.</span><span class="sxs-lookup"><span data-stu-id="c21b1-124">Use only when the remote computer is trusted by other means, for example, if the remote computer is part of a network that is physically secure and isolated or the remote computer is listed as a trusted host in the WinRM configuration.</span></span>

<span data-ttu-id="c21b1-125">La méthode de script associée est [**WSMan. SessionFlagSkipCNCheck**](wsman-sessionflagskipcncheck.md), et la méthode C++ est [**IWSManEx. SessionFlagSkipCNCheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck).</span><span class="sxs-lookup"><span data-stu-id="c21b1-125">The associated scripting method is [**WSMan.SessionFlagSkipCNCheck**](wsman-sessionflagskipcncheck.md), and the C++ method is [**IWSManEx.SessionFlagSkipCNCheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c21b1-126"><span id="WSManFlagUseNoAuthentication"></span><span id="wsmanflagusenoauthentication"></span><span id="WSMANFLAGUSENOAUTHENTICATION"></span>**WSManFlagUseNoAuthentication**</span><span class="sxs-lookup"><span data-stu-id="c21b1-126"><span id="WSManFlagUseNoAuthentication"></span><span id="wsmanflagusenoauthentication"></span><span id="WSMANFLAGUSENOAUTHENTICATION"></span>**WSManFlagUseNoAuthentication**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c21b1-127">32768 (0x8000)</span><span class="sxs-lookup"><span data-stu-id="c21b1-127">32768 (0x8000)</span></span>
</dt> <dt>



<span data-ttu-id="c21b1-128">N’utilisez aucune authentification.</span><span class="sxs-lookup"><span data-stu-id="c21b1-128">Use no authentication.</span></span> <span data-ttu-id="c21b1-129">Spécifiez cette constante lors du test d’une connexion à un ordinateur distant pour déterminer si un service qui implémente le protocole WS-Management est configuré pour écouter les demandes de données.</span><span class="sxs-lookup"><span data-stu-id="c21b1-129">Specify this constant when testing a connection to a remote computer to determine if a service that implements the WS-Management protocol is configured to listen for data requests.</span></span> <span data-ttu-id="c21b1-130">**WSManFlagUseNoAuthentication** ne peut pas être associé à une autre constante de [**session**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="c21b1-130">**WSManFlagUseNoAuthentication** cannot be combined with any other [**Session**](session.md) constant.</span></span> <span data-ttu-id="c21b1-131">La méthode de script associée est [**WSMan. SessionFlagUseNoAuthentication**](wsman-sessionflagusenoauthentication.md), et la méthode C++ est [**WSManEx. SessionFlagUseNoAuthentication**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication).</span><span class="sxs-lookup"><span data-stu-id="c21b1-131">The associated scripting method is [**WSMan.SessionFlagUseNoAuthentication**](wsman-sessionflagusenoauthentication.md), and the C++ method is [**WSManEx.SessionFlagUseNoAuthentication**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c21b1-132"><span id="WSManFlagUseDigest"></span><span id="wsmanflagusedigest"></span><span id="WSMANFLAGUSEDIGEST"></span>**WSManFlagUseDigest**</span><span class="sxs-lookup"><span data-stu-id="c21b1-132"><span id="WSManFlagUseDigest"></span><span id="wsmanflagusedigest"></span><span id="WSMANFLAGUSEDIGEST"></span>**WSManFlagUseDigest**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c21b1-133">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="c21b1-133">65536 (0x10000)</span></span>
</dt> <dt>



<span data-ttu-id="c21b1-134">Utilisez l’authentification Digest.</span><span class="sxs-lookup"><span data-stu-id="c21b1-134">Use Digest authentication.</span></span> <span data-ttu-id="c21b1-135">Seul l'ordinateur client peut initier une demande d'authentification Digest.</span><span class="sxs-lookup"><span data-stu-id="c21b1-135">Only the client computer can initiate a Digest authentication request.</span></span> <span data-ttu-id="c21b1-136">Le client envoie une demande au serveur pour s’authentifier et reçoit une chaîne de jeton du serveur.</span><span class="sxs-lookup"><span data-stu-id="c21b1-136">The client sends a request to the server to authenticate and receives a token string from the server.</span></span> <span data-ttu-id="c21b1-137">Le client envoie ensuite la demande de ressource, y compris le nom d’utilisateur et un hachage de chiffrement du mot de passe associé à la chaîne de jeton.</span><span class="sxs-lookup"><span data-stu-id="c21b1-137">The client then sends the resource request, including the user name and a cryptographic hash of the password combined with the token string.</span></span> <span data-ttu-id="c21b1-138">L’authentification Digest est prise en charge pour HTTP et HTTPs.</span><span class="sxs-lookup"><span data-stu-id="c21b1-138">Digest authentication is supported for HTTP and HTTPS.</span></span> <span data-ttu-id="c21b1-139">Les applications et scripts clients WinRM peuvent spécifier l’authentification Digest, mais pas le service.</span><span class="sxs-lookup"><span data-stu-id="c21b1-139">WinRM client scripts and applications can specify Digest authentication, but not the service.</span></span>

<span data-ttu-id="c21b1-140">La méthode de script associée est [**WSMan. SessionFlagUseDigest**](wsman-sessionflagusedigest.md), et la méthode C++ est [**IWSManEx. SessionFlagUseDigest**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest).</span><span class="sxs-lookup"><span data-stu-id="c21b1-140">The associated scripting method is [**WSMan.SessionFlagUseDigest**](wsman-sessionflagusedigest.md), and the C++ method is [**IWSManEx.SessionFlagUseDigest**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c21b1-141"><span id="WSManFlagUseNegotiate"></span><span id="wsmanflagusenegotiate"></span><span id="WSMANFLAGUSENEGOTIATE"></span>**WSManFlagUseNegotiate**</span><span class="sxs-lookup"><span data-stu-id="c21b1-141"><span id="WSManFlagUseNegotiate"></span><span id="wsmanflagusenegotiate"></span><span id="WSMANFLAGUSENEGOTIATE"></span>**WSManFlagUseNegotiate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c21b1-142">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="c21b1-142">131072 (0x20000)</span></span>
</dt> <dt>



<span data-ttu-id="c21b1-143">Utilisez l’authentification par négociation.</span><span class="sxs-lookup"><span data-stu-id="c21b1-143">Use Negotiate authentication.</span></span> <span data-ttu-id="c21b1-144">Le client envoie une demande au serveur pour s’authentifier.</span><span class="sxs-lookup"><span data-stu-id="c21b1-144">The client sends a request to the server to authenticate.</span></span> <span data-ttu-id="c21b1-145">Le serveur détermine s’il faut utiliser Kerberos ou NTLM.</span><span class="sxs-lookup"><span data-stu-id="c21b1-145">The server determines whether to use Kerberos or NTLM.</span></span> <span data-ttu-id="c21b1-146">Kerberos est sélectionné pour authentifier un compte de domaine et NTLM est sélectionné pour les comptes d’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="c21b1-146">Kerberos is selected to authenticate a domain account and NTLM is selected for local computer accounts.</span></span> <span data-ttu-id="c21b1-147">Le nom d’utilisateur doit être spécifié sous la forme domaine \\ nom d’utilisateur pour un utilisateur de domaine ou un \\ nom d’utilisateur ServerName pour un utilisateur local sur un ordinateur serveur.</span><span class="sxs-lookup"><span data-stu-id="c21b1-147">The user name should be specified in the form domain\\username for a domain user or servername\\username for a local user on a server computer.</span></span>

<span data-ttu-id="c21b1-148">Le [contrôle de compte d’utilisateur (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) affecte l’accès au service WinRM.</span><span class="sxs-lookup"><span data-stu-id="c21b1-148">[User Account Control (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) affects access to the WinRM service.</span></span> <span data-ttu-id="c21b1-149">Lorsque l’authentification par négociation est utilisée dans un groupe de travail ou un domaine, seul le compte administrateur intégré peut accéder au service.</span><span class="sxs-lookup"><span data-stu-id="c21b1-149">When Negotiate authentication is used in a workgroup or domain, only the built-in Administrator account can access the service.</span></span> <span data-ttu-id="c21b1-150">Pour autoriser tous les comptes du groupe administrateurs à accéder au service, définissez la clé de Registre suivante sur 1 : **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Policies \\ System \\ LocalAccountTokenFilterPolicy**.</span><span class="sxs-lookup"><span data-stu-id="c21b1-150">To allow all accounts in the Administrators group to access the service, set the following registry key to 1: **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Policies\\system\\LocalAccountTokenFilterPolicy**.</span></span>

<span data-ttu-id="c21b1-151">La méthode de script associée est [**WSMan. SessionFlagUseNegotiate**](wsman-sessionflagusenegotiate.md), et la méthode C++ est [**IWSManEx. SessionFlagUseNegotiate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate).</span><span class="sxs-lookup"><span data-stu-id="c21b1-151">The associated scripting method is [**WSMan.SessionFlagUseNegotiate**](wsman-sessionflagusenegotiate.md), and the C++ method is [**IWSManEx.SessionFlagUseNegotiate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c21b1-152"><span id="WSManFlagUseBasic"></span><span id="wsmanflagusebasic"></span><span id="WSMANFLAGUSEBASIC"></span>**WSManFlagUseBasic**</span><span class="sxs-lookup"><span data-stu-id="c21b1-152"><span id="WSManFlagUseBasic"></span><span id="wsmanflagusebasic"></span><span id="WSMANFLAGUSEBASIC"></span>**WSManFlagUseBasic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c21b1-153">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="c21b1-153">262144 (0x40000)</span></span>
</dt> <dt>



<span data-ttu-id="c21b1-154">Utilisez l’authentification de base.</span><span class="sxs-lookup"><span data-stu-id="c21b1-154">Use Basic authentication.</span></span> <span data-ttu-id="c21b1-155">Le client présente les informations d’identification sous la forme d’un nom d’utilisateur et d’un mot de passe, transmises directement dans le message de demande.</span><span class="sxs-lookup"><span data-stu-id="c21b1-155">The client presents credentials in the form of a user name and password, directly transmitted in the request message.</span></span> <span data-ttu-id="c21b1-156">Vous pouvez spécifier uniquement les informations d’identification qui identifient un compte d’administrateur local sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="c21b1-156">You can specify only credentials that identify a local administrator account on the remote computer.</span></span>

<span data-ttu-id="c21b1-157">La méthode de script associée est [**WSMan. SessionFlagUseBasic**](wsman-sessionflagusebasic.md), et la méthode C++ est [**IWSManEx. SessionFlagUseBasic**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic).</span><span class="sxs-lookup"><span data-stu-id="c21b1-157">The associated scripting method is [**WSMan.SessionFlagUseBasic**](wsman-sessionflagusebasic.md), and the C++ method is [**IWSManEx.SessionFlagUseBasic**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c21b1-158"><span id="WSManFlagUseKerberos"></span><span id="wsmanflagusekerberos"></span><span id="WSMANFLAGUSEKERBEROS"></span>**WSManFlagUseKerberos**</span><span class="sxs-lookup"><span data-stu-id="c21b1-158"><span id="WSManFlagUseKerberos"></span><span id="wsmanflagusekerberos"></span><span id="WSMANFLAGUSEKERBEROS"></span>**WSManFlagUseKerberos**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c21b1-159">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="c21b1-159">524288 (0x80000)</span></span>
</dt> <dt>



<span data-ttu-id="c21b1-160">Utilisez l'authentification Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c21b1-160">Use Kerberos authentication.</span></span> <span data-ttu-id="c21b1-161">Le client et le serveur s’authentifient mutuellement à l’aide des tickets Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c21b1-161">The client and server mutually authenticate using Kerberos tickets.</span></span>

<span data-ttu-id="c21b1-162">La méthode de script associée est [**WSMan. SessionFlagUseKerberos**](wsman-sessionflagusekerberos.md), et la méthode C++ est [**IWSManEx. WSMan. SessionFlagUseKerberos**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos).</span><span class="sxs-lookup"><span data-stu-id="c21b1-162">The associated scripting method is [**WSMan.SessionFlagUseKerberos**](wsman-sessionflagusekerberos.md), and the C++ method is [**IWSManEx.WSMan.SessionFlagUseKerberos**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c21b1-163"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span><span class="sxs-lookup"><span data-stu-id="c21b1-163"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c21b1-164">1048576 ()</span><span class="sxs-lookup"><span data-stu-id="c21b1-164">1048576 (0x100000)</span></span>
</dt> <dt>



<span data-ttu-id="c21b1-165">N’utilisez pas de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="c21b1-165">Use no encryption.</span></span> <span data-ttu-id="c21b1-166">Le trafic non chiffré n’est pas autorisé par défaut et doit être activé à la fois sur le client et sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="c21b1-166">Unencrypted traffic is not allowed by default and must be enabled on both the client and server.</span></span>

<span data-ttu-id="c21b1-167">La méthode de script associée est [**WSMan. SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md), et la méthode C++ est [**IWSManEx. SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span><span class="sxs-lookup"><span data-stu-id="c21b1-167">The associated scripting method is [**WSMan.SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md), and the C++ method is [**IWSManEx.SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c21b1-168"><span id="WSManFlagUseClientCertificate"></span><span id="wsmanflaguseclientcertificate"></span><span id="WSMANFLAGUSECLIENTCERTIFICATE"></span>**WSManFlagUseClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="c21b1-168"><span id="WSManFlagUseClientCertificate"></span><span id="wsmanflaguseclientcertificate"></span><span id="WSMANFLAGUSECLIENTCERTIFICATE"></span>**WSManFlagUseClientCertificate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c21b1-169">2097152 (0x200000)</span><span class="sxs-lookup"><span data-stu-id="c21b1-169">2097152 (0x200000)</span></span>
</dt> <dt>



<span data-ttu-id="c21b1-170">Utilisez l’authentification par certificat client.</span><span class="sxs-lookup"><span data-stu-id="c21b1-170">Use client certificate-based authentication.</span></span>

<span data-ttu-id="c21b1-171">La méthode de script associée est [**WSMan. SessionFlagUseClientCertificate**](wsman-sessionflaguseclientcert.md), et la méthode C++ est [**IWSManEx2. SessionFlagUseClientCertificate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate).</span><span class="sxs-lookup"><span data-stu-id="c21b1-171">The associated scripting method is [**WSMan.SessionFlagUseClientCertificate**](wsman-sessionflaguseclientcert.md), and the C++ method is [**IWSManEx2.SessionFlagUseClientCertificate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c21b1-172"><span id="WSManFlagUseCredSsp"></span><span id="wsmanflagusecredssp"></span><span id="WSMANFLAGUSECREDSSP"></span>**WSManFlagUseCredSsp**</span><span class="sxs-lookup"><span data-stu-id="c21b1-172"><span id="WSManFlagUseCredSsp"></span><span id="wsmanflagusecredssp"></span><span id="WSMANFLAGUSECREDSSP"></span>**WSManFlagUseCredSsp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c21b1-173">16777216 (0x1000000)</span><span class="sxs-lookup"><span data-stu-id="c21b1-173">16777216 (0x1000000)</span></span>
</dt> <dt>



<span data-ttu-id="c21b1-174">Utilisez l’authentification CredSSP (Credential Security Support Provider).</span><span class="sxs-lookup"><span data-stu-id="c21b1-174">Use Credential Security Support Provider (CredSSP) authentication.</span></span>

<span data-ttu-id="c21b1-175">La méthode de script associée est [**WSMan. SessionFlagUseCredSsp**](wsman-sessionflagusecredssp.md), et la méthode C++ est [**IWSManEx3. SessionFlagUseCredSsp**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex3-sessionflagusecredssp).</span><span class="sxs-lookup"><span data-stu-id="c21b1-175">The associated scripting method is [**WSMan.SessionFlagUseCredSsp**](wsman-sessionflagusecredssp.md), and the C++ method is [**IWSManEx3.SessionFlagUseCredSsp**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex3-sessionflagusecredssp).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c21b1-176"><span id="WSManFlagSkipRevocationCheck"></span><span id="wsmanflagskiprevocationcheck"></span><span id="WSMANFLAGSKIPREVOCATIONCHECK"></span>**WSManFlagSkipRevocationCheck**</span><span class="sxs-lookup"><span data-stu-id="c21b1-176"><span id="WSManFlagSkipRevocationCheck"></span><span id="wsmanflagskiprevocationcheck"></span><span id="WSMANFLAGSKIPREVOCATIONCHECK"></span>**WSManFlagSkipRevocationCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c21b1-177">0x2000000</span><span class="sxs-lookup"><span data-stu-id="c21b1-177">0x2000000</span></span>
</dt> <dt>



<span data-ttu-id="c21b1-178">Ne pas vérifier la révocation des certificats lors de l’authentification.</span><span class="sxs-lookup"><span data-stu-id="c21b1-178">Do not check for certificate revocation during authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c21b1-179"><span id="WSManFlagAllowNegotiateImplicitCredentials"></span><span id="wsmanflagallownegotiateimplicitcredentials"></span><span id="WSMANFLAGALLOWNEGOTIATEIMPLICITCREDENTIALS"></span>**WSManFlagAllowNegotiateImplicitCredentials**</span><span class="sxs-lookup"><span data-stu-id="c21b1-179"><span id="WSManFlagAllowNegotiateImplicitCredentials"></span><span id="wsmanflagallownegotiateimplicitcredentials"></span><span id="WSMANFLAGALLOWNEGOTIATEIMPLICITCREDENTIALS"></span>**WSManFlagAllowNegotiateImplicitCredentials**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c21b1-180">0x4000000</span><span class="sxs-lookup"><span data-stu-id="c21b1-180">0x4000000</span></span>
</dt> <dt>



<span data-ttu-id="c21b1-181">Autorisez les informations d’identification implicites.</span><span class="sxs-lookup"><span data-stu-id="c21b1-181">Allow implicit credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c21b1-182"><span id="WSManFlagUseSsl"></span><span id="wsmanflagusessl"></span><span id="WSMANFLAGUSESSL"></span>**WSManFlagUseSsl**</span><span class="sxs-lookup"><span data-stu-id="c21b1-182"><span id="WSManFlagUseSsl"></span><span id="wsmanflagusessl"></span><span id="WSMANFLAGUSESSL"></span>**WSManFlagUseSsl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c21b1-183">0x8000000</span><span class="sxs-lookup"><span data-stu-id="c21b1-183">0x8000000</span></span>
</dt> <dt>



<span data-ttu-id="c21b1-184">Utilisez SSL (Secure Socket Layer) pour activer le protocole HTTPs.</span><span class="sxs-lookup"><span data-stu-id="c21b1-184">Use Secure Socket Layer, enables HTTPS.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c21b1-185">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c21b1-185">Requirements</span></span>



| <span data-ttu-id="c21b1-186">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c21b1-186">Requirement</span></span> | <span data-ttu-id="c21b1-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="c21b1-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c21b1-188">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c21b1-188">Minimum supported client</span></span><br/> | <span data-ttu-id="c21b1-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c21b1-189">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="c21b1-190">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c21b1-190">Minimum supported server</span></span><br/> | <span data-ttu-id="c21b1-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c21b1-191">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c21b1-192">En-tête</span><span class="sxs-lookup"><span data-stu-id="c21b1-192">Header</span></span><br/>                   | <dl> <span data-ttu-id="c21b1-193"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c21b1-193"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c21b1-194">MIDL</span><span class="sxs-lookup"><span data-stu-id="c21b1-194">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c21b1-195"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c21b1-195"><dt>WSManDisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c21b1-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c21b1-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c21b1-197">Constantes de session</span><span class="sxs-lookup"><span data-stu-id="c21b1-197">Session Constants</span></span>](session-constants.md)
</dt> </dl>

 

 





