---
title: Différences entre les modèles objet
description: Différences entre les modèles objet
ms.assetid: a6d2a2d5-2892-461a-aa6d-7e11b504b2af
keywords:
- Lecteur Windows Media, modèle objet
- Modèle d’objet du lecteur Windows Media, différences entre les versions
- modèle objet, différences de version
- Contrôle ActiveX du lecteur Windows Media, différences entre les versions
- Contrôle ActiveX, différences de version
- Windows Media Player Mobile contrôle ActiveX, différences de version
- Windows Media Player Mobile, modèle objet
- Guide de migration, différences de version
- versions du lecteur Windows Media, modèle objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a5341067e2daad0f44fbdd7075f0f543bac2fd4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512678"
---
# <a name="differences-between-the-object-models"></a><span data-ttu-id="3a740-112">Différences entre les modèles objet</span><span class="sxs-lookup"><span data-stu-id="3a740-112">Differences Between the Object Models</span></span>

<span data-ttu-id="3a740-113">Il existe deux principales différences entre le modèle d’objet Windows Media Player 6,4 et le modèle objet Windows Media Player 7 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3a740-113">There are two primary differences between the Windows Media Player 6.4 object model and the Windows Media Player 7 or later object model.</span></span>

-   <span data-ttu-id="3a740-114">**CLSID** Le modèle objet Windows Media Player 7 ou version ultérieure est un départ complet du modèle objet version 6,4.</span><span class="sxs-lookup"><span data-stu-id="3a740-114">**CLSID** The Windows Media Player 7 or later object model is a complete departure from the version 6.4 object model.</span></span> <span data-ttu-id="3a740-115">La spécification COM (Component Object Model) requiert que toutes les interfaces existantes continuent de fonctionner dans les nouvelles versions d’un composant COM.</span><span class="sxs-lookup"><span data-stu-id="3a740-115">The Component Object Model (COM) specification requires that all existing interfaces must continue to function in new versions of a COM component.</span></span> <span data-ttu-id="3a740-116">Cela signifie que de nouvelles interfaces peuvent être ajoutées à un composant COM, mais que les interfaces existantes ne doivent jamais être modifiées, ce qui garantit que le code client plus ancien fonctionnera toujours avec le composant spécifique qu’il a été conçu pour être utilisé.</span><span class="sxs-lookup"><span data-stu-id="3a740-116">This means that new interfaces can be added to a COM component, but existing interfaces must never be altered, ensuring older client code will always work with the particular component it was designed to use.</span></span> <span data-ttu-id="3a740-117">Par conséquent, le contrôle ActiveX Windows Media Player 7 ou version ultérieure a un nouvel ID de classe : 6BF52A52-394A-11D3-B153-00C04F79FAA6.</span><span class="sxs-lookup"><span data-stu-id="3a740-117">Therefore, the Windows Media Player 7 or later ActiveX control has a new class ID: 6BF52A52-394A-11D3-B153-00C04F79FAA6.</span></span> <span data-ttu-id="3a740-118">Si vous souhaitez tirer parti de la nouvelle fonctionnalité du contrôle pour cette version, vous devez modifier votre CLSID.</span><span class="sxs-lookup"><span data-stu-id="3a740-118">If you want to take advantage of the new functionality of the control for this version, you must change your CLSID.</span></span>
-   <span data-ttu-id="3a740-119">**Modèle d’objet hiérarchique** Si vous avez utilisé le contrôle ActiveX du lecteur Windows Media 6,4, vous avez peut-être remarqué que toutes les propriétés, méthodes et événements sont accessibles par le biais du même objet : l’objet **Player** .</span><span class="sxs-lookup"><span data-stu-id="3a740-119">**Hierarchical Object Model** If you've been using the Windows Media Player 6.4 ActiveX control, you may have noticed that all the properties, methods, and events are accessed through the same object: the **Player** object.</span></span> <span data-ttu-id="3a740-120">En revanche, le modèle objet Windows Media Player 7 ou version ultérieure est organisé comme une hiérarchie d’objets.</span><span class="sxs-lookup"><span data-stu-id="3a740-120">By contrast, the Windows Media Player 7 or later object model is organized as a hierarchy of objects.</span></span> <span data-ttu-id="3a740-121">L’objet **Player** est toujours l’objet racine, mais les fonctions sont désormais accessibles par le biais de divers objets enfants.</span><span class="sxs-lookup"><span data-stu-id="3a740-121">The **Player** object is still the root object, but functions are now accessed through a variety of child objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a740-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a740-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a740-123">**Guide de migration du modèle objet**</span><span class="sxs-lookup"><span data-stu-id="3a740-123">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




