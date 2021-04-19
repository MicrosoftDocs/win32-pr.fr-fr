---
description: Vue d’ensemble de la bibliothèque managée et notes sur l’utilisation de la bibliothèque gérée de plateforme Tablet PC.
ms.assetid: d283ea1c-faf3-4222-a9a7-c67087636b86
title: Utilisation de la bibliothèque managée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1a1050705a6d74e6b183d04ec1c8f82d3954f0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106523095"
---
# <a name="using-the-managed-library"></a><span data-ttu-id="7b606-103">Utilisation de la bibliothèque managée</span><span class="sxs-lookup"><span data-stu-id="7b606-103">Using the Managed Library</span></span>

<span data-ttu-id="7b606-104">Le common language runtime est la base du Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="7b606-104">The common language runtime is the foundation of the Microsoft .NET Framework.</span></span> <span data-ttu-id="7b606-105">Vous pouvez considérer le common language runtime comme un agent qui gère le code au moment de l’exécution, en fournissant des services centraux tels que la gestion de la mémoire, la gestion des threads et la communication à distance, tout en appliquant également une sécurité de code stricte.</span><span class="sxs-lookup"><span data-stu-id="7b606-105">You can think of the common language runtime as an agent that manages code at execution time, providing core services such as memory management, thread management, and remoting, while also enforcing strict code safety.</span></span> <span data-ttu-id="7b606-106">En fait, le concept de gestion de code est un principe fondamental de la common language runtime.</span><span class="sxs-lookup"><span data-stu-id="7b606-106">In fact, the concept of code management is a fundamental principle of the common language runtime.</span></span> <span data-ttu-id="7b606-107">Le code qui cible le common language runtime est connu sous le nom de code managé.</span><span class="sxs-lookup"><span data-stu-id="7b606-107">Code that targets the common language runtime is known as managed code.</span></span> <span data-ttu-id="7b606-108">Le code qui ne cible pas le common language runtime est connu sous le nom de code natif.</span><span class="sxs-lookup"><span data-stu-id="7b606-108">Code that does not target the common language runtime is known as native code.</span></span>

<span data-ttu-id="7b606-109">La bibliothèque de classes Framework est une collection complète orientée objet de classes réutilisables que vous pouvez utiliser pour développer des applications allant des applications de ligne de commande traditionnelles ou d’interface utilisateur graphique (GUI) aux applications basées sur les dernières innovations fournies par ASP.NET et les services Web.</span><span class="sxs-lookup"><span data-stu-id="7b606-109">The Framework class library is a comprehensive, object-oriented collection of reusable classes that you can use to develop applications ranging from traditional command-line or graphical user interface (GUI) applications to applications based on the latest innovations provided by ASP.NET and Web Services.</span></span>

<span data-ttu-id="7b606-110">La bibliothèque gérée Tablet PC contient un ensemble d’objets gérés qui étend l’infrastructure pour assurer la prise en charge de l’entrée et de la sortie de l’écriture manuscrite sur Tablet PC, ainsi que l’échange de données avec d’autres ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="7b606-110">The Tablet PC Managed Library contains a set of managed objects that extends the Framework to provide support for input and output of handwriting on Tablet PC as well as data interchange with other computers.</span></span>

## <a name="exceptions"></a><span data-ttu-id="7b606-111">Exceptions</span><span class="sxs-lookup"><span data-stu-id="7b606-111">Exceptions</span></span>

