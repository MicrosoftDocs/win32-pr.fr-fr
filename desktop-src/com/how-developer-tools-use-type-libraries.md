---
title: Utilisation des bibliothèques de types par Outils de développement
description: Utilisation des bibliothèques de types par Outils de développement
ms.assetid: 260aa694-1055-4a43-93aa-69a9d7359881
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0cc0f5249075aa861a1301466f86a0f769b8bf3
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2021
ms.locfileid: "106537150"
---
# <a name="how-developer-tools-use-type-libraries"></a><span data-ttu-id="20f96-103">Utilisation des bibliothèques de types par Outils de développement</span><span class="sxs-lookup"><span data-stu-id="20f96-103">How Developer Tools Use Type Libraries</span></span>

<span data-ttu-id="20f96-104">Le diagramme suivant illustre comment les différents outils de développement interagissent avec la bibliothèque de types d’un objet COM.</span><span class="sxs-lookup"><span data-stu-id="20f96-104">The following diagram illustrates how the various development tools interact with a COM object's type library.</span></span> <span data-ttu-id="20f96-105">Chaque bibliothèque de types expose des interfaces de programmation standard que les outils peuvent appeler pour obtenir des informations sur les éléments décrits dans cette bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="20f96-105">Each type library exposes standard programmatic interfaces that tools can call to get information about the elements described in that type library.</span></span> <span data-ttu-id="20f96-106">Dans ce diagramme, GUID correspond à un identificateur global unique et à RPC pour un appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="20f96-106">In this diagram, GUID stands for globally unique identifier and RPC for remote procedure call.</span></span>

![Diagramme qui montre comment l’outil de développement interagit avec la bibliothèque de types d’un objet C O M.](images/09983c96-3f01-4ad5-8d3e-12b8ed28c35d.png)

<span data-ttu-id="20f96-108">Dans le diagramme précédent, les outils de conversion C++, tels que le compilateur MIDL et les assistants fournis par le système de développement Microsoft Visual C++, génèrent des fichiers d’en-tête et stub.</span><span class="sxs-lookup"><span data-stu-id="20f96-108">In the preceding diagram, the C++ conversion tools, such as the MIDL compiler and the wizards provided by the Microsoft Visual C++ development system, generate header and stub files.</span></span> <span data-ttu-id="20f96-109">Vous pouvez ajouter ces fichiers à votre projet afin d’utiliser l’objet COM décrit par la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="20f96-109">You can add these files to your project in order to use the COM object described by the type library.</span></span>

<span data-ttu-id="20f96-110">De même, dans Java, les outils de développement génèrent des fichiers source et de classe Java, que vous pouvez ensuite importer dans votre application.</span><span class="sxs-lookup"><span data-stu-id="20f96-110">Similarly, in Java the developer tools generate Java class and source files, which you can then import into your application.</span></span>

<span data-ttu-id="20f96-111">Dans Visual Basic, le scénario est un peu plus simple.</span><span class="sxs-lookup"><span data-stu-id="20f96-111">In Visual Basic, the scenario is somewhat simpler.</span></span> <span data-ttu-id="20f96-112">Vous n’avez pas besoin de générer des fichiers supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="20f96-112">You do not need to generate additional files.</span></span> <span data-ttu-id="20f96-113">L’environnement Visual Basic fournit des boîtes de dialogue qui répertorient les objets COM actuellement installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="20f96-113">The Visual Basic environment provides dialog boxes listing the COM objects currently installed on your computer.</span></span> <span data-ttu-id="20f96-114">Vous sélectionnez le composant que vous souhaitez appeler à partir de votre application et il est ajouté à votre projet, comme un composant ou une référence.</span><span class="sxs-lookup"><span data-stu-id="20f96-114">You select the component you want to call from your application, and it is added to your project, either as a component or a reference.</span></span>

<span data-ttu-id="20f96-115">La visionneuse OLE-COM lit une bibliothèque de types, génère un fichier IDL temporaire basé sur la bibliothèque de types et l’affiche pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="20f96-115">The OLE-COM viewer reads a type library, generates a temporary IDL file based on the type library, and displays it to users.</span></span> <span data-ttu-id="20f96-116">La visionneuse OLE-COM affiche également la syntaxe C++ pour les éléments COM listés dans la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="20f96-116">The OLE-COM viewer also displays the C++ syntax for the COM elements listed in the type library.</span></span>

<span data-ttu-id="20f96-117">Pour plus d’informations sur les bibliothèques de types, consultez [bibliothèques de types et le langage de description d’objet](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language).</span><span class="sxs-lookup"><span data-stu-id="20f96-117">For more information about type libraries, see [Type Libraries and the Object Description Language](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language).</span></span>

 

 