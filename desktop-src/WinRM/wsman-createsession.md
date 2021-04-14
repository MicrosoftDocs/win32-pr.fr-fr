---
title: Méthode WSMan. CreateSession (WSManDisp. h)
description: Crée un objet de session qui peut ensuite être utilisé pour les opérations réseau ultérieures.
ms.assetid: 299d9a95-bd30-414c-996d-6633e8b7ce52
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode CreateSession
- Méthode CreateSession Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode CreateSession
topic_type:
- apiref
api_name:
- WSMan.CreateSession
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 966fd1f43db7114d3a4c0cf4cddaa4428fcb41c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508818"
---
# <a name="wsmancreatesession-method"></a><span data-ttu-id="26f9a-106">Méthode WSMan. CreateSession</span><span class="sxs-lookup"><span data-stu-id="26f9a-106">WSMan.CreateSession method</span></span>

<span data-ttu-id="26f9a-107">Crée un objet de [**session**](session.md) qui peut ensuite être utilisé pour les opérations réseau ultérieures.</span><span class="sxs-lookup"><span data-stu-id="26f9a-107">Creates a [**Session**](session.md) object that can then be used for subsequent network operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="26f9a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26f9a-108">Syntax</span></span>


```VB
WSMan.CreateSession( _
  [ ByVal connection ], _
  [ ByVal flags ], _
  [ ByVal connectionOptions ] _
)
```



## <a name="parameters"></a><span data-ttu-id="26f9a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26f9a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26f9a-110">*connexion* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="26f9a-110">*connection* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="26f9a-111">Protocole et service auquel se connecter, y compris IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="26f9a-111">The protocol and service to connect to, including either IPv4 or IPv6.</span></span> <span data-ttu-id="26f9a-112">Le format des informations de connexion est le suivant : < ><  >< *suffixe* d’adresse de transport>.</span><span class="sxs-lookup"><span data-stu-id="26f9a-112">The format of the connection information is as follows: <*Transport*><*Address*><*Suffix*>.</span></span> <span data-ttu-id="26f9a-113">Pour obtenir des exemples, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="26f9a-113">For examples, see Remarks.</span></span> <span data-ttu-id="26f9a-114">Si aucune information de connexion n’est fournie, l’ordinateur local est utilisé.</span><span class="sxs-lookup"><span data-stu-id="26f9a-114">If no connection information is provided, the local computer is used.</span></span>

</dd> <dt>

<span data-ttu-id="26f9a-115">*indicateurs* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="26f9a-115">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="26f9a-116">Indicateurs de session qui spécifient la méthode d’authentification, telle que [*Negotiate Authentication*](windows-remote-management-glossary.md) ou [*Digest Authentication*](windows-remote-management-glossary.md), pour la connexion à un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="26f9a-116">The session flags that specify the authentication method, such as [*Negotiate authentication*](windows-remote-management-glossary.md) or [*Digest authentication*](windows-remote-management-glossary.md), for connecting to a remote computer.</span></span> <span data-ttu-id="26f9a-117">Ces indicateurs spécifient également d’autres informations de connexion de session, telles que l’encodage ou le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="26f9a-117">These flags also specify other session connection information, such as encoding or encryption.</span></span> <span data-ttu-id="26f9a-118">Ce paramètre doit contenir un ou plusieurs indicateurs dans **\_ \_ WSManSessionFlags** pour une connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="26f9a-118">This parameter must contain one or more of the flags in **\_\_WSManSessionFlags** for a remote connection.</span></span> <span data-ttu-id="26f9a-119">Pour plus d’informations, consultez [sessions, constantes](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="26f9a-119">For more information, see [Session Constants](session-constants.md).</span></span> <span data-ttu-id="26f9a-120">Aucun paramètre d’indicateur n’est requis pour une connexion à WinRM sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="26f9a-120">No flag settings are required for a connection to WinRM on the local computer.</span></span> <span data-ttu-id="26f9a-121">La valeur par défaut est **WSManFlagUseNegotiate**.</span><span class="sxs-lookup"><span data-stu-id="26f9a-121">The default is **WSManFlagUseNegotiate**.</span></span>

<span data-ttu-id="26f9a-122">Pour plus d’informations, consultez [authentification pour les connexions à distance](authentication-for-remote-connections.md) et le paramètre *connectionOptions* .</span><span class="sxs-lookup"><span data-stu-id="26f9a-122">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md) and the *connectionOptions* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="26f9a-123">*connectionOptions* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="26f9a-123">*connectionOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="26f9a-124">Pointeur vers un objet [**ConnectionOptions**](connectionoptions.md) qui contient un nom d’utilisateur et un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="26f9a-124">A pointer to a [**ConnectionOptions**](connectionoptions.md) object that contains a user name and password.</span></span> <span data-ttu-id="26f9a-125">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="26f9a-125">The default is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26f9a-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26f9a-126">Return value</span></span>

