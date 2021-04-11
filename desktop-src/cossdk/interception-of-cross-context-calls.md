---
description: Lorsqu’un objet est activé dans un contexte donné, les appels suivants à ou à partir de celui-ci, dans le contexte, sont gérés différemment des appels à travers la limite de contexte.
ms.assetid: 9e234b41-f269-4674-adc4-12018277a14b
title: Interception d’appels entre les contextes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d70bc8bff83d02b13656f9854f0e6d16cd4e173
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317881"
---
# <a name="interception-of-cross-context-calls"></a><span data-ttu-id="d1d14-103">Interception d’appels entre les contextes</span><span class="sxs-lookup"><span data-stu-id="d1d14-103">Interception of Cross-Context Calls</span></span>

<span data-ttu-id="d1d14-104">Lorsqu’un objet est activé dans un contexte donné, les appels suivants à ou à partir de celui-ci, dans le contexte, sont gérés différemment des appels à travers la limite de contexte.</span><span class="sxs-lookup"><span data-stu-id="d1d14-104">When an object is activated in a given context, subsequent calls to or from it, within the context, are handled differently than calls across the context boundary.</span></span> <span data-ttu-id="d1d14-105">Les appels à travers la limite de contexte sont gérés avec les proxies légers.</span><span class="sxs-lookup"><span data-stu-id="d1d14-105">Calls across the context boundary are handled with lightweight proxies.</span></span> <span data-ttu-id="d1d14-106">Ces proxies gèrent la médiation requise pour ajuster l’environnement d’exécution à partir d’un autre qui adapte l’appelant à un qui prend en charge l’appelé.</span><span class="sxs-lookup"><span data-stu-id="d1d14-106">These proxies handle whatever mediation is required to adjust the run-time environment from one that accommodates the caller to one that accommodates the callee.</span></span> <span data-ttu-id="d1d14-107">Ce processus est appelé *interception*.</span><span class="sxs-lookup"><span data-stu-id="d1d14-107">This process is known as *interception*.</span></span>

<span data-ttu-id="d1d14-108">L’interception des appels entre les contextes est nécessaire, car les objets dans des contextes différents ont des exigences d’exécution différentes, ce qui est précisément la raison des contextes.</span><span class="sxs-lookup"><span data-stu-id="d1d14-108">Cross-context call interception is necessary because objects in different contexts have different run-time requirements—this is precisely the reason for contexts.</span></span> <span data-ttu-id="d1d14-109">COM+ intercepte les références d’objet que vous passez en tant que paramètres de méthode et les convertit automatiquement en proxies afin qu’ils soient utilisables dans le nouveau contexte.</span><span class="sxs-lookup"><span data-stu-id="d1d14-109">COM+ intercepts any object references that you pass as method parameters and automatically converts them to proxies so that they are usable in the new context.</span></span>

<span data-ttu-id="d1d14-110">Si vous partagez des références d’objet entre des limites de contexte par d’autres moyens (par exemple, dans des variables globales), vous devez toujours utiliser [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) et [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span><span class="sxs-lookup"><span data-stu-id="d1d14-110">If you share object references across context boundaries by other means—for example, in global variables—you should always use [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) and [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span></span> <span data-ttu-id="d1d14-111">Ces fonctions peuvent traduire une référence d’objet en un proxy utilisable dans un contexte différent.</span><span class="sxs-lookup"><span data-stu-id="d1d14-111">These functions can translate an object reference into a proxy usable in a different context.</span></span> <span data-ttu-id="d1d14-112">Ne partagez jamais une référence d’objet brut entre les limites de contexte.</span><span class="sxs-lookup"><span data-stu-id="d1d14-112">Never share a raw object reference across context boundaries.</span></span>

<span data-ttu-id="d1d14-113">Le comportement des appels à travers le contexte peut avoir des conséquences indésirables dans le cas d’objets exposant des interfaces qui ne peuvent pas être marshalées.</span><span class="sxs-lookup"><span data-stu-id="d1d14-113">The behavior of calls across context can have unwanted consequences in the case of objects exposing interfaces that cannot be marshaled.</span></span> <span data-ttu-id="d1d14-114">Dans ce cas, vous souhaiterez probablement insister sur le fait que l’objet qui ne peut pas être marshalé soit uniquement activé dans le contexte de son appelant et jamais dans son propre contexte.</span><span class="sxs-lookup"><span data-stu-id="d1d14-114">In this circumstance, you are likely to want to insist that the object that cannot be marshaled be activated only in the context of its caller and never in its own context.</span></span> <span data-ttu-id="d1d14-115">Pour ce faire, sélectionnez l’option **doit être activé dans le contexte** de l’appelant sous l’onglet **activation** de la page **Propriétés** du composant.</span><span class="sxs-lookup"><span data-stu-id="d1d14-115">You can do this by selecting the **Must be activated in caller's context** option on the **Activation** tab of the component **Properties** page.</span></span> <span data-ttu-id="d1d14-116">(Pour obtenir des instructions pas à pas, consultez [application de l’activation dans le contexte de l’appelant](enforcing-activation-in-the-caller-s-context.md) .)</span><span class="sxs-lookup"><span data-stu-id="d1d14-116">(See [Enforcing Activation in the Caller's Context](enforcing-activation-in-the-caller-s-context.md) for step-by-step instructions.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1d14-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d1d14-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1d14-118">Activation du contexte</span><span class="sxs-lookup"><span data-stu-id="d1d14-118">Context activation</span></span>](context-activation.md)
</dt> </dl>

 

 
