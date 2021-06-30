---
title: Activation des styles visuels
description: Cette rubrique explique comment configurer votre application pour vous assurer que les contrôles communs s’affichent dans le style visuel préféré de l’utilisateur.
ms.assetid: eb6c2469-25b9-43c4-a6ca-391a7b2859b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4673d0a47f42f557e09f4afe46131cd48bad1b0
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102168"
---
# <a name="enabling-visual-styles"></a><span data-ttu-id="be6f1-103">Activation des styles visuels</span><span class="sxs-lookup"><span data-stu-id="be6f1-103">Enabling Visual Styles</span></span>

<span data-ttu-id="be6f1-104">Cette rubrique explique comment configurer votre application pour vous assurer que les contrôles communs s’affichent dans le style visuel préféré de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="be6f1-104">This topic explains how to configure your application to ensure that common controls are displayed in the user's preferred visual style.</span></span>

<span data-ttu-id="be6f1-105">Cette rubrique comprend les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="be6f1-105">This topic includes the following sections.</span></span>

-   [<span data-ttu-id="be6f1-106">Utilisation de manifestes ou de directives pour s’assurer que les styles visuels peuvent être appliqués aux applications</span><span class="sxs-lookup"><span data-stu-id="be6f1-106">Using Manifests or Directives to Ensure That Visual Styles Can Be Applied to Applications</span></span>](#using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications)
-   [<span data-ttu-id="be6f1-107">Utilisation de ComCtl32.dll version 6 dans une application qui utilise uniquement des extensions standard</span><span class="sxs-lookup"><span data-stu-id="be6f1-107">Using ComCtl32.dll Version 6 in an Application That Uses Only Standard Extensions</span></span>](#using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions)
-   [<span data-ttu-id="be6f1-108">À l’aide de ComCtl32 version 6 dans le panneau de configuration ou d’une DLL exécutée par RunDll32.exe</span><span class="sxs-lookup"><span data-stu-id="be6f1-108">Using ComCtl32 Version 6 in Control Panel or a DLL That Is Run by RunDll32.exe</span></span>](#using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe)
-   [<span data-ttu-id="be6f1-109">Ajout de la prise en charge de style visuel à une extension, à un plug-in, à un composant logiciel enfichable MMC ou à une DLL introduite dans un processus</span><span class="sxs-lookup"><span data-stu-id="be6f1-109">Adding Visual Style Support to an Extension, Plug-in, MMC Snap-in or a DLL That Is Brought into a Process</span></span>](#adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process)
-   [<span data-ttu-id="be6f1-110">Désactivation des styles visuels</span><span class="sxs-lookup"><span data-stu-id="be6f1-110">Turning Off Visual Styles</span></span>](#turning-off-visual-styles)
-   [<span data-ttu-id="be6f1-111">Utilisation de styles visuels avec du contenu HTML</span><span class="sxs-lookup"><span data-stu-id="be6f1-111">Using Visual Styles with HTML Content</span></span>](#using-visual-styles-with-html-content)
-   [<span data-ttu-id="be6f1-112">Quand les styles visuels ne sont pas appliqués</span><span class="sxs-lookup"><span data-stu-id="be6f1-112">When Visual Styles are not Applied</span></span>](#when-visual-styles-are-not-applied)
-   [<span data-ttu-id="be6f1-113">Rendre votre application compatible avec les versions antérieures de Windows</span><span class="sxs-lookup"><span data-stu-id="be6f1-113">Making Your Application Compatible with Earlier Versions of Windows</span></span>](#making-your-application-compatible-with-earlier-versions-of-windows)
-   [<span data-ttu-id="be6f1-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be6f1-114">Related topics</span></span>](#related-topics)

## <a name="using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications"></a><span data-ttu-id="be6f1-115">Utilisation de manifestes ou de directives pour s’assurer que les styles visuels peuvent être appliqués aux applications</span><span class="sxs-lookup"><span data-stu-id="be6f1-115">Using Manifests or Directives to Ensure That Visual Styles Can Be Applied to Applications</span></span>

<span data-ttu-id="be6f1-116">Pour permettre à votre application d’utiliser des styles visuels, vous devez utiliser ComCtl32.dll version 6 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="be6f1-116">To enable your application to use visual styles, you must use ComCtl32.dll version 6 or later.</span></span> <span data-ttu-id="be6f1-117">Étant donné que la version 6 n’est pas redistribuable, elle est disponible uniquement lorsque votre application s’exécute sur une version de Windows qui la contient.</span><span class="sxs-lookup"><span data-stu-id="be6f1-117">Because version 6 is not redistributable, it is available only when your application is running on a version of Windows that contains it.</span></span> <span data-ttu-id="be6f1-118">Windows est fourni avec les versions 5 et 6.</span><span class="sxs-lookup"><span data-stu-id="be6f1-118">Windows ships with both version 5 and version 6.</span></span> <span data-ttu-id="be6f1-119">ComCtl32.dll version 6 contient à la fois les contrôles utilisateur et les contrôles communs.</span><span class="sxs-lookup"><span data-stu-id="be6f1-119">ComCtl32.dll version 6 contains both the user controls and the common controls.</span></span> <span data-ttu-id="be6f1-120">Par défaut, les applications utilisent les contrôles utilisateur définis dans User32.dll et les contrôles communs définis dans ComCtl32.dll version 5.</span><span class="sxs-lookup"><span data-stu-id="be6f1-120">By default, applications use the user controls defined in User32.dll and the common controls defined in ComCtl32.dll version 5.</span></span> <span data-ttu-id="be6f1-121">Pour obtenir la liste des versions de DLL et leurs plateformes de distribution, consultez la page [versions de contrôle courantes](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="be6f1-121">For a list of DLL versions and their distribution platforms, see [Common Control Versions](common-control-versions.md).</span></span>

<span data-ttu-id="be6f1-122">Si vous souhaitez que votre application utilise des styles visuels, vous devez ajouter un manifeste d’application ou une directive de compilateur qui indique que ComCtl32.dll version 6 doit être utilisée si elle est disponible.</span><span class="sxs-lookup"><span data-stu-id="be6f1-122">If you want your application to use visual styles, you must add an application manifest or compiler directive that indicates that ComCtl32.dll version 6 should be used if it is available.</span></span>

<span data-ttu-id="be6f1-123">Un manifeste d’application permet à une application de spécifier les versions d’un assembly dont elle a besoin.</span><span class="sxs-lookup"><span data-stu-id="be6f1-123">An application manifest enables an application to specify which versions of an assembly it requires.</span></span> <span data-ttu-id="be6f1-124">Dans Microsoft Win32, un assembly est un ensemble de dll et une liste d’objets pouvant être mis en version qui sont contenus dans ces dll.</span><span class="sxs-lookup"><span data-stu-id="be6f1-124">In Microsoft Win32, an assembly is a set of DLLs and a list of versionable objects that are contained within those DLLs.</span></span>

<span data-ttu-id="be6f1-125">Les manifestes sont écrits en XML.</span><span class="sxs-lookup"><span data-stu-id="be6f1-125">Manifests are written in XML.</span></span> <span data-ttu-id="be6f1-126">Le nom du fichier manifeste de l’application est le nom de votre exécutable suivi de l’extension de nom de fichier. manifest ; par exemple, MyApp.exe. manifest.</span><span class="sxs-lookup"><span data-stu-id="be6f1-126">The name of the application manifest file is the name of your executable followed by the file name extension .manifest; for example, MyApp.exe.manifest.</span></span> <span data-ttu-id="be6f1-127">L’exemple de manifeste suivant montre que la première section décrit le manifeste lui-même.</span><span class="sxs-lookup"><span data-stu-id="be6f1-127">The following sample manifest shows that the first section describes the manifest itself.</span></span> <span data-ttu-id="be6f1-128">Le tableau suivant présente les attributs définis par l’élément **assemblyIdentity** dans la section Description du manifeste.</span><span class="sxs-lookup"><span data-stu-id="be6f1-128">The following table shows the attributes set by the **assemblyIdentity** element in the manifest description section.</span></span>



| <span data-ttu-id="be6f1-129">Attribut</span><span class="sxs-lookup"><span data-stu-id="be6f1-129">Attribute</span></span>             | <span data-ttu-id="be6f1-130">Description</span><span class="sxs-lookup"><span data-stu-id="be6f1-130">Description</span></span>                                                                                                                 |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be6f1-131">version</span><span class="sxs-lookup"><span data-stu-id="be6f1-131">version</span></span>               | <span data-ttu-id="be6f1-132">Version du manifeste.</span><span class="sxs-lookup"><span data-stu-id="be6f1-132">Version of the manifest.</span></span> <span data-ttu-id="be6f1-133">La version doit se présenter sous la forme major. minor. revision. Build (autrement dit, n. n. n. n, où n <= 65535).</span><span class="sxs-lookup"><span data-stu-id="be6f1-133">The version must be in the form major.minor.revision.build (that is, n.n.n.n, where n <=65535).</span></span> |
| <span data-ttu-id="be6f1-134">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="be6f1-134">processorArchitecture</span></span> | <span data-ttu-id="be6f1-135">Processeur pour lequel votre application est développée.</span><span class="sxs-lookup"><span data-stu-id="be6f1-135">Processor for which your application is developed.</span></span>                                                                          |
| <span data-ttu-id="be6f1-136">name</span><span class="sxs-lookup"><span data-stu-id="be6f1-136">name</span></span>                  | <span data-ttu-id="be6f1-137">Comprend le nom de la société, le nom du produit et le nom de l’application.</span><span class="sxs-lookup"><span data-stu-id="be6f1-137">Includes company name, product name and application name.</span></span>                                                                   |
| <span data-ttu-id="be6f1-138">type</span><span class="sxs-lookup"><span data-stu-id="be6f1-138">type</span></span>                  | <span data-ttu-id="be6f1-139">Type de votre application, tel que Win32.</span><span class="sxs-lookup"><span data-stu-id="be6f1-139">Type of your application, such as Win32.</span></span>                                                                                    |



 

<span data-ttu-id="be6f1-140">L’exemple de manifeste fournit également une description de votre application et spécifie des dépendances d’application.</span><span class="sxs-lookup"><span data-stu-id="be6f1-140">The sample manifest also provides a description of your application and specifies application dependencies.</span></span> <span data-ttu-id="be6f1-141">Le tableau suivant présente les attributs définis par l’élément **assemblyIdentity** dans la section Dependency.</span><span class="sxs-lookup"><span data-stu-id="be6f1-141">The following table shows the attributes set by the **assemblyIdentity** element in the dependency section.</span></span>



| <span data-ttu-id="be6f1-142">Attribut</span><span class="sxs-lookup"><span data-stu-id="be6f1-142">Attribute</span></span>             | <span data-ttu-id="be6f1-143">Description</span><span class="sxs-lookup"><span data-stu-id="be6f1-143">Description</span></span>                                      |
|-----------------------|--------------------------------------------------|
| <span data-ttu-id="be6f1-144">type</span><span class="sxs-lookup"><span data-stu-id="be6f1-144">type</span></span>                  | <span data-ttu-id="be6f1-145">Type du composant de dépendance, tel que Win32.</span><span class="sxs-lookup"><span data-stu-id="be6f1-145">Type of the dependency component, such as Win32.</span></span> |
| <span data-ttu-id="be6f1-146">name</span><span class="sxs-lookup"><span data-stu-id="be6f1-146">name</span></span>                  | <span data-ttu-id="be6f1-147">Nom du composant.</span><span class="sxs-lookup"><span data-stu-id="be6f1-147">Name of the component.</span></span>                           |
| <span data-ttu-id="be6f1-148">version</span><span class="sxs-lookup"><span data-stu-id="be6f1-148">version</span></span>               | <span data-ttu-id="be6f1-149">Numéro de version du composant.</span><span class="sxs-lookup"><span data-stu-id="be6f1-149">Version of the component.</span></span>                        |
| <span data-ttu-id="be6f1-150">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="be6f1-150">processorArchitecture</span></span> | <span data-ttu-id="be6f1-151">Processeur pour lequel le composant est conçu.</span><span class="sxs-lookup"><span data-stu-id="be6f1-151">Processor that the component is designed for.</span></span>    |
| <span data-ttu-id="be6f1-152">publicKeyToken</span><span class="sxs-lookup"><span data-stu-id="be6f1-152">publicKeyToken</span></span>        | <span data-ttu-id="be6f1-153">Jeton de clé utilisé avec ce composant.</span><span class="sxs-lookup"><span data-stu-id="be6f1-153">Key token used with this component.</span></span>              |
| <span data-ttu-id="be6f1-154">langage</span><span class="sxs-lookup"><span data-stu-id="be6f1-154">language</span></span>              | <span data-ttu-id="be6f1-155">Langue du composant.</span><span class="sxs-lookup"><span data-stu-id="be6f1-155">Language of the component.</span></span>                       |



 

<span data-ttu-id="be6f1-156">Voici un exemple de fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="be6f1-156">Following is an example of a manifest file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be6f1-157">Définissez l’entrée **ProcessorArchitecture** sur **« x86 »** si votre application cible la plateforme Windows 32 bits, ou sur **« amd64 »** si votre application cible la plateforme Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="be6f1-157">Set the **processorArchitecture** entry to **"X86"** if your application targets the 32 bit Windows platform, or to **"amd64"** if your application targets the 64 bit Windows platform.</span></span> <span data-ttu-id="be6f1-158">Vous pouvez également spécifier **« \* »**, ce qui garantit que toutes les plateformes sont ciblées, comme illustré dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="be6f1-158">You can also specify **"\*"**, which ensures that all platforms are targeted, as shown in the following examples.</span></span>

 


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity
    version="1.0.0.0"
    processorArchitecture="*"
    name="CompanyName.ProductName.YourApplication"
    type="win32"
/>
<description>Your application description here.</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="*"
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
</assembly>
```



<span data-ttu-id="be6f1-159">Si vous utilisez Microsoft Visual C++ 2005 ou une version ultérieure, vous pouvez ajouter la directive de compilateur suivante à votre code source au lieu de créer manuellement un manifeste.</span><span class="sxs-lookup"><span data-stu-id="be6f1-159">If you are using Microsoft Visual C++ 2005 or later, you can add the following compiler directive to your source code instead of manually creating a manifest.</span></span> <span data-ttu-id="be6f1-160">Pour une meilleure lisibilité, la directive est divisée en plusieurs lignes ici.</span><span class="sxs-lookup"><span data-stu-id="be6f1-160">For readability, the directive is broken into several lines here.</span></span>


```C++
#pragma comment(linker,"\"/manifestdependency:type='win32' \
name='Microsoft.Windows.Common-Controls' version='6.0.0.0' \
processorArchitecture='*' publicKeyToken='6595b64144ccf1df' language='*'\"")
```



<span data-ttu-id="be6f1-161">Les rubriques suivantes décrivent les étapes à suivre pour appliquer des styles visuels à différents types d’applications.</span><span class="sxs-lookup"><span data-stu-id="be6f1-161">The following topics describe the steps for applying visual styles to different types of applications.</span></span> <span data-ttu-id="be6f1-162">Notez que le format du manifeste est le même dans chaque cas.</span><span class="sxs-lookup"><span data-stu-id="be6f1-162">Notice that the manifest format is the same in each case.</span></span>

## <a name="using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions"></a><span data-ttu-id="be6f1-163">Utilisation de ComCtl32.dll version 6 dans une application qui utilise uniquement des extensions standard</span><span class="sxs-lookup"><span data-stu-id="be6f1-163">Using ComCtl32.dll Version 6 in an Application That Uses Only Standard Extensions</span></span>

<span data-ttu-id="be6f1-164">Voici quelques exemples d’applications qui n’utilisent pas d’extensions tierces.</span><span class="sxs-lookup"><span data-stu-id="be6f1-164">The following are examples of applications that do not use third-party extensions.</span></span>

-   <span data-ttu-id="be6f1-165">Calculatrice</span><span class="sxs-lookup"><span data-stu-id="be6f1-165">Calculator</span></span>
-   <span data-ttu-id="be6f1-166">FreeCell (dans Windows Vista et Windows 7)</span><span class="sxs-lookup"><span data-stu-id="be6f1-166">FreeCell (in Windows Vista and Windows 7)</span></span>
-   <span data-ttu-id="be6f1-167">Démineur (dans Windows Vista et Windows 7)</span><span class="sxs-lookup"><span data-stu-id="be6f1-167">Minesweeper (in Windows Vista and Windows 7)</span></span>
-   <span data-ttu-id="be6f1-168">Bloc-notes</span><span class="sxs-lookup"><span data-stu-id="be6f1-168">Notepad</span></span>
-   <span data-ttu-id="be6f1-169">Solitaire (dans Windows Vista et Windows 7)</span><span class="sxs-lookup"><span data-stu-id="be6f1-169">Solitaire (in Windows Vista and Windows 7)</span></span>

<span data-ttu-id="be6f1-170">**Pour créer un manifeste et permettre à votre application d’utiliser des styles visuels.**</span><span class="sxs-lookup"><span data-stu-id="be6f1-170">**To create a manifest and enable your application to use visual styles.**</span></span>

1.  <span data-ttu-id="be6f1-171">Liez à ComCtl32. lib et appelez [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span><span class="sxs-lookup"><span data-stu-id="be6f1-171">Link to ComCtl32.lib and call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span></span>
2.  <span data-ttu-id="be6f1-172">Ajoutez un fichier appelé YourApp.exe. manifest à votre arborescence source qui a le format de manifeste XML.</span><span class="sxs-lookup"><span data-stu-id="be6f1-172">Add a file called YourApp.exe.manifest to your source tree that has the XML manifest format.</span></span>
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  <span data-ttu-id="be6f1-173">Ajoutez le manifeste au fichier de ressources de votre application comme suit :</span><span class="sxs-lookup"><span data-stu-id="be6f1-173">Add the manifest to your application's resource file as follows:</span></span>
    ```C++
    CREATEPROCESS_MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.exe.manifest"
    ```

    

    > [!Note]  
    > <span data-ttu-id="be6f1-174">Lorsque vous ajoutez l’entrée précédente à la ressource, vous devez la mettre en forme sur une seule ligne.</span><span class="sxs-lookup"><span data-stu-id="be6f1-174">When you add the previous entry to the resource you must format it on one line.</span></span> <span data-ttu-id="be6f1-175">Vous pouvez également placer le fichier manifeste XML dans le même répertoire que le fichier exécutable de votre application.</span><span class="sxs-lookup"><span data-stu-id="be6f1-175">Alternatively, you can place the XML manifest file in the same directory as your application's executable file.</span></span> <span data-ttu-id="be6f1-176">Le système d’exploitation chargera d’abord le manifeste à partir du système de fichiers, puis vérifiera la section de la ressource du fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="be6f1-176">The operating system will load the manifest from the file system first, then check the resource section of the executable.</span></span> <span data-ttu-id="be6f1-177">La version du système de fichiers est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="be6f1-177">The file system version takes precedence.</span></span>

     

<span data-ttu-id="be6f1-178">Lorsque vous générez votre application, le manifeste est ajouté en tant que ressource binaire.</span><span class="sxs-lookup"><span data-stu-id="be6f1-178">When you build your application, the manifest will be added as a binary resource.</span></span>

## <a name="using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe"></a><span data-ttu-id="be6f1-179">À l’aide de ComCtl32 version 6 dans le panneau de configuration ou d’une DLL exécutée par RunDll32.exe</span><span class="sxs-lookup"><span data-stu-id="be6f1-179">Using ComCtl32 Version 6 in Control Panel or a DLL That Is Run by RunDll32.exe</span></span>

<span data-ttu-id="be6f1-180">**Pour créer un manifeste et permettre à votre application d’utiliser des styles visuels.**</span><span class="sxs-lookup"><span data-stu-id="be6f1-180">**To create a manifest and enable your application to use visual styles.**</span></span>

1.  <span data-ttu-id="be6f1-181">Liez à ComCtl32. lib et appelez [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span><span class="sxs-lookup"><span data-stu-id="be6f1-181">Link to ComCtl32.lib and call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).</span></span>
2.  <span data-ttu-id="be6f1-182">Ajoutez un fichier appelé YourApp.cpl. manifest à votre arborescence source qui a le format de manifeste XML.</span><span class="sxs-lookup"><span data-stu-id="be6f1-182">Add a file called YourApp.cpl.manifest to your source tree that has the XML manifest format.</span></span>
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  <span data-ttu-id="be6f1-183">Ajoutez le manifeste au fichier de ressources de votre application en tant qu’ID de ressource 123.</span><span class="sxs-lookup"><span data-stu-id="be6f1-183">Add the manifest to your application's resource file as resource ID 123.</span></span>

> [!Note]  
> <span data-ttu-id="be6f1-184">Lorsque vous créez une application du panneau de configuration, placez-la dans la catégorie appropriée.</span><span class="sxs-lookup"><span data-stu-id="be6f1-184">When you author a Control Panel application, place it in the appropriate category.</span></span> <span data-ttu-id="be6f1-185">Le panneau de configuration prend désormais en charge la catégorisation des applications du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="be6f1-185">Control Panel now supports categorization of Control Panel applications.</span></span> <span data-ttu-id="be6f1-186">Cela signifie qu’il est possible d’affecter des identificateurs aux applications du panneau de configuration et de les séparer en zones de tâches telles que l’ajout ou la suppression de programmes, l’apparence et les thèmes, ou la date, l’heure, la langue et les options régionales.</span><span class="sxs-lookup"><span data-stu-id="be6f1-186">This means that Control Panel applications can be assigned identifiers and separated into task areas such as Add or Remove Programs, Appearance and Themes, or Date, Time, Language, and Regional Options.</span></span>

 

## <a name="adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process"></a><span data-ttu-id="be6f1-187">Ajout de la prise en charge de style visuel à une extension, à un plug-in, à un composant logiciel enfichable MMC ou à une DLL introduite dans un processus</span><span class="sxs-lookup"><span data-stu-id="be6f1-187">Adding Visual Style Support to an Extension, Plug-in, MMC Snap-in or a DLL That Is Brought into a Process</span></span>

<span data-ttu-id="be6f1-188">La prise en charge des styles visuels peut être ajoutée à une extension, à un plug-in, à un composant logiciel enfichable MMC ou à une DLL introduite dans un processus.</span><span class="sxs-lookup"><span data-stu-id="be6f1-188">Support for visual styles can be added to an extension, plug-in, MMC snap-in, or a DLL that is brought into a process.</span></span> <span data-ttu-id="be6f1-189">Par exemple, utilisez les étapes suivantes pour ajouter la prise en charge des styles visuels pour un composant logiciel enfichable MMC (Microsoft Management Console).</span><span class="sxs-lookup"><span data-stu-id="be6f1-189">For example, use the following steps to add visual styles support for an Microsoft Management Console (MMC) snap-in.</span></span>

1.  <span data-ttu-id="be6f1-190">Compilez votre composant logiciel enfichable avec l’indicateur compatible-DISOLATION \_ \_ ou insérez l’instruction suivante avant l' \# instruction include « Windows. h ».</span><span class="sxs-lookup"><span data-stu-id="be6f1-190">Compile your snap-in with the -DISOLATION\_AWARE\_ENABLED flag or insert the following statement before the \#include "windows.h" statement.</span></span>

    ```C++
    #define ISOLATION_AWARE_ENABLED 1
    ```

    

    <span data-ttu-id="be6f1-191">Pour plus d’informations sur la prise en charge de l’ISOLATION \_ \_ , consultez [isolation des composants](/windows/desktop/SbsCs/isolating-components).</span><span class="sxs-lookup"><span data-stu-id="be6f1-191">For more information about ISOLATION\_AWARE\_ENABLED, see [Isolating Components](/windows/desktop/SbsCs/isolating-components).</span></span>

2.  <span data-ttu-id="be6f1-192">Incluez le fichier d’en-tête de contrôle commun dans votre source de composant logiciel enfichable.</span><span class="sxs-lookup"><span data-stu-id="be6f1-192">Include the common control header file in your snap-in source.</span></span>
    ```C++
    #include <commctrl.h>
    ```

    

3.  <span data-ttu-id="be6f1-193">Ajoutez un fichier nommé VotreApplication. manifest à votre arborescence source qui utilise le format de manifeste XML.</span><span class="sxs-lookup"><span data-stu-id="be6f1-193">Add a file called YourApp.manifest to your source tree that uses the XML manifest format.</span></span>
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

4.  <span data-ttu-id="be6f1-194">Ajoutez le manifeste au fichier de ressources de votre composant logiciel enfichable.</span><span class="sxs-lookup"><span data-stu-id="be6f1-194">Add the manifest to your snap-in's resource file.</span></span> <span data-ttu-id="be6f1-195">Pour plus d’informations sur l’ajout d’un manifeste à un fichier de ressources, consultez [utilisation de ComCtl32 version 6 dans une application qui utilise des extensions, des plug-ins ou une dll introduite dans un processus](/previous-versions//ms649781(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="be6f1-195">See [Using ComCtl32 Version 6 in an Application That Uses Extensions, Plug-ins, or a DLL That Is Brought into a Process](/previous-versions//ms649781(v=vs.85)) for details on adding a manifest to a resource file.</span></span>

## <a name="turning-off-visual-styles"></a><span data-ttu-id="be6f1-196">Désactivation des styles visuels</span><span class="sxs-lookup"><span data-stu-id="be6f1-196">Turning Off Visual Styles</span></span>

<span data-ttu-id="be6f1-197">Vous pouvez désactiver les styles visuels pour un contrôle ou pour tous les contrôles d’une fenêtre en appelant la fonction [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) comme suit :</span><span class="sxs-lookup"><span data-stu-id="be6f1-197">You can turn off visual styles for a control or for all controls in a window by calling the [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) function as follows:</span></span>


```C++
SetWindowTheme(hwnd, L" ", L" ");
```



<span data-ttu-id="be6f1-198">Dans l’exemple précédent, *HWND* est le handle de la fenêtre dans laquelle désactiver les styles visuels.</span><span class="sxs-lookup"><span data-stu-id="be6f1-198">In the previous example, *hwnd* is the handle of the window in which to disable visual styles.</span></span> <span data-ttu-id="be6f1-199">Après l’appel, le contrôle s’affiche sans styles visuels.</span><span class="sxs-lookup"><span data-stu-id="be6f1-199">After the call, the control renders without visual styles.</span></span>

## <a name="using-visual-styles-with-html-content"></a><span data-ttu-id="be6f1-200">Utilisation de styles visuels avec du contenu HTML</span><span class="sxs-lookup"><span data-stu-id="be6f1-200">Using Visual Styles with HTML Content</span></span>

<span data-ttu-id="be6f1-201">Les styles visuels ne sont pas appliqués aux pages HTML qui modifient les propriétés de feuilles de style en cascade (CSS) telles que l’arrière-plan ou la bordure.</span><span class="sxs-lookup"><span data-stu-id="be6f1-201">HTML pages that modify the Cascading Style Sheets (CSS) properties such as background or border do not have visual styles applied to them.</span></span> <span data-ttu-id="be6f1-202">Ils affichent l’attribut CSS spécifié.</span><span class="sxs-lookup"><span data-stu-id="be6f1-202">They display the specified CSS attribute.</span></span> <span data-ttu-id="be6f1-203">Lorsqu’ils sont spécifiés dans le cadre du contenu, la plupart des propriétés CSS s’appliquent aux éléments auxquels des styles visuels sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="be6f1-203">When specified as part of the content, most CSS properties do apply to elements that have visual styles applied.</span></span>

<span data-ttu-id="be6f1-204">Par défaut, les styles visuels sont appliqués aux contrôles HTML intrinsèques sur les pages affichées dans Microsoft Internet Explorer 6 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="be6f1-204">By default, visual styles are applied to intrinsic HTML controls on pages displayed in Microsoft Internet Explorer 6 and later versions.</span></span> <span data-ttu-id="be6f1-205">Pour désactiver les styles visuels pour une page HTML, ajoutez une balise META au</span><span class="sxs-lookup"><span data-stu-id="be6f1-205">To turn off visual styles for an HTML page, add a META tag to the</span></span> <head> <span data-ttu-id="be6f1-206">un peu plus loin dans cet article, aborde l’actualisation de chaque type de source de données.</span><span class="sxs-lookup"><span data-stu-id="be6f1-206">section.</span></span> <span data-ttu-id="be6f1-207">Cette technique s’applique également au contenu empaqueté en tant qu’applications HTML (HTA).</span><span class="sxs-lookup"><span data-stu-id="be6f1-207">This technique also applies to content packaged as HTML Applications (HTAs).</span></span> <span data-ttu-id="be6f1-208">Pour désactiver les styles visuels, la balise META doit être la suivante :</span><span class="sxs-lookup"><span data-stu-id="be6f1-208">To turn off visual styles, the META tag must be as follows:</span></span>


```
<META HTTP-EQUIV="MSThemeCompatible" CONTENT="no">
```



> [!Note]  
> <span data-ttu-id="be6f1-209">Si le paramètre de navigateur et le paramètre de balise ne correspondent pas, la page n’applique pas les styles visuels.</span><span class="sxs-lookup"><span data-stu-id="be6f1-209">If the browser setting and the tag setting do not agree, the page will not apply visual styles.</span></span> <span data-ttu-id="be6f1-210">Par exemple, si la balise META est définie sur « no » et que le navigateur est configuré pour activer les styles visuels, les styles visuels ne sont pas appliqués à la page.</span><span class="sxs-lookup"><span data-stu-id="be6f1-210">For example, if the META tag is set to "no" and the browser is set to enable visual styles, visual styles will not be applied to the page.</span></span> <span data-ttu-id="be6f1-211">Toutefois, si le navigateur ou la balise META a la valeur « Yes » et que l’autre élément n’est pas spécifié, les styles visuels sont appliqués.</span><span class="sxs-lookup"><span data-stu-id="be6f1-211">However, if either the browser or META tag is set to "yes" and the other item is not specified, visual styles will be applied.</span></span>

 

<span data-ttu-id="be6f1-212">Les styles visuels peuvent modifier la disposition de votre contenu.</span><span class="sxs-lookup"><span data-stu-id="be6f1-212">Visual styles might change the layout of your content.</span></span> <span data-ttu-id="be6f1-213">En outre, si vous définissez certains attributs sur des contrôles HTML intrinsèques, tels que la largeur d’un bouton, vous pouvez constater que l’étiquette sur le bouton est illisible dans certains styles visuels.</span><span class="sxs-lookup"><span data-stu-id="be6f1-213">Also, if you set certain attributes on intrinsic HTML controls, such as the width of a button, you might find that the label on the button is unreadable under certain visual styles.</span></span>

<span data-ttu-id="be6f1-214">Vous devez tester minutieusement votre contenu à l’aide de styles visuels pour déterminer si l’application de styles visuels a un effet néfaste sur votre contenu et votre disposition.</span><span class="sxs-lookup"><span data-stu-id="be6f1-214">You must thoroughly test your content using visual styles to determine whether applying visual styles has an adverse effect on your content and layout.</span></span>

## <a name="when-visual-styles-are-not-applied"></a><span data-ttu-id="be6f1-215">Quand les styles visuels ne sont pas appliqués</span><span class="sxs-lookup"><span data-stu-id="be6f1-215">When Visual Styles are not Applied</span></span>

<span data-ttu-id="be6f1-216">Pour éviter d’appliquer des styles visuels à une fenêtre de niveau supérieur, attribuez à la fenêtre une région non null (**SetWindowRgn**).</span><span class="sxs-lookup"><span data-stu-id="be6f1-216">To avoid applying visual styles to a top level window, give the window a non-null region (**SetWindowRgn**).</span></span> <span data-ttu-id="be6f1-217">Le système suppose qu’une fenêtre avec une région non NULL est une fenêtre spécialisée qui n’utilise pas de styles visuels.</span><span class="sxs-lookup"><span data-stu-id="be6f1-217">The system assumes that a window with a non-NULL region is a specialized window that does not use visual styles.</span></span> <span data-ttu-id="be6f1-218">Une fenêtre enfant associée à une fenêtre de niveau supérieur de styles non visuels peut toujours appliquer des styles visuels même si la fenêtre parente ne le fait pas.</span><span class="sxs-lookup"><span data-stu-id="be6f1-218">A child window associated with a non-visual-styles top level window may still apply visual styles even though the parent window does not.</span></span>

<span data-ttu-id="be6f1-219">Si vous souhaitez désactiver l’utilisation de styles visuels pour toutes les fenêtres de votre application, appelez [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) et ne transmettez pas l' \_ indicateur STAP allow non \_ client.</span><span class="sxs-lookup"><span data-stu-id="be6f1-219">If you want to disable the use of visual styles for all windows in your application, call [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) and do not pass the STAP\_ALLOW\_NONCLIENT flag.</span></span> <span data-ttu-id="be6f1-220">Si une application n’appelle pas **SetThemeAppProperties**, les valeurs d’indicateur supposées sont STAP autoriser le non- \_ \_ client \| STAP \_ autoriser les \_ contrôles \| STAP \_ autoriser le \_ contenu WEBCONTENT.</span><span class="sxs-lookup"><span data-stu-id="be6f1-220">If an application does not call **SetThemeAppProperties**, the assumed flag values are STAP\_ALLOW\_NONCLIENT \| STAP\_ALLOW\_CONTROLS \| STAP\_ALLOW\_WEBCONTENT.</span></span> <span data-ttu-id="be6f1-221">Les valeurs supposées provoquent l’application d’un style visuel à la zone non cliente, aux contrôles et au contenu Web.</span><span class="sxs-lookup"><span data-stu-id="be6f1-221">The assumed values cause the nonclient area, the controls, and web content to have a visual style applied.</span></span>

## <a name="making-your-application-compatible-with-earlier-versions-of-windows"></a><span data-ttu-id="be6f1-222">Rendre votre application compatible avec les versions antérieures de Windows</span><span class="sxs-lookup"><span data-stu-id="be6f1-222">Making Your Application Compatible with Earlier Versions of Windows</span></span>

<span data-ttu-id="be6f1-223">Une grande partie de l’architecture de style visuel est conçue pour faciliter la livraison de votre produit sur les versions antérieures de Windows qui ne prennent pas en charge la modification de l’apparence des contrôles.</span><span class="sxs-lookup"><span data-stu-id="be6f1-223">Much of the visual style architecture is designed to make it simple to continue to ship your product on earlier versions of Windows that do not support changing the appearance of controls.</span></span> <span data-ttu-id="be6f1-224">Lors de l’expédition d’une application pour plusieurs systèmes d’exploitation, tenez compte des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="be6f1-224">When shipping an application for more than one operating system, be aware of the following:</span></span>

-   <span data-ttu-id="be6f1-225">Dans les versions de Windows antérieures à Windows 8, les styles visuels sont désactivés lorsque le contraste élevé est activé.</span><span class="sxs-lookup"><span data-stu-id="be6f1-225">In versions of Windows prior to Windows 8, visual styles are off when high contrast is on.</span></span> <span data-ttu-id="be6f1-226">Pour prendre en charge le contraste élevé, une application héritée qui prend en charge les styles visuels doit fournir un chemin de code distinct pour dessiner correctement les éléments d’interface utilisateur en contraste élevé.</span><span class="sxs-lookup"><span data-stu-id="be6f1-226">To support high contrast, a legacy application that supports visual styles needs to provide a separate code path to properly draw UI elements in high contrast.</span></span> <span data-ttu-id="be6f1-227">Dans Windows 8, le contraste élevé fait partie des styles visuels. Toutefois, une application Windows 8 (qui comprend le GUID de Windows 8 dans la section compatibilité de son manifeste d’application) doit toujours fournir un chemin d’accès de code distinct pour restituer correctement avec un contraste élevé sur Windows 7.</span><span class="sxs-lookup"><span data-stu-id="be6f1-227">In Windows 8, high contrast is a part of visual styles; however, a Windows 8 application (one that includes the Windows 8 GUID in compatibility section of its application manifest) still needs to provide a separate code path to render correctly in high contrast on Windows 7 an earlier.</span></span>
-   <span data-ttu-id="be6f1-228">Si vous utilisez les fonctionnalités de ComCtl32.dll version 6, telles que l’affichage en mosaïque ou le contrôle de lien, vous devez gérer le cas où ces contrôles ne sont pas disponibles sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="be6f1-228">If you use the features in ComCtl32.dll version 6, such as the tile view or link control, you must handle the case where those controls are not available on your user's computer.</span></span> <span data-ttu-id="be6f1-229">ComCtl32.dll version 6 n’est pas redistribuable.</span><span class="sxs-lookup"><span data-stu-id="be6f1-229">ComCtl32.dll version 6 is not redistributable.</span></span>
-   <span data-ttu-id="be6f1-230">Testez votre application pour vous assurer que vous ne vous fiez pas aux fonctionnalités de ComCtl32.dll version 6 sans vérifier d’abord la version actuelle.</span><span class="sxs-lookup"><span data-stu-id="be6f1-230">Test your application to make sure you are not relying on features of ComCtl32.dll version 6 without first checking for the current version.</span></span>
-   <span data-ttu-id="be6f1-231">Ne pas lier à UxTheme. lib.</span><span class="sxs-lookup"><span data-stu-id="be6f1-231">Do not link to UxTheme.lib.</span></span>
-   <span data-ttu-id="be6f1-232">Écrire le code de gestion des erreurs pour les instances lorsque les styles visuels ne fonctionnent pas comme prévu.</span><span class="sxs-lookup"><span data-stu-id="be6f1-232">Write error-handling code for instances when visual styles do not work as expected.</span></span>
-   <span data-ttu-id="be6f1-233">L’installation du manifeste de votre application dans les versions antérieures n’affectera pas le rendu des contrôles.</span><span class="sxs-lookup"><span data-stu-id="be6f1-233">Installing your application's manifest in earlier versions will not affect the rendering of controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be6f1-234">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be6f1-234">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be6f1-235">Styles visuels</span><span class="sxs-lookup"><span data-stu-id="be6f1-235">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 
