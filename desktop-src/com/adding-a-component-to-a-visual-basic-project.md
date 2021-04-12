---
title: Ajout d’un composant à un projet Visual Basic
description: Ajout d’un composant à un projet Visual Basic
ms.assetid: 7e78853a-b134-46d7-a230-3ee8d80d05c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd64b8367b33590b972adc2439af3a2479ee920e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309734"
---
# <a name="adding-a-component-to-a-visual-basic-project"></a><span data-ttu-id="cf763-103">Ajout d’un composant à un projet Visual Basic</span><span class="sxs-lookup"><span data-stu-id="cf763-103">Adding a Component to a Visual Basic Project</span></span>

<span data-ttu-id="cf763-104">La procédure suivante décrit comment ajouter un objet COM en tant que composant à un projet de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="cf763-104">The following procedure describes how to add a COM object as a component to a Visual Basic project.</span></span> <span data-ttu-id="cf763-105">Votre application peut ensuite utiliser les classes de cet objet.</span><span class="sxs-lookup"><span data-stu-id="cf763-105">Your application can then use the classes of that object.</span></span>

<span data-ttu-id="cf763-106">L’ajout d’un contrôle en tant que composant expose les propriétés et méthodes de l’extendeur Visual Basic comme si elles faisaient partie du contrôle.</span><span class="sxs-lookup"><span data-stu-id="cf763-106">Adding a control as a component exposes the Visual Basic extender properties and methods as if they were part of the control.</span></span> <span data-ttu-id="cf763-107">En revanche, lorsque vous ajoutez un objet en tant que référence, vous pouvez uniquement utiliser la bibliothèque de types fournie par le contrôle ou la bibliothèque de types « RAW ».</span><span class="sxs-lookup"><span data-stu-id="cf763-107">In contrast, when you add an object as a reference you can only use the type library provided by the control, or the "raw" type library.</span></span>

<span data-ttu-id="cf763-108">**Pour insérer un contrôle dans un projet Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="cf763-108">**To insert a control into a Visual Basic project**</span></span>

1.  <span data-ttu-id="cf763-109">Dans le menu **Projet**, cliquez sur **Composants**.</span><span class="sxs-lookup"><span data-stu-id="cf763-109">On the **Project** menu, click **Components**.</span></span>
2.  <span data-ttu-id="cf763-110">Activez la case à cocher en regard du composant que vous souhaitez ajouter.</span><span class="sxs-lookup"><span data-stu-id="cf763-110">Click to select the check box next to the component you want to add.</span></span> <span data-ttu-id="cf763-111">Si le composant n’est pas listé, localisez le fichier. dll ou. ocx à l’aide de l’élément **Parcourir**.</span><span class="sxs-lookup"><span data-stu-id="cf763-111">If the component is not listed, locate the .dll or .ocx file using **Browse**.</span></span>
3.  <span data-ttu-id="cf763-112">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="cf763-112">Click **OK**.</span></span>

<span data-ttu-id="cf763-113">Le composant fait maintenant partie du projet et s’affiche dans la barre d’outils de l’objet.</span><span class="sxs-lookup"><span data-stu-id="cf763-113">The component is now part of the project and appears in the object toolbar.</span></span> <span data-ttu-id="cf763-114">Votre application peut créer des instances du contrôle en faisant glisser le contrôle à partir de la barre d’outils et en la déposant sur un formulaire ou une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="cf763-114">Your application can create instances of the control by dragging the control from the toolbar and dropping it onto a form or dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf763-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cf763-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf763-116">Ajout d’une référence à un projet Visual Basic</span><span class="sxs-lookup"><span data-stu-id="cf763-116">Adding a Reference to a Visual Basic Project</span></span>](adding-a-reference-to-a-visual-basic-project.md)
</dt> <dt>

[<span data-ttu-id="cf763-117">Conversion en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="cf763-117">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
</dt> </dl>

 

 




