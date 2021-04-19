---
description: Si votre application héberge une DLL, une extension, un plug-in ou un panneau de configuration tiers, vous souhaiterez peut-être activer un assembly dans votre application&\# 8212 ; sans activer également cet assembly pour les composants hébergés.
ms.assetid: 832957ca-82fc-4600-b469-512621dde921
title: Activation d’un assembly dans une application hébergeant une DLL, une extension ou un panneau de configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b04dd19b18c2cdce4783be47333b9afe53dd1ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527522"
---
# <a name="enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel"></a><span data-ttu-id="4dcdf-103">Activation d’un assembly dans une application hébergeant une DLL, une extension ou un panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="4dcdf-103">Enabling an Assembly in an Application Hosting a DLL, Extension, or Control Panel</span></span>

<span data-ttu-id="4dcdf-104">Si votre application héberge une DLL tierce, une extension, un plug-in ou un panneau de configuration, vous pouvez activer un assembly dans votre application, sans activer également cet assembly pour les composants hébergés.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-104">If your application hosts a third-party DLL, extension, plug-in, or control panel, you may want to enable an assembly in your application—without also enabling this assembly for the hosted components.</span></span> <span data-ttu-id="4dcdf-105">Cela peut être le cas lorsqu’un composant hébergé nécessite des modifications de code pour utiliser l’assembly.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-105">This can be the case when a hosted component requires code changes to use the assembly.</span></span> <span data-ttu-id="4dcdf-106">En tant que développeur d’applications, vous ne pourrez peut-être pas modifier ces composants tiers.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-106">As the application developer, you may be unable to make changes to these third-party components.</span></span> <span data-ttu-id="4dcdf-107">Dans ce cas, vous devez suivre la procédure décrite dans cette section afin que votre application puisse utiliser l’assembly sans affecter les composants hébergés.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-107">In this case, you should follow the procedure described in this section so that your application can use the assembly without affecting the hosted components.</span></span>

-   <span data-ttu-id="4dcdf-108">Pour activer un assembly dans une application sans affecter les dll, extensions, plug-ins et panneaux de contrôle hébergés, un manifeste qui décrit la dépendance de l’application sur l’assembly doit être inclus dans l’application en tant que ressource.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-108">To enable an assembly in an application without affecting any hosted DLLs, extensions, plug-ins, or control panels, a manifest that describes the application's dependence on the assembly should be included in the application as a resource.</span></span> <span data-ttu-id="4dcdf-109">Les composants hébergés qui ne sont pas activés avec l’assembly ne doivent pas inclure de manifestes décrivant cette dépendance.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-109">The hosted components that are not being enabled with the assembly should not include manifests describing this dependency.</span></span>
-   <span data-ttu-id="4dcdf-110">Pour activer un assembly dans une application et ses dll, extensions, plug-ins ou panneaux de contrôle hébergés, incluez les manifestes en tant que ressources dans l’application et ses composants hébergés.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-110">To enable an assembly in an application and its hosted DLLs, extensions, plug-ins, or control panels, include manifests as resources in both the application and its hosted components.</span></span> <span data-ttu-id="4dcdf-111">Les manifestes inclus dans l’application et dans les composants hébergés doivent chacun décrire une dépendance sur l’assembly.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-111">The manifests included in the application and in the hosted components should each describe a dependence on the assembly.</span></span> <span data-ttu-id="4dcdf-112">En général, le développeur d’applications ajoute un manifeste à l’application et le développeur de composants hébergés ajoute un manifeste à la DLL, à l’extension, au plug-in ou au panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-112">Typically, the application developer adds a manifest to the application and the hosted component developer adds a manifest to the DLL, extension, plug-in, or control panel.</span></span>

<span data-ttu-id="4dcdf-113">La méthode suivante peut être utilisée pour ajouter un manifeste à une application ou à un composant hébergé qui est une DLL, une extension, un plug-in ou un panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-113">The following method can be used to add a manifest to an application or a hosted component that is a DLL, extension, plug-in, or control panel.</span></span>

