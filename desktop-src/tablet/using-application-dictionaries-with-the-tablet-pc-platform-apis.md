---
description: Pour utiliser un dictionnaire d’applications avec l’API Tablet PC, vous devez d’abord créer un fichier avec la liste de mots pour votre dictionnaire d’applications.
ms.assetid: 6abadad1-262b-4536-8846-1c06226dc18a
title: Utilisation de dictionnaires d’applications avec les API de plateforme Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fc0e444ad2213d945c0210d07c72f9540ae16be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519285"
---
# <a name="using-application-dictionaries-with-the-tablet-pc-platform-apis"></a><span data-ttu-id="9c833-103">Utilisation de dictionnaires d’applications avec les API de plateforme Tablet PC</span><span class="sxs-lookup"><span data-stu-id="9c833-103">Using Application Dictionaries with the Tablet PC Platform APIs</span></span>

<span data-ttu-id="9c833-104">Pour utiliser un dictionnaire d’applications avec l’API Tablet PC, vous devez d’abord créer un fichier avec la liste de mots pour votre dictionnaire d’applications.</span><span class="sxs-lookup"><span data-stu-id="9c833-104">To use an application dictionary with the Tablet PC API, you must first create a file with the list of words for your application dictionary.</span></span>

<span data-ttu-id="9c833-105">La solution la plus simple consiste à utiliser un fichier texte qui contient une liste de mots.</span><span class="sxs-lookup"><span data-stu-id="9c833-105">The easiest solution for this is to use a text file that contains a list of the words.</span></span> <span data-ttu-id="9c833-106">Lorsque votre application se charge, elle lit le fichier texte et crée [**un objet liste de mots à**](inkwordlist-class.md) partir de la liste des mots du fichier.</span><span class="sxs-lookup"><span data-stu-id="9c833-106">When your application loads, it reads the text file and creates a [**WordList**](inkwordlist-class.md) object from the list of words in the file.</span></span> <span data-ttu-id="9c833-107">Pour chaque [**RecognizerContext**](inkrecognizercontext-class.md) associé au dictionnaire d’applications, définissez la propriété liste de [**mots**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) de l’objet **RecognizerContext** sur la liste de mots du fichier texte.</span><span class="sxs-lookup"><span data-stu-id="9c833-107">For each [**RecognizerContext**](inkrecognizercontext-class.md) associated with the application dictionary, set the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the **RecognizerContext** object to the word list in the text file.</span></span>

<span data-ttu-id="9c833-108">L’exemple suivant montre comment créer un objet de la collection de [**mots**](inkwordlist-class.md) à partir d’une collection [StringCollection](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="9c833-108">The following example illustrates how to create a [**WordList**](inkwordlist-class.md) object from a [StringCollection](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1) collection.</span></span> <span data-ttu-id="9c833-109">Cet exemple suppose que vous avez déjà chargé la liste des mots à partir du disque et créé une collection StringCollection à partir de ces mots.</span><span class="sxs-lookup"><span data-stu-id="9c833-109">This example assumes that you have already loaded the list of words from disk and created a StringCollection collection from these words.</span></span>


```C++
using System.Collections.Specialized;
using Microsoft.Ink;
//...
RecognizerContext theRecognizerContext;
StringCollection theUserDictionary;
//... 
// Initialize theRecognizerContext and theUserDictionary objects here.
//...
WordList theUserWordList = new WordList();
foreach (string s in theUserDictionary)
{
    theUserWordList.Add(s);
}
theRecognizerContext.WordList = theUserWordList;
```



> [!Note]  
> <span data-ttu-id="9c833-110">La propriété [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) de l’objet [**RecognizerContext**](inkrecognizercontext-class.md) doit être vide avant de définir la propriété de la propriété [**de la propriété**](inkwordlist-class.md) .</span><span class="sxs-lookup"><span data-stu-id="9c833-110">The [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object must be empty before you set the [**WordList**](inkwordlist-class.md) property.</span></span> <span data-ttu-id="9c833-111">Si la propriété [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) n’est pas vide, une exception est levée.</span><span class="sxs-lookup"><span data-stu-id="9c833-111">If the [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) property is not empty, an exception is thrown.</span></span> <span data-ttu-id="9c833-112">En outre, les mots ne doivent jamais être ajoutés à une liste de mots une fois qu’elle a été affectée à un objet **RecognizerContext** .</span><span class="sxs-lookup"><span data-stu-id="9c833-112">In addition, words should never be added to a word list after it has been assigned to a **RecognizerContext** object.</span></span> <span data-ttu-id="9c833-113">Les mots qui sont ajoutés à la liste de mots une fois qu’elle est assignée à l’objet **RecognizerContext** ne sont pas mis à jour dans le module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="9c833-113">Words that are added to the word list after it is assigned to the **RecognizerContext** object are not updated in the recognizer.</span></span> <span data-ttu-id="9c833-114">Pour mettre à jour la liste de mots, vous devez réassigner **l’objet liste de mots à** [**la propriété liste de mots de**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) l’objet **RecognizerContext** .</span><span class="sxs-lookup"><span data-stu-id="9c833-114">To update the word list you must reassign the **WordList** object to the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the **RecognizerContext** object.</span></span>

 

<span data-ttu-id="9c833-115">Pour une précision de reconnaissance maximale, combinez Factoids avec votre dictionnaire d’applications dans une relation avantageuse.</span><span class="sxs-lookup"><span data-stu-id="9c833-115">For maximum recognition accuracy, combine factoids with your application dictionary in an advantageous relationship.</span></span> <span data-ttu-id="9c833-116">Pour plus d’informations sur la relation entre les Factoids et les dictionnaires d’application, consultez [Présentation des listes de mots, du contexte de reconnaissance et de Factoids](understanding-wordlists--the-recognizercontext--and-factoids.md).</span><span class="sxs-lookup"><span data-stu-id="9c833-116">For more information about the relationship between factoids and application dictionaries, see [Understanding Word Lists, Recognizer Context, and Factoids](understanding-wordlists--the-recognizercontext--and-factoids.md).</span></span>

<span data-ttu-id="9c833-117">Pour obtenir un exemple d’utilisation de dictionnaires d’application avec le contrôle [InkEdit](inkedit-control-reference.md) , consultez [utilisation d’un dictionnaire d’applications avec InkEdit](using-an-application-dictionary-with-inkedit.md).</span><span class="sxs-lookup"><span data-stu-id="9c833-117">For an example of using application dictionaries with the [InkEdit](inkedit-control-reference.md) control, see [Using an Application Dictionary with InkEdit](using-an-application-dictionary-with-inkedit.md).</span></span>

 

 