<span data-ttu-id="7b606-112">Les objets de la bibliothèque managée dans l’API Tablet PC encapsulent les implémentations de la bibliothèque COM.</span><span class="sxs-lookup"><span data-stu-id="7b606-112">The managed library objects in the Tablet PC API wrap the COM library implementations.</span></span> <span data-ttu-id="7b606-113">Lorsque l’objet ou le contrôle de bibliothèque COM sous-jacent retourne une erreur, les API managées lèvent une exception Marshal. ThrowExceptionForHR qui fournit les détails sur l’exception COM interne.</span><span class="sxs-lookup"><span data-stu-id="7b606-113">When the underlying COM library object or control returns an error, the managed API's will throw a Marshal.ThrowExceptionForHR exception that provides the details on the inner COM exception.</span></span> <span data-ttu-id="7b606-114">Vous pouvez faire référence aux valeurs HRESULT dans la référence de la bibliothèque COM pour plus d’informations sur les erreurs pouvant être retournées.</span><span class="sxs-lookup"><span data-stu-id="7b606-114">You can refer to the HRESULT values in the COM Library Reference for details on the possible errors that may be returned.</span></span>

## <a name="object-comparison"></a><span data-ttu-id="7b606-115">Comparaison d’objets</span><span class="sxs-lookup"><span data-stu-id="7b606-115">Object Comparison</span></span>

<span data-ttu-id="7b606-116">Pour tous les objets de la bibliothèque managée de plateforme Tablet PC, est [**égal**](/previous-versions/windows/) à n’est pas substitué pour comparer correctement deux objets qui sont identiques.</span><span class="sxs-lookup"><span data-stu-id="7b606-116">For all objects in the Tablet PC Platform Managed library, [**Equals**](/previous-versions/windows/) is not overridden to correctly compare two objects that are the same.</span></span> <span data-ttu-id="7b606-117">L’interface de programmation d’applications (API) managée ne prend pas en charge la comparaison d’égalité d’objets, soit par l’intermédiaire de la fonction **Equals** , soit par le biais de l’opérateur égal (= =).</span><span class="sxs-lookup"><span data-stu-id="7b606-117">The managed application programming interface (API) does not support the comparison of objects for equality, either through the **Equals** function or through the equals (==) operator.</span></span>

## <a name="binding-to-the-latest-microsoftinkdll"></a><span data-ttu-id="7b606-118">Liaison avec la dernière Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="7b606-118">Binding to the Latest Microsoft.Ink.dll</span></span>

<span data-ttu-id="7b606-119">La dernière Microsoft.Ink.dll assembly est un remplacement compatible de Microsoft.Ink.dll version 1,0 et Microsoft.Ink.15.dll.</span><span class="sxs-lookup"><span data-stu-id="7b606-119">The latest Microsoft.Ink.dll assembly is a compatible replacement for Microsoft.Ink.dll version 1.0 and Microsoft.Ink.15.dll.</span></span> <span data-ttu-id="7b606-120">Dans la plupart des cas, vous n’avez pas besoin d’apporter des modifications à vos applications qui sont distribuées avec les anciens assemblys.</span><span class="sxs-lookup"><span data-stu-id="7b606-120">In most cases, you do not need to make any changes to your applications that are distributed with the older assemblies.</span></span> <span data-ttu-id="7b606-121">Toutefois, dans certains cas, vous devez demander à l’common language runtime Loader d’utiliser la bibliothèque de liens dynamiques (DLL) la plus récente, où les anciennes dll ont été référencées.</span><span class="sxs-lookup"><span data-stu-id="7b606-121">However, in some cases you need to instruct the common language runtime loader to use the newer dynamic-link library (DLL) wherever the older DLLs have been referenced.</span></span>

<span data-ttu-id="7b606-122">La seule fois où vous devez effectuer une liaison explicite au nouvel assembly à l’aide de la technique suivante est si votre application utilise un composant qui fait référence à l’assembly version 1,0 ou 1,5 en association avec un composant qui fait référence à un assembly de version plus récent, tel que 1,7, et si ces composants peuvent échanger des données.</span><span class="sxs-lookup"><span data-stu-id="7b606-122">The only time you need to explicitly bind to the new assembly by using the following technique is if your application uses a component that references the version 1.0 or 1.5 assembly in combination with a component that references a more recent version assembly,such as 1.7, and if those components may exchange data.</span></span>

