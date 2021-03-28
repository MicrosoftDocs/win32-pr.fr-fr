---
description: Utilisez les programmes par défaut pour définir l’expérience utilisateur par défaut.
ms.assetid: 78cd05a4-df33-42b5-91b9-826ebce04a1d
title: Programmes par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f8cd741794189e47888f4daa1d4585b2d8942cf
ms.sourcegitcommit: 1a97e0e0f92d4dcc2fb68738b910ba3910508df3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2021
ms.locfileid: "103869293"
---
# <a name="default-programs"></a><span data-ttu-id="fd60c-103">Programmes par défaut</span><span class="sxs-lookup"><span data-stu-id="fd60c-103">Default Programs</span></span>

<span data-ttu-id="fd60c-104">Utilisez les **programmes par défaut** pour définir l’expérience utilisateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="fd60c-104">Use **Default Programs** to set the default user experience.</span></span> <span data-ttu-id="fd60c-105">Les utilisateurs peuvent accéder aux **programmes par défaut** à partir du panneau de configuration ou directement à partir du menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="fd60c-105">Users can access **Default Programs** from Control Panel or directly from the **Start** menu.</span></span> <span data-ttu-id="fd60c-106">L’outil [définir l’accès aux programmes et les paramètres par défaut de l’ordinateur (SPAD)](cpl-setprogramaccess.md) , l’expérience des valeurs par défaut principales pour les utilisateurs dans Windows XP, est désormais un composant des **programmes par défaut**.</span><span class="sxs-lookup"><span data-stu-id="fd60c-106">[Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md) tool, the primary defaults experience for users in Windows XP, is now one part of **Default Programs**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd60c-107">Cette rubrique ne s’applique pas à Windows 10.</span><span class="sxs-lookup"><span data-stu-id="fd60c-107">This topic does not apply for Windows 10.</span></span> <span data-ttu-id="fd60c-108">Le mode de fonctionnement des associations de fichiers par défaut dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="fd60c-108">The way that default file associations work changed in Windows 10.</span></span> <span data-ttu-id="fd60c-109">Pour plus d’informations, consultez la section sur les **modifications apportées à la façon dont Windows 10 gère les applications par défaut** dans [cette publication](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span><span class="sxs-lookup"><span data-stu-id="fd60c-109">For more information, see the section on **Changes to how Windows 10 handles default apps** in [this post](https://blogs.windows.com/windowsexperience/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).</span></span>

 

<span data-ttu-id="fd60c-110">Quand un utilisateur définit les paramètres par défaut du programme à l’aide de **programmes par défaut**, le paramètre par défaut s’applique uniquement à cet utilisateur et non aux autres utilisateurs qui peuvent utiliser le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fd60c-110">When a user sets program defaults using **Default Programs**, the default setting applies only to that user and not to other users who might use the same computer.</span></span> <span data-ttu-id="fd60c-111">Les **programmes par défaut** fournissent un ensemble d’API (déconseillées dans Windows 8) qui permettent aux éditeurs de logiciels indépendants d’inclure leurs programmes ou applications dans le système par défaut.</span><span class="sxs-lookup"><span data-stu-id="fd60c-111">**Default Programs** provides a set of APIs (deprecated in Windows 8) that enable independent software vendors (ISVs) to include their programs or applications in the defaults system.</span></span> <span data-ttu-id="fd60c-112">L’ensemble d’API permet également aux éditeurs de logiciels indépendants de mieux gérer leur état par défaut.</span><span class="sxs-lookup"><span data-stu-id="fd60c-112">The API set also helps ISVs better manage their status as defaults.</span></span>

