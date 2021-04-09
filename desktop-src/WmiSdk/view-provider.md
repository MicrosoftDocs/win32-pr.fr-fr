---
description: Le fournisseur d’affichage est une instance et un fournisseur de méthode qui crée des classes basées sur des instances d’autres classes.
ms.assetid: e1992e10-647b-4747-8f3d-b437ef7f3770
ms.tgt_platform: multiple
title: Fournisseur de vues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e49154504dfb2f71ec19c2275851befbdbf9a48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866862"
---
# <a name="view-provider"></a><span data-ttu-id="1ed80-103">Fournisseur de vues</span><span class="sxs-lookup"><span data-stu-id="1ed80-103">View Provider</span></span>

<span data-ttu-id="1ed80-104">Le fournisseur d’affichage est une instance et un fournisseur de méthode qui crée des classes basées sur des instances d’autres classes.</span><span class="sxs-lookup"><span data-stu-id="1ed80-104">The View provider is an instance and method provider that creates new classes based on instances of other classes.</span></span> <span data-ttu-id="1ed80-105">Vous pouvez utiliser le fournisseur d’affichage pour prendre des propriétés à partir de différentes classes sources, d’espaces de noms différents ou de différents ordinateurs et combiner les propriétés en tant que classe unique.</span><span class="sxs-lookup"><span data-stu-id="1ed80-105">You can use the View provider to take properties from different source classes, different namespaces, or different computers and combine the properties as a single class.</span></span>

<span data-ttu-id="1ed80-106">En tant que fournisseur d’instance et de méthode, le fournisseur de vue prend en charge l’interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) standard et les méthodes [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) suivantes :</span><span class="sxs-lookup"><span data-stu-id="1ed80-106">As an instance and method provider, the View provider supports the standard [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface and the following [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods:</span></span>

-   [<span data-ttu-id="1ed80-107">**CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="1ed80-107">**CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="1ed80-108">**ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="1ed80-108">**ExecMethodAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="1ed80-109">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="1ed80-109">**ExecQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="1ed80-110">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="1ed80-110">**GetObjectAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="1ed80-111">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="1ed80-111">**PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

<span data-ttu-id="1ed80-112">Pour plus d’informations sur les qualificateurs utilisés pour définir des classes de fournisseur d’affichage, consultez [qualificateurs spécifiques au fournisseur de vues](qualifiers-specific-to-the-view-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1ed80-112">For more information about the qualifiers use to define View provider classes, see [Qualifiers Specific to the View Provider](qualifiers-specific-to-the-view-provider.md).</span></span>

<span data-ttu-id="1ed80-113">Pour plus d’informations sur les affichages, consultez [liaison de classes](linking-classes-together.md).</span><span class="sxs-lookup"><span data-stu-id="1ed80-113">For more information about views, see [Linking Classes Together](linking-classes-together.md).</span></span>

<span data-ttu-id="1ed80-114">Deux versions du fournisseur d’affichages sont disponibles sur les plateformes 64 bits.</span><span class="sxs-lookup"><span data-stu-id="1ed80-114">Two versions of the View provider are available on 64-bit platforms.</span></span> <span data-ttu-id="1ed80-115">Pour plus d’informations, consultez [obtention et fourniture de données sur un ordinateur 64 bits](getting-and-providing-data-on-a-64-bit-computer.md).</span><span class="sxs-lookup"><span data-stu-id="1ed80-115">For more information, see [Getting and Providing Data on a 64-bit Computer](getting-and-providing-data-on-a-64-bit-computer.md).</span></span>

<span data-ttu-id="1ed80-116">Le fournisseur d’affichage est implémenté dans ViewProv.dll.</span><span class="sxs-lookup"><span data-stu-id="1ed80-116">The View provider is implemented in ViewProv.dll.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ed80-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1ed80-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ed80-118">Fournisseurs WMI</span><span class="sxs-lookup"><span data-stu-id="1ed80-118">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 



