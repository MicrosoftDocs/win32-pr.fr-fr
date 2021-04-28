---
description: Sous-ensemble de .NET 2,0 maintenant sur Server Core
ms.assetid: f91c4604-b2d6-41e5-be66-bbc8a4f0e28e
title: Sous-ensemble de .NET 2,0 maintenant sur Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6ef839f525acf190df384e3fe8394f2b785d45
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116147"
---
# <a name="subset-of-net-20-now-on-server-core"></a><span data-ttu-id="a9c6a-103">Sous-ensemble de .NET 2,0 maintenant sur Server Core</span><span class="sxs-lookup"><span data-stu-id="a9c6a-103">Subset of .NET 2.0 Now on Server Core</span></span>

## <a name="platform"></a><span data-ttu-id="a9c6a-104">Plateforme</span><span class="sxs-lookup"><span data-stu-id="a9c6a-104">Platform</span></span>

<span data-ttu-id="a9c6a-105">**Serveurs** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a9c6a-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="a9c6a-106">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="a9c6a-106">Feature Impact</span></span>

 <span data-ttu-id="a9c6a-107">**Gravité** -faible</span><span class="sxs-lookup"><span data-stu-id="a9c6a-107">**Severity** - Low</span></span>  
<span data-ttu-id="a9c6a-108">**Fréquence** -faible</span><span class="sxs-lookup"><span data-stu-id="a9c6a-108">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="a9c6a-109">Description</span><span class="sxs-lookup"><span data-stu-id="a9c6a-109">Description</span></span>

<span data-ttu-id="a9c6a-110">L’option d’installation Server Core pour Windows Server 2008 R2 comprend désormais un sous-ensemble des .NET Framework 2,0.</span><span class="sxs-lookup"><span data-stu-id="a9c6a-110">The Server Core installation option for Windows Server 2008 R2 now includes a subset of the .NET Framework 2.0.</span></span> <span data-ttu-id="a9c6a-111">Le sous-ensemble est la fonctionnalité de .NET 2,0 qui s’aligne sur les fonctionnalités de Server Core. aucun binaire n’a été ajouté à la base Server Core pour permettre à n’importe quelle partie de .NET 2,0 de fonctionner.</span><span class="sxs-lookup"><span data-stu-id="a9c6a-111">The subset is the functionality in .NET 2.0 that aligns with the functionality in Server Core; no binaries were added to the Server Core base to allow any portion of .NET 2.0 to function.</span></span>

<span data-ttu-id="a9c6a-112">Il n’existait aucune prise en charge .NET dans l’option d’installation Server Core pour Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a9c6a-112">There was no .NET support in the Server Core installation option for Windows Server 2008.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="a9c6a-113">Manifeste de l’impact</span><span class="sxs-lookup"><span data-stu-id="a9c6a-113">Manifestation of Impact</span></span>

<span data-ttu-id="a9c6a-114">Cela permet à certaines applications basées sur .NET 2,0 de s’exécuter sur Server Core dans Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="a9c6a-114">This allows some .NET 2.0 based-applications to run on Server Core in Windows Server 2008 R2.</span></span>

## <a name="testing"></a><span data-ttu-id="a9c6a-115">Test</span><span class="sxs-lookup"><span data-stu-id="a9c6a-115">Testing</span></span>

<span data-ttu-id="a9c6a-116">Vérifiez que les classes .NET utilisées par votre code sont incluses dans Server Core.</span><span class="sxs-lookup"><span data-stu-id="a9c6a-116">Verify that the .NET classes your code uses is included in Server Core.</span></span> <span data-ttu-id="a9c6a-117">Testez également toutes les applications qui exécutent ce code sur Server Core.</span><span class="sxs-lookup"><span data-stu-id="a9c6a-117">Also test any applications that run this code on Server Core.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="a9c6a-118">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="a9c6a-118">Links to Other Resources</span></span>

-   <span data-ttu-id="a9c6a-119">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a9c6a-119">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span></span>
-   [<span data-ttu-id="a9c6a-120">Blog Server Core</span><span class="sxs-lookup"><span data-stu-id="a9c6a-120">Server Core Blog</span></span>](https://blogs.technet.com/server_core/archive/2008/11/25/net-2-0-and-server-core-in-windows-server-2008-r2.aspx)
-   <span data-ttu-id="a9c6a-121">*Voir aussi* la section Server Core du *Kit de développement logiciel (SDK) Windows Server 2008 R2* quand elle est disponible</span><span class="sxs-lookup"><span data-stu-id="a9c6a-121">*See also* the Server Core section of the *Windows Server 2008 R2 SDK* when it becomes available</span></span>

> [!Note]  
> <span data-ttu-id="a9c6a-122">Ces ressources peuvent ne pas être disponibles dans certaines langues et pays/régions.</span><span class="sxs-lookup"><span data-stu-id="a9c6a-122">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
