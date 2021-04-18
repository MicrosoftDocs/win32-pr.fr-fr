---
title: Considérations relatives à la sécurité pour les technologies d’assistance
description: Les technologies d’assistance sont des applications qui s’exécutent sur le bureau Windows et aident les utilisateurs à interagir avec le système d’exploitation et d’autres applications qui s’exécutent sur l’ordinateur, y compris les applications dans la nouvelle interface utilisateur Windows.
ms.assetid: 0c3689e1-2124-4142-b0bd-233e95ee1285
f1_keywords:
- vs.debug.error.launch_elevation_requirements
keywords:
- attribut uiAccess
- UI Automation, attribut uiAccess
- sécurité, attribut uiAccess
- requestedExecutionLevel (balise)
- UI Automation, balise requestedExecutionLevel
- UI Automation, considérations sur la sécurité
- UI Automation, fichiers manifeste
- fichiers manifeste
- contrôle de compte d’utilisateur
- sécurité, contrôle de compte d’utilisateur
- sécurité, fichiers manifeste
- sécurité, balise requestedExecutionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f2f5cf006c0adaf9b170a4ed11abd9afd52012
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2020
ms.locfileid: "106512764"
---
# <a name="security-considerations-for-assistive-technologies"></a><span data-ttu-id="d3f2e-115">Considérations relatives à la sécurité pour les technologies d’assistance</span><span class="sxs-lookup"><span data-stu-id="d3f2e-115">Security Considerations for Assistive Technologies</span></span>

<span data-ttu-id="d3f2e-116">Les technologies d’assistance sont des applications qui s’exécutent sur le bureau Windows et aident les utilisateurs à interagir avec le système d’exploitation et d’autres applications qui s’exécutent sur l’ordinateur, y compris les applications dans la nouvelle interface utilisateur Windows.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-116">Assistive technologies are applications that run on the Windows desktop and help accessibility users interact with the operating system and other applications running on the computer, including applications in the new Windows UI.</span></span> <span data-ttu-id="d3f2e-117">Les applications de technologie d’assistance fonctionnent en récupérant des informations du système d’exploitation et d’autres applications, puis en présentant les informations d’une manière accessible à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-117">Assistive technology applications work by retrieving information from the operating system and other applications, and then presenting the information in a way that is accessible to the user.</span></span> <span data-ttu-id="d3f2e-118">Une application de technologie d’assistance peut également « piloter » par programmation le système d’exploitation et d’autres applications en fonction de l’entrée de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-118">An assistive technology application can also programmatically "drive" the operating system and other applications based on input from the user.</span></span>

<span data-ttu-id="d3f2e-119">La nature des applications de technologie d’assistance exige qu’elles intertraitent les limites et qu’elles aient accès à des processus qui s’exécutent à un niveau d’intégrité plus élevé (IL).</span><span class="sxs-lookup"><span data-stu-id="d3f2e-119">The nature of assistive technology applications requires that they cross process boundaries, and that they have access to processes that run at a higher integrity level (IL) than themselves.</span></span> <span data-ttu-id="d3f2e-120">(Une application de technologie d’assistance s’exécute au moyen du langage intermédiaire.) Par exemple, quand l’utilisateur tente d’effectuer une tâche qui requiert des privilèges d’administrateur, Windows affiche une boîte de dialogue demandant à l’utilisateur de donner son consentement pour continuer.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-120">(An assistive technology application runs at medium IL.) For example, when the user attempts to perform a task that requires administrative privileges, Windows presents a dialog box asking the user for consent to continue.</span></span> <span data-ttu-id="d3f2e-121">Cette boîte de dialogue s’exécute à un IL plus élevé pour le protéger de la communication entre processus, afin que les logiciels malveillants ne puissent pas simuler l’entrée utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-121">This dialog box runs at a higher IL to protect it from cross-process communication, so that malicious software cannot simulate user input.</span></span> <span data-ttu-id="d3f2e-122">De même, l’écran d’ouverture de session de bureau s’exécute à un IL plus élevé pour l’empêcher d’être accessible à d’autres processus.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-122">Similarly, the desktop logon screen runs at a higher IL to prevent it from being accessed by other processes.</span></span>

