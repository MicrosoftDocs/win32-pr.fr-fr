---
title: Interaction avec WinEvents
description: L’heure d’exécution de l’annotation dynamique n’enverra pas de WinEvents ; Il incombe à l’annotation d’envoyer les événements appropriés, si nécessaire. Si vous devez envoyer des WinEvents, veillez à les envoyer une fois l’annotation effectuée.
ms.assetid: 657a540b-8838-4d2e-ade6-c4fa1ad08e21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2aedd09a22371f91a92eca891c77f6c424583b5
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "106512712"
---
# <a name="interaction-with-winevents"></a><span data-ttu-id="8d58b-104">Interaction avec WinEvents</span><span class="sxs-lookup"><span data-stu-id="8d58b-104">Interaction with WinEvents</span></span>

<span data-ttu-id="8d58b-105">L’heure d’exécution de l’annotation dynamique n’enverra pas de [winEvents](winevents-infrastructure.md); Il incombe à l’annotation d’envoyer les événements appropriés, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8d58b-105">The Dynamic Annotation run time will not send [WinEvents](winevents-infrastructure.md); it is the annotator's responsibility to send appropriate events, when necessary.</span></span> <span data-ttu-id="8d58b-106">Si vous devez envoyer des WinEvents, veillez à les envoyer une fois l’annotation effectuée.</span><span class="sxs-lookup"><span data-stu-id="8d58b-106">If you need to send WinEvents, be sure to send them after the annotation has taken place.</span></span>

<span data-ttu-id="8d58b-107">Par exemple, si vous utilisez [**IAccPropServices :: SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) pour définir la propriété [**Name**](name-property.md) d’un élément, envoyez un [**événement \_ \_ NameChange, d’objet d’événement**](event-constants.md) pour cet objet après que **SetPropValue** a été retourné.</span><span class="sxs-lookup"><span data-stu-id="8d58b-107">For example, if you use [**IAccPropServices::SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) to set the [**Name**](name-property.md) property of an element, send an [**EVENT\_OBJECT\_NAMECHANGE**](event-constants.md) event for that object after **SetPropValue** returns.</span></span>

<span data-ttu-id="8d58b-108">Toutefois, si vous utilisez [**IAccPropServices :: SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) pour définir ValueMap pour un Slider, aucun événement n’est nécessaire, car la définition de ValueMap ne modifie pas la valeur du curseur.</span><span class="sxs-lookup"><span data-stu-id="8d58b-108">However, if you use [**IAccPropServices::SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) to set the ValueMap for a slider, no events are required because setting the ValueMap does not change the slider's value.</span></span>

 

 




