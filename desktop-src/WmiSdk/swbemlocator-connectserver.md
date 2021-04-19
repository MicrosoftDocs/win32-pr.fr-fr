---
description: Établit une connexion à l’espace de noms sur l’ordinateur spécifié dans le paramètre strServer.
ms.assetid: 31364c68-b031-4cf0-851f-b4e302f077e0
ms.tgt_platform: multiple
title: Méthode SWbemLocator. ConnectServer (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 31c2e6de8cf1504543727cad056a3616a51182d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541994"
---
# <a name="swbemlocatorconnectserver-method"></a><span data-ttu-id="49526-103">Méthode SWbemLocator. ConnectServer</span><span class="sxs-lookup"><span data-stu-id="49526-103">SWbemLocator.ConnectServer method</span></span>

<span data-ttu-id="49526-104">La méthode **ConnectServer** de l’objet [**SWbemLocator**](swbemlocator.md) se connecte à l’espace de noms sur l’ordinateur spécifié dans le paramètre *strServer* .</span><span class="sxs-lookup"><span data-stu-id="49526-104">The **ConnectServer** method of the [**SWbemLocator**](swbemlocator.md) object connects to the namespace on the computer that is specified in the *strServer* parameter.</span></span> <span data-ttu-id="49526-105">L’ordinateur cible peut être local ou distant, mais WMI doit être installé.</span><span class="sxs-lookup"><span data-stu-id="49526-105">The target computer can be either local or remote, but it must have WMI installed.</span></span> <span data-ttu-id="49526-106">Pour obtenir des exemples et une comparaison avec le type de moniker Connection, consultez [création d’un script WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="49526-106">For examples and a comparison with the moniker type of connection, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span>

<span data-ttu-id="49526-107">À compter de Windows Vista, **SWbemLocator. ConnectServer** peut se connecter avec des ordinateurs exécutant IPv6 à l’aide d’une adresse IPv6 dans le paramètre *strServer* .</span><span class="sxs-lookup"><span data-stu-id="49526-107">Starting with Windows Vista, **SWbemLocator.ConnectServer** can connect with computers running IPv6 using an IPv6 address in the *strServer* parameter.</span></span> <span data-ttu-id="49526-108">Pour plus d’informations, consultez [prise en charge d’IPv6 et IPv6 dans WMI](ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="49526-108">For more information, see [IPv6 and IPv4 Support in WMI](ipv6-and-ipv4-support-in-wmi.md).</span></span>

<span data-ttu-id="49526-109">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="49526-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="49526-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49526-110">Syntax</span></span>


```VB
objwbemServices = .ConnectServer( _
  [ ByVal strServer ], _
  [ ByVal strNamespace ], _
  [ ByVal strUser ], _
  [ ByVal strPassword ], _
  [ ByVal strLocale ], _
  [ ByVal strAuthority ], _
  [ ByVal iSecurityFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="49526-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49526-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49526-112">*strServer* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="49526-112">*strServer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49526-113">Nom de l’ordinateur auquel vous vous connectez.</span><span class="sxs-lookup"><span data-stu-id="49526-113">Computer name to which you are connecting.</span></span> <span data-ttu-id="49526-114">Si l’ordinateur distant se trouve dans un domaine différent du compte d’utilisateur sous lequel vous vous connectez, utilisez le nom d’ordinateur complet.</span><span class="sxs-lookup"><span data-stu-id="49526-114">If the remote computer is in a different domain than the user account under which you log in, then use the fully qualified computer name.</span></span> <span data-ttu-id="49526-115">Si vous ne fournissez pas ce paramètre, l’appel est défini par défaut sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="49526-115">If you do not provide this parameter, the call defaults to the local computer.</span></span>

<span data-ttu-id="49526-116">Exemple : `server1.network.fabrikam`</span><span class="sxs-lookup"><span data-stu-id="49526-116">Example: `server1.network.fabrikam`</span></span>

<span data-ttu-id="49526-117">Vous pouvez également utiliser une adresse IP dans ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="49526-117">You also can use an IP address in this parameter.</span></span> <span data-ttu-id="49526-118">Si l’adresse IP est au format IPv6, l’ordinateur cible doit exécuter IPv6.</span><span class="sxs-lookup"><span data-stu-id="49526-118">If the IP address is in IPv6 format, the target computer must be running IPv6.</span></span> <span data-ttu-id="49526-119">Une adresse IPv4 ressemble à ceci `123.123.123.123`</span><span class="sxs-lookup"><span data-stu-id="49526-119">An address in IPv4 looks like `123.123.123.123`</span></span>

<span data-ttu-id="49526-120">Une adresse IP au format IPv6 ressemble à ce qui suit. `2010:836B:4179::836B:4179`</span><span class="sxs-lookup"><span data-stu-id="49526-120">An IP address in IPv6 format looks like `2010:836B:4179::836B:4179`</span></span>

<span data-ttu-id="49526-121">Pour plus d’informations sur DNS et IPv4, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="49526-121">For more information on DNS and IPv4, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="49526-122">*strNameSpace* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="49526-122">*strNamespace* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49526-123">Chaîne qui spécifie l’espace de noms auquel vous vous connectez.</span><span class="sxs-lookup"><span data-stu-id="49526-123">String that specifies the namespace to which you log on.</span></span> <span data-ttu-id="49526-124">Par exemple, pour vous connecter à l' \\ espace de noms racine par défaut, utilisez la racine \\ par défaut.</span><span class="sxs-lookup"><span data-stu-id="49526-124">For example, to log on to the root\\default namespace, use root\\default.</span></span> <span data-ttu-id="49526-125">Si vous ne spécifiez pas ce paramètre, la valeur par défaut est l’espace de noms configuré comme espace de noms par défaut pour les scripts.</span><span class="sxs-lookup"><span data-stu-id="49526-125">If you do not specify this parameter, it defaults to the namespace that is configured as the default namespace for scripting.</span></span> <span data-ttu-id="49526-126">Pour plus d’informations, consultez [création d’une application ou d’un script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="49526-126">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

<span data-ttu-id="49526-127">Exemple : « root \\ cimv2 »</span><span class="sxs-lookup"><span data-stu-id="49526-127">Example: "root\\CIMV2"</span></span>

</dd> <dt>

<span data-ttu-id="49526-128">*strUser* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="49526-128">*strUser* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49526-129">Nom d’utilisateur à utiliser pour se connecter.</span><span class="sxs-lookup"><span data-stu-id="49526-129">User name to use to connect.</span></span> <span data-ttu-id="49526-130">La chaîne peut être sous la forme d’un nom d’utilisateur ou d’un nom d’utilisateur de domaine \\ .</span><span class="sxs-lookup"><span data-stu-id="49526-130">The string can be in the form of either a user name or a Domain\\Username.</span></span> <span data-ttu-id="49526-131">Laissez ce paramètre vide pour utiliser le contexte de sécurité actuel.</span><span class="sxs-lookup"><span data-stu-id="49526-131">Leave this parameter blank to use the current security context.</span></span> <span data-ttu-id="49526-132">Le paramètre *strUser* doit être utilisé uniquement avec les connexions aux serveurs WMI distants.</span><span class="sxs-lookup"><span data-stu-id="49526-132">The *strUser* parameter should only be used with connections to remote WMI servers.</span></span> <span data-ttu-id="49526-133">Si vous tentez de spécifier *strUser* pour une connexion WMI locale, la tentative de connexion échoue.</span><span class="sxs-lookup"><span data-stu-id="49526-133">If you attempt to specify *strUser* for a local WMI connection, the connection attempt fails.</span></span> <span data-ttu-id="49526-134">Si l’authentification Kerberos est utilisée, le nom d’utilisateur et le mot de passe spécifiés dans *strUser* et *strPassword* ne peuvent pas être interceptés sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="49526-134">If Kerberos authentication is in use, then the username and password that is specified in *strUser* and *strPassword* cannot be intercepted on a network.</span></span> <span data-ttu-id="49526-135">Vous pouvez utiliser le format UPN pour spécifier le *strUser*.</span><span class="sxs-lookup"><span data-stu-id="49526-135">You can use the UPN format to specify the *strUser*.</span></span>

<span data-ttu-id="49526-136">Exemple : « nom_domaine \\ nom_utilisateur »</span><span class="sxs-lookup"><span data-stu-id="49526-136">Example: "DomainName\\UserName"</span></span>

> [!Note]  
> <span data-ttu-id="49526-137">Si un domaine est spécifié dans *strAuthority*, le domaine ne doit pas être spécifié ici.</span><span class="sxs-lookup"><span data-stu-id="49526-137">If a domain is specified in *strAuthority*, then the domain must not be specified here.</span></span> <span data-ttu-id="49526-138">La spécification du domaine dans les deux paramètres génère une erreur de paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="49526-138">Specifying the domain in both parameters results in an Invalid Parameter error.</span></span>

 

</dd> <dt>

<span data-ttu-id="49526-139">*strPassword* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="49526-139">*strPassword* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49526-140">Chaîne qui spécifie le mot de passe à utiliser lors de la tentative de connexion.</span><span class="sxs-lookup"><span data-stu-id="49526-140">String that specifies the password to use when attempting to connect.</span></span> <span data-ttu-id="49526-141">Laissez le paramètre vide pour utiliser le contexte de sécurité actuel.</span><span class="sxs-lookup"><span data-stu-id="49526-141">Leave the parameter blank to use the current security context.</span></span> <span data-ttu-id="49526-142">Le paramètre *strPassword* doit être utilisé uniquement avec les connexions aux serveurs WMI distants.</span><span class="sxs-lookup"><span data-stu-id="49526-142">The *strPassword* parameter should only be used with connections to remote WMI servers.</span></span> <span data-ttu-id="49526-143">Si vous tentez de spécifier *strPassword* pour une connexion WMI locale, la tentative de connexion échoue.</span><span class="sxs-lookup"><span data-stu-id="49526-143">If you attempt to specify *strPassword* for a local WMI connection, the connection attempt fails.</span></span> <span data-ttu-id="49526-144">Si l’authentification Kerberos est en cours d’utilisation, le nom d’utilisateur et le mot de passe spécifiés dans *strUser* et *strPassword* ne peuvent pas être interceptés sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="49526-144">If Kerberos authentication is in use then the username and password that is specified in *strUser* and *strPassword* cannot be intercepted on the network.</span></span>

</dd> <dt>

<span data-ttu-id="49526-145">*strLocale* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="49526-145">*strLocale* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49526-146">Chaîne qui spécifie le code de localisation.</span><span class="sxs-lookup"><span data-stu-id="49526-146">String that specifies the localization code.</span></span> <span data-ttu-id="49526-147">Si vous souhaitez utiliser les paramètres régionaux actuels, laissez-le vide.</span><span class="sxs-lookup"><span data-stu-id="49526-147">If you want to use the current locale, leave it blank.</span></span> <span data-ttu-id="49526-148">Si la valeur n’est pas vide, ce paramètre doit être une chaîne qui indique les paramètres régionaux souhaités où les informations doivent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="49526-148">If not blank, this parameter must be a string that indicates the desired locale where information must be retrieved.</span></span> <span data-ttu-id="49526-149">Pour les identificateurs de paramètres régionaux Microsoft, le format de la chaîne est « MS \_ xxxx », où xxxx est une chaîne au format hexadécimal qui indique le LCID.</span><span class="sxs-lookup"><span data-stu-id="49526-149">For Microsoft locale identifiers, the format of the string is "MS\_xxxx", where xxxx is a string in the hexadecimal form that indicates the LCID.</span></span> <span data-ttu-id="49526-150">Par exemple, l’anglais américain s’affiche sous la forme « MS \_ 409 ».</span><span class="sxs-lookup"><span data-stu-id="49526-150">For example, American English would appear as "MS\_409".</span></span>

</dd> <dt>

<span data-ttu-id="49526-151">*strAuthority* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="49526-151">*strAuthority* \[in, optional\]</span></span>
</dt> <dd>

<dt>

<span data-ttu-id="49526-152">""</span><span class="sxs-lookup"><span data-stu-id="49526-152">""</span></span>
</dt> <dd>

<span data-ttu-id="49526-153">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="49526-153">This parameter is optional.</span></span> <span data-ttu-id="49526-154">Toutefois, si elle est spécifiée, seuls Kerberos ou NTLMDomain peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="49526-154">However, if it is specified, only Kerberos or NTLMDomain can be used.</span></span>

</dd> <dt>

<span data-ttu-id="49526-155">Clé</span><span class="sxs-lookup"><span data-stu-id="49526-155">Kerberos:</span></span>
</dt> <dd>

<span data-ttu-id="49526-156">Si le paramètre *strAuthority* commence par la chaîne « Kerberos : », l’authentification Kerberos est utilisée et ce paramètre doit contenir un nom de principal Kerberos.</span><span class="sxs-lookup"><span data-stu-id="49526-156">If the *strAuthority* parameter begins with the string "Kerberos:", then Kerberos authentication is used and this parameter should contain a Kerberos principal name.</span></span> <span data-ttu-id="49526-157">Le nom principal Kerberos est spécifié sous la forme Kerberos :*Domain*, par exemple `Kerberos:fabrikam` où `fabrikam` est le serveur auquel vous tentez de vous connecter.</span><span class="sxs-lookup"><span data-stu-id="49526-157">The Kerberos principal name is specified as Kerberos:*domain*, such as `Kerberos:fabrikam` where `fabrikam` is the server to which you are attempting to connect.</span></span>

<span data-ttu-id="49526-158">Exemple : « Kerberos : domaine »</span><span class="sxs-lookup"><span data-stu-id="49526-158">Example: "Kerberos:DOMAIN"</span></span>

</dd> <dt>

<span data-ttu-id="49526-159">NTLMDomain</span><span class="sxs-lookup"><span data-stu-id="49526-159">NTLMDomain:</span></span>
</dt> <dd>

<span data-ttu-id="49526-160">Pour utiliser l’authentification NTLM (NT LAN Manager), vous devez la spécifier sous la forme NTLMDomain :*Domain*, par exemple `NTLMDomain:fabrikam` où `fabrikam` est le nom du domaine.</span><span class="sxs-lookup"><span data-stu-id="49526-160">To use NT Lan Manager (NTLM) authentication, you must specify it as NTLMDomain:*domain*, such as `NTLMDomain:fabrikam` where `fabrikam` is the name of the domain.</span></span>

<span data-ttu-id="49526-161">Exemple : « NTLMDomain : DOMAIN »</span><span class="sxs-lookup"><span data-stu-id="49526-161">Example: "NTLMDomain:DOMAIN"</span></span>

</dd> </dl>

<span data-ttu-id="49526-162">Si vous laissez ce paramètre vide, le système d’exploitation négocie avec COM pour déterminer si l’authentification NTLM ou Kerberos est utilisée.</span><span class="sxs-lookup"><span data-stu-id="49526-162">If you leave this parameter blank, the operating system negotiates with COM to determine whether NTLM or Kerberos authentication is used.</span></span> <span data-ttu-id="49526-163">Ce paramètre ne doit être utilisé qu’avec des connexions à des serveurs WMI distants.</span><span class="sxs-lookup"><span data-stu-id="49526-163">This parameter should only be used with connections to remote WMI servers.</span></span> <span data-ttu-id="49526-164">Si vous tentez de définir l’autorité pour une connexion WMI locale, la tentative de connexion échoue.</span><span class="sxs-lookup"><span data-stu-id="49526-164">If you attempt to set the authority for a local WMI connection, the connection attempt fails.</span></span>

> [!Note]  
> <span data-ttu-id="49526-165">Si le domaine est spécifié dans *strUser*, qui est l’emplacement par défaut, il ne doit pas être spécifié ici.</span><span class="sxs-lookup"><span data-stu-id="49526-165">If the domain is specified in *strUser*, which is the preferred location, then it must not be specified here.</span></span> <span data-ttu-id="49526-166">La spécification du domaine dans les deux paramètres génère une erreur de paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="49526-166">Specifying the domain in both parameters results in an Invalid Parameter error.</span></span>

 

</dd> <dt>

<span data-ttu-id="49526-167">*iSecurityFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="49526-167">*iSecurityFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49526-168">Utilisé pour passer des valeurs d’indicateur à **ConnectServer**.</span><span class="sxs-lookup"><span data-stu-id="49526-168">Used to pass flag values to **ConnectServer**.</span></span>

<dt>

<span data-ttu-id="49526-169">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="49526-169">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="49526-170">La valeur 0 pour ce paramètre entraîne le retour de l’appel à **ConnectServer** uniquement après l’établissement de la connexion au serveur.</span><span class="sxs-lookup"><span data-stu-id="49526-170">A value of 0 for this parameter causes the call to **ConnectServer** to return only after the connection to the server is established.</span></span> <span data-ttu-id="49526-171">Cela peut empêcher votre programme de répondre indéfiniment si la connexion ne peut pas être établie.</span><span class="sxs-lookup"><span data-stu-id="49526-171">This could cause your program to stop responding indefinitely if the connection cannot be established.</span></span>

</dd> <dt>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>

<span data-ttu-id="49526-172"><span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>wbemConnectFlagUseMaxWait \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="49526-172"><span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>\*\*\*\*wbemConnectFlagUseMaxWait\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="49526-173">Le retour de l’appel **ConnectServer** est garanti à 2 minutes ou moins.</span><span class="sxs-lookup"><span data-stu-id="49526-173">The **ConnectServer** call is guaranteed to return in 2 minutes or less.</span></span> <span data-ttu-id="49526-174">Utilisez cet indicateur pour empêcher votre programme de cesser de répondre indéfiniment si la connexion ne peut pas être établie.</span><span class="sxs-lookup"><span data-stu-id="49526-174">Use this flag to prevent your program from ceasing to respond indefinitely if the connection cannot be established.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="49526-175">*objwbemNamedValueSet* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="49526-175">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49526-176">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="49526-176">Typically, this is undefined.</span></span> <span data-ttu-id="49526-177">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="49526-177">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="49526-178">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="49526-178">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49526-179">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49526-179">Return value</span></span>

<span data-ttu-id="49526-180">En cas de réussite, WMI retourne un objet [**SWbemServices**](swbemservices.md) qui est lié à l’espace de noms spécifié dans *strNameSpace* sur l’ordinateur spécifié dans *strServer*.</span><span class="sxs-lookup"><span data-stu-id="49526-180">If successful, WMI returns an [**SWbemServices**](swbemservices.md) object that is bound to the namespace that is specified in *strNamespace* on the computer that is specified in *strServer*.</span></span>

## <a name="error-codes"></a><span data-ttu-id="49526-181">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="49526-181">Error codes</span></span>

<span data-ttu-id="49526-182">À la fin de la méthode **ConnectServer** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="49526-182">After the completion of the **ConnectServer** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="49526-183">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="49526-183">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="49526-184">Le nom d’utilisateur et le mot de passe actuels ou spécifiés ne sont pas valides ou ne sont pas autorisés à établir la connexion.</span><span class="sxs-lookup"><span data-stu-id="49526-184">The current or specified user name and password were not valid or authorized to make the connection.</span></span>

</dd> <dt>

<span data-ttu-id="49526-185">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="49526-185">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="49526-186">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="49526-186">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="49526-187">**wbemErrInvalidNamespace** -2147749902 (0x8004100E)</span><span class="sxs-lookup"><span data-stu-id="49526-187">**wbemErrInvalidNamespace** - 2147749902 (0x8004100E)</span></span>
</dt> <dd>

<span data-ttu-id="49526-188">L’espace de noms spécifié n’existait pas sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="49526-188">The specified namespace did not exist on the server.</span></span>

</dd> <dt>

<span data-ttu-id="49526-189">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="49526-189">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="49526-190">Un paramètre non valide a été spécifié ou l’espace de noms n’a pas pu être analysé.</span><span class="sxs-lookup"><span data-stu-id="49526-190">An invalid parameter was specified, or the namespace could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="49526-191">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="49526-191">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="49526-192">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="49526-192">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="49526-193">**wbemErrTransportFailure** -2147749909</span><span class="sxs-lookup"><span data-stu-id="49526-193">**wbemErrTransportFailure** - 2147749909</span></span>
</dt> <dd>

<span data-ttu-id="49526-194">Une erreur réseau s’est produite, empêchant le fonctionnement normal.</span><span class="sxs-lookup"><span data-stu-id="49526-194">A networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49526-195">Notes</span><span class="sxs-lookup"><span data-stu-id="49526-195">Remarks</span></span>

<span data-ttu-id="49526-196">La méthode **ConnectServer** est souvent utilisée lors de la connexion à un compte avec des informations d’identification de nom d’utilisateur et de mot de passe différentes sur un ordinateur distant, car vous ne pouvez pas spécifier un mot de passe différent dans une chaîne de [moniker](constructing-a-moniker-string.md) .</span><span class="sxs-lookup"><span data-stu-id="49526-196">The **ConnectServer** method is often used when connecting to an account with a different username and password credentials on a remote computer because you cannot specify a different password in a [moniker](constructing-a-moniker-string.md) string.</span></span> <span data-ttu-id="49526-197">Pour plus d’informations, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="49526-197">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="49526-198">L’utilisation d’une adresse IPv4 pour se connecter à un serveur distant peut entraîner un comportement inattendu.</span><span class="sxs-lookup"><span data-stu-id="49526-198">Using an IPv4 address to connect to a remote server may result in unexpected behavior.</span></span> <span data-ttu-id="49526-199">La cause la plus probable est l’obsolescence des entrées DNS dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="49526-199">The likely cause is stale DNS entries in your environment.</span></span> <span data-ttu-id="49526-200">Dans ces circonstances, l’entrée PTR périmée pour l’ordinateur est utilisée, avec des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="49526-200">In these circumstances, the stale PTR entry for the machine will be used, with unpredictable results.</span></span> <span data-ttu-id="49526-201">Pour éviter ce comportement, vous pouvez ajouter un point (".") à l’adresse IP avant d’appeler ConnectServer.</span><span class="sxs-lookup"><span data-stu-id="49526-201">To avoid this behavior, you can append a period (".") to the IP address before calling ConnectServer.</span></span> <span data-ttu-id="49526-202">Cela provoque l’échec de la recherche DNS inversée, mais peut permettre à l’appel **ConnectServer** de réussir sur l’ordinateur approprié.</span><span class="sxs-lookup"><span data-stu-id="49526-202">This causes the reverse DNS lookup to fail, but may allow the **ConnectServer** call to succeed on the correct machine.</span></span>

## <a name="examples"></a><span data-ttu-id="49526-203">Exemples</span><span class="sxs-lookup"><span data-stu-id="49526-203">Examples</span></span>

<span data-ttu-id="49526-204">L’exemple de code VBScript suivant décrit comment se connecter à un ordinateur distant pour obtenir des données [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) .</span><span class="sxs-lookup"><span data-stu-id="49526-204">The following VBScript code example describes how to connect to a remote computer to obtain [**Win32\_IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) data.</span></span> <span data-ttu-id="49526-205">Le nom de domaine spécifié dans *strDomain* est utilisé dans *strAuthority*.</span><span class="sxs-lookup"><span data-stu-id="49526-205">The domain name that is specified in *strDomain* is used in *strAuthority*.</span></span>


```VB
Const intMin = 3600
strComputer = "RemoteComputer" 
strDomain = "DomainName"  
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
Wscript.Echo

Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator") 
Set objWMIService = objSWbemLocator.ConnectServer(strComputer, _ 
                                                  "root\CIMV2", _ 
                                                  strUser, _ 
                                                  strPassword, _ 
                                                  "MS_409", _ 
                                                  "NTLMDomain:" + strDomain) 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_IP4RouteTable",,48) 
For Each objItem in colItems
    WScript.Echo "Age in Minutes: " & int(objItem.Age/intMin) & VBNewLine _
               & "Description:    " & objItem.Description & VBNewLine _
               & "Destination:    " & objItem.Destination & VBNewLine _
               & "InterfaceIndex: " & objItem.InterfaceIndex & VBNewLine _
               & "Mask:           " & objItem.Mask & VBNewLine _
               & "Metric1:        " & objItem.Metric1 & VBNewLine _
               & "Metric2:        " & objItem.Metric2 & VBNewLine _
               & "Metric3:        " & objItem.Metric3 & VBNewLine _
               & "Metric4:        " & objItem.Metric4 & VBNewLine _
               & "Metric5:        " & objItem.Metric5 & VBNewLine _
               & "Name:           " & objItem.Name & VBNewLine _
               & "NextHop:        " & objItem.NextHop & VBNewLine _
               & "Protocol:       " & objItem.Protocol & VBNewLine _
               & "Type: " & objItem.Type
    WScript.Echo
   </example>
Next
```



<span data-ttu-id="49526-206">L’extrait de code PowerShell suivant accède à un serveur distant et répertorie les classes WMI disponibles.</span><span class="sxs-lookup"><span data-stu-id="49526-206">The following PowerShell snippet access a remote server and lists the available WMI classes.</span></span>


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a><span data-ttu-id="49526-207">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49526-207">Requirements</span></span>



| <span data-ttu-id="49526-208">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49526-208">Requirement</span></span> | <span data-ttu-id="49526-209">Valeur</span><span class="sxs-lookup"><span data-stu-id="49526-209">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49526-210">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49526-210">Minimum supported client</span></span><br/> | <span data-ttu-id="49526-211">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49526-211">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="49526-212">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49526-212">Minimum supported server</span></span><br/> | <span data-ttu-id="49526-213">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49526-213">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49526-214">En-tête</span><span class="sxs-lookup"><span data-stu-id="49526-214">Header</span></span><br/>                   | <dl> <span data-ttu-id="49526-215"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="49526-215"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="49526-216">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="49526-216">Type library</span></span><br/>             | <dl> <span data-ttu-id="49526-217"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="49526-217"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="49526-218">DLL</span><span class="sxs-lookup"><span data-stu-id="49526-218">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49526-219"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49526-219"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="49526-220">CLSID</span><span class="sxs-lookup"><span data-stu-id="49526-220">CLSID</span></span><br/>                    | <span data-ttu-id="49526-221">CLSID \_ SWbemLocator</span><span class="sxs-lookup"><span data-stu-id="49526-221">CLSID\_SWbemLocator</span></span><br/>                                                          |
| <span data-ttu-id="49526-222">IID</span><span class="sxs-lookup"><span data-stu-id="49526-222">IID</span></span><br/>                      | <span data-ttu-id="49526-223">IID \_ ISWbemLocator</span><span class="sxs-lookup"><span data-stu-id="49526-223">IID\_ISWbemLocator</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="49526-224">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49526-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49526-225">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="49526-225">**SWbemLocator**</span></span>](swbemlocator.md)
</dt> <dt>

[<span data-ttu-id="49526-226">**M**</span><span class="sxs-lookup"><span data-stu-id="49526-226">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="49526-227">Connexion à WMI sur un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="49526-227">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="49526-228">Création d’un script WMI</span><span class="sxs-lookup"><span data-stu-id="49526-228">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
</dt> </dl>

 