<span data-ttu-id="7b606-123">La meilleure façon d’indiquer au chargeur common language runtime d’utiliser la DLL la plus récente consiste à rediriger les versions d’assembly au niveau de l’application.</span><span class="sxs-lookup"><span data-stu-id="7b606-123">The best way to instruct the common language runtime loader to use the newer DLL is to redirect assembly versions at the application level.</span></span> <span data-ttu-id="7b606-124">Vous pouvez spécifier que votre application utilise la version la plus récente de l’assembly en plaçant des informations de liaison d’assembly dans le fichier de configuration de votre application.</span><span class="sxs-lookup"><span data-stu-id="7b606-124">You can specify that your application use the newer version of the assembly by putting assembly binding information in your application's configuration file.</span></span> <span data-ttu-id="7b606-125">Pour plus d’informations sur la redirection des versions d’assembly au niveau de l’application, consultez [redirection des versions d’assembly](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue), en particulier la section « Spécification d’une liaison d’assembly dans des fichiers de configuration ».</span><span class="sxs-lookup"><span data-stu-id="7b606-125">For more information about redirecting assembly versions at the application level, see [Redirecting Assembly Versions](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue), specifically the section "Specifying Assembly Binding in Configuration Files."</span></span>

<span data-ttu-id="7b606-126">Vous devrez créer un fichier de configuration dans le même répertoire que votre fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="7b606-126">You will need to create a configuration file in the same directory as your executable file.</span></span> <span data-ttu-id="7b606-127">Le fichier de configuration doit porter le même nom que votre exécutable, suivi de l’extension de fichier. config.</span><span class="sxs-lookup"><span data-stu-id="7b606-127">The configuration file must have the same name as your executable, followed by the .config file extension.</span></span> <span data-ttu-id="7b606-128">Par exemple, pour une application, MyApp.exe, le fichier de configuration doit être le fichier MyApp.exe.config.</span><span class="sxs-lookup"><span data-stu-id="7b606-128">For example, for an application, MyApp.exe, the configuration file must be the MyApp.exe.config file.</span></span> <span data-ttu-id="7b606-129">Le fichier de configuration utilise un élément [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) pour forcer toutes les versions antérieures à être mappées à la dernière version, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="7b606-129">The configuration file uses a [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) element to force all prior versions to be mapped to the latest version, as shown in the following example:</span></span>

`<bindingRedirect oldVersion="0.0.0.0-1.7.2600.xxxx" newVersion="1.7.2600.xxxx" />`

<span data-ttu-id="7b606-130">Pour plus d’informations sur les fichiers de configuration, y compris des exemples de construction du Extensible Markup Language (XML) pour le fichier de configuration, consultez [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) et [redirection des versions d’assembly](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue).</span><span class="sxs-lookup"><span data-stu-id="7b606-130">For more information about configuration files, including examples of how to construct the Extensible Markup Language (XML) for the configuration file, see both [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) and [Redirecting Assembly Versions](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue).</span></span>

<span data-ttu-id="7b606-131">Les applications créées avec Microsoft Windows XP Tablet PC Edition Kit de développement 1,7 et versions ultérieures sont automatiquement liées à la nouvelle version de l’assembly Microsoft. Ink.</span><span class="sxs-lookup"><span data-stu-id="7b606-131">Applications created with Microsoft Windows XP Tablet PC Edition Development Kit 1.7 and later versions are automatically bound to the new version of the Microsoft.Ink assembly.</span></span> <span data-ttu-id="7b606-132">Pour plus d’informations sur la liaison d’assembly, consultez [Comment le runtime localise les assemblys](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp).</span><span class="sxs-lookup"><span data-stu-id="7b606-132">For more information about assembly binding see [How the Runtime Locates Assemblies](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp).</span></span>

