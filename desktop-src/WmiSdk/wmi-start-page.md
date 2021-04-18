---
description: Windows Management Instrumentation (WMI) est l’infrastructure de données et d’opérations de gestion sur les systèmes d’exploitation Windows.
ms.assetid: 4804152f-2042-4c6a-83c6-75c5e1ab7a04
ms.tgt_platform: multiple
title: Windows Management Instrumentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec2313ca7ee744ebe6f14be42a33e2e5878960b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533829"
---
# <a name="windows-management-instrumentation"></a><span data-ttu-id="3380e-103">Windows Management Instrumentation</span><span class="sxs-lookup"><span data-stu-id="3380e-103">Windows Management Instrumentation</span></span>

## <a name="purpose"></a><span data-ttu-id="3380e-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="3380e-104">Purpose</span></span>

<span data-ttu-id="3380e-105">Windows Management Instrumentation (WMI) est l’infrastructure de données et d’opérations de gestion sur les systèmes d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="3380e-105">Windows Management Instrumentation (WMI) is the infrastructure for management data and operations on Windows-based operating systems.</span></span> <span data-ttu-id="3380e-106">Vous pouvez écrire des scripts ou des applications WMI pour automatiser des tâches administratives sur des ordinateurs distants, mais WMI fournit également des données de gestion à d’autres parties du système d’exploitation et des produits, par exemple System Center Operations Manager, anciennement Microsoft Operations Manager (MOM) ou Windows Remote Management ([WinRM](/windows/desktop/WinRM/portal)).</span><span class="sxs-lookup"><span data-stu-id="3380e-106">You can write WMI scripts or applications to automate administrative tasks on remote computers but WMI also supplies management data to other parts of the operating system and products, for example System Center Operations Manager, formerly Microsoft Operations Manager (MOM), or Windows Remote Management ([WinRM](/windows/desktop/WinRM/portal)).</span></span>

