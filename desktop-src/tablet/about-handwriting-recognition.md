---
description: Tablet PC comprend une technologie permettant de reconnaître l’entrée manuscrite qui est le plus souvent sous la forme d’une écriture manuscrite.
ms.assetid: 614971a8-2b56-40d4-abb6-aba5ded01883
title: À propos de la reconnaissance de l’écriture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ff794f018cd0019a5013bacf8b9edfbe45018d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532323"
---
# <a name="about-handwriting-recognition"></a><span data-ttu-id="d5bd1-103">À propos de la reconnaissance de l’écriture</span><span class="sxs-lookup"><span data-stu-id="d5bd1-103">About Handwriting Recognition</span></span>

<span data-ttu-id="d5bd1-104">Tablet PC comprend une technologie permettant de reconnaître l’entrée manuscrite qui est le plus souvent sous la forme d’une écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="d5bd1-104">Tablet PC includes technology for recognizing ink input that is most commonly in the form of handwriting.</span></span> <span data-ttu-id="d5bd1-105">Le module logiciel qui fournit la reconnaissance porte le nom de module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="d5bd1-105">The software module that provides the recognition is called a recognizer.</span></span> <span data-ttu-id="d5bd1-106">Un module de reconnaissance reconnaît une langue, un groupe de langues associées ou une classe d’objets connexes tels que des notes musicales, des gestes système ou des formes géométriques.</span><span class="sxs-lookup"><span data-stu-id="d5bd1-106">A recognizer recognizes one language, a group of related languages, or a class of related objects such as musical notes, system gestures, or geometric shapes.</span></span> <span data-ttu-id="d5bd1-107">Vous pouvez ajouter dynamiquement des modules de reconnaissance au système des services d’encre.</span><span class="sxs-lookup"><span data-stu-id="d5bd1-107">You can dynamically add recognizers to the ink services system.</span></span>

## <a name="recognition-steps"></a><span data-ttu-id="d5bd1-108">Étapes de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="d5bd1-108">Recognition Steps</span></span>

<span data-ttu-id="d5bd1-109">La reconnaissance est gérée à l’aide d’un contexte de module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="d5bd1-109">Recognition is handled through the use of a recognizer context.</span></span> <span data-ttu-id="d5bd1-110">La reconnaissance se compose de quatre étapes de base :</span><span class="sxs-lookup"><span data-stu-id="d5bd1-110">Recognition consists of four basic steps:</span></span>

1.  <span data-ttu-id="d5bd1-111">Configuration des contraintes de reconnaissance en :</span><span class="sxs-lookup"><span data-stu-id="d5bd1-111">Setting up the recognition constraints by:</span></span>
    -   <span data-ttu-id="d5bd1-112">Sélection du module de reconnaissance et du mode de saisie (contraintes géométriques).</span><span class="sxs-lookup"><span data-stu-id="d5bd1-112">Selecting the recognizer and input mode (geometric constraints).</span></span>
    -   <span data-ttu-id="d5bd1-113">Définition des contraintes de langue.</span><span class="sxs-lookup"><span data-stu-id="d5bd1-113">Setting the language constraints.</span></span> <span data-ttu-id="d5bd1-114">Par exemple, vous pouvez limiter l’entrée à des caractères alphanumériques ou vous pouvez passer des schémas pour aider le module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="d5bd1-114">For example, you can restrict input to alphanumeric characters or you can pass schemas to assist the recognizer.</span></span>
2.  <span data-ttu-id="d5bd1-115">Envoi d’une entrée manuscrite au module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="d5bd1-115">Sending ink to the recognizer.</span></span>
3.  <span data-ttu-id="d5bd1-116">Traitement de l’entrée (reconnaissance).</span><span class="sxs-lookup"><span data-stu-id="d5bd1-116">Processing the input (recognizing).</span></span>
4.  <span data-ttu-id="d5bd1-117">Retour des résultats de la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="d5bd1-117">Returning the results of the recognition.</span></span>

<span data-ttu-id="d5bd1-118">Les étapes 2 et 3 peuvent être répétées dans une boucle, ou tous les traits d’encre peuvent être ajoutés à l’encre avant une tentative de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="d5bd1-118">Steps 2 and 3 may be repeated in a loop, or all of the ink strokes may be added to the ink before recognition is attempted.</span></span>