<span data-ttu-id="4dcdf-114">**Pour activer un assembly dans une application ou un composant hébergé.**</span><span class="sxs-lookup"><span data-stu-id="4dcdf-114">**To enable an assembly in an application or hosted component.**</span></span>

1.  <span data-ttu-id="4dcdf-115">Créez un manifeste qui décrit la dépendance de l’application ou de l’extension sur l’assembly.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-115">Author a manifest that describes the dependence of the application or extension on the assembly.</span></span>

    <span data-ttu-id="4dcdf-116">Par exemple, le manifeste pour « YourApplication » peut être créé en copiant l’exemple de manifeste suivant et en remplaçant les valeurs appropriées pour **assemblyIdentity**, **ProcessorArchitecture** et **Description**.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-116">For example, the manifest for "YourApplication" can be created by copying the following sample manifest and substituting correct values for **assemblyIdentity**, **processorArchitecture**, and **description**.</span></span> <span data-ttu-id="4dcdf-117">Définissez la valeur de **ProcessorArchitecture** sur x86 si vous générez sur une plateforme 32 bits et sur ia64 si vous générez sur une plateforme 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-117">Set the value of **processorArchitecture** to x86 if building on a 32-bit platform and to ia64 if building on a 64-bit platform.</span></span> <span data-ttu-id="4dcdf-118">L’élément **Description** contient une description d’option de l’application.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-118">The **description** element contains an option description of the application.</span></span> <span data-ttu-id="4dcdf-119">Pour plus d’informations sur le format du manifeste, consultez [manifestes d’application](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="4dcdf-119">For more information about the manifest format, see [application manifests](application-manifests.md).</span></span>

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

2.  <span data-ttu-id="4dcdf-120">Créez une ressource dans l’application ou l’extension de type RT \_ ID de manifeste 2.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-120">Create a resource in the application or extension of type RT\_MANIFEST id 2.</span></span>

    <span data-ttu-id="4dcdf-121">Par exemple, si le nom de l’application est VotreApplication, l’application doit contenir les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="4dcdf-121">For example, if the application's name is YourApp, the application should contain the following:</span></span>

    ``` syntax
    #define MANIFEST_RESOURCE_ID 2
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

3.  <span data-ttu-id="4dcdf-122">Compilez l’application avec l’indicateur compatible-DISOLATION \_ \_ , ou insérez cette instruction avant l' \# instruction include « Windows. h ».</span><span class="sxs-lookup"><span data-stu-id="4dcdf-122">Compile the application with the -DISOLATION\_AWARE\_ENABLED flag, or insert this statement before the \#include "Windows.h" statement.</span></span> <span data-ttu-id="4dcdf-123">Dans le cas d’une application avec plusieurs modules, l’indicateur de prise en charge de DISOLATION \_ \_ est requis sur tous les modules.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-123">In the case of an application with multiple modules, the -DISOLATION\_AWARE\_ENABLED flag is required on all modules.</span></span>

    ``` syntax
    #define ISOLATION_AWARE_ENABLED 1
    ```

4.  <span data-ttu-id="4dcdf-124">Effectuez un test pour vérifier que les assemblys utilisés par l’application fonctionnent correctement dans l’application et le composant hébergé.</span><span class="sxs-lookup"><span data-stu-id="4dcdf-124">Test to ensure that assemblies that are used by the application work correctly in the application and hosted component.</span></span>

<span data-ttu-id="4dcdf-125">Pour plus d’informations sur l’ajout d’un assembly aux applications sans extensions, consultez [activation d’un assembly dans une application sans extensions](enabling-an-assembly-in-an-application-without-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="4dcdf-125">For more information about adding an assembly to applications without extensions, see [Enabling an Assembly in an Application Without Extensions](enabling-an-assembly-in-an-application-without-extensions.md).</span></span>

 

 



