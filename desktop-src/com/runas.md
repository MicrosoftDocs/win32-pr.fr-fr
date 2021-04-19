---
title: RunAs
description: Configure une classe pour qu’elle s’exécute sous un compte d’utilisateur spécifique lorsqu’elle est activée par un client distant sans être écrite comme une application de service.
ms.assetid: 2325a7da-8acd-41f4-a658-36a02532505a
keywords:
- Valeur de Registre RunAs COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3139d12864eb92cc153b919dc4b9b9a4059379d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106509682"
---
# <a name="runas"></a><span data-ttu-id="6ca3f-104">RunAs</span><span class="sxs-lookup"><span data-stu-id="6ca3f-104">RunAs</span></span>

<span data-ttu-id="6ca3f-105">Configure une classe pour qu’elle s’exécute sous un compte d’utilisateur spécifique lorsqu’elle est activée par un client distant sans être écrite comme une application de service.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-105">Configures a class to run under a specific user account when activated by a remote client without being written as a service application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="6ca3f-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="6ca3f-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RunAs = value
```

## <a name="remarks"></a><span data-ttu-id="6ca3f-107">Notes</span><span class="sxs-lookup"><span data-stu-id="6ca3f-107">Remarks</span></span>

<span data-ttu-id="6ca3f-108">La valeur spécifie le nom d’utilisateur et doit être au format *nom d'* utilisateur, *domaine ***\\*** nom* d’utilisateur ou de la chaîne « utilisateur interactif ».</span><span class="sxs-lookup"><span data-stu-id="6ca3f-108">The value specifies the user name and must be either of the form *UserName*, *Domain ***\\*** UserName* or of the string "Interactive User".</span></span> <span data-ttu-id="6ca3f-109">Vous pouvez également spécifier les chaînes « NT Authority \\ LocalService » (pour le service local) et « NT Authority \\ NetworkService » (pour service réseau).</span><span class="sxs-lookup"><span data-stu-id="6ca3f-109">You can also specify the strings "nt authority\\localservice" (for Local Service) and "nt authority\\networkservice" (for Network Service).</span></span> <span data-ttu-id="6ca3f-110">Vous pouvez également spécifier la chaîne « NT Authority \\ System » lorsque {*AppID \_ GUID*} fait référence à un serveur com déjà démarré ou à une entrée dans la table de classe.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-110">You can also specify the string "nt authority\\system" when {*AppID\_GUID*} refers to a COM server that is already started or that has an entry in the class table.</span></span> <span data-ttu-id="6ca3f-111">Toutefois, vous ne pouvez pas utiliser « NT Authority \\ System » avec un serveur com qui n’est pas déjà démarré.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-111">However, you cannot use "nt authority\\system" with a COM server that is not already started.</span></span> <span data-ttu-id="6ca3f-112">Le mot de passe par défaut pour « NT Authority \\ LocalService », « NT Authority \\ NetworkService » et « NT Authority \\ System » est «» (chaîne vide).</span><span class="sxs-lookup"><span data-stu-id="6ca3f-112">The default password for "nt authority\\localservice", "nt authority\\networkservice", and "nt authority\\system" is "" (empty string).</span></span>

> [!Note]  
> <span data-ttu-id="6ca3f-113">À compter de Windows Vista, un mot de passe vide n’est plus requis pour configurer les paramètres « autorité NT \\ LocalService », « autorité NT \\ NetworkService » et « système d’autorité NT \\ ». </span><span class="sxs-lookup"><span data-stu-id="6ca3f-113">As of Windows Vista, an empty password is no longer required to configure the "nt authority\\localservice", "nt authority\\networkservice" and "nt authority\\system" **RunAs** settings.</span></span>

 

<span data-ttu-id="6ca3f-114">Les classes configurées pour s’exécuter en tant qu’utilisateur particulier ne peuvent pas être inscrites sous une autre identité, donc les appels à [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) avec ce CLSID échouent, sauf si le processus a été lancé par com pour le compte d’une demande d’activation réelle.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-114">Classes configured to run as a particular user may not be registered under any other identity, so calls to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) with this CLSID fail unless the process was launched by COM on behalf of an actual activation request.</span></span>

<span data-ttu-id="6ca3f-115">Le nom d’utilisateur est extrait de la valeur **runas** sous la clé **AppID** de la classe.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-115">The user-name is taken from the **RunAs** value under the class's **AppID** key.</span></span> <span data-ttu-id="6ca3f-116">Si le nom d’utilisateur est « utilisateur interactif », le serveur est exécuté dans l’identité de l’utilisateur actuellement connecté et est connecté au bureau interactif.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-116">If the user name is "Interactive User", the server is run in the identity of the user currently logged on and is connected to the interactive desktop.</span></span>

<span data-ttu-id="6ca3f-117">Dans le cas contraire, le mot de passe est récupéré à partir d’une partie du Registre qui est disponible uniquement pour les administrateurs de l’ordinateur et sur le système.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-117">Otherwise, the password is retrieved from a portion of the registry that is available only to administrators of the computer and to the system.</span></span> <span data-ttu-id="6ca3f-118">Le nom d’utilisateur et le mot de passe sont ensuite utilisés pour créer une session de connexion dans laquelle le serveur est exécuté.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-118">The user-name and password are then used to create a logon session in which the server is run.</span></span> <span data-ttu-id="6ca3f-119">Lorsqu’il est lancé de cette manière, l’utilisateur s’exécute avec sa propre station de travail et sa propre station Windows et ne partage pas les handles de fenêtre, le presse-papiers ou d’autres éléments de l’interface utilisateur avec l’utilisateur interactif ou un autre utilisateur s’exécutant dans d’autres comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-119">When launched in this way, the user runs with its own desktop and window station and does not share window-handles, the clipboard, or other UI elements with the interactive user or other user running in other user accounts.</span></span>

<span data-ttu-id="6ca3f-120">Pour établir un mot de passe pour une classe **runas** , vous devez utiliser l’outil d’administration DCOMCNFG installé dans le répertoire système.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-120">To establish a password for a **RunAs** class, you must use the DCOMCNFG administrative tool installed in the system directory.</span></span>

<span data-ttu-id="6ca3f-121">Pour les identités **runas** utilisées par les serveurs DCOM, le compte d’utilisateur spécifié dans la valeur doit disposer des droits pour ouvrir une session en tant que tâche.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-121">For **RunAs** identities used by DCOM servers, the user account specified in the value must have the rights to log on as a batch job.</span></span> <span data-ttu-id="6ca3f-122">Ce droit peut être ajouté à l’aide de l’outil d’administration stratégie de sécurité locale.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-122">This right can be added using Local Security Policy administrative tool.</span></span> <span data-ttu-id="6ca3f-123">Accédez à **stratégies locales** et ouvrez **attribution des droits utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-123">Go to **Local Policies** and open **User Rights Assignment**.</span></span> <span data-ttu-id="6ca3f-124">Sélectionnez **ouvrir une session en tant que tâche**, puis ajoutez le compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-124">Select **Log on as a batch job**, and add the user account.</span></span>

<span data-ttu-id="6ca3f-125">La valeur **runas** n’est pas utilisée pour les serveurs configurés pour être exécutés en tant que services.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-125">The **RunAs** value is not used for servers configured to be run as services.</span></span> <span data-ttu-id="6ca3f-126">Les services COM qui doivent s’exécuter sous une identité autre que LocalSystem doivent définir le nom d’utilisateur et le mot de passe appropriés à l’aide de l’applet du panneau de configuration des services ou des fonctions du contrôleur de service.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-126">COM services that need to run under an identity other than LocalSystem should set the appropriate user name and password using the services control panel applet or the service controller functions.</span></span> <span data-ttu-id="6ca3f-127">(Pour plus d’informations sur ces fonctions, consultez [services](/windows/desktop/Services/services).)</span><span class="sxs-lookup"><span data-stu-id="6ca3f-127">(For more information about these functions, see [Services](/windows/desktop/Services/services).)</span></span>

> [!Note]  
> <span data-ttu-id="6ca3f-128">À compter de Microsoft Windows Server 2003, la classe AppID est lue explicitement à partir de **HKEY \_ local \_ machine \\ Software \\ classes \\ AppID**, qui, contrairement à la plupart des clés de Registre, n’est pas interchangeable avec l' **\_ \_ \\ AppID racine des classes HKEY**.</span><span class="sxs-lookup"><span data-stu-id="6ca3f-128">As of Microsoft Windows Server 2003, the class AppID is explicitly read from **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\AppID**, which, unlike most registry keys, is not interchangeable with **HKEY\_CLASSES\_ROOT\\AppID**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6ca3f-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6ca3f-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ca3f-130">Inscription des serveurs COM</span><span class="sxs-lookup"><span data-stu-id="6ca3f-130">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 