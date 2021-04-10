---
description: Interfaces du distributeur de ressources COM+
ms.assetid: 66ee4dd6-15d2-49e8-89a3-6fbb5770cabf
title: Interfaces du distributeur de ressources COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a6ea5c5c09f67f86b42ebf5b881f1d19ad1501
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860857"
---
# <a name="com-resource-dispenser-interfaces"></a><span data-ttu-id="2e807-103">Interfaces du distributeur de ressources COM+</span><span class="sxs-lookup"><span data-stu-id="2e807-103">COM+ Resource Dispenser Interfaces</span></span>

<span data-ttu-id="2e807-104">Les composants d’application utilisent des distributeurs de ressources pour accéder aux informations partagées.</span><span class="sxs-lookup"><span data-stu-id="2e807-104">Application components use resource dispensers to access shared information.</span></span> <span data-ttu-id="2e807-105">Les interfaces décrites dans le tableau suivant fournissent des informations de référence détaillées pour les développeurs de distributeurs de ressources.</span><span class="sxs-lookup"><span data-stu-id="2e807-105">The interfaces described in the following table provide detailed reference information for developers of resource dispensers.</span></span>



| <span data-ttu-id="2e807-106">Interfaces</span><span class="sxs-lookup"><span data-stu-id="2e807-106">Interfaces</span></span>                                                | <span data-ttu-id="2e807-107">Description</span><span class="sxs-lookup"><span data-stu-id="2e807-107">Description</span></span>                                                                                                               |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e807-108">**IDispenserDriver**</span><span class="sxs-lookup"><span data-stu-id="2e807-108">**IDispenserDriver**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver)<br/>   | <span data-ttu-id="2e807-109">Cette interface est appelée par le détenteur du distributeur de ressources pour créer, inscrire, évaluer et détruire une ressource.</span><span class="sxs-lookup"><span data-stu-id="2e807-109">This interface is called by the resource dispenser holder to create, enlist, evaluate, and destroy a resource.</span></span><br/> |
| [<span data-ttu-id="2e807-110">**IDispenserManager**</span><span class="sxs-lookup"><span data-stu-id="2e807-110">**IDispenserManager**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager)<br/> | <span data-ttu-id="2e807-111">Les distributeurs de ressources utilisent cette interface pour se connecter au gestionnaire du distributeur.</span><span class="sxs-lookup"><span data-stu-id="2e807-111">Resource dispensers use this interface to connect to the dispenser manager.</span></span><br/>                                    |
| [<span data-ttu-id="2e807-112">**IHolder**</span><span class="sxs-lookup"><span data-stu-id="2e807-112">**IHolder**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder)<br/>                     | <span data-ttu-id="2e807-113">Cette interface est utilisée pour préparer et gérer les ressources.</span><span class="sxs-lookup"><span data-stu-id="2e807-113">This interface is used to prepare and handle resources.</span></span><br/>                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="2e807-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2e807-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e807-115">Concepts du distributeur de ressources COM+</span><span class="sxs-lookup"><span data-stu-id="2e807-115">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="2e807-116">Types utilisés dans les interfaces de distributeur de ressources COM+</span><span class="sxs-lookup"><span data-stu-id="2e807-116">Types Used in COM+ Resource Dispenser Interfaces</span></span>](types-used-in-com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 




