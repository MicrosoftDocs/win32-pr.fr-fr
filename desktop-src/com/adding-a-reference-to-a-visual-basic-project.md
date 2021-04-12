---
title: Ajout d’une référence à un projet Visual Basic
description: Ajout d’une référence à un projet Visual Basic
ms.assetid: 635b1fe9-e592-42d7-a0ee-34fea205f412
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b29b99610464287f34e9c78e44319c16b4d47c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309733"
---
# <a name="adding-a-reference-to-a-visual-basic-project"></a><span data-ttu-id="11bee-103">Ajout d’une référence à un projet Visual Basic</span><span class="sxs-lookup"><span data-stu-id="11bee-103">Adding a Reference to a Visual Basic Project</span></span>

<span data-ttu-id="11bee-104">La procédure suivante décrit comment ajouter une référence à un objet COM à un projet de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="11bee-104">The following procedure describes how to add a reference to a COM object to a Visual Basic project.</span></span> <span data-ttu-id="11bee-105">Votre application peut ensuite utiliser les classes de cet objet.</span><span class="sxs-lookup"><span data-stu-id="11bee-105">Your application can then use the classes of that object.</span></span>

<span data-ttu-id="11bee-106">Quand vous ajoutez un objet en tant que référence, vous pouvez uniquement utiliser la bibliothèque de types fournie par le contrôle ou la bibliothèque de types « RAW ».</span><span class="sxs-lookup"><span data-stu-id="11bee-106">When you add an object as a reference, you can only use the type library provided by the control, or the "raw" type library.</span></span> <span data-ttu-id="11bee-107">En revanche, l’ajout d’un contrôle en tant que composant expose également les propriétés et méthodes de l’extendeur Visual Basic comme si elles faisaient partie du contrôle.</span><span class="sxs-lookup"><span data-stu-id="11bee-107">In contrast, adding a control as a component also exposes the Visual Basic extender properties and methods as if they were part of the control.</span></span>

<span data-ttu-id="11bee-108">**Pour créer une référence Visual Basic à un composant**</span><span class="sxs-lookup"><span data-stu-id="11bee-108">**To make a Visual Basic reference to a component**</span></span>

1.  <span data-ttu-id="11bee-109">Dans le menu **Projet**, cliquez sur **Références**.</span><span class="sxs-lookup"><span data-stu-id="11bee-109">On the **Project** menu, click **References**.</span></span>
2.  <span data-ttu-id="11bee-110">Activez la case à cocher en regard du composant que vous souhaitez ajouter.</span><span class="sxs-lookup"><span data-stu-id="11bee-110">Click to select the check box next to the component you want to add.</span></span> <span data-ttu-id="11bee-111">Si le composant n’est pas listé, localisez le fichier. dll ou. ocx à l’aide de l’élément **Parcourir**.</span><span class="sxs-lookup"><span data-stu-id="11bee-111">If the component is not listed, locate the .dll or .ocx file using **Browse**.</span></span>
3.  <span data-ttu-id="11bee-112">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="11bee-112">Click **OK**.</span></span>

<span data-ttu-id="11bee-113">Le composant fait maintenant partie du projet.</span><span class="sxs-lookup"><span data-stu-id="11bee-113">The component is now part of the project.</span></span> <span data-ttu-id="11bee-114">Votre application peut créer des instances de classe à l’aide du mot clé **New** .</span><span class="sxs-lookup"><span data-stu-id="11bee-114">Your application can create class instances using the **New** keyword.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11bee-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="11bee-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11bee-116">Ajout d’un composant à un projet Visual Basic</span><span class="sxs-lookup"><span data-stu-id="11bee-116">Adding a Component to a Visual Basic Project</span></span>](adding-a-component-to-a-visual-basic-project.md)
</dt> <dt>

[<span data-ttu-id="11bee-117">Conversion en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="11bee-117">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
</dt> </dl>

 

 




