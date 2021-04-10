---
description: En plus de reconnaître du texte, les module de reconnaissance peuvent reconnaître une classe d’objets connexes.
ms.assetid: 53b6137d-2998-4a3b-b469-3d1204ea194b
title: Identificateurs d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a258c8486bcf773f5f94c4de51c501e107fac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952535"
---
# <a name="object-recognizers"></a><span data-ttu-id="46a93-103">Identificateurs d’objets</span><span class="sxs-lookup"><span data-stu-id="46a93-103">Object Recognizers</span></span>

<span data-ttu-id="46a93-104">En plus de reconnaître du texte, les module de reconnaissance peuvent reconnaître une classe d’objets connexes.</span><span class="sxs-lookup"><span data-stu-id="46a93-104">In addition to recognizing text, recognizers can recognize a class of related objects.</span></span> <span data-ttu-id="46a93-105">Les détecteurs d’objets reconnaissent les formes générales, en fonction de leur rôle.</span><span class="sxs-lookup"><span data-stu-id="46a93-105">Object recognizers recognize general shapes, according to their purpose.</span></span> <span data-ttu-id="46a93-106">Les identificateurs d’objet sont utilisés pour reconnaître :</span><span class="sxs-lookup"><span data-stu-id="46a93-106">Object recognizers are used to recognize:</span></span>

-   <span data-ttu-id="46a93-107">Notes musicales</span><span class="sxs-lookup"><span data-stu-id="46a93-107">Musical notes</span></span>
-   <span data-ttu-id="46a93-108">Formes géométriques</span><span class="sxs-lookup"><span data-stu-id="46a93-108">Geometric shapes</span></span>
-   <span data-ttu-id="46a93-109">Équations mathématiques</span><span class="sxs-lookup"><span data-stu-id="46a93-109">Math equations</span></span>
-   <span data-ttu-id="46a93-110">Éléments de l’organigramme</span><span class="sxs-lookup"><span data-stu-id="46a93-110">Flow chart elements</span></span>

<span data-ttu-id="46a93-111">En règle générale, les objets reconnus par ce module de reconnaissance sont dans une relation spatiale ou fonctionnelle à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="46a93-111">Usually, the objects that are recognized by such a recognizer are in a two-dimensional spatial or functional relationship with each other.</span></span> <span data-ttu-id="46a93-112">Par exemple, dans les relations complexes d’une équation mathématique, un module de reconnaissance peut retourner des résultats différents pour une limite supérieure sur un entier défini, par opposition à un numérateur dans une fraction.</span><span class="sxs-lookup"><span data-stu-id="46a93-112">For example, within the complex relationships in a math equation, a recognizer can return different results for an upper limit on a definite integral as opposed to a numerator in a fraction.</span></span>

<span data-ttu-id="46a93-113">En raison de la nature très générale de ces relations, il est extrêmement difficile de définir l’ensemble des interfaces qui fonctionnent pour chaque module de reconnaissance d’objets.</span><span class="sxs-lookup"><span data-stu-id="46a93-113">Because of the very general nature of these relationships, it is extremely difficult to define the set of interfaces that will work for every object recognizer.</span></span>

<span data-ttu-id="46a93-114">La technologie Tablet PC fournit une infrastructure de base pour les identificateurs d’objet dans la bibliothèque managée et les interfaces d’automatisation.</span><span class="sxs-lookup"><span data-stu-id="46a93-114">The Tablet PC Technology provides a basic framework for object recognizers in the Managed Library and Automation interfaces.</span></span> <span data-ttu-id="46a93-115">Toutefois, vous devez développer des interfaces personnalisées qui décrivent des relations spatiales complexes entre des objets reconnus pour chaque module de reconnaissance d’objet.</span><span class="sxs-lookup"><span data-stu-id="46a93-115">However, you must develop custom interfaces that describe complex spatial relationships between recognized objects for each object recognizer.</span></span> <span data-ttu-id="46a93-116">Plus précisément, pour les regroupements d’objets, la plateforme fournit l’objet [**RecognizerContext**](inkrecognizercontext-class.md) de base permettant d’associer l’objet [**Ink**](inkdisp-class.md) au contexte du module de reconnaissance et d’appeler le module de reconnaissance pour effectuer la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="46a93-116">Specifically, for object recognizers, the platform provides the basic [**RecognizerContext**](inkrecognizercontext-class.md) object for associating the [**Ink**](inkdisp-class.md) object with the recognizer context and for calling the recognizer to perform the recognition.</span></span>

 

 



