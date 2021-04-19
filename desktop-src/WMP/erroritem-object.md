---
title: Objet ErrorItem
description: L’objet ErrorItem permet d’accéder aux informations sur les erreurs.
ms.assetid: 14bc9c12-98c6-4b72-9ae5-d6afeb1303f9
keywords:
- Objet ErrorItem lecteur Windows Media
topic_type:
- apiref
api_name:
- ErrorItem Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c273d00477363c66c49dfa1f77a66dab42c711cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106509013"
---
# <a name="erroritem-object"></a><span data-ttu-id="43b77-104">Objet ErrorItem</span><span class="sxs-lookup"><span data-stu-id="43b77-104">ErrorItem Object</span></span>

<span data-ttu-id="43b77-105">L’objet **ErrorItem** permet d’accéder aux informations sur les erreurs.</span><span class="sxs-lookup"><span data-stu-id="43b77-105">The **ErrorItem** object provides a way to access error information.</span></span>

<span data-ttu-id="43b77-106">L’objet **ErrorItem** prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="43b77-106">The **ErrorItem** object supports the following properties.</span></span>



| <span data-ttu-id="43b77-107">Propriété</span><span class="sxs-lookup"><span data-stu-id="43b77-107">Property</span></span>                                           | <span data-ttu-id="43b77-108">Description</span><span class="sxs-lookup"><span data-stu-id="43b77-108">Description</span></span>                                                                                     |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43b77-109">condition</span><span class="sxs-lookup"><span data-stu-id="43b77-109">condition</span></span>](erroritem-condition.md)               | <span data-ttu-id="43b77-110">Récupère une valeur indiquant la condition de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="43b77-110">Retrieves a value indicating the condition for the error.</span></span>                                       |
| [<span data-ttu-id="43b77-111">customUrl</span><span class="sxs-lookup"><span data-stu-id="43b77-111">customUrl</span></span>](erroritem-customurl.md)               | <span data-ttu-id="43b77-112">Récupère l’URL d’un site Web qui affiche des informations spécifiques sur l’échec du téléchargement du codec.</span><span class="sxs-lookup"><span data-stu-id="43b77-112">Retrieves the URL of a website that displays specific information about codec download failure.</span></span> |
| [<span data-ttu-id="43b77-113">errorCode</span><span class="sxs-lookup"><span data-stu-id="43b77-113">errorCode</span></span>](erroritem-errorcode.md)               | <span data-ttu-id="43b77-114">Récupère le code d’erreur actuel.</span><span class="sxs-lookup"><span data-stu-id="43b77-114">Retrieves the current error code.</span></span>                                                               |
| [<span data-ttu-id="43b77-115">errorContext</span><span class="sxs-lookup"><span data-stu-id="43b77-115">errorContext</span></span>](erroritem-errorcontext.md)         | <span data-ttu-id="43b77-116">Récupère une valeur indiquant le contexte de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="43b77-116">Retrieves a value indicating the context of the error.</span></span>                                          |
| [<span data-ttu-id="43b77-117">errorDescription</span><span class="sxs-lookup"><span data-stu-id="43b77-117">errorDescription</span></span>](erroritem-errordescription.md) | <span data-ttu-id="43b77-118">Récupère une description de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="43b77-118">Retrieves a description of the error.</span></span>                                                           |
| <span data-ttu-id="43b77-119">**corriger**</span><span class="sxs-lookup"><span data-stu-id="43b77-119">**remedy**</span></span>                                         | <span data-ttu-id="43b77-120">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="43b77-120">Reserved for future use.</span></span>                                                                        |



 

<span data-ttu-id="43b77-121">L’objet **ErrorItem** est accessible par le biais des méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="43b77-121">The **ErrorItem** object is accessed through the following methods.</span></span>



| <span data-ttu-id="43b77-122">Object</span><span class="sxs-lookup"><span data-stu-id="43b77-122">Object</span></span>                    | <span data-ttu-id="43b77-123">Méthode</span><span class="sxs-lookup"><span data-stu-id="43b77-123">Method</span></span>                   |
|---------------------------|--------------------------|
| [<span data-ttu-id="43b77-124">Error</span><span class="sxs-lookup"><span data-stu-id="43b77-124">Error</span></span>](error-object.md) | [<span data-ttu-id="43b77-125">item</span><span class="sxs-lookup"><span data-stu-id="43b77-125">item</span></span>](error-item.md)   |
| [<span data-ttu-id="43b77-126">Média</span><span class="sxs-lookup"><span data-stu-id="43b77-126">Media</span></span>](media-object.md) | [<span data-ttu-id="43b77-127">error</span><span class="sxs-lookup"><span data-stu-id="43b77-127">error</span></span>](media-error.md) |



 

<span data-ttu-id="43b77-128">À des fins d’illustration, *joueur*. *erreur*. *Item*(*index*) est utilisé dans les sections de syntaxe de référence.</span><span class="sxs-lookup"><span data-stu-id="43b77-128">For purposes of illustration, *player*.*error*.*item*(*index*) is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="43b77-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43b77-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43b77-130">**Référence du modèle objet pour l’écriture de scripts**</span><span class="sxs-lookup"><span data-stu-id="43b77-130">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




