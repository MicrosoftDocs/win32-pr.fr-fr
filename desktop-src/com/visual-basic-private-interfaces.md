---
title: Interfaces privées Visual Basic
description: Interfaces privées Visual Basic
ms.assetid: 782e5d87-680e-4d0c-b1e6-cf97d1a37ce5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af32f46c02b9b76cdf3dd83e9a22a028aaa88d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029856"
---
# <a name="visual-basic-private-interfaces"></a><span data-ttu-id="51ae2-103">Interfaces privées Visual Basic</span><span class="sxs-lookup"><span data-stu-id="51ae2-103">Visual Basic Private Interfaces</span></span>

<span data-ttu-id="51ae2-104">Deux interfaces implémentées par Visual Basic sont identifiées ici pour les catégories de composants.</span><span class="sxs-lookup"><span data-stu-id="51ae2-104">Two interfaces that are implemented by Visual Basic are identified here for component categories.</span></span> <span data-ttu-id="51ae2-105">Il n’est pas prévu que les contrôles requièrent ces catégories, car il est possible que les contrôles offrent d’autres fonctionnalités lorsque celles-ci ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="51ae2-105">It is not expected that controls should require these categories because it is possible for controls to offer alternative functionality when these are not available.</span></span>

<span data-ttu-id="51ae2-106">L’interface [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) permet aux contrôles de mieux s’intégrer à l’environnement de Visual Basic lors de la mise en forme des données.</span><span class="sxs-lookup"><span data-stu-id="51ae2-106">The [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) interface allows controls to better integrate into the Visual Basic environment when formatting data.</span></span>

<span data-ttu-id="51ae2-107">CATID-{02496840-3AC4-11cf-87B9-00AA006C8166} CATID \_ VBFormat</span><span class="sxs-lookup"><span data-stu-id="51ae2-107">CATID - {02496840-3AC4-11cf-87B9-00AA006C8166} CATID\_VBFormat</span></span>

<span data-ttu-id="51ae2-108">L’interface [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) permet à un contrôle d’énumérer d’autres contrôles sur le formulaire VB.</span><span class="sxs-lookup"><span data-stu-id="51ae2-108">The [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) interface allows a control to enumerate other controls on the VB form.</span></span>

<span data-ttu-id="51ae2-109">CATID-{02496841-3AC4-11cf-87B9-00AA006C8166} CATID \_ VBGetControl</span><span class="sxs-lookup"><span data-stu-id="51ae2-109">CATID - {02496841-3AC4-11cf-87B9-00AA006C8166} CATID\_VBGetControl</span></span>

<span data-ttu-id="51ae2-110">Deux interfaces privées supplémentaires, [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) et [**IGetOleObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject), sont décrites ici, même si elles ne définissent pas les catégories de composants.</span><span class="sxs-lookup"><span data-stu-id="51ae2-110">Two additional private interfaces, [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) and [**IGetOleObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject), are described here even though they do not define component categories.</span></span> <span data-ttu-id="51ae2-111">L’utilisation de ces quatre interfaces n’est pas recommandée, car elles ne sont pas prises en charge par les conteneurs autres que Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="51ae2-111">Use of these four interfaces is not recommended because they are not supported by containers other than Visual Basic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="51ae2-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="51ae2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51ae2-113">Catégories de composant</span><span class="sxs-lookup"><span data-stu-id="51ae2-113">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 




