---
title: Interface IWMDRMIndividualizationStatus
description: L’interface IWMDRMIndividualizationStatus permet la récupération d’informations d’État avancées sur la progression de l’individualisation. Cette interface est fournie avec des événements MEWMDRMIndividualizationProgress.
ms.assetid: 3a148005-22fa-4495-a47c-d9463db16293
keywords:
- Format Windows Media de l’interface IWMDRMIndividualizationStatus
- Interface IWMDRMIndividualizationStatus format Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19a369bf9b70d9a43af8a48f13f1b8bbb87525b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941241"
---
# <a name="iwmdrmindividualizationstatus-interface"></a><span data-ttu-id="e87f5-105">Interface IWMDRMIndividualizationStatus</span><span class="sxs-lookup"><span data-stu-id="e87f5-105">IWMDRMIndividualizationStatus interface</span></span>

<span data-ttu-id="e87f5-106">L’interface **IWMDRMIndividualizationStatus** permet la récupération d’informations d’État avancées sur la progression de l’individualisation.</span><span class="sxs-lookup"><span data-stu-id="e87f5-106">The **IWMDRMIndividualizationStatus** interface enables retrieval of advanced status information about the progress of individualization.</span></span>

<span data-ttu-id="e87f5-107">Cette interface est fournie avec des événements MEWMDRMIndividualizationProgress.</span><span class="sxs-lookup"><span data-stu-id="e87f5-107">This interface is delivered with MEWMDRMIndividualizationProgress events.</span></span> <span data-ttu-id="e87f5-108">De nombreux événements de ce type sont générés entre un appel à [**IWMDRMSecurity ::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) et l’achèvement du processus d’individualisation, qui est signalé par la génération d’un événement **MEWMDRMIndividualizationCompleted** .</span><span class="sxs-lookup"><span data-stu-id="e87f5-108">Many such events are generated between a call to [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) and the completion of the individualization process, which is signaled by the generation of an **MEWMDRMIndividualizationCompleted** event.</span></span>

<span data-ttu-id="e87f5-109">Pour récupérer un pointeur vers une instance de l’interface **IWMDRMIndividualizationStatus** , vous devez d’abord appeler la méthode **IMFMediaEvent :: GetValue** de l’événement Progress.</span><span class="sxs-lookup"><span data-stu-id="e87f5-109">To retrieve a pointer to an instance of the **IWMDRMIndividualizationStatus** interface, you must first call the **IMFMediaEvent::GetValue** method of the progress event.</span></span> <span data-ttu-id="e87f5-110">La valeur récupérée à partir de l’événement est un pointeur vers l’interface **IUnknown** de l’objet qui implémente l’interface **IWMDRMIndividualizationStatus** .</span><span class="sxs-lookup"><span data-stu-id="e87f5-110">The value you retrieve from the event is a pointer to the **IUnknown** interface of the object that implements the **IWMDRMIndividualizationStatus** interface.</span></span>

## <a name="members"></a><span data-ttu-id="e87f5-111">Membres</span><span class="sxs-lookup"><span data-stu-id="e87f5-111">Members</span></span>

<span data-ttu-id="e87f5-112">L’interface **IWMDRMIndividualizationStatus** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e87f5-112">The **IWMDRMIndividualizationStatus** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e87f5-113">**IWMDRMIndividualizationStatus** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e87f5-113">**IWMDRMIndividualizationStatus** also has these types of members:</span></span>

-   [<span data-ttu-id="e87f5-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e87f5-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e87f5-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e87f5-115">Methods</span></span>

<span data-ttu-id="e87f5-116">L’interface **IWMDRMIndividualizationStatus** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e87f5-116">The **IWMDRMIndividualizationStatus** interface has these methods.</span></span>



| <span data-ttu-id="e87f5-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="e87f5-117">Method</span></span>                                                       | <span data-ttu-id="e87f5-118">Description</span><span class="sxs-lookup"><span data-stu-id="e87f5-118">Description</span></span>                                                        |
|:-------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="e87f5-119">**GetStatus**</span><span class="sxs-lookup"><span data-stu-id="e87f5-119">**GetStatus**</span></span>](iwmdrmindividualizationstatus-getstatus.md) | <span data-ttu-id="e87f5-120">Récupère des informations détaillées sur l’individualisation.</span><span class="sxs-lookup"><span data-stu-id="e87f5-120">Retrieves detailed information about individualization.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="e87f5-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e87f5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e87f5-122">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="e87f5-122">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