> [!Note]  
> <span data-ttu-id="3380e-107">La documentation suivante est destinée aux développeurs et aux administrateurs informatiques.</span><span class="sxs-lookup"><span data-stu-id="3380e-107">The following documentation is targeted for developers and IT administrators.</span></span> <span data-ttu-id="3380e-108">Si vous êtes un utilisateur final qui a rencontré un message d’erreur concernant WMI, vous devez accéder à [support Microsoft](https://support.microsoft.com/) et rechercher le code d’erreur que vous voyez dans le message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="3380e-108">If you are an end-user that has experienced an error message concerning WMI, you should go to [Microsoft Support](https://support.microsoft.com/) and search for the error code you see on the error message.</span></span> <span data-ttu-id="3380e-109">Pour plus d’informations sur la résolution des problèmes liés aux scripts WMI et au service WMI, consultez [WMI ne fonctionne pas.](/previous-versions/tn-archive/ff406382(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="3380e-109">For more information about troubleshooting problems with WMI scripts and the WMI service, see [WMI Isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10))</span></span>

 

> [!Note]  
> <span data-ttu-id="3380e-110">WMI est entièrement pris en charge par Microsoft ; Toutefois, la version la plus récente des scripts et du contrôle d’administration est disponible par le biais de l’infrastructure de gestion Windows (MI).</span><span class="sxs-lookup"><span data-stu-id="3380e-110">WMI is fully supported by Microsoft; however, the latest version of administrative scripting and control is available through the Windows Management Infrastructure (MI).</span></span> <span data-ttu-id="3380e-111">MI est entièrement compatible avec les versions précédentes de WMI et fournit un hôte de fonctionnalités et d’avantages qui facilitent la conception et le développement de fournisseurs et de clients.</span><span class="sxs-lookup"><span data-stu-id="3380e-111">MI is fully compatible with previous versions of WMI, and provides a host of features and benefits that make designing and developing providers and clients easier than ever.</span></span> <span data-ttu-id="3380e-112">Pour plus d’informations, consultez [infrastructure de gestion Windows (mi)](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure).</span><span class="sxs-lookup"><span data-stu-id="3380e-112">For more information, see [Windows Management Infrastructure (MI)](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="3380e-113">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="3380e-113">Where applicable</span></span>

<span data-ttu-id="3380e-114">WMI peut être utilisé dans toutes les applications Windows et s’avère particulièrement utile dans les applications d’entreprise et les scripts d’administration.</span><span class="sxs-lookup"><span data-stu-id="3380e-114">WMI can be used in all Windows-based applications, and is most useful in enterprise applications and administrative scripts.</span></span>

<span data-ttu-id="3380e-115">Les administrateurs système peuvent trouver des informations sur l’utilisation de WMI dans le [scriptcenter](https://www.microsoft.com/technet/scriptcenter/default.mspx)TechNet et dans divers ouvrages sur WMI.</span><span class="sxs-lookup"><span data-stu-id="3380e-115">System administrators can find information about using WMI at the TechNet [ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx), and in various books about WMI.</span></span> <span data-ttu-id="3380e-116">Pour plus d’informations, consultez [informations supplémentaires](further-information.md).</span><span class="sxs-lookup"><span data-stu-id="3380e-116">For more information, see [Further Information](further-information.md).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="3380e-117">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="3380e-117">Developer audience</span></span>

<span data-ttu-id="3380e-118">WMI est conçu pour les programmeurs qui utilisent C/C++, l’application Microsoft Visual Basic, ou un langage de script qui a un moteur sur Windows et gère les objets Microsoft ActiveX.</span><span class="sxs-lookup"><span data-stu-id="3380e-118">WMI is designed for programmers who use C/C++, the Microsoft Visual Basic application, or a scripting language that has an engine on Windows and handles Microsoft ActiveX objects.</span></span> <span data-ttu-id="3380e-119">Bien qu’une certaine connaissance de la programmation COM soit utile, les développeurs C++ qui écrivent des applications peuvent trouver de bons exemples pour commencer à [créer une application WMI à l’aide de C++](creating-a-wmi-application-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="3380e-119">While some familiarity with COM programming is helpful, C++ developers who are writing applications can find good examples for getting started at [Creating a WMI Application Using C++](creating-a-wmi-application-using-c-.md).</span></span>

<span data-ttu-id="3380e-120">Pour développer des fournisseurs de code managé ou des applications en C# ou Visual Basic .NET à l’aide du .NET Framework, consultez [WMI dans .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).</span><span class="sxs-lookup"><span data-stu-id="3380e-120">To develop managed code providers or applications in C# or Visual Basic .NET using the .NET Framework, see [WMI in .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).</span></span>

<span data-ttu-id="3380e-121">De nombreux administrateurs et professionnels de l’informatique accèdent à WMI via PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3380e-121">Many administrators and IT professionals access WMI through PowerShell.</span></span> <span data-ttu-id="3380e-122">L’applet de commande obtenir-WMI pour PowerShell vous permet de récupérer des informations pour un référentiel WMI local ou distant.</span><span class="sxs-lookup"><span data-stu-id="3380e-122">The Get-WMI cmdlet for PowerShell enables you to retrieve information for a local or remote WMI repository.</span></span> <span data-ttu-id="3380e-123">Par conséquent, plusieurs rubriques et classes, en particulier dans la section [création de clients WMI](creating-wmi-clients.md) , contiennent des exemples PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3380e-123">As such, a number of topics and classes, especially in the [Creating WMI Clients](creating-wmi-clients.md) section, contain PowerShell examples.</span></span> <span data-ttu-id="3380e-124">Pour plus d’informations sur l’utilisation de PowerShell, consultez [Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) et [écriture de scripts avec Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).</span><span class="sxs-lookup"><span data-stu-id="3380e-124">For additional information on using PowerShell, see [Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) and [Scripting with Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="3380e-125">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="3380e-125">Run-time requirements</span></span>

<span data-ttu-id="3380e-126">Pour plus d’informations sur le système d’exploitation requis pour utiliser un élément d’API spécifique ou une classe WMI, consultez la section relative à la configuration requise de chaque rubrique dans la documentation WMI.</span><span class="sxs-lookup"><span data-stu-id="3380e-126">For more information about which operating system is required to use a specific API element or WMI class, see the Requirements section of each topic in the WMI documentation.</span></span>

<span data-ttu-id="3380e-127">Si un composant attendu semble manquer, consultez [disponibilité du système d’exploitation des composants WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="3380e-127">If an expected component appears to be missing, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

<span data-ttu-id="3380e-128">Vous n’avez pas besoin de télécharger ou d’installer un kit de développement logiciel (SDK) spécifique pour créer des scripts ou des applications pour WMI.</span><span class="sxs-lookup"><span data-stu-id="3380e-128">You do not need to download or install a specific software development (SDK) in order to create scripts or applications for WMI.</span></span> <span data-ttu-id="3380e-129">Toutefois, certains outils d’administration WMI sont utiles aux développeurs.</span><span class="sxs-lookup"><span data-stu-id="3380e-129">However, there are some WMI administrative tools that developers find useful.</span></span> <span data-ttu-id="3380e-130">Pour plus d’informations, consultez la section téléchargements dans [informations supplémentaires](further-information.md).</span><span class="sxs-lookup"><span data-stu-id="3380e-130">For more information, see the Downloads section in [Further Information](further-information.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3380e-131">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="3380e-131">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="3380e-132">À propos de WMI</span><span class="sxs-lookup"><span data-stu-id="3380e-132">About WMI</span></span>](about-wmi.md)
</dt> <dd>

<span data-ttu-id="3380e-133">Informations générales sur WMI.</span><span class="sxs-lookup"><span data-stu-id="3380e-133">General information about WMI.</span></span>

</dd> <dt>

[<span data-ttu-id="3380e-134">Utilisation de WMI</span><span class="sxs-lookup"><span data-stu-id="3380e-134">Using WMI</span></span>](using-wmi.md)
</dt> <dd>

<span data-ttu-id="3380e-135">Informations sur le développement d’applications pour utiliser WMI, qui comprend des informations sur les outils.</span><span class="sxs-lookup"><span data-stu-id="3380e-135">Information about how to develop applications to use WMI, which includes information about tools.</span></span>

</dd> <dt>

[<span data-ttu-id="3380e-136">Référence WMI</span><span class="sxs-lookup"><span data-stu-id="3380e-136">WMI Reference</span></span>](wmi-reference.md)
</dt> <dd>

<span data-ttu-id="3380e-137">Documentation relative aux classes WMI, aux classes WMI C++, à l’API COM WMI, à l’API de script et à d’autres documents de référence WMI.</span><span class="sxs-lookup"><span data-stu-id="3380e-137">Documentation about the WMI classes, WMI C++ classes, WMI COM API, Scripting API, and other WMI reference material.</span></span>

</dd> </dl>

 

 