> [!Note]  
> <span data-ttu-id="7b606-133">L’utilisation de la stratégie d’application pour effectuer une liaison à l’assembly mis à jour ne fonctionne pas pour les applications qui utilisent la classe [diviseur](/previous-versions/ms583616(v=vs.100)) ou la classe [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="7b606-133">Using application policy to bind to the updated assembly does not work for applications that use the [Divider](/previous-versions/ms583616(v=vs.100)) class or the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) class.</span></span> <span data-ttu-id="7b606-134">Les applications qui utilisent l’une de ces classes doivent continuer à utiliser Microsoft.Ink.15.dll ou être recompilées après avoir fait référence à l’assembly mis à jour.</span><span class="sxs-lookup"><span data-stu-id="7b606-134">Applications that use either of those classes must either continue to use Microsoft.Ink.15.dll or be recompiled after referencing the updated assembly.</span></span>

 

## <a name="working-with-events"></a><span data-ttu-id="7b606-135">Utilisation des événements</span><span class="sxs-lookup"><span data-stu-id="7b606-135">Working with Events</span></span>

<span data-ttu-id="7b606-136">Si le code d’un gestionnaire d’événements pour l’un des objets managés lève une exception, l’exception n’est pas remise à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7b606-136">If the code within an event handler for any of the managed objects throws an exception, the exception is not delivered to the user.</span></span> <span data-ttu-id="7b606-137">Pour vous assurer que les exceptions sont remises, utilisez des blocs try-catch dans vos gestionnaires d’événements pour les événements managés.</span><span class="sxs-lookup"><span data-stu-id="7b606-137">To ensure that exceptions are delivered, use try-catch blocks in your event handlers for managed events.</span></span>

## <a name="managing-forms"></a><span data-ttu-id="7b606-138">Gestion des formulaires</span><span class="sxs-lookup"><span data-stu-id="7b606-138">Managing Forms</span></span>

