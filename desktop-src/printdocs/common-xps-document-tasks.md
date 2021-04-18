---
description: Cette page répertorie certaines des tâches de programmation couramment effectuées avec l’API de document XPS.
ms.assetid: ced2098f-5462-40d7-a728-4e53f7f41003
title: Tâches courantes de programmation de documents XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c40ee0c901b9d906d4d59c69bab4cfc22d8208
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519692"
---
# <a name="common-xps-document-programming-tasks"></a><span data-ttu-id="8b02d-103">Tâches courantes de programmation de documents XPS</span><span class="sxs-lookup"><span data-stu-id="8b02d-103">Common XPS Document Programming Tasks</span></span>

<span data-ttu-id="8b02d-104">Cette page répertorie certaines des tâches de programmation couramment effectuées avec l’API de document XPS.</span><span class="sxs-lookup"><span data-stu-id="8b02d-104">This page lists some of the programming tasks that are commonly performed with the XPS Document API.</span></span>

## <a name="common-xps-document-tasks"></a><span data-ttu-id="8b02d-105">Tâches courantes relatives aux documents XPS</span><span class="sxs-lookup"><span data-stu-id="8b02d-105">Common XPS Document Tasks</span></span>

<span data-ttu-id="8b02d-106">Les exemples de code suivants illustrent certaines des tâches de programmation qui sont couramment exécutées lorsque l’API de document XPS est utilisée pour travailler avec un modèle d’objet XPS.</span><span class="sxs-lookup"><span data-stu-id="8b02d-106">The following code examples illustrate some of the programming tasks that are commonly performed when the XPS Document API is used for working with an XPS OM.</span></span>

<dl>

[<span data-ttu-id="8b02d-107">Initialiser un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="8b02d-107">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)  
[<span data-ttu-id="8b02d-108">Créer un modèle d’objet XPS vide</span><span class="sxs-lookup"><span data-stu-id="8b02d-108">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)  
[<span data-ttu-id="8b02d-109">Lire un document XPS dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="8b02d-109">Read an XPS Document into an XPS OM</span></span>](read-an-xps-document-into-an-xps-om.md)  
[<span data-ttu-id="8b02d-110">Naviguer dans le modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="8b02d-110">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)  
[<span data-ttu-id="8b02d-111">Écrire du texte dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="8b02d-111">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)  
[<span data-ttu-id="8b02d-112">Dessiner des graphiques dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="8b02d-112">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)  
[<span data-ttu-id="8b02d-113">Placer des images dans un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="8b02d-113">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)  
[<span data-ttu-id="8b02d-114">Écrire un modèle OM XPS dans un document XPS</span><span class="sxs-lookup"><span data-stu-id="8b02d-114">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)  
[<span data-ttu-id="8b02d-115">Imprimer un modèle OM XPS</span><span class="sxs-lookup"><span data-stu-id="8b02d-115">Print an XPS OM</span></span>](print-an-xps-om.md)  
[<span data-ttu-id="8b02d-116">Utilisation des interfaces de collection XPS OM</span><span class="sxs-lookup"><span data-stu-id="8b02d-116">Working with XPS OM Collection Interfaces</span></span>](working-with-xps-object-model-collection-interfaces.md)  
</dl>

## <a name="disclaimer"></a><span data-ttu-id="8b02d-117">Clause d'exclusion de responsabilité</span><span class="sxs-lookup"><span data-stu-id="8b02d-117">Disclaimer</span></span>

<span data-ttu-id="8b02d-118">Les exemples de code ne sont pas destinés à être des programmes complets et fonctionnels.</span><span class="sxs-lookup"><span data-stu-id="8b02d-118">Code examples are not intended to be complete and working programs.</span></span> <span data-ttu-id="8b02d-119">Les exemples de code qui sont référencés sur cette page, par exemple, n’effectuent pas la vérification des paramètres, la vérification des erreurs ou la gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="8b02d-119">The code examples that are referenced on this page, for example, do not perform parameter checking, error checking, or error handling.</span></span> <span data-ttu-id="8b02d-120">Utilisez ces exemples comme point de départ, puis ajoutez le code nécessaire pour créer une application fiable.</span><span class="sxs-lookup"><span data-stu-id="8b02d-120">Use these examples as a starting point, and then add the code necessary to create a robust application.</span></span> <span data-ttu-id="8b02d-121">Pour plus d’informations sur les valeurs de retour **HRESULT** et les stratégies de gestion des erreurs, consultez [gestion des erreurs dans com](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="8b02d-121">For more information about **HRESULT** return values and error handling strategies, see [Error Handling in COM](../com/error-handling-in-com.md).</span></span>

<span data-ttu-id="8b02d-122">Pour pouvoir utiliser des interfaces OM XPS, COM doit être initialisé dans le thread, comme le montre l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="8b02d-122">Before XPS OM interfaces can be used, COM must be initialized in the thread, as shown in the following example code.</span></span>


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



<span data-ttu-id="8b02d-123">Par souci de clarté, ces exemples de code utilisent un modèle d’objet XPS très simple, qui peut ne pas être suffisamment complexe pour votre application.</span><span class="sxs-lookup"><span data-stu-id="8b02d-123">For clarity, these code examples use a very simple XPS OM, one that might not be complex enough for your application.</span></span> <span data-ttu-id="8b02d-124">En guise de cas, dans les exemples de code qui ajoutent du contenu à une page, les éléments visuels d’une page sont ajoutés directement à la liste des objets visuels de la page. Toutefois, dans la pratique, vous pouvez regrouper des objets visuels dans des objets canevas, afin que plusieurs objets puissent être traités comme un groupe.</span><span class="sxs-lookup"><span data-stu-id="8b02d-124">As a case in point, in the code examples that add content to a page, the visual elements of a page are added directly to the page's list of visual objects; in practice, however, you might want to group visual objects into canvas objects, so that multiple objects could be acted upon as a group.</span></span> <span data-ttu-id="8b02d-125">Ainsi, pour activer la prise en charge d’un même contenu pour plusieurs tailles de page, vous pouvez regrouper le contenu visuel d’une page dans un objet Canvas unique, puis appliquer une transformation à la zone de dessin pour l’adapter à la taille de page actuelle.</span><span class="sxs-lookup"><span data-stu-id="8b02d-125">Thus, to enable support of the same content for more than one page size, you could group the visual content of a page into a single canvas object, and then apply a transform to the canvas to scale it to the current page size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b02d-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8b02d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b02d-127">Gestion des erreurs dans COM</span><span class="sxs-lookup"><span data-stu-id="8b02d-127">Error Handling in COM</span></span>](../com/error-handling-in-com.md)
</dt> <dt>

[<span data-ttu-id="8b02d-128">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="8b02d-128">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