<span data-ttu-id="fd60c-113">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="fd60c-113">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="fd60c-114">Présentation des programmes par défaut et de l’ensemble des API associées</span><span class="sxs-lookup"><span data-stu-id="fd60c-114">Introduction to Default Programs and Its Related API Set</span></span>](#introduction-to-default-programs-and-its-related-api-set)
-   [<span data-ttu-id="fd60c-115">Inscription d’une application pour une utilisation avec les programmes par défaut</span><span class="sxs-lookup"><span data-stu-id="fd60c-115">Registering an Application for Use with Default Programs</span></span>](#registering-an-application-for-use-with-default-programs)
    -   [<span data-ttu-id="fd60c-116">ProgID</span><span class="sxs-lookup"><span data-stu-id="fd60c-116">ProgIDs</span></span>](#progids)
    -   [<span data-ttu-id="fd60c-117">Sous-clé d’inscription et descriptions de valeur</span><span class="sxs-lookup"><span data-stu-id="fd60c-117">Registration Subkey and Value Descriptions</span></span>](#registration-subkey-and-value-descriptions)
    -   [<span data-ttu-id="fd60c-118">RegisteredApplications</span><span class="sxs-lookup"><span data-stu-id="fd60c-118">RegisteredApplications</span></span>](#registeredapplications)
    -   [<span data-ttu-id="fd60c-119">Exemple d’inscription complète</span><span class="sxs-lookup"><span data-stu-id="fd60c-119">Full Registration Example</span></span>](#full-registration-example)
-   [<span data-ttu-id="fd60c-120">Devenir le navigateur par défaut</span><span class="sxs-lookup"><span data-stu-id="fd60c-120">Becoming the Default Browser</span></span>](#becoming-the-default-browser)
-   [<span data-ttu-id="fd60c-121">Interface utilisateur des programmes par défaut</span><span class="sxs-lookup"><span data-stu-id="fd60c-121">Default Programs UI</span></span>](#default-programs-ui)
-   [<span data-ttu-id="fd60c-122">Meilleures pratiques pour l’utilisation des programmes par défaut</span><span class="sxs-lookup"><span data-stu-id="fd60c-122">Best Practices for Using Default Programs</span></span>](#best-practices-for-using-default-programs)
    -   [<span data-ttu-id="fd60c-123">Pendant l’installation</span><span class="sxs-lookup"><span data-stu-id="fd60c-123">During Installation</span></span>](#during-installation)
    -   [<span data-ttu-id="fd60c-124">Après l’installation</span><span class="sxs-lookup"><span data-stu-id="fd60c-124">After Installation</span></span>](#after-installation)
-   [<span data-ttu-id="fd60c-125">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="fd60c-125">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="fd60c-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fd60c-126">Related topics</span></span>](#related-topics)

## <a name="introduction-to-default-programs-and-its-related-api-set"></a><span data-ttu-id="fd60c-127">Présentation des programmes par défaut et de l’ensemble des API associées</span><span class="sxs-lookup"><span data-stu-id="fd60c-127">Introduction to Default Programs and Its Related API Set</span></span>

<span data-ttu-id="fd60c-128">Les **programmes par défaut** sont principalement conçus pour les applications qui utilisent des types de fichiers standard, tels que des fichiers. mp3 ou. jpg ou des protocoles standard, tels que http ou mailto.</span><span class="sxs-lookup"><span data-stu-id="fd60c-128">**Default Programs** is primarily designed for applications that use standard file types such as .mp3 or .jpg files or standard protocols, such as HTTP or mailto.</span></span> <span data-ttu-id="fd60c-129">Les applications qui utilisent leurs propres protocoles et associations de fichiers propriétaires n’utilisent généralement pas les fonctionnalités des **programmes par défaut** .</span><span class="sxs-lookup"><span data-stu-id="fd60c-129">Applications that use their own proprietary protocols and file associations do not typically use the **Default Programs** functionality.</span></span>

<span data-ttu-id="fd60c-130">Une fois que vous avez inscrit une application pour la fonctionnalité **programmes par défaut** , les options et fonctionnalités suivantes sont disponibles à l’aide de l’API Set :</span><span class="sxs-lookup"><span data-stu-id="fd60c-130">After you register an application for **Default Programs** functionality, the following options and functionality are available by using the API set:</span></span>

-   <span data-ttu-id="fd60c-131">Restaure toutes les valeurs par défaut enregistrées pour une application.</span><span class="sxs-lookup"><span data-stu-id="fd60c-131">Restore all registered defaults for an application.</span></span> <span data-ttu-id="fd60c-132">Déconseillé pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fd60c-132">Deprecated for Windows 8.</span></span>
-   <span data-ttu-id="fd60c-133">Restaure une valeur par défaut enregistrée pour une application.</span><span class="sxs-lookup"><span data-stu-id="fd60c-133">Restore a single registered default for an application.</span></span> <span data-ttu-id="fd60c-134">Déconseillé pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fd60c-134">Deprecated for Windows 8.</span></span>
-   <span data-ttu-id="fd60c-135">Interrogez le propriétaire d’une valeur par défaut spécifique dans un appel unique au lieu de rechercher dans le registre.</span><span class="sxs-lookup"><span data-stu-id="fd60c-135">Query for the owner of a specific default in a single call instead of searching the registry.</span></span> <span data-ttu-id="fd60c-136">Vous pouvez rechercher la valeur par défaut d’une association de fichier, d’un protocole ou d’un verbe canonique du menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="fd60c-136">You can query for the default of a file association, protocol, or **Start** menu canonical verb.</span></span>
-   <span data-ttu-id="fd60c-137">Lancer une interface utilisateur pour une application spécifique où un utilisateur peut définir des valeurs par défaut individuelles.</span><span class="sxs-lookup"><span data-stu-id="fd60c-137">Launch a UI for a specific application where a user can set individual defaults.</span></span>
-   <span data-ttu-id="fd60c-138">Supprimer toutes les associations par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd60c-138">Remove all per-user associations.</span></span>

<span data-ttu-id="fd60c-139">Les **programmes par défaut** fournissent également une interface utilisateur qui vous permet d’inscrire une application afin de fournir des informations supplémentaires à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd60c-139">**Default Programs** also provides a UI that enables you to register an application in order to provide additional information to the user.</span></span> <span data-ttu-id="fd60c-140">Par exemple, une application signée numériquement peut inclure une URL vers la page d’hébergement du fabricant.</span><span class="sxs-lookup"><span data-stu-id="fd60c-140">For example, a digitally signed application can include a URL to the manufacturer's home page.</span></span>

<span data-ttu-id="fd60c-141">L’utilisation de l’ensemble d’API associé peut permettre à une application de fonctionner correctement sous la fonctionnalité de contrôle de compte d’utilisateur (UAC) introduite dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fd60c-141">Use of the associated API set can help an application function correctly under the user account control (UAC) feature introduced in Windows Vista.</span></span> <span data-ttu-id="fd60c-142">Sous UAC, un administrateur apparaît comme utilisateur standard dans le système, afin que l’administrateur ne puisse généralement pas écrire dans la sous-arborescence de l' **\_ \_ ordinateur local HKEY** .</span><span class="sxs-lookup"><span data-stu-id="fd60c-142">Under UAC, an administrator appears to the system as a standard user, so that administrator cannot typically write to the **HKEY\_LOCAL\_MACHINE** subtree.</span></span> <span data-ttu-id="fd60c-143">Cette restriction est une fonctionnalité de sécurité qui empêche un processus d’agir en tant qu’administrateur sans la connaissance de l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="fd60c-143">This restriction is a security feature that prevents a process from acting as an administrator without the administrator's knowledge.</span></span>

<span data-ttu-id="fd60c-144">L’installation d’un programme par un utilisateur s’effectue généralement sous la forme d’un processus élevé.</span><span class="sxs-lookup"><span data-stu-id="fd60c-144">Installation of a program by a user is typically performed as an elevated process.</span></span> <span data-ttu-id="fd60c-145">Toutefois, les tentatives effectuées par une application pour modifier les comportements d’association par défaut au niveau de l’ordinateur après l’installation seront infructueuses.</span><span class="sxs-lookup"><span data-stu-id="fd60c-145">However, attempts by an application to modify default association behaviors at a machine level post-installation will be unsuccessful.</span></span> <span data-ttu-id="fd60c-146">Au lieu de cela, les valeurs par défaut doivent être inscrites sur un niveau par utilisateur, ce qui empêche plusieurs utilisateurs de remplacer les valeurs par défaut des autres.</span><span class="sxs-lookup"><span data-stu-id="fd60c-146">Instead, defaults must be registered on a per-user level, which prevents multiple users from overwriting each other's defaults.</span></span>

<span data-ttu-id="fd60c-147">La structure hiérarchique du Registre pour les associations de fichiers et de protocoles donne la priorité aux valeurs par défaut par utilisateur par rapport aux valeurs par défaut au niveau de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fd60c-147">The hierarchical registry structure for file and protocol associations gives precedence to per-user defaults over machine-level defaults.</span></span> <span data-ttu-id="fd60c-148">Certaines applications incluent des points dans leur code qui élèvent temporairement leurs droits lorsqu’ils revendiquent les valeurs par défaut inscrites dans **HKEY \_ local \_ machine**.</span><span class="sxs-lookup"><span data-stu-id="fd60c-148">Some applications include points in their code that temporarily elevate their rights when they claim defaults registered in **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="fd60c-149">Ces applications peuvent présenter des résultats inattendus si une autre application est déjà inscrite en tant que valeur par défaut par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd60c-149">These applications might experience unexpected results if another application is already registered as the per-user default.</span></span> <span data-ttu-id="fd60c-150">L’utilisation de **programmes par défaut** empêche cette ambiguïté et garantit des résultats attendus pour chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd60c-150">Use of **Default Programs** prevents this ambiguity and guarantees expected results on a per-user level.</span></span>

## <a name="registering-an-application-for-use-with-default-programs"></a><span data-ttu-id="fd60c-151">Inscription d’une application pour une utilisation avec les programmes par défaut</span><span class="sxs-lookup"><span data-stu-id="fd60c-151">Registering an Application for Use with Default Programs</span></span>

<span data-ttu-id="fd60c-152">Cette section présente les sous-clés et les valeurs de Registre nécessaires pour inscrire une application avec des **programmes par défaut**.</span><span class="sxs-lookup"><span data-stu-id="fd60c-152">This section shows you the registry subkeys and values needed to register an application with **Default Programs**.</span></span> <span data-ttu-id="fd60c-153">Elle contient un exemple complet.</span><span class="sxs-lookup"><span data-stu-id="fd60c-153">It includes a full example.</span></span>

<span data-ttu-id="fd60c-154">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="fd60c-154">This section contains the following topics:</span></span>

-   [<span data-ttu-id="fd60c-155">ProgID</span><span class="sxs-lookup"><span data-stu-id="fd60c-155">ProgIDs</span></span>](#progids)
-   [<span data-ttu-id="fd60c-156">Sous-clé d’inscription et descriptions de valeur</span><span class="sxs-lookup"><span data-stu-id="fd60c-156">Registration Subkey and Value Descriptions</span></span>](#registration-subkey-and-value-descriptions)
-   [<span data-ttu-id="fd60c-157">RegisteredApplications</span><span class="sxs-lookup"><span data-stu-id="fd60c-157">RegisteredApplications</span></span>](#registeredapplications)
-   [<span data-ttu-id="fd60c-158">Exemple d’inscription complète</span><span class="sxs-lookup"><span data-stu-id="fd60c-158">Full Registration Example</span></span>](#full-registration-example)

<span data-ttu-id="fd60c-159">Les **programmes par défaut** requièrent que chaque application enregistre explicitement les associations de fichiers, les associations MIME et les protocoles pour lesquels l’application doit être listée comme une valeur par défaut possible.</span><span class="sxs-lookup"><span data-stu-id="fd60c-159">**Default Programs** requires each application to register explicitly the file associations, MIME associations, and protocols for which the application should be listed as a possible default.</span></span> <span data-ttu-id="fd60c-160">Vous inscrivez les associations à l’aide des éléments de registre suivants, qui sont expliqués en détail plus loin dans cette rubrique, sous la sous [-clé d’inscription et les descriptions de valeurs](#registration-subkey-and-value-descriptions):</span><span class="sxs-lookup"><span data-stu-id="fd60c-160">You register the associations by using the following registry elements, which are explained in detail later in this topic under [Registration Subkey and Value Descriptions](#registration-subkey-and-value-descriptions):</span></span>

```
HKEY_LOCAL_MACHINE
   %ApplicationCapabilityPath%
      ApplicationDescription
      ApplicationName
      Hidden
      FileAssociations
         .file-extension1
         .file-extension2
         ...
         .file-extensionX
      MIMEAssociations
         MIME
      Startmenu
         StartmenuInternet
         Mail
      UrlAssociations
         url-scheme
   SOFTWARE
      RegisteredApplications
         Unique Application Name = %ApplicationCapabilityPath%
```

<span data-ttu-id="fd60c-161">L’exemple suivant montre les entrées de Registre pour un navigateur contoso fictif appelé WebBrowser :</span><span class="sxs-lookup"><span data-stu-id="fd60c-161">The following example shows the registry entries for a fictional Contoso browser that is called WebBrowser:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Contoso
         WebBrowser
            Capabilities
               ApplicationDescription = This award-winning Contoso browser is better than ever. Search the Internet and find exactly what you want in just seconds. Use integrated tabs and new phishing detectors to enhance your Internet experience.
               FileAssociations
                  .htm = ContosoHTML
                  .html = ContosoHTML
                  .shtml = ContosoHTML
                  .xht = ContosoHTML
                  .xhtml = ContosoHTML
               Startmenu
                  StartmenuInternet = Contoso.exe
               UrlAssociations
                  http = Contoso.Url.Http
                  https = Contoso.Url.Https
                  ftp = Contoso.Url.ftp
   SOFTWARE
      RegisteredApplications
         Contoso.WebBrowser.1.06 = SOFTWARE\Contoso\WebBrowser\Capabilities
```

### <a name="progids"></a><span data-ttu-id="fd60c-162">ProgID</span><span class="sxs-lookup"><span data-stu-id="fd60c-162">ProgIDs</span></span>

<span data-ttu-id="fd60c-163">Une application doit fournir un [ProgID](fa-progids.md)spécifique.</span><span class="sxs-lookup"><span data-stu-id="fd60c-163">An application must provide a specific [ProgID](fa-progids.md).</span></span> <span data-ttu-id="fd60c-164">Veillez à inclure toutes les informations qui sont généralement écrites dans la sous-clé générique par défaut pour l’extension.</span><span class="sxs-lookup"><span data-stu-id="fd60c-164">Be sure to include all the information that is typically written into the generic default subkey for the extension.</span></span> <span data-ttu-id="fd60c-165">Par exemple, le lecteur multimédia fiction Litware fournit la sous-clé de laLitwarePlayer11.AssocFile.MP3de classes de logiciels **HKEY \_ local \_ machine** propre à l’application \\  \\  \\ \*\*\*\* .</span><span class="sxs-lookup"><span data-stu-id="fd60c-165">For example, the fictional Litware media player provides the application-specific **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Classes**\\**LitwarePlayer11.AssocFile.MP3** subkey.</span></span> <span data-ttu-id="fd60c-166">Cette sous-clé contient toutes les informations de la sous-clé par défaut générique **HKEY \_ local \_ machine** \\ **Software** \\ **classes** \\ **. mp3** , ainsi que toutes les informations supplémentaires que l’application doit inscrire.</span><span class="sxs-lookup"><span data-stu-id="fd60c-166">That subkey includes all the information in the generic default subkey **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Classes**\\ **.mp3** plus any additional information that you want the application to register.</span></span> <span data-ttu-id="fd60c-167">Cela garantit que si l’utilisateur restaure l’Association. mp3 dans Litware Player, les informations de Litware Player sont intactes et n’ont pas été remplacées par une autre application.</span><span class="sxs-lookup"><span data-stu-id="fd60c-167">This ensures that if the user restores the .mp3 association to the Litware player, the Litware player's information is intact and has not been overwritten by another application.</span></span> <span data-ttu-id="fd60c-168">(Le remplacement peut se produire si la sous-clé par défaut est la seule source de ces informations.)</span><span class="sxs-lookup"><span data-stu-id="fd60c-168">(Overwriting might occur if the default subkey is the only source of that information.)</span></span>

<span data-ttu-id="fd60c-169">Lorsque vous mappez un ProgID à un protocole ou une extension de nom de fichier, une application peut mapper un-à-un ou un-à-plusieurs.</span><span class="sxs-lookup"><span data-stu-id="fd60c-169">When you map a ProgID to a file name extension or protocol, an application can map one-to-one or one-to-many.</span></span> <span data-ttu-id="fd60c-170">Dans l’exemple Contoso, ContosoHTML pointe vers un ProgID unique qui fournit des informations ShellExecute pour les extensions. htm,. html,. shtml,. XHT et. XHTML.</span><span class="sxs-lookup"><span data-stu-id="fd60c-170">In the Contoso example, ContosoHTML points to a single ProgID that provides shellexecute information for the .htm, .html, .shtml, .xht, and .xhtml extensions.</span></span> <span data-ttu-id="fd60c-171">Comme il existe un ProgID différent pour chaque protocole, lorsque vous utilisez des protocoles, vous permettez à chaque protocole d’avoir sa propre chaîne d’exécution.</span><span class="sxs-lookup"><span data-stu-id="fd60c-171">Because a different ProgID exists for each protocol, when you use protocols you enable each protocol to have its own execution string.</span></span>

<span data-ttu-id="fd60c-172">Lorsque votre type MIME peut être affiché inline dans un navigateur, le ProgID du type MIME doit contenir la sous-clé **CLSID** qui utilise l’identificateur de classe (CLSID) de l’application correspondante.</span><span class="sxs-lookup"><span data-stu-id="fd60c-172">When your MIME type can be viewed inline in a browser, the ProgID for the MIME type must contain the **CLSID** subkey that uses the class identifier (CLSID) of the corresponding application.</span></span> <span data-ttu-id="fd60c-173">Ce CLSID est utilisé dans une recherche par rapport au CLSID dans la base de données MIME qui est stockée dans le **\_ \_** \\  \\  \\  \\ type **de contenu de la base de données de la base de données MIME de** la classe de \\ l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="fd60c-173">This CLSID is used in a lookup against the CLSID in the MIME database that is stored in **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Classes**\\**MIME**\\**Database**\\**Content Type**.</span></span> <span data-ttu-id="fd60c-174">Si votre type MIME n’est pas destiné à être affiché inline dans un navigateur, cette étape peut être omise.</span><span class="sxs-lookup"><span data-stu-id="fd60c-174">If your MIME type is not intended to be viewed inline in a browser, this step can be omitted.</span></span>

### <a name="registration-subkey-and-value-descriptions"></a><span data-ttu-id="fd60c-175">Sous-clé d’inscription et descriptions de valeur</span><span class="sxs-lookup"><span data-stu-id="fd60c-175">Registration Subkey and Value Descriptions</span></span>

<span data-ttu-id="fd60c-176">Cette section décrit les sous-clés et les valeurs de Registre individuelles utilisées pour l’inscription d’une application avec les **programmes par défaut**, comme illustré précédemment.</span><span class="sxs-lookup"><span data-stu-id="fd60c-176">This section describes the individual registry subkeys and values used in registering an application with **Default Programs**, as illustrated previously.</span></span>

### <a name="capabilities"></a><span data-ttu-id="fd60c-177">Fonctions</span><span class="sxs-lookup"><span data-stu-id="fd60c-177">Capabilities</span></span>

<span data-ttu-id="fd60c-178">La sous-clé **Capabilities** contient toutes les informations sur les **programmes par défaut** pour une application spécifique.</span><span class="sxs-lookup"><span data-stu-id="fd60c-178">The **Capabilities** subkey contains all the **Default Programs** information for a specific application.</span></span> <span data-ttu-id="fd60c-179">L’espace réservé% ApplicationCapabilityPath% fait référence au chemin d’accès du registre de **HKEY \_ Current \_ User** ou **HKEY \_ local \_ machine** à la sous-clé **Capabilities** de l’application.</span><span class="sxs-lookup"><span data-stu-id="fd60c-179">The placeholder %ApplicationCapabilityPath% refers to the registry path from either **HKEY\_CURRENT\_USER** or **HKEY\_LOCAL\_MACHINE** to the application's **Capabilities** subkey.</span></span> <span data-ttu-id="fd60c-180">Cette sous-clé contient les valeurs significatives indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fd60c-180">This subkey contains the significant values shown in the following table.</span></span>



| <span data-ttu-id="fd60c-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd60c-181">Value</span></span>                  | <span data-ttu-id="fd60c-182">Type</span><span class="sxs-lookup"><span data-stu-id="fd60c-182">Type</span></span>                       | <span data-ttu-id="fd60c-183">Signification</span><span class="sxs-lookup"><span data-stu-id="fd60c-183">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd60c-184">ApplicationDescription</span><span class="sxs-lookup"><span data-stu-id="fd60c-184">ApplicationDescription</span></span> | <span data-ttu-id="fd60c-185">REG \_ SZ ou reg \_ développé \_ SZ</span><span class="sxs-lookup"><span data-stu-id="fd60c-185">REG\_SZ or REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="fd60c-186">**Requis**.</span><span class="sxs-lookup"><span data-stu-id="fd60c-186">**Required**.</span></span> <span data-ttu-id="fd60c-187">Pour permettre à un utilisateur d’effectuer un choix d’affectation par défaut informé, une application doit fournir une chaîne décrivant les fonctionnalités de l’application.</span><span class="sxs-lookup"><span data-stu-id="fd60c-187">To enable a user to make an informed default assignment choice, an application must provide a string that describes the application's capabilities.</span></span> <span data-ttu-id="fd60c-188">Bien que l’exemple Contoso précédent affecte la description directement à la valeur ApplicationDescription, les applications fournissent généralement la description en tant que ressource incorporée dans un fichier. dll pour faciliter la localisation.</span><span class="sxs-lookup"><span data-stu-id="fd60c-188">Although the previous Contoso example assigns the description directly to the ApplicationDescription value, applications typically provide the description as a resource that is embedded in a .dll file to facilitate localization.</span></span> <span data-ttu-id="fd60c-189">Si ApplicationDescription n’est pas fourni, l’application n’apparaît pas dans les listes d’interface utilisateur des programmes potentiels par défaut.</span><span class="sxs-lookup"><span data-stu-id="fd60c-189">If ApplicationDescription is not provided, the application does not appear in UI lists of potential default programs.</span></span>                                                            |
| <span data-ttu-id="fd60c-190">ApplicationName</span><span class="sxs-lookup"><span data-stu-id="fd60c-190">ApplicationName</span></span>        | <span data-ttu-id="fd60c-191">REG \_ SZ ou reg \_ développé \_ SZ</span><span class="sxs-lookup"><span data-stu-id="fd60c-191">REG\_SZ or REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="fd60c-192">**Facultatif.**</span><span class="sxs-lookup"><span data-stu-id="fd60c-192">**Optional.**</span></span> <span data-ttu-id="fd60c-193">Nom sous lequel le programme apparaît dans l’interface utilisateur des programmes par défaut.</span><span class="sxs-lookup"><span data-stu-id="fd60c-193">The name by which the program appears in the Default Programs UI.</span></span> <span data-ttu-id="fd60c-194">Si ces données ne sont pas fournies par l’application, le nom du programme exécutable associé au premier ProgID enregistré pour l’application est utilisé dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd60c-194">If this data is not provided by the application, the name of the executable program that is associated with the first registered ProgID for the application is used in the UI.</span></span> <span data-ttu-id="fd60c-195">ApplicationName doit toujours correspondre au nom enregistré sous [RegisteredApplications](#registeredapplications).</span><span class="sxs-lookup"><span data-stu-id="fd60c-195">ApplicationName must always match the name that is registered under [RegisteredApplications](#registeredapplications).</span></span> <span data-ttu-id="fd60c-196">Vous pouvez utiliser ApplicationName si vous souhaitez que différents types d’application, tels qu’un navigateur et un client de messagerie, pointent vers le même fichier exécutable lorsqu’ils apparaissent sous la forme de noms différents.</span><span class="sxs-lookup"><span data-stu-id="fd60c-196">You can use ApplicationName if you want different application types, such as a browser and an email client, to point to the same executable file while they appear as different names.</span></span><br/> |
| <span data-ttu-id="fd60c-197">Hidden</span><span class="sxs-lookup"><span data-stu-id="fd60c-197">Hidden</span></span>                 | <span data-ttu-id="fd60c-198">\_valeur DWORD reg</span><span class="sxs-lookup"><span data-stu-id="fd60c-198">REG\_DWORD</span></span>                 | <span data-ttu-id="fd60c-199">**Facultatif.**</span><span class="sxs-lookup"><span data-stu-id="fd60c-199">**Optional.**</span></span> <span data-ttu-id="fd60c-200">Définissez cette valeur sur 1 pour supprimer l’application de la liste des programmes dans la boîte de dialogue **définir vos programmes par défaut** .</span><span class="sxs-lookup"><span data-stu-id="fd60c-200">Set this value to 1 to suppress the application from the list of programs in the **Set your default programs** dialog.</span></span> <span data-ttu-id="fd60c-201">Si cette valeur est égale à 0 ou absente, l’application s’affiche normalement dans la liste.</span><span class="sxs-lookup"><span data-stu-id="fd60c-201">If this value is 0 or not present, then the application appears in the list normally.</span></span>                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="fileassociations"></a><span data-ttu-id="fd60c-202">FileAssociations</span><span class="sxs-lookup"><span data-stu-id="fd60c-202">FileAssociations</span></span>

<span data-ttu-id="fd60c-203">La sous-clé **FileAssociations** contient des associations de fichiers spécifiques revendiquées par l’application.</span><span class="sxs-lookup"><span data-stu-id="fd60c-203">The **FileAssociations** subkey contains specific file associations that are claimed by the application.</span></span> <span data-ttu-id="fd60c-204">Ces revendications sont stockées en tant que valeurs, avec une valeur pour chaque extension.</span><span class="sxs-lookup"><span data-stu-id="fd60c-204">These claims are stored as values, with one value for each extension.</span></span> <span data-ttu-id="fd60c-205">Les associations pointent vers un ProgID spécifique à l’application au lieu d’un ProgID générique.</span><span class="sxs-lookup"><span data-stu-id="fd60c-205">Associations point to an application-specific ProgID instead of a generic ProgID.</span></span> <span data-ttu-id="fd60c-206">Toutefois, il n’est pas nécessaire que toutes les associations pointent vers le même ProgID.</span><span class="sxs-lookup"><span data-stu-id="fd60c-206">However, all associations are not required to point to the same ProgID.</span></span>

### <a name="mimeassociations"></a><span data-ttu-id="fd60c-207">MIMEAssociations</span><span class="sxs-lookup"><span data-stu-id="fd60c-207">MIMEAssociations</span></span>

<span data-ttu-id="fd60c-208">La sous-clé **MIMEAssociations** contient des types MIME spécifiques revendiqués par l’application.</span><span class="sxs-lookup"><span data-stu-id="fd60c-208">The **MIMEAssociations** subkey contains specific MIME types that are claimed by the application.</span></span> <span data-ttu-id="fd60c-209">Ces revendications sont stockées en tant que valeurs, avec une valeur pour chaque type MIME.</span><span class="sxs-lookup"><span data-stu-id="fd60c-209">These claims are stored as values, with one value for each MIME type.</span></span> <span data-ttu-id="fd60c-210">Le nom de la valeur de chaque type MIME doit correspondre exactement au nom MIME stocké dans la base de données MIME.</span><span class="sxs-lookup"><span data-stu-id="fd60c-210">The value name for each MIME type must exactly match the MIME name that is stored in the MIME database.</span></span> <span data-ttu-id="fd60c-211">La valeur doit également être assignée à un ProgID spécifique à l’application qui contient le CLSID correspondant de l’application.</span><span class="sxs-lookup"><span data-stu-id="fd60c-211">The value must also be assigned an application-specific ProgID that contains the corresponding CLSID of the application.</span></span>

### <a name="startmenu"></a><span data-ttu-id="fd60c-212">Restauré</span><span class="sxs-lookup"><span data-stu-id="fd60c-212">Startmenu</span></span>

<span data-ttu-id="fd60c-213">La sous-clé **restauré** est associée à l’adresse **Internet** et aux entrées de **courrier électronique** attribuables par l’utilisateur dans le menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="fd60c-213">The **Startmenu** subkey is associated with the user-assignable **Internet** and **E-mail** entries in the **Start** menu.</span></span> <span data-ttu-id="fd60c-214">Une application doit s’inscrire séparément en tant que contendeur pour ces entrées.</span><span class="sxs-lookup"><span data-stu-id="fd60c-214">An application must register separately as a contender for those entries.</span></span> <span data-ttu-id="fd60c-215">Pour plus d’informations, consultez [inscription de programmes avec des types de clients](reg-middleware-apps.md).</span><span class="sxs-lookup"><span data-stu-id="fd60c-215">For more information, see [Registering Programs with Client Types](reg-middleware-apps.md).</span></span>

> [!Note]  
> <span data-ttu-id="fd60c-216">À compter de Windows 7, il n’y a plus d’entrées **Internet** et de **messagerie électronique** dans le menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="fd60c-216">As of Windows 7, there are no longer **Internet** and **E-mail** entries in the **Start** menu.</span></span> <span data-ttu-id="fd60c-217">Les données de Registre associées à l’entrée de **courrier électronique** sont toujours utilisées pour le client MAPI par défaut, mais les données de Registre associées à l’entrée **Internet** ne sont pas utilisées par Windows.</span><span class="sxs-lookup"><span data-stu-id="fd60c-217">The registry data associated with the **E-mail** entry is still used for the default MAPI client, but the registry data associated with the **Internet** entry is not used by Windows at all.</span></span>

 

<span data-ttu-id="fd60c-218">En associant l’inscription du menu **Démarrer** à une application avec son inscription de **programmes par défaut** , l’application apparaît comme une valeur par défaut potentielle dans l’interface utilisateur **définir les associations** .</span><span class="sxs-lookup"><span data-stu-id="fd60c-218">By associating the **Start** menu registration of an application with its **Default Programs** registration, the application appears as a potential default in the **Set associations** UI.</span></span> <span data-ttu-id="fd60c-219">Si l’utilisateur a choisi l’application comme valeur par défaut, puis choisit de restaurer toutes les valeurs par défaut de l’application ultérieurement, l’application est restaurée à sa position de menu **Démarrer** pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd60c-219">If the user has chosen the application as the default and then chooses to restore all application defaults later, the application is restored to its **Start** menu position for that user.</span></span> <span data-ttu-id="fd60c-220">Pour plus d’informations et une illustration, consultez la section de l' [interface utilisateur des programmes par défaut](#default-programs-ui) plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="fd60c-220">For more information and an illustration, see the [Default Programs UI](#default-programs-ui) section later in this topic.</span></span>

<span data-ttu-id="fd60c-221">La sous-clé **restauré** comporte deux entrées : StartMenuInternet et mail, qui correspondent aux positions canoniques de **messagerie** et **Internet** dans le menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="fd60c-221">The **Startmenu** subkey has two entries: StartMenuInternet and Mail, which correspond to the canonical **Internet** and **E-mail** positions in the **Start** menu.</span></span> <span data-ttu-id="fd60c-222">Une application affecte StartMenuInternet ou mail une valeur égale au nom de la sous-clé inscrite de l’application sous **HKEY \_ local \_ machine** \\ **Software** \\ **clients** \\ **StartMenuInternet** ou **HKEY \_ local \_ machine** \\ **Software** \\ **clients** \\ **mail** (comme décrit dans [inscription de programmes avec des types de client](reg-middleware-apps.md)).</span><span class="sxs-lookup"><span data-stu-id="fd60c-222">An application assigns either StartMenuInternet or Mail a value equal to the name of the application's registered subkey under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** or **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** (as described in [Registering Programs with Client Types](reg-middleware-apps.md)).</span></span>

<span data-ttu-id="fd60c-223">Dans le cas de la position canonique par **courrier électronique** dans le menu **Démarrer** , elle représente le client MAPI par défaut et est donc supposée être en mesure de transmettre des appels MAPI.</span><span class="sxs-lookup"><span data-stu-id="fd60c-223">In the case of the **E-mail** canonical position in the **Start** menu, it represents the default MAPI client and is therefore assumed capable of handing MAPI calls.</span></span> <span data-ttu-id="fd60c-224">Sous Windows 7, bien qu’il n’y ait plus de position canonique par **courrier électronique** dans le menu **Démarrer** , cette sous-clé continue à être utilisée pour le client MAPI par défaut.</span><span class="sxs-lookup"><span data-stu-id="fd60c-224">Under Windows 7, while there is no longer an **E-mail** canonical position in the **Start** menu, this subkey continues to be used for the default MAPI client.</span></span> <span data-ttu-id="fd60c-225">Une application revendiquant la valeur par défaut du courrier doit s’inscrire en tant que gestionnaire MAPI sous la sous-clé suivante :</span><span class="sxs-lookup"><span data-stu-id="fd60c-225">An application claiming the mail default should register as a MAPI handler under the following subkey:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
```

<span data-ttu-id="fd60c-226">Si un client de messagerie ne peut pas prendre en charge MAPI mais souhaite toujours faire face à la position canonique de **messagerie** du menu **Démarrer** , il peut inscrire une ligne de commande sous la sous-clé suivante :</span><span class="sxs-lookup"><span data-stu-id="fd60c-226">If a mail client cannot support MAPI but still wants to contend for the **Start** menu **E-mail** canonical position, it can register a command line under the following subkey:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            CanonicalName
               shell
                  open
                     command
```

<span data-ttu-id="fd60c-227">En outre, sous **HKEY \_ local \_ machine** \\ **Software** \\ **clients** \\ **mail** \\ *CanonicalName* , ajoutez une valeur par défaut avec le nom de l’application.</span><span class="sxs-lookup"><span data-stu-id="fd60c-227">Also, under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail**\\*CanonicalName* add a default value with the application name.</span></span>

<span data-ttu-id="fd60c-228">Ces entrées permettent à l’application d’être lancée à partir de la position du **message électronique** du menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="fd60c-228">These entries allow the application to be launched from the **Start** menu's **E-mail** position.</span></span> <span data-ttu-id="fd60c-229">Notez que les appels MAPI sont toujours effectués à l’application et passent par le gestionnaire MAPI précédent, ou échouent si aucun gestionnaire MAPI n’a été défini.</span><span class="sxs-lookup"><span data-stu-id="fd60c-229">Note that MAPI calls are still made to the application, and either fall through to the prior MAPI handler, or fail if no MAPI handler has been set.</span></span> <span data-ttu-id="fd60c-230">Pour plus d’informations, consultez [inscription de programmes avec des types de clients](reg-middleware-apps.md).</span><span class="sxs-lookup"><span data-stu-id="fd60c-230">For more information, see [Registering Programs with Client Types](reg-middleware-apps.md).</span></span>

### <a name="urlassociations"></a><span data-ttu-id="fd60c-231">UrlAssociations</span><span class="sxs-lookup"><span data-stu-id="fd60c-231">UrlAssociations</span></span>

<span data-ttu-id="fd60c-232">La sous-clé **UrlAssociations** contient les protocoles d’URL spécifiques revendiqués par l’application.</span><span class="sxs-lookup"><span data-stu-id="fd60c-232">The **UrlAssociations** subkey contains the specific URL protocols that are claimed by the application.</span></span> <span data-ttu-id="fd60c-233">Ces revendications sont stockées en tant que valeurs, avec une valeur pour chaque protocole.</span><span class="sxs-lookup"><span data-stu-id="fd60c-233">These claims are stored as values, with one value for each protocol.</span></span> <span data-ttu-id="fd60c-234">Chaque protocole doit pointer vers un ProgID spécifique à l’application et non vers un ProgID générique.</span><span class="sxs-lookup"><span data-stu-id="fd60c-234">Each protocol must point to an application-specific ProgID instead of to a generic ProgID.</span></span> <span data-ttu-id="fd60c-235">Comme mentionné dans l’exemple de contoso, vous pouvez utiliser un ProgID différent pour chaque protocole afin que chacun ait sa propre chaîne d’exécution.</span><span class="sxs-lookup"><span data-stu-id="fd60c-235">As mentioned in the Contoso example, you can use a different ProgID for each protocol in order for each to have its own execution string.</span></span>

### <a name="registeredapplications"></a><span data-ttu-id="fd60c-236">RegisteredApplications</span><span class="sxs-lookup"><span data-stu-id="fd60c-236">RegisteredApplications</span></span>

<span data-ttu-id="fd60c-237">La sous-clé complète de **RegisteredApplications** est :</span><span class="sxs-lookup"><span data-stu-id="fd60c-237">The full subkey for **RegisteredApplications** is:</span></span>

<span data-ttu-id="fd60c-238">**HKEY \_ \_** \\  \\ **RegisteredApplications** logiciel de l’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="fd60c-238">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**RegisteredApplications**</span></span>

<span data-ttu-id="fd60c-239">Cette sous-clé fournit au système d’exploitation l’emplacement du registre des informations sur les **programmes par défaut** de l’application.</span><span class="sxs-lookup"><span data-stu-id="fd60c-239">This subkey provides the operating system with the registry location of the **Default Programs** information for the application.</span></span> <span data-ttu-id="fd60c-240">L’emplacement est stocké sous la forme d’une valeur dont le nom doit correspondre au nom de l’application.</span><span class="sxs-lookup"><span data-stu-id="fd60c-240">The location is stored as a value whose name must match the name of the application.</span></span>

### <a name="full-registration-example"></a><span data-ttu-id="fd60c-241">Exemple d’inscription complète</span><span class="sxs-lookup"><span data-stu-id="fd60c-241">Full Registration Example</span></span>

<span data-ttu-id="fd60c-242">Cet exemple montre les sous-clés et les valeurs utilisées lors de l’inscription du lecteur multimédia Litware-fiction.</span><span class="sxs-lookup"><span data-stu-id="fd60c-242">This example shows the subkeys and values that are used in registering the fictional Litware media player.</span></span> <span data-ttu-id="fd60c-243">L’exemple comprend les entrées ProgID afin d’illustrer la façon dont elles s’ajustent.</span><span class="sxs-lookup"><span data-stu-id="fd60c-243">The example includes the ProgID entries in order to show how it all fits together.</span></span>

<span data-ttu-id="fd60c-244">La sous-clé suivante montre le ProgID spécifique à l’application pour le type MIME. mp3 :</span><span class="sxs-lookup"><span data-stu-id="fd60c-244">The following subkey shows the application-specific ProgID for the .mp3 MIME type:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.MIME.MP3
            CLSID
               (Default) = {CD3AFA76-B84F-48F0-9393-7EDC34128127}
```

<span data-ttu-id="fd60c-245">Ensuite, il s’agit du ProgID propre à l’application qui associe le programme Litware à l’extension de nom de fichier. mp3.</span><span class="sxs-lookup"><span data-stu-id="fd60c-245">Next is the application-specific ProgID that associates the Litware program with the .mp3 file name extension.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MP3
            (Default) = MP3 Format Sound
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

<span data-ttu-id="fd60c-246">Les entrées suivantes affichent le ProgID combiné pour le type MIME. MPEG et l’extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd60c-246">The next entries show the combined ProgID for both the .mpeg MIME type and file name extension.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         LitwarePlayer11.AssocFile.MPG
            (Default) = Movie Clip
            CLSID
               (Default) = {D92B76F4-CFA0-4b93-866B-7730FEB4CD7B}
            DefaultIcon
               (Default) = %ProgramFiles%\Litware\litware.dll, 0
            shell
               open
                  command
                     (Default) = %ProgramFiles%\Litware\litware.exe
```

<span data-ttu-id="fd60c-247">Les entrées suivantes inscrivent le programme Litware dans les **programmes par défaut** et utilisent les ProgID précédemment enregistrés</span><span class="sxs-lookup"><span data-stu-id="fd60c-247">The next entries register the Litware program in **Default Programs** and use the previously registered ProgIDs</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Litware
         LitwarePlayer
            Capabilities
               ApplicationDescription = The new Litware Media Player breaks new ground in exciting fictional programs.
               FileAssociations
                  .mp3 = LitwarePlayer11.AssocFile.MP3
                  .mpeg = LitwarePlayer11.AssocFile.MPG
               MimeAssociations
                  audio/mp3 = LitwarePlayer11.MIME.MP3
                  audio/mpeg = LitwarePlayer11.AssocFile.MPG
```

<span data-ttu-id="fd60c-248">Enfin, cet exemple inscrit l’emplacement de l’inscription des **programmes Litware par défaut** .</span><span class="sxs-lookup"><span data-stu-id="fd60c-248">Lastly, this example registers the location of the Litware **Default Programs** registration.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      RegisteredApplications
         Litware Player = Software\Litware\LitwarePlayer\Capabilities
```

## <a name="becoming-the-default-browser"></a><span data-ttu-id="fd60c-249">Devenir le navigateur par défaut</span><span class="sxs-lookup"><span data-stu-id="fd60c-249">Becoming the Default Browser</span></span>

<span data-ttu-id="fd60c-250">L’inscription du navigateur doit suivre les meilleures pratiques décrites dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="fd60c-250">Browser registration must follow the best practices outlined in this topic.</span></span> <span data-ttu-id="fd60c-251">Lorsque le navigateur est installé, Windows peut présenter à l’utilisateur une notification système par l’intermédiaire de laquelle l’utilisateur peut sélectionner le navigateur comme système par défaut.</span><span class="sxs-lookup"><span data-stu-id="fd60c-251">When the browser is installed, Windows can present the user with a system notification through which the user can select the browser as the system default.</span></span> <span data-ttu-id="fd60c-252">Cette notification s’affiche lorsque ces conditions sont remplies :</span><span class="sxs-lookup"><span data-stu-id="fd60c-252">This notification is shown when these conditions are met:</span></span>

-   <span data-ttu-id="fd60c-253">Le programme d’installation du navigateur appelle [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) à l’aide de l’indicateur **SHCNE \_ ASSOCCHANGED** pour indiquer à Windows que de nouveaux gestionnaires de protocole ont été inscrits.</span><span class="sxs-lookup"><span data-stu-id="fd60c-253">The browser's installer calls [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) with the **SHCNE\_ASSOCCHANGED** flag to tell Windows that new protocol handlers have been registered.</span></span>
-   <span data-ttu-id="fd60c-254">Windows détecte qu’une ou plusieurs nouvelles applications sont inscrites pour gérer à la fois les protocoles http://et https://, et l’utilisateur n’a pas encore été notifié.</span><span class="sxs-lookup"><span data-stu-id="fd60c-254">Windows detects that one or more new applications have registered to handle both http:// and https:// protocols, and the user has not yet been notified.</span></span> <span data-ttu-id="fd60c-255">En d’autres termes, aucun des éléments suivants n’a été présenté à l’utilisateur : une notification système publiant l’application, un menu volant OpenWith contenant l’application ou la page définir les paramètres par défaut des utilisateurs (SUD) de l’application.</span><span class="sxs-lookup"><span data-stu-id="fd60c-255">In other words, none of the following have been shown to the user: a system notification advertising the application, an OpenWith flyout that contains the application, or the Set User Defaults (SUD) Control Panel page for the application.</span></span>

<span data-ttu-id="fd60c-256">L’exemple suivant montre le code d’inscription recommandé que le programme d’installation du navigateur doit exécuter après avoir écrit ses clés de registre.</span><span class="sxs-lookup"><span data-stu-id="fd60c-256">The following example shows the recommended registration code that the browser's installer should run after it writes its registry keys.</span></span>

<span data-ttu-id="fd60c-257">[**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) informe tout d’abord le système que de nouveaux choix d’association sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="fd60c-257">[**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) first notifies the system that new association choices are available.</span></span> <span data-ttu-id="fd60c-258">L’appel **SHChangeNotify** est requis pour garantir le bon fonctionnement des paramètres système par défaut.</span><span class="sxs-lookup"><span data-stu-id="fd60c-258">The **SHChangeNotify** call is required to ensure the proper functioning of system defaults.</span></span>

<span data-ttu-id="fd60c-259">Une instruction [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) autorise ensuite les processus système à gérer la notification.</span><span class="sxs-lookup"><span data-stu-id="fd60c-259">A [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) statement then allows time for system processes to handle the notification.</span></span>


```C++
void NotifySystemOfNewRegistration()
{
    SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_DWORD | SHCNF_FLUSH, nullptr, nullptr);
    Sleep(1000);
}
```



<span data-ttu-id="fd60c-260">Si l’utilisateur ignore ou ignore la notification ou le menu volant qui en résulte sans effectuer de nouvelle sélection de navigateur par défaut, le navigateur par défaut reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="fd60c-260">If the user dismisses or ignores the resulting notification or flyout without making a new default browser selection, the default browser remains unchanged.</span></span> <span data-ttu-id="fd60c-261">Notez que l’utilisateur peut également modifier le navigateur par défaut à tout moment à l’aide d’autres mécanismes, y compris définir les paramètres par défaut de l’utilisateur dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="fd60c-261">Note that the user can also change the default browser at any time through other mechanisms, including Set User Defaults in the Control Panel.</span></span>

## <a name="default-programs-ui"></a><span data-ttu-id="fd60c-262">Interface utilisateur des programmes par défaut</span><span class="sxs-lookup"><span data-stu-id="fd60c-262">Default Programs UI</span></span>

<span data-ttu-id="fd60c-263">Les illustrations de cette section illustrent l’interface utilisateur des **programmes par défaut** , telle qu’elle est affichée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd60c-263">The illustrations in this section show the UI for **Default Programs** as seen by the user.</span></span>

<span data-ttu-id="fd60c-264">L’illustration suivante montre la fenêtre principale **programmes par défaut** du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="fd60c-264">The following illustration shows the main **Default Programs** window in Control Panel.</span></span>

![capture d’écran de la page d’entrée programmes par défaut](images/defaultprogramsmain.png)

<span data-ttu-id="fd60c-266">Quand un utilisateur choisit l’option **définir vos programmes par défaut** , la fenêtre suivante s’affiche.</span><span class="sxs-lookup"><span data-stu-id="fd60c-266">When a user chooses the **Set your default programs** option, the following window appears.</span></span> <span data-ttu-id="fd60c-267">Les utilisateurs peuvent utiliser cette page pour affecter un programme par défaut pour tous les types de fichiers et protocoles pour lesquels le programme est une option par défaut.</span><span class="sxs-lookup"><span data-stu-id="fd60c-267">Users can use this page to assign a default program for all file types and protocols for which the program is a possible default.</span></span> <span data-ttu-id="fd60c-268">Comme indiqué dans l’illustration suivante, tous les programmes [inscrits](#registering-an-application-for-use-with-default-programs) et l’icône de programme s’affichent dans la zone **programmes** sur la gauche.</span><span class="sxs-lookup"><span data-stu-id="fd60c-268">As shown in the following illustration, all [registered](#registering-an-application-for-use-with-default-programs) programs and the program icon appear in the **Programs** box on the left.</span></span>

![capture d’écran de la page définir vos programmes par défaut](images/setyourdefaultprograms.png)

<span data-ttu-id="fd60c-270">Lorsque l’utilisateur sélectionne un programme dans la liste, l’icône et le fournisseur du programme s’affichent.</span><span class="sxs-lookup"><span data-stu-id="fd60c-270">When the user selects a program from the list, the program icon and provider are displayed.</span></span> <span data-ttu-id="fd60c-271">Si l’URL est incorporée dans le certificat signé numériquement, le programme peut également afficher une URL.</span><span class="sxs-lookup"><span data-stu-id="fd60c-271">If the URL is embedded in the program's digitally signed certificate, the program can also display a URL.</span></span> <span data-ttu-id="fd60c-272">Les programmes qui ne sont pas signés numériquement ne peuvent pas afficher une URL.</span><span class="sxs-lookup"><span data-stu-id="fd60c-272">Programs that are not digitally signed cannot display a URL.</span></span>

<span data-ttu-id="fd60c-273">Le texte descriptif, qui est fourni par le programme lors de l’inscription, est également affiché.</span><span class="sxs-lookup"><span data-stu-id="fd60c-273">Descriptive text, which is supplied by the program during registration, is also displayed.</span></span> <span data-ttu-id="fd60c-274">Ce texte est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="fd60c-274">This text is required.</span></span> <span data-ttu-id="fd60c-275">Sous la zone Description, vous pouvez indiquer le nombre de valeurs par défaut actuellement affectées par le programme à partir du nombre complet qu’il est inscrit pour gérer.</span><span class="sxs-lookup"><span data-stu-id="fd60c-275">Beneath the description box is an indication of how many defaults the program is currently assigned out of the full number it is registered to handle.</span></span>

<span data-ttu-id="fd60c-276">Pour affecter ou restaurer un programme comme valeur par défaut pour tous les fichiers et protocoles pour lesquels il est inscrit, l’utilisateur clique sur l’option **définir ce programme comme programme par défaut** .</span><span class="sxs-lookup"><span data-stu-id="fd60c-276">To assign or restore a program as the default for all files and protocols for which it is registered, the user clicks the **Set this program as default** option.</span></span>

<span data-ttu-id="fd60c-277">Pour assigner des types de fichiers et des protocoles individuels à un programme, l’utilisateur clique sur l’option **choisir les paramètres par défaut pour ce programme** , qui affiche une fenêtre **définir les associations pour un programme** comme celle de l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="fd60c-277">To assign individual file types and protocols to a program, the user clicks the **Choose defaults for this program** option, which displays a **Set associations for a program** window like the one in the following illustration.</span></span>

> [!Note]  
> <span data-ttu-id="fd60c-278">Nous vous recommandons d’appeler les **associations Set pour un programme** à l’aide de [**IApplicationAssociationRegistrationUI :: LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui).</span><span class="sxs-lookup"><span data-stu-id="fd60c-278">We recommend you call the **Set associations for a program** by using [**IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui).</span></span>

 

![capture d’écran de la page définir les associations pour un programme](images/setassociationsforaprogram.png)

## <a name="best-practices-for-using-default-programs"></a><span data-ttu-id="fd60c-280">Meilleures pratiques pour l’utilisation des programmes par défaut</span><span class="sxs-lookup"><span data-stu-id="fd60c-280">Best Practices for Using Default Programs</span></span>

<span data-ttu-id="fd60c-281">Cette section présente les meilleures pratiques pour l’utilisation des **programmes par défaut** lorsque vous inscrivez des applications.</span><span class="sxs-lookup"><span data-stu-id="fd60c-281">This section provides best practice guidelines for using **Default Programs** when you register applications.</span></span> <span data-ttu-id="fd60c-282">Il offre également des suggestions de conception pour la création d’une application qui fournit aux utilisateurs des fonctionnalités optimales de **programmes par défaut** .</span><span class="sxs-lookup"><span data-stu-id="fd60c-282">It also offers design suggestions for creating an application that provides users with optimal **Default Programs** functionality.</span></span>

### <a name="during-installation"></a><span data-ttu-id="fd60c-283">Pendant l’installation</span><span class="sxs-lookup"><span data-stu-id="fd60c-283">During Installation</span></span>

<span data-ttu-id="fd60c-284">En plus des procédures d’installation normalement recommandées sous Windows XP, une application Windows Vista ou version ultérieure doit s’inscrire auprès de la fonctionnalité **programmes par défaut** pour tirer parti de ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="fd60c-284">In addition to the installation procedures normally practiced under Windows XP, a Windows Vista or later based application must register with the **Default Programs** feature to take advantage of its functionality.</span></span>

<span data-ttu-id="fd60c-285">Procédez comme suit lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="fd60c-285">Perform the following sequence of steps during installation.</span></span> <span data-ttu-id="fd60c-286">Les étapes 1-3 correspondent aux étapes qui ont été utilisées dans Windows XP. l’étape 4 est une nouveauté de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fd60c-286">Steps 1-3 match the steps that were used in Windows XP; step 4 was new in Windows Vista.</span></span>

1.  <span data-ttu-id="fd60c-287">Installez les fichiers binaires nécessaires.</span><span class="sxs-lookup"><span data-stu-id="fd60c-287">Install the necessary binary files.</span></span>
2.  <span data-ttu-id="fd60c-288">Écrivez les ProgID sur \_ la \_ machine locale HKEY.</span><span class="sxs-lookup"><span data-stu-id="fd60c-288">Write ProgIDs to HKEY\_LOCAL\_MACHINE.</span></span> <span data-ttu-id="fd60c-289">Notez que les applications doivent créer des ProgID spécifiques à l’application pour leurs associations.</span><span class="sxs-lookup"><span data-stu-id="fd60c-289">Note that applications must create application-specific ProgIDs for their associations.</span></span>
3.  <span data-ttu-id="fd60c-290">Inscrivez l’application avec les **programmes par défaut** comme expliqué précédemment dans [inscription d’une application pour une utilisation avec les programmes par défaut](#registering-an-application-for-use-with-default-programs).</span><span class="sxs-lookup"><span data-stu-id="fd60c-290">Register the application with **Default Programs** as previously explained in [Registering an Application for Use with Default Programs](#registering-an-application-for-use-with-default-programs).</span></span>

### <a name="after-installation"></a><span data-ttu-id="fd60c-291">Après l’installation</span><span class="sxs-lookup"><span data-stu-id="fd60c-291">After Installation</span></span>

<span data-ttu-id="fd60c-292">Cette section explique comment l’invite de l’application doit d’abord présenter ses options par défaut à chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd60c-292">This section discusses how the application prompt should first present its default options to each user.</span></span> <span data-ttu-id="fd60c-293">Il explique également comment une application peut surveiller son état par défaut pour ses associations et protocoles possibles.</span><span class="sxs-lookup"><span data-stu-id="fd60c-293">It also discusses how an application can monitor its status as the default for its possible associations and protocols.</span></span>

### <a name="first-run-experiences"></a><span data-ttu-id="fd60c-294">Expériences de première exécution</span><span class="sxs-lookup"><span data-stu-id="fd60c-294">First Run Experiences</span></span>

<span data-ttu-id="fd60c-295">Lorsque l’application est exécutée par un utilisateur pour la première fois, il est recommandé que l’application affiche l’interface utilisateur pour l’utilisateur qui comprend généralement les deux choix suivants :</span><span class="sxs-lookup"><span data-stu-id="fd60c-295">When the application is run by a user for the first time, it is recommended that the application display UI to the user that typically includes these two choices:</span></span>

-   <span data-ttu-id="fd60c-296">Acceptez les paramètres d’application par défaut.</span><span class="sxs-lookup"><span data-stu-id="fd60c-296">Accept the default application settings.</span></span> <span data-ttu-id="fd60c-297">Cette option est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="fd60c-297">This option is selected by default.</span></span>
-   <span data-ttu-id="fd60c-298">Personnaliser les paramètres d’application par défaut.</span><span class="sxs-lookup"><span data-stu-id="fd60c-298">Customize the default application settings.</span></span>

<span data-ttu-id="fd60c-299">Avant Windows 8, si l’utilisateur accepte les paramètres par défaut, votre application appelle [**IApplicationAssociationRegistration :: SetAppAsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall), qui convertit toutes les associations au niveau de l’ordinateur déclarées lors de l’installation en paramètres par utilisateur pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd60c-299">Prior to Windows 8, if the user accepts the default settings, your application calls [**IApplicationAssociationRegistration::SetAppAsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall), which converts all machine-level associations that are declared during installation to per-user settings for that user.</span></span>

<span data-ttu-id="fd60c-300">Si l’utilisateur décide de personnaliser les paramètres, votre application appelle [**IApplicationAssociationRegistrationUI :: LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) pour afficher l’interface utilisateur d’association de fichiers.</span><span class="sxs-lookup"><span data-stu-id="fd60c-300">If the user decides to customize the settings, your application calls [**IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) to display the file association UI.</span></span> <span data-ttu-id="fd60c-301">L’illustration suivante montre cette fenêtre pour le lecteur multimédia Litware-fiction.</span><span class="sxs-lookup"><span data-stu-id="fd60c-301">The following illustration shows this window for the fictional Litware media player.</span></span>

![capture d’écran de la page définir des associations pour un programme pour Litware](images/setassociationsforaprogramforlitware.png)

<span data-ttu-id="fd60c-303">La fenêtre Association de fichiers affiche les valeurs par défaut inscrites par l’application et indique également la valeur par défaut actuelle pour d’autres extensions et protocoles.</span><span class="sxs-lookup"><span data-stu-id="fd60c-303">The file association window shows the defaults that the application registered and also shows the current default for other extensions and protocols.</span></span> <span data-ttu-id="fd60c-304">Une fois que l’utilisateur a fini de personnaliser ses valeurs par défaut, il clique sur le bouton **Enregistrer** pour valider les modifications.</span><span class="sxs-lookup"><span data-stu-id="fd60c-304">After the user finishes customizing their defaults, they click the **Save** button to commit the changes.</span></span> <span data-ttu-id="fd60c-305">Si l’utilisateur clique sur **Annuler**, la fenêtre se ferme sans enregistrer les modifications.</span><span class="sxs-lookup"><span data-stu-id="fd60c-305">If the user clicks **Cancel**, the window closes without saving changes.</span></span>

<span data-ttu-id="fd60c-306">Vous devez utiliser cette interface utilisateur pour vos applications au lieu de créer les vôtres.</span><span class="sxs-lookup"><span data-stu-id="fd60c-306">You should use this UI for your applications instead of creating your own.</span></span> <span data-ttu-id="fd60c-307">En procédant ainsi, vous enregistrez les ressources qui ont été préalablement requises pour développer l’interface utilisateur d’association de fichiers.</span><span class="sxs-lookup"><span data-stu-id="fd60c-307">By doing so, you save the resources that were previously required to develop file association UI.</span></span> <span data-ttu-id="fd60c-308">Vous garantissez également que les associations sont correctement enregistrées.</span><span class="sxs-lookup"><span data-stu-id="fd60c-308">You also guarantee that associations are saved correctly.</span></span>

### <a name="set-an-application-to-check-whether-it-is-the-default"></a><span data-ttu-id="fd60c-309">Définir une application pour vérifier s’il s’agit de la valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fd60c-309">Set an Application to Check Whether It Is the Default</span></span>

> [!Note]  
> <span data-ttu-id="fd60c-310">Cette fonction n’est plus prise en charge dans Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fd60c-310">This is no longer supported as of Windows 8.</span></span>

 

<span data-ttu-id="fd60c-311">En règle générale, les applications vérifient si elles sont définies comme valeurs par défaut lorsqu’elles sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="fd60c-311">Applications typically check whether they are set as the default when they are run.</span></span> <span data-ttu-id="fd60c-312">Définissez vos applications pour effectuer cette vérification en appelant [**IApplicationAssociationRegistration :: QueryAppIsDefault**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) ou [**IApplicationAssociationRegistration :: QueryAppIsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall).</span><span class="sxs-lookup"><span data-stu-id="fd60c-312">Set your applications to make this check by calling [**IApplicationAssociationRegistration::QueryAppIsDefault**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) or [**IApplicationAssociationRegistration::QueryAppIsDefaultAll**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall).</span></span>

<span data-ttu-id="fd60c-313">Si l’application détermine qu’il ne s’agit pas de la valeur par défaut, elle peut présenter une interface utilisateur qui demande à l’utilisateur s’il faut accepter la situation actuelle ou pour que l’application soit la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="fd60c-313">If the application determines that it is not the default, it can present UI that asks the user whether to accept the current situation or to make the application the default.</span></span> <span data-ttu-id="fd60c-314">Incluez toujours une case à cocher dans cette interface utilisateur qui est sélectionnée par défaut et qui présente l’option ne pas être à nouveau demandée.</span><span class="sxs-lookup"><span data-stu-id="fd60c-314">Always include a check box in this UI that is selected by default and that presents the option not to be asked again.</span></span>

> [!Note]  
> <span data-ttu-id="fd60c-315">Le choix de la valeur par défaut doit être piloté par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd60c-315">The choice of default should be user driven.</span></span> <span data-ttu-id="fd60c-316">Une application ne doit jamais réclamer une valeur par défaut sans demander à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd60c-316">An application should never reclaim a default without asking the user.</span></span>

 

<span data-ttu-id="fd60c-317">L’illustration suivante montre un exemple de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="fd60c-317">The following illustration shows an example dialog box.</span></span>

![capture d’écran d’un exemple de boîte de dialogue](images/notthedefaultui.png)

## <a name="additional-resources"></a><span data-ttu-id="fd60c-319">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="fd60c-319">Additional Resources</span></span>

-   [<span data-ttu-id="fd60c-320">**IApplicationAssociationRegistration**</span><span class="sxs-lookup"><span data-stu-id="fd60c-320">**IApplicationAssociationRegistration**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration)
-   [<span data-ttu-id="fd60c-321">**IApplicationAssociationRegistrationUI**</span><span class="sxs-lookup"><span data-stu-id="fd60c-321">**IApplicationAssociationRegistrationUI**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui)

## <a name="related-topics"></a><span data-ttu-id="fd60c-322">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fd60c-322">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd60c-323">Meilleures pratiques pour les associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="fd60c-323">Best Practices for File Associations</span></span>](fa-best-practices.md)
</dt> <dt>

[<span data-ttu-id="fd60c-324">Exemple de scénario d’association de fichiers</span><span class="sxs-lookup"><span data-stu-id="fd60c-324">File Association Sample Scenario</span></span>](fa-sample-scenarios.md)
</dt> <dt>

[<span data-ttu-id="fd60c-325">Instructions pour la gestion des applications par défaut dans Windows Vista et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="fd60c-325">Guidelines for Managing Default Applications in Windows Vista and Later</span></span>](vista-managing-defaults.md)
</dt> <dt>

[<span data-ttu-id="fd60c-326">Définir l’accès aux programmes et les paramètres par défaut de l’ordinateur (SPAD)</span><span class="sxs-lookup"><span data-stu-id="fd60c-326">Set Program Access and Computer Defaults (SPAD)</span></span>](cpl-setprogramaccess.md)
</dt> </dl>

 

 
