---
title: Traduction de la syntaxe d’objet COM pour les langages de programmation
description: Traduction de la syntaxe d’objet COM pour les langages de programmation
ms.assetid: 021e0085-c720-401e-9637-76580e67b307
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9d1ec65e5b4ff8f3b61106a4b7a8c9ee3134b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839882"
---
# <a name="translating-com-object-syntax-for-programming-languages"></a><span data-ttu-id="9a580-103">Traduction de la syntaxe d’objet COM pour les langages de programmation</span><span class="sxs-lookup"><span data-stu-id="9a580-103">Translating COM Object Syntax for Programming Languages</span></span>

<span data-ttu-id="9a580-104">Pour appeler un objet COM à partir d’une application écrite dans un langage de programmation autre que celui utilisé pour écrire l’objet COM, vous devez d’abord traduire la syntaxe de l’objet dans votre langage de programmation.</span><span class="sxs-lookup"><span data-stu-id="9a580-104">To call a COM object from an application written in a programming language other than the one used to write the COM object, you must first translate the object's syntax to your programming language.</span></span> <span data-ttu-id="9a580-105">Ceci peut être effectué en suivant les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9a580-105">This can be done using the following steps:</span></span>

1.  <span data-ttu-id="9a580-106">Affichez la bibliothèque de types de l’objet COM dans la syntaxe de votre langage de programmation.</span><span class="sxs-lookup"><span data-stu-id="9a580-106">View the COM object's type library in your programming language's syntax.</span></span> <span data-ttu-id="9a580-107">Cela vous fournit des descriptions des classes, des interfaces, des méthodes, des propriétés et des événements de l’objet dans la syntaxe de langage que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="9a580-107">Doing this provides you with descriptions of the object's classes, interfaces, methods, properties and events in the language syntax you use.</span></span>

    <span data-ttu-id="9a580-108">Les produits de développement Microsoft proposent plusieurs outils pour vous aider à afficher et à convertir les bibliothèques de types.</span><span class="sxs-lookup"><span data-stu-id="9a580-108">Microsoft developer products provide several tools to assist you in viewing and converting type libraries.</span></span> <span data-ttu-id="9a580-109">Pour plus d’informations, consultez [visionneuses de bibliothèques de types et outils de conversion](type-library-viewers-and-conversion-tools.md) et [Comment outils de développement utiliser des bibliothèques de types](how-developer-tools-use-type-libraries.md).</span><span class="sxs-lookup"><span data-stu-id="9a580-109">For more information, see [Type Library Viewers and Conversion Tools](type-library-viewers-and-conversion-tools.md) and [How Developer Tools Use Type Libraries](how-developer-tools-use-type-libraries.md).</span></span>

    <span data-ttu-id="9a580-110">Une fois que vous pouvez afficher la bibliothèque de types de l’objet dans votre langage de programmation préféré, vous pouvez comparer sa syntaxe à celle figurant dans la documentation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9a580-110">Once you can view the object's type library in your preferred programming language, you can compare its syntax to that in the documentation for the object.</span></span> <span data-ttu-id="9a580-111">Si l’objet est documenté dans un langage de programmation autre que celui que vous utilisez, les types de données et la syntaxe peuvent différer, mais les descriptions des paramètres, les valeurs de retour et les fonctionnalités de l’objet doivent être identiques.</span><span class="sxs-lookup"><span data-stu-id="9a580-111">If the object is documented in a programming language other than the one you are using, the data types and syntax may differ, but descriptions of parameters, return values, and the object's functionality should be the same.</span></span>

2.  <span data-ttu-id="9a580-112">Prenez en compte les considérations spéciales relatives à la traduction de votre langage de programmation.</span><span class="sxs-lookup"><span data-stu-id="9a580-112">Take into account any special considerations for translating to your programming language.</span></span>

    <span data-ttu-id="9a580-113">Étant donné que chaque langage de programmation définit des concepts qui peuvent ne pas avoir d’équivalent dans d’autres langages, certaines des fonctionnalités d’un objet peuvent fonctionner différemment dans un autre langage ou ne pas être disponibles du tout.</span><span class="sxs-lookup"><span data-stu-id="9a580-113">Because each programming language defines concepts that may not have an equivalent in other languages, some of an object's functionality may work differently in another language, or not be available at all.</span></span> <span data-ttu-id="9a580-114">Par exemple, le langage de programmation Visual Basic ne reconnaît pas les types de données non signés C++, tels que **unsignedÂ long**.</span><span class="sxs-lookup"><span data-stu-id="9a580-114">For example, the Visual Basic programming language does not recognize C++ unsigned data types, such as **unsignedÂ long**.</span></span> <span data-ttu-id="9a580-115">Une application écrite en Visual Basic ne peut pas utiliser les méthodes COM qui acceptent ou retournent des variables de type de données non signées.</span><span class="sxs-lookup"><span data-stu-id="9a580-115">An application written in Visual Basic cannot use COM methods that accept or return unsigned data type variables.</span></span>

3.  <span data-ttu-id="9a580-116">Ajoutez le code compilé de l’objet COM à votre projet.</span><span class="sxs-lookup"><span data-stu-id="9a580-116">Add the COM object's compiled code to your project.</span></span> <span data-ttu-id="9a580-117">Le code compilé est généralement contenu dans un fichier. dll ou. ocx.</span><span class="sxs-lookup"><span data-stu-id="9a580-117">The compiled code is typically contained in a .dll or .ocx file.</span></span> <span data-ttu-id="9a580-118">Cette étape est nécessaire pour que le compilateur reconnaisse les classes de l’objet COM.</span><span class="sxs-lookup"><span data-stu-id="9a580-118">This step is necessary for the compiler to recognize the COM object's classes.</span></span> <span data-ttu-id="9a580-119">Une fois que vous avez ajouté l’objet COM, votre application peut utiliser ses classes et interfaces.</span><span class="sxs-lookup"><span data-stu-id="9a580-119">After you add the COM object, your application can use its classes and interfaces.</span></span>

<span data-ttu-id="9a580-120">Les rubriques suivantes décrivent comment traduire et utiliser des objets COM dans différents langages de programmation :</span><span class="sxs-lookup"><span data-stu-id="9a580-120">The following topics describe how to translate and use COM objects in a variety of programming languages:</span></span>

-   [<span data-ttu-id="9a580-121">Traduire en C++</span><span class="sxs-lookup"><span data-stu-id="9a580-121">Translating to C++</span></span>](translating-to-c--.md)
-   [<span data-ttu-id="9a580-122">Conversion en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9a580-122">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
-   [<span data-ttu-id="9a580-123">Conversion en Java</span><span class="sxs-lookup"><span data-stu-id="9a580-123">Translating to Java</span></span>](translating-to-java.md)

<span data-ttu-id="9a580-124">Ces rubriques décrivent les outils et les processus de conversion fournis par les produits de développement Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9a580-124">These topics describe conversion tools and processes provided by Microsoft developer products.</span></span> <span data-ttu-id="9a580-125">Pour obtenir des instructions sur la façon de programmer des objets COM à l’aide des outils de développement créés par d’autres sociétés, consultez la documentation de ces outils de développement.</span><span class="sxs-lookup"><span data-stu-id="9a580-125">For instructions on how to program COM objects using development tools created by other companies, see those development tools' documentation.</span></span>

 

 




