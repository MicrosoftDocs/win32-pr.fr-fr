---
description: Si votre application n’héberge pas de DLL, d’extension, de plug-in ou de panneau de configuration, vous pouvez utiliser la méthode décrite dans cette section pour activer un assembly pour votre application.
ms.assetid: d043ec1b-ac31-45fb-9232-eec42aef4ac3
title: Activation d’un assembly dans une application sans extensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1bbcfe510f5a3cdbce323f01cb9342ce236c7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535659"
---
# <a name="enabling-an-assembly-in-an-application-without-extensions"></a><span data-ttu-id="5b8e5-103">Activation d’un assembly dans une application sans extensions</span><span class="sxs-lookup"><span data-stu-id="5b8e5-103">Enabling an Assembly in an Application Without Extensions</span></span>

<span data-ttu-id="5b8e5-104">Si votre application n’héberge pas de DLL, d’extension, de plug-in ou de panneau de configuration, vous pouvez utiliser la méthode décrite dans cette section pour activer un assembly pour votre application.</span><span class="sxs-lookup"><span data-stu-id="5b8e5-104">If your application does not host a DLL, extension, plug-in, or control panel, you can use the method described in this section to enable an assembly for your application.</span></span> <span data-ttu-id="5b8e5-105">Pour plus d’informations sur l’ajout d’un assembly aux applications avec des extensions, consultez [activation d’un assembly dans une application hébergeant une dll, une extension ou le panneau de configuration](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).</span><span class="sxs-lookup"><span data-stu-id="5b8e5-105">For more information about adding an assembly to applications with extensions, see [Enabling an Assembly in an Application Hosting a DLL, Extension, or Control Panel](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).</span></span>

<span data-ttu-id="5b8e5-106">**Pour activer un assembly dans une application sans aucun composant hébergé**</span><span class="sxs-lookup"><span data-stu-id="5b8e5-106">**To enable an assembly in an application without any hosted components**</span></span>

1.  <span data-ttu-id="5b8e5-107">Créez un manifeste qui décrit la dépendance de l’application ou de l’extension sur l’assembly.</span><span class="sxs-lookup"><span data-stu-id="5b8e5-107">Author a manifest that describes the dependence of the application or extension on the assembly.</span></span>

    <span data-ttu-id="5b8e5-108">Par exemple, le manifeste pour « YourApplication » peut être créé en copiant l’exemple de manifeste suivant et en remplaçant les valeurs appropriées pour **assemblyIdentity**, **ProcessorArchitecture** et **Description**.</span><span class="sxs-lookup"><span data-stu-id="5b8e5-108">For example, the manifest for "YourApplication" can be created by copying the following sample manifest and substituting correct values for **assemblyIdentity**, **processorArchitecture**, and **description**.</span></span> <span data-ttu-id="5b8e5-109">Définissez la valeur de **ProcessorArchitecture** sur x86 si vous générez sur une plateforme 32 bits, et sur ia64 si vous générez sur une plateforme 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5b8e5-109">Set the value of **processorArchitecture** to x86 if building on a 32-bit platform, and to ia64 if building on a 64-bit platform.</span></span> <span data-ttu-id="5b8e5-110">L’élément **Description** contient une description d’option de l’application.</span><span class="sxs-lookup"><span data-stu-id="5b8e5-110">The **description** element contains an option description of the application.</span></span> <span data-ttu-id="5b8e5-111">Pour plus d’informations sur le format du manifeste, consultez [manifestes d’application](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="5b8e5-111">For more information about the manifest format, see [application manifests](application-manifests.md).</span></span>

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="x86"
        name="YourCompanyName.YourDivision.YourApp"
        type="win32"
    />
    <description>Your app description here</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Proseware.Research.SampleAssembly"
                version="6.0.0.0"
                processorArchitecture="X86"
                publicKeyToken="0000000000000000"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

2.  <span data-ttu-id="5b8e5-112">Ajoutez le manifeste à l’application en tant que ressource dans le fichier d’en-tête binaire de l’application.</span><span class="sxs-lookup"><span data-stu-id="5b8e5-112">Add the manifest to the application as a resource in the application's binary executable header file.</span></span> <span data-ttu-id="5b8e5-113">Il n’est pas recommandé d’ajouter le manifeste à l’application en tant que fichier manifeste externe.</span><span class="sxs-lookup"><span data-stu-id="5b8e5-113">It is not recommended that you add the manifest to the application as an external manifest file.</span></span>

    <span data-ttu-id="5b8e5-114">Pour ajouter le manifeste en tant que ressource, créez une ressource dans l’application de type RT \_ ID de manifeste 1.</span><span class="sxs-lookup"><span data-stu-id="5b8e5-114">To add the manifest as a resource, create a resource in the application of type RT\_MANIFEST id 1.</span></span> <span data-ttu-id="5b8e5-115">Par exemple, si le nom de l’application est VotreApplication, le fichier d’en-tête de l’application doit contenir les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="5b8e5-115">For example, if the application's name is YourApp, the application's header file should contain the following:</span></span>

    ``` syntax
    #define MANIFEST_RESOURCE_ID 1
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

    <span data-ttu-id="5b8e5-116">Si vous ajoutez plutôt le manifeste en tant que fichier manifeste externe, assurez-vous que l’installation copie le fichier manifeste dans le dossier contenant le fichier exécutable de l’application.</span><span class="sxs-lookup"><span data-stu-id="5b8e5-116">If you instead add the manifest as an external manifest file, be sure that the installation copies the manifest file into the folder containing the application's executable file.</span></span>

3.  <span data-ttu-id="5b8e5-117">Testez pour vérifier que les assemblys utilisés par l’application fonctionnent correctement dans l’application.</span><span class="sxs-lookup"><span data-stu-id="5b8e5-117">Test to ensure that assemblies used by the application work correctly in the application.</span></span>

 

 



