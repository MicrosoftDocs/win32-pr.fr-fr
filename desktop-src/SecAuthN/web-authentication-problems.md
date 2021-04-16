---
description: Cette rubrique décrit des conseils de dépannage pour l’utilisation des API du Service Broker d’authentification Web pour vos pages Web.
ms.assetid: 25A024AA-9A70-40A5-BF5E-452FD148D0D2
title: Problèmes d’authentification web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc4611461effd9cbc5546059e71fc8ca3f1f0be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571117"
---
# <a name="web-authentication-problems"></a><span data-ttu-id="759a5-103">Problèmes d’authentification web</span><span class="sxs-lookup"><span data-stu-id="759a5-103">Web authentication problems</span></span>

<span data-ttu-id="759a5-104">Cette rubrique décrit des conseils de dépannage pour l’utilisation des API du Service Broker d’authentification Web pour vos pages Web.</span><span class="sxs-lookup"><span data-stu-id="759a5-104">This topic describes troubleshooting tips for using the Web Authentication Broker APIs for your web pages.</span></span>

-   [<span data-ttu-id="759a5-105">Journaux des opérations</span><span class="sxs-lookup"><span data-stu-id="759a5-105">Operational logs</span></span>](#operational-logs)
-   [<span data-ttu-id="759a5-106">Utilisation de Fiddler avec le Service Broker d’authentification Web</span><span class="sxs-lookup"><span data-stu-id="759a5-106">Using Fiddler with Web Authentication Broker</span></span>](#using-fiddler-with-web-authentication-broker)
-   [<span data-ttu-id="759a5-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="759a5-107">Related topics</span></span>](#related-topics)

## <a name="operational-logs"></a><span data-ttu-id="759a5-108">Journaux des opérations</span><span class="sxs-lookup"><span data-stu-id="759a5-108">Operational logs</span></span>

<span data-ttu-id="759a5-109">Il est souvent possible de déterminer ce qui ne fonctionne pas à l’aide des journaux des opérations.</span><span class="sxs-lookup"><span data-stu-id="759a5-109">Often you can determine what is not working by using the operational logs.</span></span> <span data-ttu-id="759a5-110">Il existe un canal de journal des événements dédié Microsoft-Windows-webauth \\ opérationnel qui permet aux développeurs de sites Web de comprendre comment leurs pages Web sont traitées par le répartiteur d’authentification Web.</span><span class="sxs-lookup"><span data-stu-id="759a5-110">There is a dedicated event log channel Microsoft-Windows-WebAuth\\Operational that allows website developers to understand how their web pages are being processed by the Web Authentication Broker.</span></span> <span data-ttu-id="759a5-111">Pour l’activer, lancez eventvwr.exe et activez le journal des opérations sous l’application et les services \\ Microsoft \\ Windows \\ webauth.</span><span class="sxs-lookup"><span data-stu-id="759a5-111">To enable it, launch eventvwr.exe and enable Operational log under the Application and Services\\Microsoft\\Windows\\WebAuth.</span></span> <span data-ttu-id="759a5-112">En outre, le répartiteur d’authentification Web ajoute une chaîne unique à la chaîne de l’agent utilisateur pour s’identifier sur le serveur Web.</span><span class="sxs-lookup"><span data-stu-id="759a5-112">Also, the Web Authentication Broker appends a unique string to the user agent string to identify itself on the web server.</span></span> <span data-ttu-id="759a5-113">Cette chaîne est « MSAuthHost/1.0 ».</span><span class="sxs-lookup"><span data-stu-id="759a5-113">The string is "MSAuthHost/1.0".</span></span> <span data-ttu-id="759a5-114">Notez que le numéro de version est susceptible de changer dans le futur. Vous ne devez donc pas nécessairement utiliser ce numéro de version dans votre code.</span><span class="sxs-lookup"><span data-stu-id="759a5-114">Note that the version number may change in the future, so you should not to depend on that version number in your code.</span></span> <span data-ttu-id="759a5-115">Voici un exemple de la chaîne complète de l’agent utilisateur :</span><span class="sxs-lookup"><span data-stu-id="759a5-115">An example of the full user agent string is as follows:</span></span>

`User-Agent: Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.2; Win64; x64; Trident/6.0; MSAuthHost/1.0)`

<span data-ttu-id="759a5-116">Exemple d’utilisation des journaux des opérations</span><span class="sxs-lookup"><span data-stu-id="759a5-116">Example of using operational logs</span></span>

1.  <span data-ttu-id="759a5-117">Activer les journaux des opérations</span><span class="sxs-lookup"><span data-stu-id="759a5-117">Enable operational logs</span></span>
2.  <span data-ttu-id="759a5-118">Exécuter une application sociale contoso</span><span class="sxs-lookup"><span data-stu-id="759a5-118">Run Contoso social application</span></span>![Observateur d’événements affichant les journaux opérationnels WebAuth](images/wab-figure15.png)
3.  <span data-ttu-id="759a5-120">Les entrées de journaux générées peuvent être utilisées pour comprendre le comportement du Service Broker d’authentification Web plus en détail.</span><span class="sxs-lookup"><span data-stu-id="759a5-120">The generated logs entries can be used to understand the behavior of Web Authentication Broker in greater detail.</span></span> <span data-ttu-id="759a5-121">Dans ce cas, ces entrées peuvent être les suivantes :</span><span class="sxs-lookup"><span data-stu-id="759a5-121">In this case, these can include:</span></span>
    -   <span data-ttu-id="759a5-122">Début de la navigation : consigne le moment où AuthHost démarre, et contient des informations sur les URL de démarrage et de terminaison.</span><span class="sxs-lookup"><span data-stu-id="759a5-122">Navigation Start: Logs when the AuthHost is started and contains information about the start and termination URLs.</span></span>
    -   ![Illustration des détails de la section Début de la navigation](images/wab-figure16.png)
    -   <span data-ttu-id="759a5-124">Achèvement de la navigation : consigne l’achèvement du chargement d’une page web.</span><span class="sxs-lookup"><span data-stu-id="759a5-124">Navigation Complete: Logs the completion of loading a web page.</span></span>
    -   <span data-ttu-id="759a5-125">Balise META : consigne le moment où une balise META est rencontrée, y compris les détails.</span><span class="sxs-lookup"><span data-stu-id="759a5-125">Meta Tag: Logs when a meta-tag is encountered including the details.</span></span>
    -   <span data-ttu-id="759a5-126">Arrêt de la navigation : navigation arrêtée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="759a5-126">Navigation Terminate: Navigation terminated by the user.</span></span>
    -   <span data-ttu-id="759a5-127">Erreur de navigation : AuthHost rencontre une erreur de navigation au niveau d’une URL incluant HttpStatusCode.</span><span class="sxs-lookup"><span data-stu-id="759a5-127">Navigation Error: AuthHost encounters a navigation error at a URL including HttpStatusCode.</span></span>
    -   <span data-ttu-id="759a5-128">Fin de la navigation : une URL de terminaison est rencontrée.</span><span class="sxs-lookup"><span data-stu-id="759a5-128">Navigation End: Terminating URL is encountered.</span></span>

## <a name="using-fiddler-with-web-authentication-broker"></a><span data-ttu-id="759a5-129">Utilisation de Fiddler avec le Service Broker d’authentification Web</span><span class="sxs-lookup"><span data-stu-id="759a5-129">Using Fiddler with Web Authentication Broker</span></span>

<span data-ttu-id="759a5-130">Le débogueur Web Fiddler peut être utilisé avec les applications Windows 8.</span><span class="sxs-lookup"><span data-stu-id="759a5-130">The Fiddler web debugger can be used with Windows 8 apps.</span></span>

1.  <span data-ttu-id="759a5-131">Étant donné qu’AuthHost s’exécute dans son propre conteneur d’application pour lui donner la fonctionnalité réseau privé, vous devez définir une clé de Registre : Windows Registry Editor Version 5.00</span><span class="sxs-lookup"><span data-stu-id="759a5-131">Since the AuthHost runs in its own app container to give it the private network capability, you must set a registry key: Windows Registry Editor Version 5.00</span></span>

    <span data-ttu-id="759a5-132">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Image File Execution Options** \\ **authhost.exe** \\ **EnablePrivateNetwork** = 00000001</span><span class="sxs-lookup"><span data-stu-id="759a5-132">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Image File Execution Options**\\**authhost.exe**\\**EnablePrivateNetwork** = 00000001</span></span><dl> <dt>

                     Data type
</dt> <dd>                     <span data-ttu-id="759a5-133">DWORD</span><span class="sxs-lookup"><span data-stu-id="759a5-133">DWORD</span></span></dd> </dl>

2.  <span data-ttu-id="759a5-134">Ajoutez une règle pour AuthHost, car c’est de là que provient le trafic sortant.</span><span class="sxs-lookup"><span data-stu-id="759a5-134">Add a rule for the AuthHost as this is what is generating the outbound traffic.</span></span>
    ```cmd
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.a.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
    D:\Windows\System32>CheckNetIsolation.exe LoopbackExempt -s
    List Loopback Exempted AppContainers
    [1] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
        SID:  S-1-15-2-1973105767-3975693666-32999980-3747492175-1074076486-3102532000-500629349
    [2] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
        SID:  S-1-15-2-166260-4150837609-3669066492-3071230600-3743290616-3683681078-2492089544
    [3] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.a.p_8wekyb3d8bbwe
        SID:  S-1-15-2-3506084497-1208594716-3384433646-2514033508-1838198150-1980605558-3480344935
    ```

    

3.  <span data-ttu-id="759a5-135">Ajoutez une règle de pare-feu pour le trafic entrant vers Fiddler.</span><span class="sxs-lookup"><span data-stu-id="759a5-135">Add a firewall rule for incoming traffic to Fiddler.</span></span>

<span data-ttu-id="759a5-136">Pour plus d’informations, consultez [le blog sur l’utilisation du débogueur Web Fiddler avec les applications du Windows Store](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications).</span><span class="sxs-lookup"><span data-stu-id="759a5-136">For more information, see [Blog on using Fiddler web debugger with Windows Store apps](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications).</span></span>

## <a name="related-topics"></a><span data-ttu-id="759a5-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="759a5-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="759a5-138">Considérations sur le développement de pages web</span><span class="sxs-lookup"><span data-stu-id="759a5-138">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="759a5-139">Forum aux questions sur le Service Broker d’authentification Web</span><span class="sxs-lookup"><span data-stu-id="759a5-139">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.md)
</dt> <dt>

[<span data-ttu-id="759a5-140">Exemple d’application du SDK du Broker d’authentification Web</span><span class="sxs-lookup"><span data-stu-id="759a5-140">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="759a5-141">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="759a5-141">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041)
</dt> </dl>

 

 
