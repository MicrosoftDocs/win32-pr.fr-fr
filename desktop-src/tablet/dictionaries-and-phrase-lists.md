---
description: Le lexique, ou la liste des mots possibles utilisés par le modèle de langage d’un module de reconnaissance particulier, est contenu dans un ou plusieurs dictionnaires.
ms.assetid: e975a75f-ab88-4164-afc8-3b817988504d
title: Dictionnaires et listes d’expressions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f88dc2f6b05eea322b6e88dda1f986b3c54b7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528295"
---
# <a name="dictionaries-and-phrase-lists"></a><span data-ttu-id="38eb7-103">Dictionnaires et listes d’expressions</span><span class="sxs-lookup"><span data-stu-id="38eb7-103">Dictionaries and Phrase lists</span></span>

<span data-ttu-id="38eb7-104">Le lexique, ou la liste des mots possibles utilisés par le modèle de langage d’un module de reconnaissance particulier, est contenu dans un ou plusieurs dictionnaires.</span><span class="sxs-lookup"><span data-stu-id="38eb7-104">The lexicon, or list of possible words used by a particular recognizer's language model, is contained in one or more dictionaries.</span></span> <span data-ttu-id="38eb7-105">Le module de reconnaissance recherche tous les dictionnaires disponibles sur le système lors de la compilation des correspondances de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="38eb7-105">The recognizer searches all dictionaries available on the system when compiling recognition matches.</span></span> <span data-ttu-id="38eb7-106">Vous pouvez utiliser les API Microsoft Speech (SAPI) pour modifier certains de ces dictionnaires.</span><span class="sxs-lookup"><span data-stu-id="38eb7-106">You can use the Microsoft Speech APIs (SAPI) to modify some of these dictionaries.</span></span>

<span data-ttu-id="38eb7-107">Une liste d’expressions fournit une autre méthode de modification du vocabulaire du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="38eb7-107">A phrase list provides another means of modifying the recognizer's vocabulary.</span></span> <span data-ttu-id="38eb7-108">L’ajout de mots à une liste d’expressions étend le vocabulaire ; Ajouter des mots, puis contraindre le module de reconnaissance pour utiliser uniquement la liste d’expressions (contrairement à la liste d’expressions et aux dictionnaires), limite le vocabulaire.</span><span class="sxs-lookup"><span data-stu-id="38eb7-108">Adding words to a phrase list extends the vocabulary; adding words and then constraining the recognizer to use only the phrase list (as opposed to the phrase list and the dictionaries) restricts the vocabulary.</span></span>

<span data-ttu-id="38eb7-109">Les versions précédentes des API de technologie Tablet PC reposaient sur le concept de listes de mots.</span><span class="sxs-lookup"><span data-stu-id="38eb7-109">Previous releases of the Tablet PC Technology APIs relied on the concept of word lists.</span></span> <span data-ttu-id="38eb7-110">Les listes de mots sont presque identiques aux listes d’expressions et sont utilisées dans le même but quand vous travaillez directement avec un objet [**RecognizerContext**](inkrecognizercontext-class.md) dans une application activée pour l’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="38eb7-110">Word lists are almost identical to phrase lists and are used for the same purpose when working directly with a [**RecognizerContext**](inkrecognizercontext-class.md) object in an application that is ink enabled.</span></span> <span data-ttu-id="38eb7-111">Pour plus d’informations sur l’emplacement et le moment d’utilisation des listes de mots, consultez [définition du contexte pour les contrôles Ink-Enabled](setting-context-for-ink-enabled-controls.md).</span><span class="sxs-lookup"><span data-stu-id="38eb7-111">For more details about where and when to use word lists, see [Setting Context for Ink-Enabled Controls](setting-context-for-ink-enabled-controls.md).</span></span>

<span data-ttu-id="38eb7-112">Lorsque la taille de la liste avec laquelle vous souhaitez étendre le lexique dépasse 100 000 mots, nous vous recommandons d’utiliser un dictionnaire à la place d’une liste de mots ou d’expressions.</span><span class="sxs-lookup"><span data-stu-id="38eb7-112">When the size of the list with which you want to extend the lexicon exceeds 100,000 words, we recommend that you use a dictionary instead of a word list or phrase list.</span></span>

 

 



