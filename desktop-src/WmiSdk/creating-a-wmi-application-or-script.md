---
description: Tout langage de script, tel que VBScript, qui fonctionne avec les objets ActiveX peut accéder aux données WMI. Les applications peuvent accéder à WMI en C++, à l’aide de l’API COM pour WMI ou dans Visual Basic, à l’aide de la bibliothèque de types wbemdisp. tlb et de l’API de script pour WMI. .
ms.assetid: c0d18827-6b36-4817-8cd9-06cd0f267b28
ms.tgt_platform: multiple
title: Création d’une application ou d’un script WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b27e3cffd7e4d9bea4ce36e7c0da77ae5d72cdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521941"
---
# <a name="creating-a-wmi-application-or-script"></a><span data-ttu-id="a03ed-105">Création d’une application ou d’un script WMI</span><span class="sxs-lookup"><span data-stu-id="a03ed-105">Creating a WMI Application or Script</span></span>

<span data-ttu-id="a03ed-106">Tout langage de script, tel que VBScript, qui fonctionne avec les objets ActiveX peut accéder aux données WMI.</span><span class="sxs-lookup"><span data-stu-id="a03ed-106">Any scripting language, such as VBScript, that works with ActiveX objects can access WMI data.</span></span> <span data-ttu-id="a03ed-107">Les applications peuvent accéder à WMI en C++, à l’aide [de l’API com pour WMI](com-api-for-wmi.md) ou dans Visual Basic, à l’aide de la [bibliothèque de types](using-the-wmi-scripting-type-library.md) wbemdisp. tlb et de l' [API de script pour WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="a03ed-107">Applications can access WMI in C++, using the [COM API for WMI](com-api-for-wmi.md) or in Visual Basic, using the Wbemdisp.tlb [type library](using-the-wmi-scripting-type-library.md) and the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span> <span data-ttu-id="a03ed-108">.</span><span class="sxs-lookup"><span data-stu-id="a03ed-108">.</span></span> <span data-ttu-id="a03ed-109">Vous pouvez obtenir des données via WMI en écrivant un script, une page de Active Server (ASP) ou une application HTML (HTA).</span><span class="sxs-lookup"><span data-stu-id="a03ed-109">You can obtain data through WMI by writing a script, an Active Server Page (ASP), or an HTML application (HTA).</span></span> <span data-ttu-id="a03ed-110">Vous pouvez également utiliser Windows PowerShell pour obtenir des données ou écrire des scripts.</span><span class="sxs-lookup"><span data-stu-id="a03ed-110">You can also use Windows PowerShell to obtain data or write scripts.</span></span> <span data-ttu-id="a03ed-111">Pour plus d’informations, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) et [prise en main avec Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="a03ed-111">For more information, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) and [Getting Started with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span></span> <span data-ttu-id="a03ed-112">Le ScriptCenter TechNet [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) de contient des centaines d’exemples de script.</span><span class="sxs-lookup"><span data-stu-id="a03ed-112">The TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) contains hundreds of scripting examples.</span></span> <span data-ttu-id="a03ed-113">Pour plus d’informations sur l’impression et les ressources en ligne, consultez plus d' [informations](further-information.md).</span><span class="sxs-lookup"><span data-stu-id="a03ed-113">For more information about print and online resources, see [Further Information](further-information.md).</span></span>

<span data-ttu-id="a03ed-114">La procédure suivante décrit comment se connecter au service WMI et au magasin de données.</span><span class="sxs-lookup"><span data-stu-id="a03ed-114">The following procedure describes how to connect to the WMI service and data store.</span></span>

<span data-ttu-id="a03ed-115">**Pour vous connecter au service WMI et à la Banque de données**</span><span class="sxs-lookup"><span data-stu-id="a03ed-115">**To connect to the WMI service and data store**</span></span>

1.  <span data-ttu-id="a03ed-116">Localisez le service WMI sur un ordinateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="a03ed-116">Locate the WMI service on a specific machine.</span></span>
2.  <span data-ttu-id="a03ed-117">Connectez-vous à un ou plusieurs espaces de noms WMI.</span><span class="sxs-lookup"><span data-stu-id="a03ed-117">Connect to one or more WMI namespaces.</span></span>

<span data-ttu-id="a03ed-118">Ces opérations sont différentes en C++, Visual Basic, .NET Framework langages ou lors de l’utilisation d’un script.</span><span class="sxs-lookup"><span data-stu-id="a03ed-118">These operations are different in C++, Visual Basic, .NET Framework languages, or when using a script.</span></span> <span data-ttu-id="a03ed-119">Les scripts et les applications Visual Basic doivent accéder aux classes dont les instances sont fournies avec des données par les fournisseurs existants.</span><span class="sxs-lookup"><span data-stu-id="a03ed-119">Scripts and Visual Basic applications must access classes whose instances are supplied with data by existing providers.</span></span> <span data-ttu-id="a03ed-120">Mais les applications écrites en C++ peuvent en faire plus.</span><span class="sxs-lookup"><span data-stu-id="a03ed-120">But applications written in C++ can do more.</span></span> <span data-ttu-id="a03ed-121">Par exemple, une application écrite en C++ peut envoyer des événements, mais un script WMI peut s’abonner uniquement pour recevoir des événements.</span><span class="sxs-lookup"><span data-stu-id="a03ed-121">For example, an application written in C++ can send events, but a WMI script can only subscribe to receive events.</span></span>

<span data-ttu-id="a03ed-122">Un fournisseur WMI peut être écrit uniquement en C++ ou à l’aide de l' .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="a03ed-122">A WMI provider can be written only in C++ or using the .NET Framework.</span></span> <span data-ttu-id="a03ed-123">Pour plus d’informations sur l’écriture d’applications en C# ou Visual Basic .NET, consultez [vue d’ensemble de WMI .net](/previous-versions/bb404655(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="a03ed-123">For more information about writing applications in C# or Visual Basic .NET, see [WMI .NET Overview](/previous-versions/bb404655(v=vs.90)).</span></span>

<span data-ttu-id="a03ed-124">Pour plus d’informations sur la création d’applications et de scripts pour WMI, consultez :</span><span class="sxs-lookup"><span data-stu-id="a03ed-124">For more information about creating applications and scripts for WMI, see:</span></span>

-   [<span data-ttu-id="a03ed-125">Création d’une application WMI à l’aide de C++</span><span class="sxs-lookup"><span data-stu-id="a03ed-125">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
-   [<span data-ttu-id="a03ed-126">Création d’un script WMI</span><span class="sxs-lookup"><span data-stu-id="a03ed-126">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
-   [<span data-ttu-id="a03ed-127">Création d’un client WMI géré</span><span class="sxs-lookup"><span data-stu-id="a03ed-127">Creating a Managed WMI Client</span></span>](creating-a-managed-wmi-client.md)

<span data-ttu-id="a03ed-128">Pour effectuer la plupart des tâches, utilisez les [classes WMI](wmi-classes.md)préinstallées.</span><span class="sxs-lookup"><span data-stu-id="a03ed-128">To perform most tasks, use the preinstalled [WMI classes](wmi-classes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a03ed-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a03ed-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a03ed-130">Utilisation de WMI</span><span class="sxs-lookup"><span data-stu-id="a03ed-130">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 
