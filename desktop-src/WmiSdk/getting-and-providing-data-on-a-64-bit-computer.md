---
description: Les applications clientes et les scripts qui accèdent aux fournisseurs standard WMI 32 bits continuent de fonctionner normalement lorsqu’ils s’exécutent sur un système d’exploitation 64 bits.
ms.assetid: 68819bea-a48d-4de1-a50d-f03ae04775f5
ms.tgt_platform: multiple
title: Obtention et fourniture de données sur un ordinateur 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7d8ff5430a7c47b652bfbcca05d2f53ba857d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567683"
---
# <a name="getting-and-providing-data-on-a-64-bit-computer"></a><span data-ttu-id="9618e-103">Obtention et fourniture de données sur un ordinateur 64 bits</span><span class="sxs-lookup"><span data-stu-id="9618e-103">Getting and Providing Data on a 64-bit Computer</span></span>

<span data-ttu-id="9618e-104">Les applications clientes et les scripts qui accèdent aux fournisseurs standard WMI 32 bits continuent de fonctionner normalement lorsqu’ils s’exécutent sur un système d’exploitation 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9618e-104">Client applications and scripts that access standard WMI 32-bit providers continue to operate normally when running on a 64-bit operating system.</span></span> <span data-ttu-id="9618e-105">Seuls deux fournisseurs préinstallés, le [fournisseur de Registre système](/previous-versions/windows/desktop/regprov/system-registry-provider) et le [fournisseur de vues](view-provider.md), ont des versions 64 bits qui s’exécutent côte à côte avec les versions 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9618e-105">Only two preinstalled providers, the [System Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider) and the [View provider](view-provider.md), have 64-bit versions which run side-by-side with the 32-bit versions.</span></span> <span data-ttu-id="9618e-106">Toutefois, une application 32 bits qui demande des instances de Windows Driver Model de 32 bits reçoit les instances de classe WDM 64 bits par défaut sur un système d’exploitation 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9618e-106">However, a 32-bit application that requests 32-bit Windows Driver Model (WDM) instances receives the default 64-bit WDM class instances on a 64-bit operating system.</span></span>

## <a name="accessing-default-and-nondefault-provider-data"></a><span data-ttu-id="9618e-107">Accès aux données de fournisseur par défaut et par défaut</span><span class="sxs-lookup"><span data-stu-id="9618e-107">Accessing Default and Nondefault Provider Data</span></span>

<span data-ttu-id="9618e-108">En règle générale, les writers de fournisseur n’incluent pas les versions 32 bits et 64 bits d’un fournisseur dans le même système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="9618e-108">Generally, provider writers do not include both 32-bit and 64-bit versions of a provider in the same operating system.</span></span> <span data-ttu-id="9618e-109">S’il n’existe aucun fournisseur 64 bits, un fournisseur 32 bits peut continuer à s’exécuter via les fonctionnalités de WOW64.</span><span class="sxs-lookup"><span data-stu-id="9618e-109">If no 64-bit provider exists, a 32-bit provider can continue to run through the facilities of WOW64.</span></span> <span data-ttu-id="9618e-110">Un fournisseur 64 bits peut également fournir des données à une application 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9618e-110">A 64-bit provider can likewise supply data to a 32-bit application.</span></span> <span data-ttu-id="9618e-111">Pour plus d’informations, consultez [fourniture de données WMI sur une plateforme 64 bits](providing-wmi-data-on-a-64-bit-platform.md).</span><span class="sxs-lookup"><span data-stu-id="9618e-111">For more information, see [Providing WMI Data on a 64-bit Platform](providing-wmi-data-on-a-64-bit-platform.md).</span></span>

<span data-ttu-id="9618e-112">Si deux versions existent, les applications clientes et les scripts peuvent utiliser les paramètres de contexte disponibles dans l' [API com](com-api-for-wmi.md) et l' [API de script](scripting-api-for-wmi.md) pour se connecter explicitement à un fournisseur WMI non par défaut spécifique, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="9618e-112">If two versions exist, client applications and scripts can use the context parameters available in the [COM API](com-api-for-wmi.md) and the [Scripting API](scripting-api-for-wmi.md) to connect explicitly to a specific nondefault WMI provider, if it is available.</span></span> <span data-ttu-id="9618e-113">Pour plus d’informations, consultez [demande de données WMI sur une plateforme 64 bits](requesting-wmi-data-on-a-64-bit-platform.md).</span><span class="sxs-lookup"><span data-stu-id="9618e-113">For more information, see [Requesting WMI Data on a 64-bit Platform](requesting-wmi-data-on-a-64-bit-platform.md).</span></span>

<span data-ttu-id="9618e-114">Le diagramme suivant montre les connexions par défaut et par défaut, en utilisant le registre comme exemple pour lequel deux fournisseurs peuvent coexister côte à côte sur une plateforme 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9618e-114">The following diagram shows the default and nondefault connections, using the registry as an example for which two providers can exist side-by-side on a 64-bit platform.</span></span>

![connexions par défaut et par défaut sur une plateforme 64 bits](images/32-64bit-registry.png)

## <a name="related-topics"></a><span data-ttu-id="9618e-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9618e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9618e-117">Demande de données WMI sur une plateforme 64 bits</span><span class="sxs-lookup"><span data-stu-id="9618e-117">Requesting WMI Data on a 64-bit Platform</span></span>](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[<span data-ttu-id="9618e-118">Fourniture de données WMI sur une plateforme 64 bits</span><span class="sxs-lookup"><span data-stu-id="9618e-118">Providing WMI Data on a 64-bit Platform</span></span>](providing-wmi-data-on-a-64-bit-platform.md)
</dt> </dl>

 

 
