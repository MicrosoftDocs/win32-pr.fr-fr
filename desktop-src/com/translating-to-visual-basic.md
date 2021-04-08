---
title: Conversion en Visual Basic
description: Conversion en Visual Basic
ms.assetid: 48672d0c-b0d7-4820-91d4-d985030396f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c45e7beedaaa3983b1be1503b5ce443a3adf4d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840285"
---
# <a name="translating-to-visual-basic"></a><span data-ttu-id="094d1-103">Conversion en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="094d1-103">Translating to Visual Basic</span></span>

<span data-ttu-id="094d1-104">Vous pouvez ajouter un objet COM à votre projet Visual Basic en tant que référence ou composant.</span><span class="sxs-lookup"><span data-stu-id="094d1-104">You can add a COM object to your Visual Basic project either as a reference or a component.</span></span> <span data-ttu-id="094d1-105">Une fois que l’objet est ajouté à votre projet, votre application peut accéder à ses classes et interfaces.</span><span class="sxs-lookup"><span data-stu-id="094d1-105">Once the object is added to your project, your application can access its classes and interfaces.</span></span> <span data-ttu-id="094d1-106">Vous pouvez ensuite utiliser l’Explorateur d’objets Visual Basic pour afficher les informations de la bibliothèque de types de l’objet dans la syntaxe Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="094d1-106">You can then use the Visual Basic Object Browser to view the object's type library information in Visual Basic syntax.</span></span>

<span data-ttu-id="094d1-107">En général, les contrôles sont ajoutés à un projet en tant que composants et les éléments qui ne sont pas des contrôles sont ajoutés en tant que références.</span><span class="sxs-lookup"><span data-stu-id="094d1-107">Typically, controls are added to a project as a components and noncontrols are added as references.</span></span> <span data-ttu-id="094d1-108">Lorsqu’un objet COM est ajouté en tant que composant, il apparaît dans la boîte à outils Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="094d1-108">When a COM object is added as a component, it appears in the Visual Basic toolbox.</span></span> <span data-ttu-id="094d1-109">Les nouvelles instances de cet objet sont créées en faisant glisser l’icône de l’objet de la boîte à outils vers un formulaire de Visual Basic ou un autre type de conteneur.</span><span class="sxs-lookup"><span data-stu-id="094d1-109">New instances of that object are created by dragging the object icon from the toolbox onto a Visual Basic form or other type of container.</span></span> <span data-ttu-id="094d1-110">Les nouvelles instances d’objets COM ajoutées en tant que références sont créées à l’aide du mot clé **New** .</span><span class="sxs-lookup"><span data-stu-id="094d1-110">New instances of COM objects added as references are created using the **new** keyword.</span></span>

<span data-ttu-id="094d1-111">La distinction entre l’utilisation d’une classe comme référence et d’un composant est subtile mais importante.</span><span class="sxs-lookup"><span data-stu-id="094d1-111">The distinction between using a class as a reference versus a component is subtle but important.</span></span> <span data-ttu-id="094d1-112">Quand vous ajoutez un objet en tant que référence, vous pouvez utiliser uniquement la bibliothèque de types fournie par le contrôle ou la bibliothèque de types « RAW ».</span><span class="sxs-lookup"><span data-stu-id="094d1-112">When you add an object as a reference, you can use only the type library that the control provides, or the "raw" type library.</span></span>

<span data-ttu-id="094d1-113">Si vous ajoutez un contrôle en tant que composant, Visual Basic fusionne les propriétés et les méthodes extendeur du formulaire dans lequel le contrôle est incorporé avec la bibliothèque de types du contrôle, fournissant ainsi une version encapsulée et étendue de la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="094d1-113">If you add a control as a component, Visual Basic merges the extender properties and methods of the form in which the control is embedded with the control's type library, thus providing a wrapped, extended version of the type library.</span></span> <span data-ttu-id="094d1-114">Avec cette version de la bibliothèque de types, vous pouvez utiliser des propriétés d’extendeur telles que Top et Left comme si elles faisaient partie du contrôle, au lieu du conteneur du contrôle.</span><span class="sxs-lookup"><span data-stu-id="094d1-114">With this version of the type library, you can use extender properties such as Top and Left as if they were part of the control, instead of the control's container.</span></span>

<span data-ttu-id="094d1-115">Visual Basic ne prend actuellement pas en charge plusieurs bibliothèques de types générées dans un fichier. dll unique.</span><span class="sxs-lookup"><span data-stu-id="094d1-115">Visual Basic does not currently support multiple type libraries built into a single .dll file.</span></span> <span data-ttu-id="094d1-116">Si vous exécutez dans une DLL qui incorpore plusieurs bibliothèques de types, vous devez obtenir des copies autonomes des bibliothèques de types à partir de la source qui a fourni l’objet afin d’utiliser l’objet avec Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="094d1-116">If you run into a DLL that incorporates multiple type libraries, you should get stand-alone copies of the type libraries from the source that supplied the object in order to use the object with Visual Basic.</span></span>

<span data-ttu-id="094d1-117">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="094d1-117">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="094d1-118">Conversion en Visual Basic à partir de C++</span><span class="sxs-lookup"><span data-stu-id="094d1-118">Translating to Visual Basic from C++</span></span>](translating-to-visual-basic-from-c--.md)
-   [<span data-ttu-id="094d1-119">Conversion en Visual Basic à partir de Java</span><span class="sxs-lookup"><span data-stu-id="094d1-119">Translating to Visual Basic from Java</span></span>](translating-to-visual-basic-from-java.md)
-   [<span data-ttu-id="094d1-120">Ajout d’un composant à un projet Visual Basic</span><span class="sxs-lookup"><span data-stu-id="094d1-120">Adding a Component to a Visual Basic Project</span></span>](adding-a-component-to-a-visual-basic-project.md)
-   [<span data-ttu-id="094d1-121">Ajout d’une référence à un projet Visual Basic</span><span class="sxs-lookup"><span data-stu-id="094d1-121">Adding a Reference to a Visual Basic Project</span></span>](adding-a-reference-to-a-visual-basic-project.md)
-   [<span data-ttu-id="094d1-122">Explorateur d’objets Visual Basic</span><span class="sxs-lookup"><span data-stu-id="094d1-122">Visual Basic Object Browser</span></span>](visual-basic-object-browser.md)

## <a name="related-topics"></a><span data-ttu-id="094d1-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="094d1-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="094d1-124">Traduire en C++</span><span class="sxs-lookup"><span data-stu-id="094d1-124">Translating to C++</span></span>](translating-to-c--.md)
</dt> <dt>

[<span data-ttu-id="094d1-125">Conversion en Java</span><span class="sxs-lookup"><span data-stu-id="094d1-125">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




