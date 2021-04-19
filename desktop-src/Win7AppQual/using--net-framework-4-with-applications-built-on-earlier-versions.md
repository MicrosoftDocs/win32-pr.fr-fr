---
description: Utilisation de .NET Framework 4 avec des applications basées sur des versions antérieures
ms.assetid: 287E25AD-A560-40DA-A4E6-C46A3123914E
title: Utilisation de .NET Framework 4 avec des applications basées sur des versions antérieures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30eb8f4be1c50904b8d5760f456f3fe20bdd3da
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314942"
---
# <a name="using-net-framework-4-with-applications-built-on-earlier-versions"></a><span data-ttu-id="647c1-103">Utilisation de .NET Framework 4 avec des applications basées sur des versions antérieures</span><span class="sxs-lookup"><span data-stu-id="647c1-103">Using .NET Framework 4 with Applications Built on Earlier Versions</span></span>

## <a name="platform"></a><span data-ttu-id="647c1-104">Plate-forme</span><span class="sxs-lookup"><span data-stu-id="647c1-104">Platform</span></span>

 <span data-ttu-id="647c1-105">**Clients** -Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="647c1-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="647c1-106">**Serveurs** -windows Server 2003, windows Server 2008, windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="647c1-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="647c1-107">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="647c1-107">Feature Impact</span></span>

 <span data-ttu-id="647c1-108">**Gravité** -faible</span><span class="sxs-lookup"><span data-stu-id="647c1-108">**Severity** - Low</span></span>  
<span data-ttu-id="647c1-109">**Fréquence** -élevée</span><span class="sxs-lookup"><span data-stu-id="647c1-109">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="647c1-110">Description</span><span class="sxs-lookup"><span data-stu-id="647c1-110">Description</span></span>

<span data-ttu-id="647c1-111">Le .NET Framework 4 est hautement compatible avec les applications générées à l’aide des versions de .NET Framework antérieures.</span><span class="sxs-lookup"><span data-stu-id="647c1-111">The .NET Framework 4 is highly compatible with applications that are built by using earlier .NET Framework versions.</span></span> <span data-ttu-id="647c1-112">Les principales modifications apportées à .NET Framework 4 sont l’amélioration de la sécurité, de la conformité aux normes, de l’exactitude, de la fiabilité et des performances.</span><span class="sxs-lookup"><span data-stu-id="647c1-112">The primary changes in .NET Framework 4 are to improve security, standards compliance, correctness, reliability, and performance.</span></span>

<span data-ttu-id="647c1-113">Toutefois, .NET Framework 4 n’utilise pas automatiquement sa version du common language runtime (CLR) pour exécuter des applications générées à l’aide de versions antérieures du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="647c1-113">However, .NET Framework 4 does not automatically use its version of the common language runtime (CLR) to run applications that are built by using earlier versions of the .NET Framework.</span></span>

## <a name="manifestation"></a><span data-ttu-id="647c1-114">Manifestation</span><span class="sxs-lookup"><span data-stu-id="647c1-114">Manifestation</span></span>

<span data-ttu-id="647c1-115">Si vous avez créé une application à l’aide d’un .NET Framework antérieur et qu’un utilisateur ouvre cette application sur un ordinateur qui a à la fois .NET Framework 4 et la version antérieure du .NET Framework installée, l’application utilise la version CLR antérieure.</span><span class="sxs-lookup"><span data-stu-id="647c1-115">If you built an application by using an earlier .NET Framework and a user opens that application on a computer that has both .NET Framework 4 and the earlier version of the .NET Framework installed, the application uses the earlier CLR version.</span></span>

<span data-ttu-id="647c1-116">Toutefois, si le .NET Framework 4 est la seule version du runtime qui est installée sur l’ordinateur, l’application lève une exception et invite l’utilisateur à installer la version du Runtime par rapport à laquelle vous avez créé l’application.</span><span class="sxs-lookup"><span data-stu-id="647c1-116">However, if the .NET Framework 4 is the only runtime version that is installed on the computer, the application throws an exception and asks the user to install the runtime version that you built the application against.</span></span>