<span data-ttu-id="d3f2e-123">Les applications de technologie d’assistance doivent généralement accéder aux éléments de l’interface utilisateur du système protégé, ou à d’autres processus qui peuvent s’exécuter à un niveau de privilège plus élevé.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-123">Assistive technology applications typically need access to the protected system UI elements, or to other processes that might be running at a higher privilege level.</span></span> <span data-ttu-id="d3f2e-124">Par conséquent, les applications de technologie d’assistance doivent être approuvées par le système et doivent s’exécuter avec des privilèges spéciaux.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-124">Therefore, assistive technology applications must be trusted by the system, and must run with special privileges.</span></span>

<span data-ttu-id="d3f2e-125">Pour obtenir l’accès à des processus IL plus élevés, une application de technologie d’assistance doit définir l’indicateur UIAccess dans le manifeste de l’application et être lancé par un utilisateur disposant de privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-125">To get access to higher IL processes, an assistive technology application must set the UIAccess flag in the application's manifest and be launched by a user with administrator privileges.</span></span>

> [!NOTE]
> <span data-ttu-id="d3f2e-126">Les privilèges d’accès sont limités comme suit :</span><span class="sxs-lookup"><span data-stu-id="d3f2e-126">Access privileges are constrained as follows:</span></span>
>
> - <span data-ttu-id="d3f2e-127">Une application qui n’a pas de UIAccess dans le manifeste commence par le langage intermédiaire moyen et ne peut pas accéder à l’interface utilisateur du processus avec élévation de privilèges (IL est de taille moyenne + « IL ».</span><span class="sxs-lookup"><span data-stu-id="d3f2e-127">An application that doesn't have UIAccess in the manifest starts with medium IL and cannot access elevated ("medium+" IL) process UI.</span></span>
> - <span data-ttu-id="d3f2e-128">Une application qui possède l’UIAccess dans le manifeste et qui est lancée par un utilisateur qui ne se trouve pas dans le groupe administrateurs, commence par le langage intermédiaire « moyen + » et ne peut pas accéder à l’interface utilisateur avec élévation de privilèges (rien ne s’exécute en langage intermédiaire « élevé », comme les applications lancées par un **clic droit > exécuter en tant qu’administrateur**).</span><span class="sxs-lookup"><span data-stu-id="d3f2e-128">An application that has UIAccess in the manifest and is launched by a user who is not in the administrators group, starts as "medium+" IL and cannot access elevated UI (nothing running as "high" IL, such as apps launched through a **Right click -> Run as administrator**).</span></span>
> - <span data-ttu-id="d3f2e-129">Une application dispose d’un accès à l’interface utilisateur et elle est lancée par un utilisateur administrateur qui démarre en tant qu’il « High » et peut accéder à l’interface utilisateur avec élévation de privilèges, car elle a le même il.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-129">An application has UI Access and is launched by an admin user starts as "high" IL and can access elevated UI because it has the same IL.</span></span>
>
> <span data-ttu-id="d3f2e-130">L’UIAccess n’est pas suffisant pour qu’un processus se déplace jusqu’à la limite IL.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-130">UIAccess is not enough for a process to move up through the IL boundary.</span></span>

<span data-ttu-id="d3f2e-131">En plus d’avoir accès à des processus IL plus élevés, une application de technologie d’assistance avec ces privilèges peut s’exécuter en tant qu’application de niveau supérieur dans l’ordre de plan à tout moment, ce qui signifie qu’une application de technologie d’assistance peut être visible et disponible chaque fois que l’utilisateur en a besoin.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-131">In addition to having access to higher IL processes, an assistive technology application with these privileges can run as the topmost application in the z-order at any time, meaning that an assistive technology application can be visible and available whenever the user needs it.</span></span>

> [!Important]
> <span data-ttu-id="d3f2e-132">Aucun des scénarios ci-dessus ne permet d’accéder à l’interface utilisateur qui s’exécute sous le système IL.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-132">None of the previously listed scenarios provide access to UI running under the system IL.</span></span> <span data-ttu-id="d3f2e-133">Cela est possible uniquement si le processus est lancé dans le Bureau de contrôle de compte d’utilisateur (UAC) sous système (et IL système).</span><span class="sxs-lookup"><span data-stu-id="d3f2e-133">This is only possible if the process is launched in the user account control (UAC) desktop under SYSTEM (and system IL).</span></span> <span data-ttu-id="d3f2e-134">Dans ce cas, la définition de l’UIAccess n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-134">In this case, setting UIAccess has no effect.</span></span>

## <a name="uiaccess-requirements-for-assistive-technology-applications"></a><span data-ttu-id="d3f2e-135">Exigences UIAccess pour les applications de technologie d’assistance</span><span class="sxs-lookup"><span data-stu-id="d3f2e-135">UIAccess Requirements for Assistive Technology Applications</span></span>

<span data-ttu-id="d3f2e-136">Une application de technologie d’assistance est une application de bureau Windows Windows qui interagit avec d’autres processus en cours d’exécution sur le bureau et dans la nouvelle interface utilisateur Windows pour obtenir des informations à partir du système et des applications.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-136">An assistive technology application is a Windows Windows desktop application that interacts with other processes running on the desktop and in the new Windows UI to get information from the system and applications.</span></span> <span data-ttu-id="d3f2e-137">L’application de technologie d’assistance peut ensuite fournir les informations aux utilisateurs d’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-137">The assistive technology application can then provide the information to accessibility users.</span></span>

<span data-ttu-id="d3f2e-138">Une application de technologie d’assistance obtient l’accès à d’autres processus en définissant l’indicateur UIAccess dans le manifeste de l’application.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-138">An assistive technology application gets access to other processes by setting the UIAccess flag in the application manifest.</span></span> <span data-ttu-id="d3f2e-139">Pour utiliser l’indicateur UIAccess, une application de technologie d’assistance doit remplir les conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-139">To use the UIAccess flag, an assistive technology application must meet the following requirements.</span></span>

-   <span data-ttu-id="d3f2e-140">Exigez l’affichage, l’interaction ou la prise en compte des informations provenant d’une autre application pour fournir des informations pour un scénario d’accessibilité, et/ou</span><span class="sxs-lookup"><span data-stu-id="d3f2e-140">Require to display, interact with, or reflect information from another application to provide information for an accessibility scenario, and/or</span></span>
-   <span data-ttu-id="d3f2e-141">Pour obtenir ou afficher ces informations, exigez l’exécution en tant que fenêtre supérieure.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-141">Require running as the top-most window to obtain or display this information.</span></span>

<span data-ttu-id="d3f2e-142">Pour utiliser l’UIAccess, une application de technologie d’assistance doit :</span><span class="sxs-lookup"><span data-stu-id="d3f2e-142">To use UIAccess, an assistive technology application needs to:</span></span>

-   <span data-ttu-id="d3f2e-143">Être signé avec un certificat pour interagir avec les applications qui s’exécutent à un niveau de privilège supérieur.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-143">Be signed with a certificate to interact with applications running at a higher privilege level.</span></span>
-   <span data-ttu-id="d3f2e-144">Être approuvé par le système.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-144">Be trusted by the system.</span></span> <span data-ttu-id="d3f2e-145">L’application doit être installée dans un emplacement sécurisé nécessitant l’accès à une invite de contrôle de compte d’utilisateur (UAC).</span><span class="sxs-lookup"><span data-stu-id="d3f2e-145">The application must be installed in a secure location that requires a user account control (UAC) prompt for access.</span></span> <span data-ttu-id="d3f2e-146">Par exemple, le dossier Program Files.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-146">For example, the Program Files folder.</span></span>
-   <span data-ttu-id="d3f2e-147">Être généré avec un fichier manifeste qui comprend l’indicateur uiAccess.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-147">Be built with a manifest file that includes the uiAccess flag.</span></span>

<span data-ttu-id="d3f2e-148">L’UIAccess ne doit pas être utilisé :</span><span class="sxs-lookup"><span data-stu-id="d3f2e-148">UIAccess should not be used:</span></span>

-   <span data-ttu-id="d3f2e-149">Par les applications qui ne sont pas des technologies d’assistance.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-149">By applications that are not assistive technologies.</span></span>
-   <span data-ttu-id="d3f2e-150">Par les applications de technologie d’assistance qui affichent des informations ou une interface utilisateur qui ne s’applique pas au scénario d’accessibilité qu’ils ciblent.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-150">By assistive technology applications that display information or UI that is not relevant to the accessibility scenario they target.</span></span>
-   <span data-ttu-id="d3f2e-151">Par les applications qui souhaitent juste apparaître au-dessus d’autres applications dans la nouvelle interface utilisateur Windows.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-151">By applications that just want to appear above other applications in the new Windows UI.</span></span>
    > [!Note]  
    > <span data-ttu-id="d3f2e-152">Les applications développées pour la nouvelle interface utilisateur Windows n’ont pas UIAccess comme option disponible.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-152">Applications developed for the new Windows UI do not have UIAccess as an available option.</span></span>

     

## <a name="setting-uiaccess-in-the-application-manifest-file"></a><span data-ttu-id="d3f2e-153">Définition de l’UIAccess dans le fichier manifeste de l’application</span><span class="sxs-lookup"><span data-stu-id="d3f2e-153">Setting UIAccess in the Application Manifest File</span></span>

<span data-ttu-id="d3f2e-154">Pour accéder à l’interface utilisateur du système protégé, les applications doivent être générées avec un fichier manifeste qui comprend un attribut spécial dans le fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-154">To gain access to the protected system UI, applications must be built with a manifest file that includes a special attribute in the manifest file.</span></span> <span data-ttu-id="d3f2e-155">Cet attribut **UIAccess** est inclus dans la balise **requestedExecutionLevel** , comme illustré dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-155">This **uiAccess** attribute is included in the **requestedExecutionLevel** tag, as shown in the following code example.</span></span>


```XML
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3"> 
    <security> 
        <requestedPrivileges> 
        <requestedExecutionLevel 
            level="highestAvailable" 
            uiAccess="true" /> 
        </requestedPrivileges> 
    </security> 
</trustInfo> 
```



<span data-ttu-id="d3f2e-156">La valeur de l’attribut **Level** dans ce code est un exemple uniquement.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-156">The value of the **level** attribute in this code is an example only.</span></span>

<span data-ttu-id="d3f2e-157">L' **UIAccess** est « false » par défaut.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-157">**UIAccess** is "false" by default.</span></span> <span data-ttu-id="d3f2e-158">Si l’attribut est omis ou s’il n’existe aucun manifeste, l’application ne peut pas accéder à l’interface utilisateur protégée.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-158">If the attribute is omitted, or if there is no manifest, the application cannot gain access to the protected UI.</span></span>

<span data-ttu-id="d3f2e-159">Pour plus d’informations sur la sécurité Windows, sur la signature des applications et sur la création de manifestes, consultez [Windows Vista et Windows Server 2008 Developer Story : Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10)) sur MSDN.</span><span class="sxs-lookup"><span data-stu-id="d3f2e-159">For more information on Windows security, on signing applications, and on creating manifests, see [The Windows Vista and Windows Server 2008 Developer Story: Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10)) on MSDN.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3f2e-160">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3f2e-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3f2e-161">Notions de base d’UI Automation</span><span class="sxs-lookup"><span data-stu-id="d3f2e-161">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 