## <a name="samples-and-related-topics"></a><span data-ttu-id="d5bd1-119">Exemples et Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5bd1-119">Samples and Related Topics</span></span>

<span data-ttu-id="d5bd1-120">L' [exemple de reconnaissance avancée](advanced-recognition-sample.md) montre comment utiliser des détecteurs avec des objets [**Ink**](inkdisp-class.md) pour effectuer la reconnaissance de l’encre.</span><span class="sxs-lookup"><span data-stu-id="d5bd1-120">[Advanced Recognition Sample](advanced-recognition-sample.md) demonstrates how to use recognizers with [**Ink**](inkdisp-class.md) objects to perform ink recognition.</span></span>

<span data-ttu-id="d5bd1-121">L' [exemple de modèle de dll de reconnaissance](recognizer-dll-sample-template.md) contient un modèle pour la création d’une dll de module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="d5bd1-121">[Recognizer DLL Sample Template](recognizer-dll-sample-template.md) contains a template for creating a recognizer DLL.</span></span> <span data-ttu-id="d5bd1-122">Le modèle contient des fonctions pour l’inscription et l’annulation de l’inscription du serveur, ainsi que des squelettes pour les fonctions de reconnaissance principales.</span><span class="sxs-lookup"><span data-stu-id="d5bd1-122">The template contains functions for registering and unregistering the server, as well as skeletons for primary recognizer functions.</span></span>

<span data-ttu-id="d5bd1-123">Les sections suivantes décrivent les concepts de base qui sous-tendent la technologie de reconnaissance de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="d5bd1-123">The following sections describe the basic concepts behind the Tablet PC recognition technology.</span></span> <span data-ttu-id="d5bd1-124">Pour plus d’informations sur la création de détecteurs personnalisés, consultez [création d’un module de reconnaissance](creating-a-recognizer.md).</span><span class="sxs-lookup"><span data-stu-id="d5bd1-124">For detailed information about creating custom recognizers, see [Creating a Recognizer](creating-a-recognizer.md).</span></span>

-   [<span data-ttu-id="d5bd1-125">Reconnaissance de texte</span><span class="sxs-lookup"><span data-stu-id="d5bd1-125">Text Recognizers</span></span>](text-recognizers.md)
-   [<span data-ttu-id="d5bd1-126">Identificateurs d’objets</span><span class="sxs-lookup"><span data-stu-id="d5bd1-126">Object Recognizers</span></span>](object-recognizers.md)
-   [<span data-ttu-id="d5bd1-127">Utilisation de la collection Recognizers</span><span class="sxs-lookup"><span data-stu-id="d5bd1-127">Using the Recognizers Collection</span></span>](using-the-recognizers-collection.md)
-   [<span data-ttu-id="d5bd1-128">Contexte du module de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="d5bd1-128">Recognizer Context</span></span>](recognizer-context.md)
-   [<span data-ttu-id="d5bd1-129">Segments de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="d5bd1-129">Recognition Segments</span></span>](recognition-segments.md)
-   [<span data-ttu-id="d5bd1-130">Reconnaissance du texte en angle</span><span class="sxs-lookup"><span data-stu-id="d5bd1-130">Recognition of Angled Text</span></span>](recognition-of-angled-text.md)
-   [<span data-ttu-id="d5bd1-131">Prise en charge de la réorganisation de la séquence de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="d5bd1-131">Recognizer Stroke Reordering Support</span></span>](recognizer-stroke-reordering-support.md)
-   [<span data-ttu-id="d5bd1-132">Dictionnaires et Factoids</span><span class="sxs-lookup"><span data-stu-id="d5bd1-132">Dictionaries and Factoids</span></span>](dictionaries-and-factoids.md)
-   <span data-ttu-id="d5bd1-133">[Propriété \[ de confiance sur la reconnaissance\]](confidence-property--about-recognition.md)</span><span class="sxs-lookup"><span data-stu-id="d5bd1-133">[Confidence Property \[About Recognition\]](confidence-property--about-recognition.md)</span></span>
-   [<span data-ttu-id="d5bd1-134">Alternatives</span><span class="sxs-lookup"><span data-stu-id="d5bd1-134">Alternates</span></span>](alternates.md)
-   [<span data-ttu-id="d5bd1-135">Segments d’encre et alternatives</span><span class="sxs-lookup"><span data-stu-id="d5bd1-135">Ink Segments and Alternates</span></span>](ink-segments-and-alternates.md)

 

 