## <a name="solution"></a><span data-ttu-id="647c1-117">Solution</span><span class="sxs-lookup"><span data-stu-id="647c1-117">Solution</span></span>

<span data-ttu-id="647c1-118">Pour exécuter des applications générées avec des versions antérieures de .NET Framework avec .NET Framework 4, vous devez compiler votre application pour cibler la version de .NET Framework 4 en la spécifiant dans les propriétés de votre projet dans Microsoft Visual Studio, ou vous pouvez spécifier .NET Framework 4 dans l' [**<supportedRuntime> élément**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) dans un fichier de configuration de l’application.</span><span class="sxs-lookup"><span data-stu-id="647c1-118">To run applications that are built with earlier .NET Framework versions with .NET Framework 4, you must compile your application to target the .NET Framework 4 version by specifying it in the properties for your project in Microsoft Visual Studio, or you can specify .NET Framework 4 in the [**<supportedRuntime> element**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) in an application configuration file.</span></span>

<span data-ttu-id="647c1-119">Pour plus d’informations sur la migration vers le .NET Framework 4, consultez [Guide de migration vers le .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) et [compatibilité des versions dans le .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="647c1-119">For more information about how to migrate to the .NET Framework 4, see [Migration Guide to the .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) and [Version Compatibility in the .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).</span></span>

## <a name="compatibility-tests"></a><span data-ttu-id="647c1-120">Tests de compatibilité</span><span class="sxs-lookup"><span data-stu-id="647c1-120">Compatibility Tests</span></span>

<span data-ttu-id="647c1-121">Après avoir apporté les modifications, testez votre application pour vous assurer qu’elle s’exécute correctement.</span><span class="sxs-lookup"><span data-stu-id="647c1-121">After you make the changes, test your application to make sure that it runs correctly.</span></span> <span data-ttu-id="647c1-122">Vous pouvez tester la compatibilité comme décrit dans la rubrique [compatibilité des applications .NET Framework 4](/previous-versions/dd889541(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="647c1-122">You can test compatibility as described in the [.NET Framework 4 Application Compatibility](/previous-versions/dd889541(v=msdn.10)) topic.</span></span>

<span data-ttu-id="647c1-123">Si votre application ou composant ne fonctionne pas après l’installation de .NET Framework 4, envoyez un bogue sur le site Web [Microsoft Connect](https://connect.microsoft.com/visualstudio) .</span><span class="sxs-lookup"><span data-stu-id="647c1-123">If your application or component does not work after .NET Framework 4 is installed, submit a bug through the [Microsoft Connect](https://connect.microsoft.com/visualstudio) website.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="647c1-124">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="647c1-124">Links to Other Resources</span></span>

-   <span data-ttu-id="647c1-125">[**<supportedRuntime> appartient**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="647c1-125">[**<supportedRuntime> element**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))</span></span>
-   <span data-ttu-id="647c1-126">[Guide de migration vers .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="647c1-126">[Migration Guide to the .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))</span></span>
-   <span data-ttu-id="647c1-127">[Compatibilité de versions dans le .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="647c1-127">[Version Compatibility in the .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))</span></span>
-   <span data-ttu-id="647c1-128">**Procédure pas à pas de compatibilité des applications .NET Framework 4 RTM :**<https://msdn.microsoft.com/library/dd889541.aspx></span><span class="sxs-lookup"><span data-stu-id="647c1-128">**.NET Framework 4 RTM Application Compatibility Walkthrough:**<https://msdn.microsoft.com/library/dd889541.aspx></span></span>
-   [<span data-ttu-id="647c1-129">Microsoft Connect</span><span class="sxs-lookup"><span data-stu-id="647c1-129">Microsoft Connect</span></span>](https://connect.microsoft.com/)

 

 
