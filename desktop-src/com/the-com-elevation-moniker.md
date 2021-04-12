---
title: Moniker d’élévation COM
description: Le moniker d’élévation COM autorise les applications qui s’exécutent sous le contrôle de compte d’utilisateur (UAC) à activer des classes COM avec des privilèges élevés. Pour plus d’informations, consultez focus sur le moindre privilège.
ms.assetid: 1595ebb8-65af-4609-b3e7-a21209e64391
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc80774764cb99e63ed3334a8c0f9c8cedd2500
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463806"
---
# <a name="the-com-elevation-moniker"></a><span data-ttu-id="4f009-104">Moniker d’élévation COM</span><span class="sxs-lookup"><span data-stu-id="4f009-104">The COM Elevation Moniker</span></span>

<span data-ttu-id="4f009-105">Le moniker d’élévation COM autorise les applications qui s’exécutent sous le contrôle de compte d’utilisateur (UAC) à activer des classes COM avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="4f009-105">The COM elevation moniker allows applications that are running under user account control (UAC) to activate COM classes with elevated privileges.</span></span> <span data-ttu-id="4f009-106">Pour plus d’informations, consultez [focus sur le moindre privilège](/previous-versions/dotnet/articles/aa480194(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="4f009-106">For more information, see [Focus on Least Privilege](/previous-versions/dotnet/articles/aa480194(v=msdn.10)).</span></span>

## <a name="when-to-use-the-elevation-moniker"></a><span data-ttu-id="4f009-107">Quand utiliser le moniker d’élévation</span><span class="sxs-lookup"><span data-stu-id="4f009-107">When to Use the Elevation Moniker</span></span>

<span data-ttu-id="4f009-108">Le moniker d’élévation est utilisé pour activer une classe COM afin d’accomplir une fonction spécifique et limitée qui requiert des privilèges élevés, tels que la modification de la date et de l’heure système.</span><span class="sxs-lookup"><span data-stu-id="4f009-108">The elevation moniker is used to activate a COM class to accomplish a specific and limited function that requires elevated privileges, such as changing the system date and time.</span></span>

<span data-ttu-id="4f009-109">L’élévation nécessite la participation à la fois d’une classe COM et de son client.</span><span class="sxs-lookup"><span data-stu-id="4f009-109">Elevation requires participation from both a COM class and its client.</span></span> <span data-ttu-id="4f009-110">La classe COM doit être configurée pour prendre en charge l’élévation en annotant son entrée de Registre, comme décrit dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="4f009-110">The COM class must be configured to support elevation by annotating its registry entry, as described in the Requirements section.</span></span> <span data-ttu-id="4f009-111">Le client COM doit demander une élévation à l’aide du moniker d’élévation.</span><span class="sxs-lookup"><span data-stu-id="4f009-111">The COM client must request elevation by using the elevation moniker.</span></span>

<span data-ttu-id="4f009-112">Le moniker d’élévation n’est pas destiné à fournir la compatibilité des applications.</span><span class="sxs-lookup"><span data-stu-id="4f009-112">The elevation moniker is not intended to provide application compatibility.</span></span> <span data-ttu-id="4f009-113">Par exemple, si vous souhaitez exécuter une application COM héritée telle que WinWord comme un serveur avec élévation de privilèges, vous devez configurer l’exécutable du client COM pour exiger une élévation, plutôt que d’activer la classe de l’application héritée avec le moniker d’élévation.</span><span class="sxs-lookup"><span data-stu-id="4f009-113">For example, if you want to run a legacy COM application such as WinWord as an elevated server, you should configure the COM client executable to require elevation, rather than activating the legacy application's class with the elevation moniker.</span></span> <span data-ttu-id="4f009-114">Lorsque le client COM avec élévation de privilèges appelle [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) à l’aide du CLSID de l’application héritée, l’état élevé du client est transmis au processus serveur.</span><span class="sxs-lookup"><span data-stu-id="4f009-114">When the elevated COM client calls [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) using the legacy application's CLSID, the client's elevated state will flow to the server process.</span></span>

<span data-ttu-id="4f009-115">Toutes les fonctionnalités COM ne sont pas compatibles avec l’élévation.</span><span class="sxs-lookup"><span data-stu-id="4f009-115">Not all COM functionality is compatible with elevation.</span></span> <span data-ttu-id="4f009-116">Les fonctionnalités qui ne fonctionnent pas incluent :</span><span class="sxs-lookup"><span data-stu-id="4f009-116">The functionality that will not work includes:</span></span>

-   <span data-ttu-id="4f009-117">L’élévation ne passe pas d’un client à un serveur COM distant.</span><span class="sxs-lookup"><span data-stu-id="4f009-117">Elevation does not flow from a client to a remote COM server.</span></span> <span data-ttu-id="4f009-118">Si un client Active un serveur COM distant avec le moniker d’élévation, le serveur n’est pas élevé, même s’il prend en charge l’élévation.</span><span class="sxs-lookup"><span data-stu-id="4f009-118">If a client activates a remote COM server with the elevation moniker, the server will not be elevated, even if it supports elevation.</span></span>
-   <span data-ttu-id="4f009-119">Si une classe COM avec élévation de privilèges utilise l’emprunt d’identité pendant un appel COM, elle risque de perdre ses privilèges élevés pendant l’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="4f009-119">If an elevated COM class uses impersonation during a COM call, it might lose its elevated privileges during the impersonation.</span></span>
-   <span data-ttu-id="4f009-120">Si un serveur COM avec élévation de privilèges enregistre une classe dans la table ROT (Running Object Table), la classe ne sera pas disponible pour les clients non élevés.</span><span class="sxs-lookup"><span data-stu-id="4f009-120">If an elevated COM server registers a class in the running object table (ROT), the class will not be available to non-elevated clients.</span></span>
-   <span data-ttu-id="4f009-121">Un processus élevé à l’aide du mécanisme de contrôle de compte d’utilisateur ne charge pas les classes par utilisateur lors des activations COM.</span><span class="sxs-lookup"><span data-stu-id="4f009-121">A process elevated by using the UAC mechanism does not load per-user classes during COM activations.</span></span> <span data-ttu-id="4f009-122">Pour les applications COM, cela signifie que les classes COM de l’application doivent être installées dans la ruche de Registre **HKEY \_ local \_ machine** si l’application doit être utilisée à la fois par des comptes non privilégiés et privilégiés.</span><span class="sxs-lookup"><span data-stu-id="4f009-122">For COM applications, this means that the application's COM classes must be installed in the **HKEY\_LOCAL\_MACHINE** registry hive if the application is to be used both by non-privileged and privileged accounts.</span></span> <span data-ttu-id="4f009-123">Les classes COM de l’application doivent uniquement être installées dans la ruche des **\_ utilisateurs HKEY** si l’application n’est jamais utilisée par des comptes privilégiés.</span><span class="sxs-lookup"><span data-stu-id="4f009-123">The application's COM classes need only be installed in the **HKEY\_USERS** hive if the application is never used by privileged accounts.</span></span>
-   <span data-ttu-id="4f009-124">La fonction glisser-déplacer n’est pas autorisée pour les applications avec élévation de privilèges non élevées.</span><span class="sxs-lookup"><span data-stu-id="4f009-124">Drag and drop is not allowed from non-elevated to elevated applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f009-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f009-125">Requirements</span></span>

<span data-ttu-id="4f009-126">Afin d’utiliser le moniker d’élévation pour activer une classe COM, la classe doit être configurée pour s’exécuter en tant qu’utilisateur de lancement ou en tant qu’identité d’application’Activate As Activator'.</span><span class="sxs-lookup"><span data-stu-id="4f009-126">In order to use the elevation moniker to activate a COM class, the class must be configured to run as the launching user or the 'Activate as Activator' application identity.</span></span> <span data-ttu-id="4f009-127">Si la classe est configurée pour s’exécuter sous n’importe quelle autre identité, l’activation retourne l’erreur la valeur de CO \_ E \_ runas \_ \_ doit \_ être \_ AAA.</span><span class="sxs-lookup"><span data-stu-id="4f009-127">If the class is configured to run under any other identity, the activation returns the error CO\_E\_RUNAS\_VALUE\_MUST\_BE\_AAA.</span></span>

<span data-ttu-id="4f009-128">La classe doit également être annotée avec un nom d’affichage « convivial » compatible avec l’interface utilisateur multilingue (MUI).</span><span class="sxs-lookup"><span data-stu-id="4f009-128">The class must also be annotated with a "friendly" display name that is multilingual user interface (MUI) compatible.</span></span> <span data-ttu-id="4f009-129">Pour cela, vous devez disposer de l’entrée de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="4f009-129">This requires the following registry entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      LocalizedString = displayName
```

<span data-ttu-id="4f009-130">Si cette entrée est manquante, l’activation renvoie le message d’erreur «le \_ \_ DisplayName est manquant \_ .</span><span class="sxs-lookup"><span data-stu-id="4f009-130">If this entry is missing, the activation returns the error CO\_E\_MISSING\_DISPLAYNAME.</span></span> <span data-ttu-id="4f009-131">Si le fichier MUI est manquant, le code d’erreur de la fonction [**RegLoadMUIStringW**](/windows/desktop/api/winreg/nf-winreg-regloadmuistringa) est retourné.</span><span class="sxs-lookup"><span data-stu-id="4f009-131">If the MUI file is missing, the error code from the [**RegLoadMUIStringW**](/windows/desktop/api/winreg/nf-winreg-regloadmuistringa) function is returned.</span></span>

<span data-ttu-id="4f009-132">Si vous le souhaitez, pour spécifier une icône d’application à afficher par l’interface utilisateur du contrôle de compte d’utilisateur, ajoutez la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="4f009-132">Optionally, to specify an application icon to be displayed by the UAC user interface, add the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         IconReference = applicationIcon
```

<span data-ttu-id="4f009-133">**IconReference** utilise le même format que **LocalizedString**:</span><span class="sxs-lookup"><span data-stu-id="4f009-133">**IconReference** uses the same format as **LocalizedString**:</span></span>

<span data-ttu-id="4f009-134">@*pathtobinary*,*-resourcenumber*</span><span class="sxs-lookup"><span data-stu-id="4f009-134">@*pathtobinary*,*-resourcenumber*</span></span>

<span data-ttu-id="4f009-135">En outre, le composant COM doit être signé pour que l’icône s’affiche.</span><span class="sxs-lookup"><span data-stu-id="4f009-135">In addition, the COM component must be signed for the icon to be displayed.</span></span>

<span data-ttu-id="4f009-136">La classe COM doit également être annotée comme étant compatible LUA.</span><span class="sxs-lookup"><span data-stu-id="4f009-136">The COM class must also be annotated as LUA-Enabled.</span></span> <span data-ttu-id="4f009-137">Pour cela, vous devez disposer de l’entrée de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="4f009-137">This requires the following registry entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         Enabled = 1
```

<span data-ttu-id="4f009-138">Si cette entrée est manquante, l’activation retourne l’erreur CO \_ E \_ Elévation \_ désactivée.</span><span class="sxs-lookup"><span data-stu-id="4f009-138">If this entry is missing, then the activation returns the error CO\_E\_ELEVATION\_DISABLED.</span></span>

<span data-ttu-id="4f009-139">Notez que ces entrées doivent exister dans la \_ ruche HKEY local \_ machine, et non dans la \_ ruche HKEY Current \_ User ou HKEY \_ users.</span><span class="sxs-lookup"><span data-stu-id="4f009-139">Note that these entries must exist in the HKEY\_LOCAL\_MACHINE hive, not the HKEY\_CURRENT\_USER or HKEY\_USERS hive.</span></span> <span data-ttu-id="4f009-140">Cela empêche les utilisateurs d’élever les classes COM qu’ils n’ont pas également les privilèges nécessaires pour s’inscrire.</span><span class="sxs-lookup"><span data-stu-id="4f009-140">This prevents users from elevating COM classes that they did not also have the privileges to register.</span></span>

## <a name="the-elevation-moniker-and-the-elevation-ui"></a><span data-ttu-id="4f009-141">Moniker de l’élévation et interface utilisateur d’élévation</span><span class="sxs-lookup"><span data-stu-id="4f009-141">The Elevation Moniker and the Elevation UI</span></span>

<span data-ttu-id="4f009-142">Si le client est déjà élevé, l’utilisation du moniker d’élévation n’entraîne pas l’affichage de l’interface utilisateur d’élévation.</span><span class="sxs-lookup"><span data-stu-id="4f009-142">If the client is already elevated, using the elevation moniker will not cause the Elevation UI to display.</span></span>

## <a name="how-to-use-the-elevation-moniker"></a><span data-ttu-id="4f009-143">Comment utiliser le moniker d’élévation</span><span class="sxs-lookup"><span data-stu-id="4f009-143">How to Use the Elevation Moniker</span></span>

<span data-ttu-id="4f009-144">Le moniker d’élévation est un moniker COM standard, similaire aux monikers de session, de partition ou de file d’attente.</span><span class="sxs-lookup"><span data-stu-id="4f009-144">The elevation moniker is a standard COM moniker, similar to the session, partition, or queue monikers.</span></span> <span data-ttu-id="4f009-145">Il dirige une demande d’activation vers un serveur spécifié avec le niveau d’élévation spécifié.</span><span class="sxs-lookup"><span data-stu-id="4f009-145">It directs an activation request to a specified server with the specified elevation level.</span></span> <span data-ttu-id="4f009-146">Le CLSID à activer apparaît dans la chaîne de moniker.</span><span class="sxs-lookup"><span data-stu-id="4f009-146">The CLSID to be activated appears in the moniker string.</span></span>

<span data-ttu-id="4f009-147">Le moniker d’élévation prend en charge les jetons de niveau d’exécution suivants :</span><span class="sxs-lookup"><span data-stu-id="4f009-147">The elevation moniker supports the following Run level tokens:</span></span>

1.  <span data-ttu-id="4f009-148">Administrateur</span><span class="sxs-lookup"><span data-stu-id="4f009-148">Administrator</span></span>
2.  <span data-ttu-id="4f009-149">Le plus élevé</span><span class="sxs-lookup"><span data-stu-id="4f009-149">Highest</span></span>

<span data-ttu-id="4f009-150">La syntaxe est la suivante :</span><span class="sxs-lookup"><span data-stu-id="4f009-150">The syntax for this is as follows:</span></span>

``` syntax
Elevation:Administrator!new:{guid}
Elevation:Highest!new:{guid}
```

<span data-ttu-id="4f009-151">La syntaxe précédente utilise le moniker « New » pour retourner une instance de la classe COM spécifiée par *GUID*.</span><span class="sxs-lookup"><span data-stu-id="4f009-151">The preceding syntax uses the "new" moniker to return an instance of the COM class specified by *guid*.</span></span> <span data-ttu-id="4f009-152">Notez que le moniker « New » utilise en interne l’interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) pour obtenir un objet de classe, puis appelle [**IClassFactory :: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) sur ce dernier.</span><span class="sxs-lookup"><span data-stu-id="4f009-152">Note that the "new" moniker internally uses the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface to obtain a class object and then calls [**IClassFactory::CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) on it.</span></span>

<span data-ttu-id="4f009-153">Le moniker de l’élévation peut également être utilisé pour obtenir un objet de classe, qui implémente [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span><span class="sxs-lookup"><span data-stu-id="4f009-153">The elevation moniker can also be used to get a class object, which implements [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="4f009-154">L’appelant appelle ensuite [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) pour recevoir une instance d’objet.</span><span class="sxs-lookup"><span data-stu-id="4f009-154">The caller then calls [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) to get an object instance.</span></span> <span data-ttu-id="4f009-155">La syntaxe est la suivante :</span><span class="sxs-lookup"><span data-stu-id="4f009-155">The syntax for this is as follows:</span></span>

``` syntax
Elevation:Administrator!clsid:{guid}
```

## <a name="sample-code"></a><span data-ttu-id="4f009-156">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="4f009-156">Sample code</span></span>

<span data-ttu-id="4f009-157">L’exemple de code suivant montre comment utiliser le moniker d’élévation.</span><span class="sxs-lookup"><span data-stu-id="4f009-157">The following code example shows how to use the elevation moniker.</span></span> <span data-ttu-id="4f009-158">Il part du principe que vous avez déjà initialisé COM sur le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="4f009-158">It assumes that you have already initialized COM on the current thread.</span></span>


```C++
HRESULT CoCreateInstanceAsAdmin(HWND hwnd, REFCLSID rclsid, REFIID riid, __out void ** ppv)
{
    BIND_OPTS3 bo;
    WCHAR  wszCLSID[50];
    WCHAR  wszMonikerName[300];

    StringFromGUID2(rclsid, wszCLSID, sizeof(wszCLSID)/sizeof(wszCLSID[0])); 
    HRESULT hr = StringCchPrintf(wszMonikerName, sizeof(wszMonikerName)/sizeof(wszMonikerName[0]), L"Elevation:Administrator!new:%s", wszCLSID);
    if (FAILED(hr))
        return hr;
    memset(&bo, 0, sizeof(bo));
    bo.cbStruct = sizeof(bo);
    bo.hwnd = hwnd;
    bo.dwClassContext  = CLSCTX_LOCAL_SERVER;
    return CoGetObject(wszMonikerName, &bo, riid, ppv);
}
```



<span data-ttu-id="4f009-159">[**Liaison \_ OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) est une nouveauté de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4f009-159">[**BIND\_OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) is new in Windows Vista.</span></span> <span data-ttu-id="4f009-160">Elle est dérivée de [**Bind \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1).</span><span class="sxs-lookup"><span data-stu-id="4f009-160">It is derived from [**BIND\_OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1).</span></span>

<span data-ttu-id="4f009-161">Le seul ajout est un champ **HWND** , **HWND**.</span><span class="sxs-lookup"><span data-stu-id="4f009-161">The only addition is an **HWND** field, **hwnd**.</span></span> <span data-ttu-id="4f009-162">Ce handle représente une fenêtre qui devient le propriétaire de l’interface utilisateur d’élévation, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="4f009-162">This handle represents a window that becomes the owner of the Elevation UI, if applicable.</span></span>

<span data-ttu-id="4f009-163">Si **HWND** a la **valeur null**, com appellera [GetActiveWindow](/windows/win32/api/winuser/nf-winuser-getactivewindow) pour trouver un handle de fenêtre associé au thread actuel.</span><span class="sxs-lookup"><span data-stu-id="4f009-163">If **hwnd** is **NULL**, COM will call [GetActiveWindow](/windows/win32/api/winuser/nf-winuser-getactivewindow) to find a window handle associated with the current thread.</span></span> <span data-ttu-id="4f009-164">Ce cas peut se produire si le client est un script, qui ne peut pas remplir une structure [**\_ OPTS3 de liaison**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) .</span><span class="sxs-lookup"><span data-stu-id="4f009-164">This case might occur if the client is a script, which cannot fill in a [**BIND\_OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) structure.</span></span> <span data-ttu-id="4f009-165">Dans ce cas, COM essaiera d’utiliser la fenêtre associée au thread de script.</span><span class="sxs-lookup"><span data-stu-id="4f009-165">In this case, COM will try to use the window associated with the script thread.</span></span>

## <a name="over-the-shoulder-ots-elevation"></a><span data-ttu-id="4f009-166">Élévation à l’épaule (OTS)</span><span class="sxs-lookup"><span data-stu-id="4f009-166">Over-The-Shoulder (OTS) Elevation</span></span>

<span data-ttu-id="4f009-167">L’élévation de la valeur par rapport à l’épaule (OTS) fait référence au scénario dans lequel un client exécute un serveur COM avec les informations d’identification d’un administrateur plutôt que son propre.</span><span class="sxs-lookup"><span data-stu-id="4f009-167">Over-the-shoulder (OTS) elevation refers to the scenario in which a client runs a COM server with an administrator's credentials rather than his or her own.</span></span> <span data-ttu-id="4f009-168">(Le terme « à l’épaule » signifie que l’administrateur regarde l’épaule du client au fur et à mesure que le client exécute le serveur.)</span><span class="sxs-lookup"><span data-stu-id="4f009-168">(The term "over the shoulder" means that the administrator is watching over the client's shoulder as the client runs the server.)</span></span>

<span data-ttu-id="4f009-169">Ce scénario peut provoquer un problème pour les appels COM dans le serveur, car le serveur peut ne pas appeler [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) de manière explicite (autrement dit, par programmation) ou implicitement (c’est-à-dire, de manière déclarative, à l’aide du registre).</span><span class="sxs-lookup"><span data-stu-id="4f009-169">This scenario might cause a problem for COM calls into the server, because the server might not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) either explicitly (that is, programmatically) or implicitly (that is, declaratively, using the registry).</span></span> <span data-ttu-id="4f009-170">Pour ces serveurs, COM calcule un descripteur de sécurité qui autorise uniquement les administrateurs SELF, SYSTEM et builtin \\ à effectuer des appels com sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="4f009-170">For such servers, COM computes a security descriptor that allows only SELF, SYSTEM, and Builtin\\Administrators to makes COM calls into the server.</span></span> <span data-ttu-id="4f009-171">Cette configuration ne fonctionne pas dans les scénarios OTS.</span><span class="sxs-lookup"><span data-stu-id="4f009-171">This arrangement will not work in OTS scenarios.</span></span> <span data-ttu-id="4f009-172">Au lieu de cela, le serveur doit appeler **CoInitializeSecurity**, de manière explicite ou implicite, et spécifier une liste de contrôle d’accès qui comprend le SID et le système du groupe interactif.</span><span class="sxs-lookup"><span data-stu-id="4f009-172">Instead, the server must call **CoInitializeSecurity**, either explicitly or implicitly, and specify an ACL that includes the INTERACTIVE group SID and SYSTEM.</span></span>

<span data-ttu-id="4f009-173">L’exemple de code suivant montre comment créer un descripteur de sécurité (SD) avec le SID de groupe interactif.</span><span class="sxs-lookup"><span data-stu-id="4f009-173">The following code example shows how to create a security descriptor (SD) with the INTERACTIVE group SID.</span></span>

``` syntax
BOOL GetAccessPermissionsForLUAServer(SECURITY_DESCRIPTOR **ppSD)
{
// Local call permissions to IU, SY
    LPWSTR lpszSDDL = L"O:BAG:BAD:(A;;0x3;;;IU)(A;;0x3;;;SY)";
    SECURITY_DESCRIPTOR *pSD;
    *ppSD = NULL;

    if (ConvertStringSecurityDescriptorToSecurityDescriptorW(lpszSDDL, SDDL_REVISION_1, (PSECURITY_DESCRIPTOR *)&pSD, NULL))
    {
        *ppSD = pSD;
        return TRUE;
    }

    return FALSE;
}
```

<span data-ttu-id="4f009-174">L’exemple de code suivant montre comment appeler [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) implicitement avec le SD à partir de l’exemple de code précédent :</span><span class="sxs-lookup"><span data-stu-id="4f009-174">The following code example shows how to call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) implicitly with the SD from the previous code example:</span></span>


```C++
// hKey is the HKCR\AppID\{GUID} key
BOOL SetAccessPermissions(HKEY hkey, PSECURITY_DESCRIPTOR pSD)
{
    BOOL bResult = FALSE;
    DWORD dwLen = GetSecurityDescriptorLength(pSD);
    LONG lResult;
    lResult = RegSetValueExA(hkey, 
        "AccessPermission",
        0,
        REG_BINARY,
        (BYTE*)pSD,
        dwLen);
    if (lResult != ERROR_SUCCESS) goto done;
    bResult = TRUE;
done:
    return bResult;
}
```



<span data-ttu-id="4f009-175">L’exemple de code suivant montre comment appeler [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) explicitement avec le SD ci-dessus :</span><span class="sxs-lookup"><span data-stu-id="4f009-175">The following code example shows how to call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) explicitly with the above SD:</span></span>


```C++
// Absolute SD values
PSECURITY_DESCRIPTOR pAbsSD = NULL;
DWORD AbsSdSize = 0;
PACL  pAbsAcl = NULL;
DWORD AbsAclSize = 0;
PACL  pAbsSacl = NULL;
DWORD AbsSaclSize = 0;
PSID  pAbsOwner = NULL;
DWORD AbsOwnerSize = 0;
PSID  pAbsGroup = NULL;
DWORD AbsGroupSize = 0;

MakeAbsoluteSD (
    pSD,
    pAbsSD,
    &AbsSdSize,
    pAbsAcl,
    &AbsAclSize,
    pAbsSacl,
    &AbsSaclSize,
    pAbsOwner,
    &AbsOwnerSize,
    pAbsGroup,
    &AbsGroupSize
);

if (ERROR_INSUFFICIENT_BUFFER == GetLastError())
{
    pAbsSD = (PSECURITY_DESCRIPTOR)LocalAlloc(LMEM_FIXED, AbsSdSize);
    pAbsAcl = (PACL)LocalAlloc(LMEM_FIXED, AbsAclSize);
    pAbsSacl = (PACL)LocalAlloc(LMEM_FIXED, AbsSaclSize);
    pAbsOwner = (PSID)LocalAlloc(LMEM_FIXED, AbsOwnerSize);
    pAbsGroup = (PSID)LocalAlloc(LMEM_FIXED, AbsGroupSize);

    if ( ! (pAbsSD && pAbsAcl && pAbsSacl && pAbsOwner && pAbsGroup))
    {
        hr = E_OUTOFMEMORY;
        goto Cleanup;
    }
    if ( ! MakeAbsoluteSD(
        pSD,
        pAbsSD,
        &AbsSdSize,
        pAbsAcl,
        &AbsAclSize,
        pAbsSacl,
        &AbsSaclSize,
        pAbsOwner,
        &AbsOwnerSize,
        pAbsGroup,
        &AbsGroupSize
        ))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        goto Cleanup;
    }
}
else
{
    hr = HRESULT_FROM_WIN32(GetLastError());
    goto Cleanup;
}

// Call CoinitilizeSecurity.
```



## <a name="com-permissions-and-mandatory-access-labels"></a><span data-ttu-id="4f009-176">Autorisations COM et étiquettes d’accès obligatoires</span><span class="sxs-lookup"><span data-stu-id="4f009-176">COM Permissions and Mandatory Access Labels</span></span>

<span data-ttu-id="4f009-177">Windows Vista introduit la notion d' *étiquettes d’accès obligatoires* dans les descripteurs de sécurité.</span><span class="sxs-lookup"><span data-stu-id="4f009-177">Windows Vista introduces the notion of *mandatory access labels* in security descriptors.</span></span> <span data-ttu-id="4f009-178">L’étiquette détermine si les clients peuvent obtenir un accès en exécution à un objet COM.</span><span class="sxs-lookup"><span data-stu-id="4f009-178">The label dictates whether clients can get execute access to a COM object.</span></span> <span data-ttu-id="4f009-179">L’étiquette est spécifiée dans la partie liste de contrôle d’accès système (SACL) du descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="4f009-179">The label is specified in the system access control list (SACL) portion of the security descriptor.</span></span> <span data-ttu-id="4f009-180">Dans Windows Vista, COM prend en charge l’étiquette obligatoire nom du système non en cours d' \_ \_ \_ \_ exécution \_ .</span><span class="sxs-lookup"><span data-stu-id="4f009-180">In Windows Vista, COM supports the SYSTEM\_MANDATORY\_LABEL\_NO\_EXECUTE\_UP label.</span></span> <span data-ttu-id="4f009-181">Les listes SACL dans les autorisations COM sont ignorées sur les systèmes d’exploitation antérieurs à Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4f009-181">SACLs in the COM permissions are ignored on operating systems prior to Windows Vista.</span></span>

<span data-ttu-id="4f009-182">À compter de Windows Vista, dcomcnfg.exe ne prend pas en charge la modification du niveau d’intégrité (IL) dans les autorisations COM.</span><span class="sxs-lookup"><span data-stu-id="4f009-182">As of Windows Vista, dcomcnfg.exe does not support changing the integrity level (IL) in COM permissions.</span></span> <span data-ttu-id="4f009-183">Elle doit être définie par programmation.</span><span class="sxs-lookup"><span data-stu-id="4f009-183">It must be set programmatically.</span></span>

<span data-ttu-id="4f009-184">L’exemple de code suivant montre comment créer un descripteur de sécurité COM avec une étiquette qui autorise les demandes de lancement/activation à partir de tous les clients IL bas.</span><span class="sxs-lookup"><span data-stu-id="4f009-184">The following code example shows how to create a COM security descriptor with a label that allows launch/activation requests from all LOW IL clients.</span></span> <span data-ttu-id="4f009-185">Notez que les étiquettes sont valides pour les autorisations de lancement/activation et d’appel.</span><span class="sxs-lookup"><span data-stu-id="4f009-185">Note that the labels are valid for Launch/Activation and Call permissions.</span></span> <span data-ttu-id="4f009-186">Par conséquent, il est possible d’écrire un serveur COM qui interdit le lancement, l’activation ou les appels des clients avec un langage intermédiaire donné.</span><span class="sxs-lookup"><span data-stu-id="4f009-186">Thus, it is possible to write a COM server that disallows launch, activation or calls from clients with a certain IL.</span></span> <span data-ttu-id="4f009-187">Pour plus d’informations sur les niveaux d’intégrité, consultez la section « fonctionnement du mécanisme d’intégrité de Windows Vista » dans [présentation et utilisation du mode protégé d’Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4f009-187">For more information about integrity levels, see the section "Understanding Windows Vista's Integrity Mechanism" in [Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/).</span></span>


```C++
BOOL GetLaunchActPermissionsWithIL (SECURITY_DESCRIPTOR **ppSD)
{
// Allow World Local Launch/Activation permissions. Label the SD for LOW IL Execute UP
    LPWSTR lpszSDDL = L"O:BAG:BAD:(A;;0xb;;;WD)S:(ML;;NX;;;LW)";
    if (ConvertStringSecurityDescriptorToSecurityDescriptorW(lpszSDDL, SDDL_REVISION_1, (PSECURITY_DESCRIPTOR *)&pSD, NULL))
    {
        *ppSD = pSD;
        return TRUE;
    }
}

BOOL SetLaunchActPermissions(HKEY hkey, PSECURITY_DESCRIPTOR pSD)
{
    
    BOOL bResult = FALSE;
    DWORD dwLen = GetSecurityDescriptorLength(pSD);
    LONG lResult;
    lResult = RegSetValueExA(hkey, 
        "LaunchPermission",
        0,
        REG_BINARY,
        (BYTE*)pSD,
        dwLen);
    if (lResult != ERROR_SUCCESS) goto done;
    bResult = TRUE;
done:
    return bResult;
};
```



## <a name="cocreateinstance-and-integrity-levels"></a><span data-ttu-id="4f009-188">CoCreateInstance et niveaux d’intégrité</span><span class="sxs-lookup"><span data-stu-id="4f009-188">CoCreateInstance and Integrity Levels</span></span>

<span data-ttu-id="4f009-189">Le comportement de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) a été modifié dans Windows Vista pour empêcher les clients il de se lier aux serveurs COM par défaut.</span><span class="sxs-lookup"><span data-stu-id="4f009-189">The behavior of [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) has changed in Windows Vista, to prevent Low IL clients from binding to COM servers by default.</span></span> <span data-ttu-id="4f009-190">Le serveur doit autoriser explicitement ces liaisons en spécifiant la liste SACL.</span><span class="sxs-lookup"><span data-stu-id="4f009-190">The server must explicitly allow such bindings by specifying the SACL.</span></span> <span data-ttu-id="4f009-191">Les modifications apportées à **CoCreateInstance** sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="4f009-191">The changes to **CoCreateInstance** are as follows:</span></span>

1.  <span data-ttu-id="4f009-192">Lors du lancement d’un processus serveur COM, le langage intermédiaire du jeton de processus serveur est défini sur le langage intermédiaire du client ou du serveur, selon la valeur la plus basse.</span><span class="sxs-lookup"><span data-stu-id="4f009-192">When launching a COM server process, the IL in the server process token is set to the client or server token IL, whichever is lower.</span></span>
2.  <span data-ttu-id="4f009-193">Par défaut, COM empêche les clients IL bas de se lier aux instances en cours d’exécution de tous les serveurs COM.</span><span class="sxs-lookup"><span data-stu-id="4f009-193">By default, COM will prevent Low IL clients from binding to running instances of any COM servers.</span></span> <span data-ttu-id="4f009-194">Pour autoriser la liaison, le descripteur de sécurité de lancement/activation d’un serveur COM doit contenir une liste SACL qui spécifie l’étiquette IL faible (consultez la section précédente pour l’exemple de code pour créer un tel descripteur de sécurité).</span><span class="sxs-lookup"><span data-stu-id="4f009-194">To allow the bind, a COM server's Launch/Activation security descriptor must contain a SACL that specifies the Low IL label (see the previous section for the sample code to create such a security descriptor).</span></span>

## <a name="elevated-servers-and-rot-registrations"></a><span data-ttu-id="4f009-195">Serveurs élevés et inscriptions ROT</span><span class="sxs-lookup"><span data-stu-id="4f009-195">Elevated Servers and ROT Registrations</span></span>

<span data-ttu-id="4f009-196">Si un serveur COM souhaite s’inscrire dans la table ROT (Running Object Table) et autoriser n’importe quel client à accéder à l’inscription, il doit utiliser l' \_ indicateur ROTFLAGS ALLOWANYCLIENT.</span><span class="sxs-lookup"><span data-stu-id="4f009-196">If a COM server wishes to register in the running object table (ROT) and allow any client to access the registration, it must use the ROTFLAGS\_ALLOWANYCLIENT flag.</span></span> <span data-ttu-id="4f009-197">Un serveur COM « Activate As Activator » ne peut pas spécifier ROTFLAGS \_ ALLOWANYCLIENT, car le gestionnaire de contrôle des services DCOM (DCOMSCM) applique un contrôle d’usurpation d’identité à cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="4f009-197">An "Activate As Activator" COM server cannot specify ROTFLAGS\_ALLOWANYCLIENT because the DCOM service control manager (DCOMSCM) enforces a spoof check against this flag.</span></span> <span data-ttu-id="4f009-198">Par conséquent, dans Windows Vista, COM ajoute la prise en charge d’une nouvelle entrée de Registre qui permet au serveur de stipuler que ses inscriptions ROT sont mises à la disposition de n’importe quel client :</span><span class="sxs-lookup"><span data-stu-id="4f009-198">Therefore, in Windows Vista, COM adds support for a new registry entry that allows the server to stipulate that its ROT registrations be made available to any client:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\AppID
   {APPID}
      ROTFlags
```

<span data-ttu-id="4f009-199">La seule valeur valide pour cette entrée de Registre \_ DWORD est :</span><span class="sxs-lookup"><span data-stu-id="4f009-199">The only valid value for this REG\_DWORD entry is:</span></span>

``` syntax
ROTREGFLAGS_ALLOWANYCLIENT 0x1
```

<span data-ttu-id="4f009-200">L’entrée doit exister dans la ruche **HKEY \_ local \_ machine** .</span><span class="sxs-lookup"><span data-stu-id="4f009-200">The entry must exist in the **HKEY\_LOCAL\_MACHINE** hive.</span></span>

<span data-ttu-id="4f009-201">Cette entrée fournit un serveur « Activate As Activator » avec les mêmes fonctionnalités que celles fournies par ROTFLAGS \_ ALLOWANYCLIENT pour un serveur runas.</span><span class="sxs-lookup"><span data-stu-id="4f009-201">This entry provides an "Activate As Activator" server with the same functionality that ROTFLAGS\_ALLOWANYCLIENT provides for a RunAs server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f009-202">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4f009-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f009-203">Sécurité dans COM</span><span class="sxs-lookup"><span data-stu-id="4f009-203">Security in COM</span></span>](security-in-com.md)
</dt> <dt>

[<span data-ttu-id="4f009-204">Présentation et utilisation d’Internet Explorer en mode protégé</span><span class="sxs-lookup"><span data-stu-id="4f009-204">Understanding and Working in Protected Mode Internet Explorer</span></span>](/previous-versions/windows/internet-explorer/ie-developer/)
</dt> </dl>

 

 