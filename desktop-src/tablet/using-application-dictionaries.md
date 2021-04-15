---
description: Par défaut, le module de reconnaissance utilise un dictionnaire système qui contient tous les mots couramment écrits dans une langue.
ms.assetid: 2ddf04dd-613b-4570-9474-0e33208c4012
title: Utilisation des dictionnaires d’applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74dfda443a688af9dfcec44a81f0e5ed2d50846c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484785"
---
# <a name="using-application-dictionaries"></a><span data-ttu-id="74488-103">Utilisation des dictionnaires d’applications</span><span class="sxs-lookup"><span data-stu-id="74488-103">Using Application Dictionaries</span></span>

<span data-ttu-id="74488-104">Par défaut, le module de reconnaissance utilise un dictionnaire système qui contient tous les mots couramment écrits dans une langue.</span><span class="sxs-lookup"><span data-stu-id="74488-104">By default, the recognizer uses a system dictionary that contains all of the commonly written words in a language.</span></span> <span data-ttu-id="74488-105">En outre, le module de reconnaissance possède un dictionnaire utilisateur qui contient des mots que l’utilisateur a ajoutés au dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="74488-105">In addition, the recognizer has a user dictionary that contains words that the user has added to the dictionary.</span></span> <span data-ttu-id="74488-106">Les utilisateurs ajoutent un mot au dictionnaire de l’utilisateur via le panneau de saisie Tablet PC par le biais de sélections dans :</span><span class="sxs-lookup"><span data-stu-id="74488-106">Users add a word to the user dictionary through Tablet PC Input Panel through selections in:</span></span>

-   <span data-ttu-id="74488-107">Liste alternative (lors de l’écriture).</span><span class="sxs-lookup"><span data-stu-id="74488-107">The alternate list (when writing).</span></span>
-   <span data-ttu-id="74488-108">Le menu Speech Tools (en parlant).</span><span class="sxs-lookup"><span data-stu-id="74488-108">The Speech Tools menu (when speaking).</span></span>

<span data-ttu-id="74488-109">Si vous concevez une application dans laquelle vous prévoyez que l’utilisateur écrira des mots qui ne se trouvent pas dans le dictionnaire système ou le dictionnaire de l’utilisateur, créez un dictionnaire d’applications.</span><span class="sxs-lookup"><span data-stu-id="74488-109">If you are designing an application into which you anticipate the user will write words that are not found in either the system dictionary or the user dictionary, create an application dictionary.</span></span> <span data-ttu-id="74488-110">Un dictionnaire d’applications améliore la précision de la reconnaissance en fournissant au module de reconnaissance une liste personnalisée de mots susceptibles d’être entrés comme écriture manuscrite dans une application.</span><span class="sxs-lookup"><span data-stu-id="74488-110">An application dictionary further improves recognition accuracy by providing the recognizer with an additional customized list of words likely to be entered as handwriting into an application.</span></span>

<span data-ttu-id="74488-111">Vous créez un dictionnaire d’applications à l' [**aide de l’objet de**](inkwordlist-class.md) la demande.</span><span class="sxs-lookup"><span data-stu-id="74488-111">You create an application dictionary by using the [**WordList**](inkwordlist-class.md) object.</span></span> <span data-ttu-id="74488-112">Le dictionnaire d’applications qui en résulte augmente la précision de la reconnaissance en fournissant au module de reconnaissance une liste de mots attendus.</span><span class="sxs-lookup"><span data-stu-id="74488-112">The ensuing application dictionary increases recognition accuracy by providing the recognizer with a list of expected words.</span></span> <span data-ttu-id="74488-113">Par exemple, un dictionnaire d’applications qui contient une terminologie médicale augmente la précision de la reconnaissance au sein d’une application développée pour l’industrie médicale dans laquelle les termes sont susceptibles d’être écrits.</span><span class="sxs-lookup"><span data-stu-id="74488-113">For example, an application dictionary that contains medical terminology increases recognition accuracy within an application developed for the medical industry into which the terms are likely to be written.</span></span>

<span data-ttu-id="74488-114">À titre d’exemple, lors de la conception d’un formulaire pour qu’un utilisateur puisse commander des instruments de musique, créez un objet de la feuille de [**mots**](inkwordlist-class.md) qui contient les noms des fabricants d’instruments les plus courants.</span><span class="sxs-lookup"><span data-stu-id="74488-114">As another example, when designing a form for someone to order musical instruments, create a [**WordList**](inkwordlist-class.md) object that contains the names of the most common instrument manufacturers.</span></span> <span data-ttu-id="74488-115">Définissez la propriété de la plage de [**mots**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) de l’objet [**RecognizerContext**](inkrecognizercontext-class.md) sur l’objet **de la sorte** que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="74488-115">Set the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object to the **WordList** object you created.</span></span> <span data-ttu-id="74488-116">Cette liste de mots est ensuite transmise à la reconnaissance par l’objet **RecognizerContext** .</span><span class="sxs-lookup"><span data-stu-id="74488-116">This list of words is then passed to the recognizer by the **RecognizerContext** object.</span></span> <span data-ttu-id="74488-117">Le dictionnaire d’applications augmente la précision de la reconnaissance lorsque ces noms sont écrits dans un champ de l’application.</span><span class="sxs-lookup"><span data-stu-id="74488-117">The application dictionary increases recognition accuracy when those names are written in a field in the application.</span></span>

<span data-ttu-id="74488-118">Les rubriques suivantes décrivent comment utiliser les dictionnaires d’applications.</span><span class="sxs-lookup"><span data-stu-id="74488-118">The following topics describe how to use application dictionaries.</span></span>

-   [<span data-ttu-id="74488-119">Compréhension des listes de mots, du contexte de reconnaissance et des Factoids</span><span class="sxs-lookup"><span data-stu-id="74488-119">Understanding Word Lists, Recognizer Context, and Factoids</span></span>](understanding-wordlists--the-recognizercontext--and-factoids.md)
-   [<span data-ttu-id="74488-120">Utilisation de dictionnaires d’applications avec les API de plateforme Tablet PC</span><span class="sxs-lookup"><span data-stu-id="74488-120">Using Application Dictionaries with the Tablet PC Platform APIs</span></span>](using-application-dictionaries-with-the-tablet-pc-platform-apis.md)
-   [<span data-ttu-id="74488-121">Création de dictionnaires personnalisés pour la reconnaissance de l’écriture manuscrite</span><span class="sxs-lookup"><span data-stu-id="74488-121">Creating Custom Dictionaries for Handwriting Recognition</span></span>](creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2.md)

 

 



