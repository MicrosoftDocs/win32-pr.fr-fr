---
description: Les développeurs peuvent étendre l’infrastructure WMI en développant des fournisseurs WMI.
ms.assetid: 87bc5d10-a5d7-444b-b823-4e1a2d63efb3
ms.tgt_platform: multiple
title: Création de fournisseurs WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980d3cd10b7108397a577d54ef93e502fb28d1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042841"
---
# <a name="creating-wmi-providers"></a><span data-ttu-id="3f15e-103">Création de fournisseurs WMI</span><span class="sxs-lookup"><span data-stu-id="3f15e-103">Creating WMI Providers</span></span>

<span data-ttu-id="3f15e-104">Les développeurs peuvent étendre l’infrastructure WMI en développant des fournisseurs WMI.</span><span class="sxs-lookup"><span data-stu-id="3f15e-104">Developers can extend the WMI infrastructure by developing WMI providers.</span></span> <span data-ttu-id="3f15e-105">Les fournisseurs WMI sont des objets COM qui implémentent un ensemble d’interfaces spécifié et, jusqu’à récemment, ont toujours été implémentées en C++.</span><span class="sxs-lookup"><span data-stu-id="3f15e-105">WMI providers are COM objects that implement a specified set of interfaces and, until recently, were always implemented in C++.</span></span> <span data-ttu-id="3f15e-106">Vous pouvez désormais utiliser des langages managés tels que C# pour implémenter des fournisseurs WMI.</span><span class="sxs-lookup"><span data-stu-id="3f15e-106">You can now use managed languages like C# to implement WMI providers.</span></span> <span data-ttu-id="3f15e-107">La version 3,5 du .NET Framework a introduit l’infrastructure des extensions fournisseur WMI qui rend cela possible.</span><span class="sxs-lookup"><span data-stu-id="3f15e-107">Version 3.5 of the .NET framework introduced the WMI Provider Extensions framework that makes this possible.</span></span> <span data-ttu-id="3f15e-108">Pour en savoir plus sur la création de fournisseurs WMI à l’aide de ce Framework, consultez l’article [écrire des fournisseurs WMI couplés à l’aide de l’extension de fournisseur WMI.NET 2,0](/previous-versions/dotnet/articles/cc268228(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="3f15e-108">To learn more about creating WMI providers by using that framework, read the article, [Writing coupled WMI providers using WMI.NET Provider Extension 2.0](/previous-versions/dotnet/articles/cc268228(v=msdn.10)).</span></span>

> [!Note]  
> <span data-ttu-id="3f15e-109">Vous pouvez également créer un fournisseur à l’aide de l’infrastructure de gestion Windows (MI), la version nouvelle génération de WMI.</span><span class="sxs-lookup"><span data-stu-id="3f15e-109">You can also create a provider using Windows Management Infrastructure (MI), the next-generation version of WMI.</span></span> <span data-ttu-id="3f15e-110">Pour plus d’informations, consultez [comment implémenter un fournisseur mi](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider).</span><span class="sxs-lookup"><span data-stu-id="3f15e-110">For more information, see [How to Implement an MI Provider](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider).</span></span>

 

<span data-ttu-id="3f15e-111">Le tableau suivant décrit le contenu de cette section.</span><span class="sxs-lookup"><span data-stu-id="3f15e-111">The following table describes the contents in this section.</span></span>



| <span data-ttu-id="3f15e-112">Rubrique</span><span class="sxs-lookup"><span data-stu-id="3f15e-112">Topic</span></span>                                                      | <span data-ttu-id="3f15e-113">Description</span><span class="sxs-lookup"><span data-stu-id="3f15e-113">Description</span></span>                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="3f15e-114">Fourniture de données à WMI</span><span class="sxs-lookup"><span data-stu-id="3f15e-114">Providing Data to WMI</span></span>](providing-data-to-wmi.md)         | <span data-ttu-id="3f15e-115">Fournit une vue d’ensemble des étapes nécessaires à la création d’un fournisseur WMI.</span><span class="sxs-lookup"><span data-stu-id="3f15e-115">Provides an overview of the steps involved in creating a WMI provider.</span></span>         |
| [<span data-ttu-id="3f15e-116">Développement d’un fournisseur WMI</span><span class="sxs-lookup"><span data-stu-id="3f15e-116">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md) | <span data-ttu-id="3f15e-117">Décrit les tâches que vous devez effectuer lors de la création de différents types de fournisseurs WMI.</span><span class="sxs-lookup"><span data-stu-id="3f15e-117">Describes tasks you must perform when creating various types of WMI providers.</span></span> |



 

 

 