<span data-ttu-id="26f9a-127">Objet de [**session**](session.md) qui peut ensuite être utilisé pour effectuer des opérations WinRM locales ou distantes.</span><span class="sxs-lookup"><span data-stu-id="26f9a-127">A [**Session**](session.md) object that can then be used to perform local or remote WinRM operations.</span></span>

## <a name="remarks"></a><span data-ttu-id="26f9a-128">Notes</span><span class="sxs-lookup"><span data-stu-id="26f9a-128">Remarks</span></span>

<span data-ttu-id="26f9a-129">La méthode **CreateSession** Initialise l’objet de [**session**](session.md) en rassemblant des paramètres, tels que des indicateurs, des informations d’identification et une chaîne de connexion pour le paramètre de *connexion* .</span><span class="sxs-lookup"><span data-stu-id="26f9a-129">The **CreateSession** method initializes the [**Session**](session.md) object by gathering parameters, such as flags, credentials, and a connection string for the *connection* parameter.</span></span> <span data-ttu-id="26f9a-130">**CreateSession** ne se connecte pas réellement à l’ordinateur local ou distant.</span><span class="sxs-lookup"><span data-stu-id="26f9a-130">**CreateSession** does not actually connect to the local or remote computer.</span></span> <span data-ttu-id="26f9a-131">Si la connexion ne peut pas être établie, un échec se produit lors de la première opération de **session** , telle qu’une opération d' [**extraction**](session-get.md) ou d' [**énumération**](session-enumerate.md), après l’appel à **CreateSession**.</span><span class="sxs-lookup"><span data-stu-id="26f9a-131">If the connection cannot be established, a failure occurs on the first **Session** operation, such as a [**Get**](session-get.md) or [**Enumerate**](session-enumerate.md), after the call to **CreateSession**.</span></span> <span data-ttu-id="26f9a-132">Ce comportement diffère d’une connexion [*WMI*](windows-remote-management-glossary.md) à un [*espace de noms*](windows-remote-management-glossary.md) sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="26f9a-132">This behavior differs from a [*WMI*](windows-remote-management-glossary.md) connection to a [*namespace*](windows-remote-management-glossary.md) on a remote computer.</span></span> <span data-ttu-id="26f9a-133">Pour plus d’informations, consultez [Windows Remote Management et WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="26f9a-133">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="26f9a-134">L’exemple de code VBScript suivant est utilisé pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="26f9a-134">The following VBScript code example is used to call this method.</span></span>


```VB
Set session = _
    wsman.CreateSession("<Transport><Address><Suffix>")
```



<span data-ttu-id="26f9a-135">Les exemples suivants illustrent les différents formats utilisés pour spécifier les informations de connexion dans le paramètre de *connexion* (lors de la création d’une session HTTPS, le champ *adresse*> <doit correspondre au nom du certificat de l’ordinateur serveur, sinon une défaillance se produit) :</span><span class="sxs-lookup"><span data-stu-id="26f9a-135">The following examples show the different formats used to specify connection information in the *connection* parameter (when creating an HTTPS session, the <*Address*> field must match the server computer certificate name, otherwise a failure occurs):</span></span>

-   <span data-ttu-id="26f9a-136">"https://service"</span><span class="sxs-lookup"><span data-stu-id="26f9a-136">"https://service"</span></span>

    <span data-ttu-id="26f9a-137">Utilise le protocole HTTPs pour se connecter à l’emplacement du service Web par défaut.</span><span class="sxs-lookup"><span data-stu-id="26f9a-137">Uses HTTPS to connect to the default web service location.</span></span>

-   <span data-ttu-id="26f9a-138">"https://service.corp.com/websvcs/wsman"</span><span class="sxs-lookup"><span data-stu-id="26f9a-138">"https://service.corp.com/websvcs/wsman"</span></span>

    <span data-ttu-id="26f9a-139">Utilise le protocole HTTPs pour se connecter à l’emplacement du service Web spécifique.</span><span class="sxs-lookup"><span data-stu-id="26f9a-139">Uses HTTPS to connect to the specific web service location.</span></span>

-   <span data-ttu-id="26f9a-140">"https:// \[ E3D7:0000:0000:0000:51F4:9BC8 : c0a8:6420 \] "</span><span class="sxs-lookup"><span data-stu-id="26f9a-140">"https://\[E3D7:0000:0000:0000:51F4:9BC8:C0A8:6420\]"</span></span>

    <span data-ttu-id="26f9a-141">Utilise HTTPs et IPv6 avec le port par défaut.</span><span class="sxs-lookup"><span data-stu-id="26f9a-141">Uses HTTPS and IPv6 with the default port.</span></span>

-   <span data-ttu-id="26f9a-142">« https:// \[ E3D7:0000:0000:0000:51F4:9BC8 : c0a8:6420 \] : 9999/WSMan »</span><span class="sxs-lookup"><span data-stu-id="26f9a-142">"https://\[E3D7:0000:0000:0000:51F4:9BC8:C0A8:6420\]:9999/wsman"</span></span>

    <span data-ttu-id="26f9a-143">Utilise HTTPs et IPv6 avec le port donné.</span><span class="sxs-lookup"><span data-stu-id="26f9a-143">Uses HTTPS and IPv6 with the given port.</span></span>

## <a name="examples"></a><span data-ttu-id="26f9a-144">Exemples</span><span class="sxs-lookup"><span data-stu-id="26f9a-144">Examples</span></span>

<span data-ttu-id="26f9a-145">L’exemple de code VBScript suivant crée une session sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="26f9a-145">The following VBScript code example creates a session on the local computer.</span></span>


```VB
 Set NewSession = Wsman.CreateSession   
   
```



<span data-ttu-id="26f9a-146">L’exemple de code VBScript suivant crée une session sur un ordinateur distant qui est identifié par une adresse IP.</span><span class="sxs-lookup"><span data-stu-id="26f9a-146">The following VBScript code example creates a session on a remote computer that is identified by an IP address.</span></span> <span data-ttu-id="26f9a-147">Le script fournit un nom d’utilisateur et un mot de passe pour un compte.</span><span class="sxs-lookup"><span data-stu-id="26f9a-147">The script supplies a user name and password for an account.</span></span> <span data-ttu-id="26f9a-148">Les indicateurs **WSManFlagCredUserNamePassword** et **WSManFlagUseBasic** sont combinés pour indiquer que le compte est un compte local sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="26f9a-148">The flags **WSManFlagCredUserNamePassword** and **WSManFlagUseBasic** are combined to indicate that the account is a local account on the remote computer.</span></span> <span data-ttu-id="26f9a-149">Si la création de la session échoue, le script se termine.</span><span class="sxs-lookup"><span data-stu-id="26f9a-149">If the creation of the session fails, the script terminates.</span></span> <span data-ttu-id="26f9a-150">Le script utilise les méthodes qui retournent la constante, telles que [**WSMan. SessionFlagUseBasic**](wsman-sessionflagusebasic.md).</span><span class="sxs-lookup"><span data-stu-id="26f9a-150">The script uses the methods that return the constant, such as [**WSMan.SessionFlagUseBasic**](wsman-sessionflagusebasic.md).</span></span>

<span data-ttu-id="26f9a-151">Pour exécuter ce script, sachez que vous devez configurer les paramètres de configuration par défaut pour le client et le serveur afin d’autoriser le trafic non chiffré et l’authentification de base (**AllowUnencrypted** a la valeur **true** et Basic défini sur **true**).</span><span class="sxs-lookup"><span data-stu-id="26f9a-151">To run this script, be aware that you must configure the default configuration settings for both client and server to allow unencrypted traffic and Basic authentication (**AllowUnencrypted** set to **True** and Basic set to **True**).</span></span> <span data-ttu-id="26f9a-152">Pour plus d’informations, consultez [installation et configuration de Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="26f9a-152">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>


```VB
iFlags = WSMan.SessionFlagUseBasic Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



<span data-ttu-id="26f9a-153">Dans l’exemple de code VBScript suivant, le compte est un compte de domaine et l’authentification par négociation est utilisée.</span><span class="sxs-lookup"><span data-stu-id="26f9a-153">In the following VBScript code example, the account is a domain account and Negotiate authentication is used.</span></span> <span data-ttu-id="26f9a-154">Avec l’authentification Negotiate, vous devez spécifier le nom d’utilisateur en tant que `computername\username` ou `ipaddress\username` .</span><span class="sxs-lookup"><span data-stu-id="26f9a-154">With Negotiate authentication, you must specify the user name as `computername\username` or `ipaddress\username`.</span></span>


```VB
iFlags = WSMan.SessionFlagUseNegotiate Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyComputer\MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



## <a name="requirements"></a><span data-ttu-id="26f9a-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26f9a-155">Requirements</span></span>



| <span data-ttu-id="26f9a-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26f9a-156">Requirement</span></span> | <span data-ttu-id="26f9a-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="26f9a-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="26f9a-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26f9a-158">Minimum supported client</span></span><br/> | <span data-ttu-id="26f9a-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26f9a-159">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="26f9a-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26f9a-160">Minimum supported server</span></span><br/> | <span data-ttu-id="26f9a-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26f9a-161">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="26f9a-162">En-tête</span><span class="sxs-lookup"><span data-stu-id="26f9a-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="26f9a-163"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="26f9a-163"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="26f9a-164">MIDL</span><span class="sxs-lookup"><span data-stu-id="26f9a-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="26f9a-165"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="26f9a-165"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="26f9a-166">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="26f9a-166">Library</span></span><br/>                  | <dl> <span data-ttu-id="26f9a-167"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="26f9a-167"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="26f9a-168">DLL</span><span class="sxs-lookup"><span data-stu-id="26f9a-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26f9a-169"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26f9a-169"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="26f9a-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26f9a-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26f9a-171">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="26f9a-171">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="26f9a-172">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="26f9a-172">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> <dt>

[<span data-ttu-id="26f9a-173">**session**</span><span class="sxs-lookup"><span data-stu-id="26f9a-173">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="26f9a-174">Authentification des connexions à distance</span><span class="sxs-lookup"><span data-stu-id="26f9a-174">Authentication for Remote Connections</span></span>](authentication-for-remote-connections.md)
</dt> <dt>

[<span data-ttu-id="26f9a-175">Installation et configuration de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="26f9a-175">Installation and Configuration for Windows Remote Management</span></span>](installation-and-configuration-for-windows-remote-management.md)
</dt> </dl>

 

 