<span data-ttu-id="7b606-139">La classe [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) et ses classes de base ne définissent pas de finaliseur.</span><span class="sxs-lookup"><span data-stu-id="7b606-139">The [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) class and its base classes do not define a finalizer.</span></span> <span data-ttu-id="7b606-140">Pour nettoyer vos ressources sur un formulaire, écrivez une sous-classe qui fournit un finaliseur (par exemple, le \# destructeur C à l’aide de ~) qui appelle [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="7b606-140">To clean up your resources on a form, write a subclass that provides a finalizer (for example, the C\# destructor using the ~) that calls [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1).</span></span> <span data-ttu-id="7b606-141">Pour effectuer le nettoyage, le finaliseur remplace la méthode dispose, puis appelle la méthode dispose de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="7b606-141">To do the cleanup the finalizer overrides Dispose and then calls the base class Dispose.</span></span> <span data-ttu-id="7b606-142">Ne faites pas référence à d’autres objets qui nécessitent la méthode [Finalize](/previous-versions/windows/) dans la méthode dispose lorsque le paramètre Boolean a la **valeur false**, car ces objets ont peut-être déjà été finalisés.</span><span class="sxs-lookup"><span data-stu-id="7b606-142">Do not refer to other objects that require the [Finalize](/previous-versions/windows/) method in the Dispose method when the Boolean parameter is **FALSE**, because those objects may already have been finalized.</span></span> <span data-ttu-id="7b606-143">Pour plus d’informations sur la libération de ressources [, consultez méthodes Finalize et destructeurs](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp).</span><span class="sxs-lookup"><span data-stu-id="7b606-143">For more information about releasing resources see [Finalize Methods and Destructors](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp).</span></span>

## <a name="forms-and-the-recognizercontext"></a><span data-ttu-id="7b606-144">Forms et RecognizerContext</span><span class="sxs-lookup"><span data-stu-id="7b606-144">Forms and the RecognizerContext</span></span>

<span data-ttu-id="7b606-145">Les événements [RecognizerContext](/previous-versions/ms552546(v=vs.100)) s’exécutent dans un thread différent du thread sur lequel se trouve le formulaire.</span><span class="sxs-lookup"><span data-stu-id="7b606-145">[RecognizerContext](/previous-versions/ms552546(v=vs.100)) events run in a different thread than the thread that the form is on.</span></span> <span data-ttu-id="7b606-146">Dans Windows Forms, les contrôles sont liés à un thread spécifique et ne sont pas thread-safe.</span><span class="sxs-lookup"><span data-stu-id="7b606-146">Controls in Windows Forms are bound to a specific thread and are not thread safe.</span></span> <span data-ttu-id="7b606-147">Par conséquent, vous devez utiliser l’une des méthodes Invoke du contrôle pour marshaler l’appel au thread approprié.</span><span class="sxs-lookup"><span data-stu-id="7b606-147">Therefore, you must use one of the control's invoke methods to marshal the call to the proper thread.</span></span> <span data-ttu-id="7b606-148">Quatre méthodes sur un contrôle sont thread-safe : les méthodes [Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1), [BeginInvoke](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1), [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1)et [CreateGraphics](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="7b606-148">Four methods on a control are thread safe: the [Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1), [BeginInvoke](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1), [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1), and [CreateGraphics](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) methods.</span></span> <span data-ttu-id="7b606-149">Pour tous les autres appels de méthode, utilisez l’une de ces méthodes Invoke lors de l’appel à partir d’un thread différent.</span><span class="sxs-lookup"><span data-stu-id="7b606-149">For all other method calls, use one of these invoke methods when calling from a different thread.</span></span> <span data-ttu-id="7b606-150">Pour plus d’informations sur l’utilisation de ces méthodes, consultez [manipulation de contrôles à partir de threads](/previous-versions/757y83z4(v=vs.140)).</span><span class="sxs-lookup"><span data-stu-id="7b606-150">For more information on using these methods, see [Manipulating Controls from Threads](/previous-versions/757y83z4(v=vs.140)).</span></span>

## <a name="waiting-for-events"></a><span data-ttu-id="7b606-151">En attente d’événements</span><span class="sxs-lookup"><span data-stu-id="7b606-151">Waiting for Events</span></span>

<span data-ttu-id="7b606-152">L’environnement Tablet PC est multithread.</span><span class="sxs-lookup"><span data-stu-id="7b606-152">The Tablet PC environment is multithreaded.</span></span> <span data-ttu-id="7b606-153">Utilisez la fonction [**CoWaitForMultipleHandles**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) au lieu d’autres méthodes d’attente pour permettre aux appels com (Component Object Model) réentrants d’entrer votre MTA (Multithreaded Apartment) pendant que votre application attend un événement.</span><span class="sxs-lookup"><span data-stu-id="7b606-153">Use the [**CoWaitForMultipleHandles**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) function instead of other wait methods to allow re-entrant Component Object Model (COM) calls to enter your multithreaded apartment (MTA) while your application is waiting on an event.</span></span>

## <a name="using-ink-strokes-collections"></a><span data-ttu-id="7b606-154">Utilisation de collections de traits d’encre</span><span class="sxs-lookup"><span data-stu-id="7b606-154">Using Ink Strokes Collections</span></span>

<span data-ttu-id="7b606-155">Les instances des collections de [traits](/previous-versions/ms552701(v=vs.100)) obtenues à partir d’un objet [Ink](/previous-versions/aa515768(v=msdn.10)) ne sont pas récupérées par le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="7b606-155">Instances of [Strokes](/previous-versions/ms552701(v=vs.100)) collections which are obtained from an [Ink](/previous-versions/aa515768(v=msdn.10)) object are not garbage collected.</span></span> <span data-ttu-id="7b606-156">Afin d’éviter une fuite de mémoire, chaque fois que vous utilisez l’une de ces collections, utilisez l’instruction « using », comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7b606-156">In order to avoid a memory leak, any time that you are working with one of these collections, make use of the "using" statement as shown below.</span></span>


```C++
using (Strokes strokes = myInk.Strokes)
{
    int i = strokes.Count;
}
```



## <a name="disposing-managed-objects-and-controls"></a><span data-ttu-id="7b606-157">Suppression d’objets et de contrôles managés</span><span class="sxs-lookup"><span data-stu-id="7b606-157">Disposing Managed Objects and Controls</span></span>

<span data-ttu-id="7b606-158">Pour éviter une fuite de mémoire, vous devez appeler explicitement la méthode [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) sur tout objet ou contrôle Tablet PC auquel un gestionnaire d’événements a été attaché avant que l’objet ou le contrôle ne soit hors de portée.</span><span class="sxs-lookup"><span data-stu-id="7b606-158">To avoid a memory leak you must explicitly call the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method on any Tablet PC object or control to which an event handler has been attached before the object or control goes out of scope.</span></span>

<span data-ttu-id="7b606-159">Pour améliorer les performances de votre application, supprimez manuellement les objets, contrôles et collections suivants lorsqu’ils ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="7b606-159">To improve the performance of your application, manually dispose of the following objects, controls, and collection when they are no longer needed.</span></span>

-   <span data-ttu-id="7b606-160">[Séparateur](/previous-versions/ms583616(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="7b606-160">[Divider](/previous-versions/ms583616(v=vs.100))</span></span>
-   <span data-ttu-id="7b606-161">[Entrée manuscrite](/previous-versions/aa515768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7b606-161">[Ink](/previous-versions/aa515768(v=msdn.10))</span></span>
-   <span data-ttu-id="7b606-162">[Collecte](/previous-versions/ms583683(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="7b606-162">[InkCollector](/previous-versions/ms583683(v=vs.100))</span></span>
-   <span data-ttu-id="7b606-163">[InkEdit](/previous-versions/ms552265(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="7b606-163">[InkEdit](/previous-versions/ms552265(v=vs.100))</span></span>
-   <span data-ttu-id="7b606-164">[InkOverlay](/previous-versions/ms552322(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="7b606-164">[InkOverlay](/previous-versions/ms552322(v=vs.100))</span></span>
-   <span data-ttu-id="7b606-165">[InkPicture](/previous-versions/aa514604(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7b606-165">[InkPicture](/previous-versions/aa514604(v=msdn.10))</span></span>
-   <span data-ttu-id="7b606-166">[PenInputPanel](/previous-versions/aa514041(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7b606-166">[PenInputPanel](/previous-versions/aa514041(v=msdn.10))</span></span>
-   <span data-ttu-id="7b606-167">[RecognizerContext](/previous-versions/ms552546(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="7b606-167">[RecognizerContext](/previous-versions/ms552546(v=vs.100))</span></span>
-   <span data-ttu-id="7b606-168">[Traits](/previous-versions/ms552701(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="7b606-168">[Strokes](/previous-versions/ms552701(v=vs.100))</span></span>

<span data-ttu-id="7b606-169">L’exemple C suivant \# illustre certains scénarios dans lesquels la méthode [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) est utilisée.</span><span class="sxs-lookup"><span data-stu-id="7b606-169">The following C\# example demonstrates some scenarios in which the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method is used.</span></span>


```C++
// A field for a Divider object
private Microsoft.Ink.Divider theDivider;

// A method that creates a Divider object
public void CreateDivider()
{
    // Make sure any previous Divider object was disposed of.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
    // Create the Divider object.
    theDivider = new Microsoft.Ink.Divider();

    // The remainder of the method
}

// A method that disposes of the Divider object
public void DisposeDivider()
{
    // The remainder of the method

    // Dispose of the Divider object.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
}

// A method that uses a local PenInputPanel object.
public void UsePenInputPanel()
{
    // Create the PenInputPanel object.
    Microsoft.Ink.PenInputPanel thePenInputPanel =
        new Microsoft.Ink.PenInputPanel();

    // The remainder of the method

    // Dispose of the PenInputPanel object before exiting.
    thePenInputPanel.Dispose();
    thePenInputPanel = null;
}
```



 

 