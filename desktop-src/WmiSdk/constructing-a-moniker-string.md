---
description: Le format de chaîne de moniker est semblable à celui d’un chemin d’accès d’objet WMI standard. Pour plus d’informations, consultez Configuration requise pour le chemin d’accès de l’objet WMI.
ms.assetid: 1aacc523-2a2f-43f5-96a3-aa0387cbae3e
ms.tgt_platform: multiple
title: Construction d’une chaîne de moniker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e54e29b3c8f14890dc1cedd5907059308e8d22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318950"
---
# <a name="constructing-a-moniker-string"></a><span data-ttu-id="66797-104">Construction d’une chaîne de moniker</span><span class="sxs-lookup"><span data-stu-id="66797-104">Constructing a Moniker String</span></span>

<span data-ttu-id="66797-105">Le format de chaîne de moniker est semblable à celui d’un chemin d’accès d’objet WMI standard.</span><span class="sxs-lookup"><span data-stu-id="66797-105">The moniker string format is similar to that of a standard WMI object path.</span></span> <span data-ttu-id="66797-106">Pour plus d’informations, consultez [Configuration requise pour le chemin d’accès de l’objet WMI](wmi-object-path-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="66797-106">For more information, see [WMI Object Path Requirements](wmi-object-path-requirements.md).</span></span>

<span data-ttu-id="66797-107">Un moniker comprend les parties suivantes :</span><span class="sxs-lookup"><span data-stu-id="66797-107">A moniker has the following parts:</span></span>

-   <span data-ttu-id="66797-108">Préfixe WinMgmts : (obligatoire).</span><span class="sxs-lookup"><span data-stu-id="66797-108">The prefix WinMgmts: (mandatory).</span></span> <span data-ttu-id="66797-109">Le préfixe indique à Windows Script Host (WSH) que le code suivant utilisera les objets de l' [API de script](scripting-api-objects.md).</span><span class="sxs-lookup"><span data-stu-id="66797-109">The prefix instructs the Windows Script Host (WSH) that the following code will be using the [Scripting API objects](scripting-api-objects.md).</span></span>
-   <span data-ttu-id="66797-110">Un composant paramètres de sécurité (facultatif)</span><span class="sxs-lookup"><span data-stu-id="66797-110">A security settings component (optional)</span></span>
-   <span data-ttu-id="66797-111">Composant de chemin d’accès d’objet WMI (facultatif)</span><span class="sxs-lookup"><span data-stu-id="66797-111">A WMI object path component (optional)</span></span>

<span data-ttu-id="66797-112">Vous ne pouvez pas spécifier un mot de passe dans une chaîne de moniker WMI.</span><span class="sxs-lookup"><span data-stu-id="66797-112">You cannot specify a password in a WMI moniker string.</span></span> <span data-ttu-id="66797-113">Si vous devez modifier le mot de passe (paramètre *strPassword* ) ou le type d’authentification (paramètre *strAuthority* ) lors de la connexion à WMI, appelez [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="66797-113">If you must change the password (*strPassword* parameter) or the type of authentication (*strAuthority* parameter) when connecting to WMI, then call [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span> <span data-ttu-id="66797-114">N’oubliez pas que vous pouvez uniquement spécifier le mot de passe et l’autorité dans connexions aux ordinateurs distants.</span><span class="sxs-lookup"><span data-stu-id="66797-114">Be aware that you can only specify the password and authority in connections to remote computers.</span></span> <span data-ttu-id="66797-115">Toute tentative de définition de ces paramètres dans un script en cours d’exécution sur l’ordinateur local génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="66797-115">Attempting to set these in a script that is running on the local computer results in a error.</span></span> <span data-ttu-id="66797-116">Pour plus d’informations sur l’utilisation des paramètres de sécurité et des composants de chemin d’accès de l’objet, consultez [paramètres de sécurité WMI](/previous-versions/tn-archive/ee156574(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="66797-116">For more information about when the security settings and object path components are used, see [WMI Security Settings](/previous-versions/tn-archive/ee156574(v=technet.10)).</span></span>

<span data-ttu-id="66797-117">Le moniker suivant spécifie l’objet [**SWbemServices**](swbemservices.md) qui représente la valeur par défaut racine de l’espace de noms \\ , avec l’emprunt d’identité activé et le privilège wbemPrivilegeDebug (SeDebugPrivilege) activé, et le privilège wbemPrivilegeSecurity (SeSecurityPrivilege) désactivé.</span><span class="sxs-lookup"><span data-stu-id="66797-117">The following moniker specifies the [**SWbemServices**](swbemservices.md) object that represents the namespace root\\default, with impersonation on and the wbemPrivilegeDebug (SeDebugPrivilege) privilege enabled, and the wbemPrivilegeSecurity (SeSecurityPrivilege) privilege disabled.</span></span>


```VB
"winmgmts:{impersonationLevel=impersonate," & "(debug,!security)}!root\default"
```



> [!Note]
>
> <span data-ttu-id="66797-118">Tous les littéraux de chaîne ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="66797-118">All string literals are case-insensitive.</span></span>
>
> <span data-ttu-id="66797-119">Le préfixe «  ! » sur un privilège indique que le privilège doit être désactivé. l’omission de ce préfixe implique que le privilège doit être activé.</span><span class="sxs-lookup"><span data-stu-id="66797-119">The "!" prefix on a privilege indicates that the privilege is to be disabled; the omission of this prefix implies that the privilege is to be enabled.</span></span>
>
> <span data-ttu-id="66797-120">Le préfixe «  ! » est utilisé sur le nom ou l’espace de noms de l’ordinateur lorsque les paramètres de sécurité sont spécifiés entre crochets avant le nom ou l’espace de noms de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="66797-120">The "!" prefix is used on the computer name or namespace when security settings are specified in brackets before the computer name or namespace.</span></span>

 

<span data-ttu-id="66797-121">Les assignations par défaut suivantes sont autorisées lors de la spécification du chemin d’accès à l’objet :</span><span class="sxs-lookup"><span data-stu-id="66797-121">The following default assignments are allowed when specifying the object path:</span></span>

-   <span data-ttu-id="66797-122">Le nom de l’ordinateur peut être omis du chemin d’accès de l’objet. dans ce cas, le nom de l’ordinateur local est utilisé.</span><span class="sxs-lookup"><span data-stu-id="66797-122">The computer machine name can be omitted from the object path, in which case the local machine name is assumed.</span></span>
-   <span data-ttu-id="66797-123">L’espace de noms peut être omis du chemin d’accès de l’objet, auquel cas l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="66797-123">The namespace can be omitted from the object path, in which case the default namespace is assumed.</span></span>

    <span data-ttu-id="66797-124">Cela est déterminé par la valeur de la clé de Registre **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **Scripting** \\ **par défaut espace de noms**, la valeur par défaut est « root \\ cimv2 ».</span><span class="sxs-lookup"><span data-stu-id="66797-124">This is determined by the value of the registry key **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\**Scripting**\\**Default Namespace**, the default value is "Root\\CIMv2".</span></span>

-   <span data-ttu-id="66797-125">Une classe ou une instance peut également être spécifiée, auquel cas l’objet retourné est un objet WMI plutôt qu’un objet services.</span><span class="sxs-lookup"><span data-stu-id="66797-125">A class or instance can also be specified, in which case the returned object is a WMI object rather than a services object.</span></span>

> [!Note]  
> <span data-ttu-id="66797-126">Si une classe ou une instance est spécifiée, vous ne pouvez pas omettre l’espace de noms lors de la spécification du nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="66797-126">If a class or instance is specified, you cannot omit the namespace when specifying the computer machine name.</span></span>

 

<span data-ttu-id="66797-127">Pour obtenir une référence des constantes de privilège utilisées sur la chaîne de moniker WMI, consultez [constantes de privilège](privilege-constants.md)et descripteurs « Scripting Short Name ».</span><span class="sxs-lookup"><span data-stu-id="66797-127">For a reference of the Privilege Constants used on WMI moniker string, see [Privilege Constants](privilege-constants.md), and the "Scripting short name" descriptors.</span></span>

## <a name="valid-moniker-strings"></a><span data-ttu-id="66797-128">Chaînes de moniker valides</span><span class="sxs-lookup"><span data-stu-id="66797-128">Valid Moniker Strings</span></span>

<span data-ttu-id="66797-129">Les exemples suivants illustrent des chaînes de moniker valides.</span><span class="sxs-lookup"><span data-stu-id="66797-129">The following examples show valid moniker strings.</span></span>

<span data-ttu-id="66797-130">Le moniker suivant identifie l’espace de noms par défaut sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="66797-130">The following moniker identifies the default namespace on the local computer.</span></span> <span data-ttu-id="66797-131">Un objet [**SWbemServices**](swbemservices.md) est retourné.</span><span class="sxs-lookup"><span data-stu-id="66797-131">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
WinMgmts:
```



<span data-ttu-id="66797-132">Le moniker suivant identifie l’espace de noms par défaut sur l’ordinateur MonServeur.</span><span class="sxs-lookup"><span data-stu-id="66797-132">The following moniker identifies the default namespace on the computer myServer.</span></span> <span data-ttu-id="66797-133">Un objet [**SWbemServices**](swbemservices.md) est retourné.</span><span class="sxs-lookup"><span data-stu-id="66797-133">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
"WinMgmts://myServer"
```



<span data-ttu-id="66797-134">Le moniker suivant identifie l' \\ espace de noms CIMV2 racine sur l’ordinateur MonServeur.</span><span class="sxs-lookup"><span data-stu-id="66797-134">The following moniker identifies the root\\cimv2 namespace on the myServer computer.</span></span> <span data-ttu-id="66797-135">Un objet [**SWbemServices**](swbemservices.md) est retourné.</span><span class="sxs-lookup"><span data-stu-id="66797-135">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
"WinMgmts://myServer/root/cimv2"
```



<span data-ttu-id="66797-136">Le moniker suivant identifie l' \\ espace de noms CIMV2 racine sur le serveur local.</span><span class="sxs-lookup"><span data-stu-id="66797-136">The following moniker identifies the root\\cimv2 namespace on the local server.</span></span> <span data-ttu-id="66797-137">Un objet [**SWbemServices**](swbemservices.md) est retourné.</span><span class="sxs-lookup"><span data-stu-id="66797-137">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
"WinMgmts:root/cimv2"
```



<span data-ttu-id="66797-138">Le moniker suivant identifie la classe de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) dans l' \\ espace de noms CIMV2 racine sur le serveur MyServer.</span><span class="sxs-lookup"><span data-stu-id="66797-138">The following moniker identifies the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in the root\\cimv2 namespace on the myServer server.</span></span> <span data-ttu-id="66797-139">Un objet [**SWbemObject**](swbemobject.md) est retourné.</span><span class="sxs-lookup"><span data-stu-id="66797-139">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" _
    & "!//myServer/root/cimv2:Win32_LogicalDisk"
```



<span data-ttu-id="66797-140">Le moniker suivant identifie la classe de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) dans l' \\ espace de noms CIMV2 racine sur le serveur local.</span><span class="sxs-lookup"><span data-stu-id="66797-140">The following moniker identifies the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in the root\\cimv2 namespace on the local server.</span></span> <span data-ttu-id="66797-141">Un objet [**SWbemObject**](swbemobject.md) est retourné.</span><span class="sxs-lookup"><span data-stu-id="66797-141">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk"
```



<span data-ttu-id="66797-142">Le moniker suivant identifie la classe de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) dans l’espace de noms par défaut sur le serveur local.</span><span class="sxs-lookup"><span data-stu-id="66797-142">The following moniker identifies the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in the default namespace on the local server.</span></span> <span data-ttu-id="66797-143">Un objet [**SWbemObject**](swbemobject.md) est retourné.</span><span class="sxs-lookup"><span data-stu-id="66797-143">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk"
```



<span data-ttu-id="66797-144">Le moniker suivant identifie l’instance du [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondant au lecteur C : dans l’espace de noms de script par défaut sur le serveur local.</span><span class="sxs-lookup"><span data-stu-id="66797-144">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the default scripting namespace on the local server.</span></span> <span data-ttu-id="66797-145">Un objet [**SWbemObject**](swbemobject.md) est retourné.</span><span class="sxs-lookup"><span data-stu-id="66797-145">An [**SWbemObject**](swbemobject.md) object is returned.</span></span> <span data-ttu-id="66797-146">L’espace de noms par défaut pour les scripts est déterminé par le paramètre de configuration de l’espace de noms par défaut tel que spécifié dans le contrôle WMI.</span><span class="sxs-lookup"><span data-stu-id="66797-146">The default namespace for scripting is determined by the default namespace configuration setting as specified in the WMI Control.</span></span> <span data-ttu-id="66797-147">Pour plus d’informations, consultez [définition de la sécurité de l’espace de noms avec le contrôle WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="66797-147">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>


```VB
"WinMgmts::Win32_LogicalDisk='C:'"
```



<span data-ttu-id="66797-148">Le moniker suivant identifie l’instance du [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondant au lecteur C : dans l' \\ espace de noms CIMV2 racine sur le serveur monserveur.</span><span class="sxs-lookup"><span data-stu-id="66797-148">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the root\\cimv2 namespace on the myServer server.</span></span> <span data-ttu-id="66797-149">Un objet [**SWbemObject**](swbemobject.md) est retourné.</span><span class="sxs-lookup"><span data-stu-id="66797-149">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!//myServer/root/cimv2:Win32_LogicalDisk="C:""
```



<span data-ttu-id="66797-150">Le moniker suivant identifie l’instance du [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondant au lecteur C : dans l' \\ espace de noms CIMV2 racine sur le serveur local.</span><span class="sxs-lookup"><span data-stu-id="66797-150">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the root\\cimv2 namespace on the local server.</span></span> <span data-ttu-id="66797-151">Un objet [**SWbemObject**](swbemobject.md) est retourné.</span><span class="sxs-lookup"><span data-stu-id="66797-151">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk="C:""
```



<span data-ttu-id="66797-152">Le moniker suivant identifie l’instance du [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) correspondant au lecteur C : dans l’espace de noms par défaut sur le serveur local.</span><span class="sxs-lookup"><span data-stu-id="66797-152">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the default namespace on the local server.</span></span> <span data-ttu-id="66797-153">Un objet [**SWbemObject**](swbemobject.md) est retourné.</span><span class="sxs-lookup"><span data-stu-id="66797-153">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk="C:""
```



<span data-ttu-id="66797-154">Le moniker suivant définit le niveau d’emprunt d’identité sur emprunter l’identité et définit le \_ privilège de débogage de la se.</span><span class="sxs-lookup"><span data-stu-id="66797-154">The following moniker sets the impersonation level to impersonate and sets the SE\_DEBUG privilege.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate, (Debug)}"
```



<span data-ttu-id="66797-155">Le moniker suivant définit le niveau d’emprunt d’identité sur emprunter l’identité et définit le \_ privilège de débogage de la se.</span><span class="sxs-lookup"><span data-stu-id="66797-155">The following moniker sets the impersonation level to impersonate and sets the SE\_DEBUG privilege.</span></span> <span data-ttu-id="66797-156">Elle révoque également le privilège d’arrêt de la SE \_ .</span><span class="sxs-lookup"><span data-stu-id="66797-156">It also revokes the SE\_SHUTDOWN privilege.</span></span>


```VB
"WinMgmts:{impersonate,(Debug,!Shutdown)}"
```



<span data-ttu-id="66797-157">Le moniker suivant récupère les descriptions localisées de l’anglais américain pour la classe **MyClass** à partir de l' \\ espace de noms WMI racine.</span><span class="sxs-lookup"><span data-stu-id="66797-157">The following moniker retrieves American English localized descriptions for the **myclass** class from the root\\wmi namespace.</span></span>


```VB
"WinMgmts:[locale=ms_409]!root/wmi:myclass"
```



<span data-ttu-id="66797-158">Le moniker suivant demande l’authentification Kerberos à l’aide du serveur mondomaine principal \\ .</span><span class="sxs-lookup"><span data-stu-id="66797-158">The following moniker requests Kerberos authentication using the principal mydomain\\server.</span></span>


```VB
"Winmgmts:{impersonationLevel=delegate," _
    & "authority=kerberos:mydomain\server}" _
    & "!//myserver/root/default:__cimomidentification=@"
```



<span data-ttu-id="66797-159">Le moniker suivant demande l’authentification NTLM à l’aide du domaine mydomain.</span><span class="sxs-lookup"><span data-stu-id="66797-159">The following moniker requests NTLM authentication using the mydomain domain.</span></span>


```VB
"Winmgmts:{impersonationLevel=impersonate," & _
    "authority=ntlmdomain:mydomain} " & _
    "!//myserver/root/default:__cimomidentification=@
```



<span data-ttu-id="66797-160">L’exemple de code VBScript suivant montre comment combiner des paramètres de sécurité et de paramètres régionaux dans un moniker.</span><span class="sxs-lookup"><span data-stu-id="66797-160">The following VBScript code example shows how to combine security and locale parameters in a moniker.</span></span>


```VB
'*****************************************************************
'   Name    :  Moniker.vbs
'
'   Purpose :  This example shows how to set various 
'              parameters in a moniker. 
'****************************************************************

Set myobj = GetObject("WINMGMTS:" _
            & "{impersonationLevel=impersonate," _
            & "authenticationLevel=pktPrivacy," _
            & "authority=ntlmdomain:mydomain," _
            & "(Debug,!Shutdown)}" _
            & "[locale=ms_409]" _
            & "!\\User1\ROOT\CIMV2:Win32_LogicalDisk=""C:""")

wscript.echo "File system = " & myobj.filesystem
```



> [!Note]
>
> Bien que les monikers fournissent un accès plus direct aux objets, dans certains cas, l’utilisation répétée de monikers peut être moins efficace que le code équivalent qui se connecte explicitement à WMI. <span data-ttu-id="66797-162">Si les performances de l’application sont un facteur important, envisagez d’utiliser les autres mécanismes.</span><span class="sxs-lookup"><span data-stu-id="66797-162">If application performance is a consideration, consider using the alternative mechanisms.</span></span>
>
> <span data-ttu-id="66797-163">Il n’est pas possible d’utiliser la fonction **GetObject** fournie par VBScript pour mettre à jour ou définir des données lors de l’exécution de scripts incorporés dans une page HTML, car Microsoft Internet Explorer refuse l’utilisation de cet appel pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="66797-163">It is not possible to use the **GetObject** function provided by VBScript to update or set data when running scripts embedded within an HTML page, as Microsoft Internet Explorer denies the use of this call for security reasons.</span></span>

 

 

 
