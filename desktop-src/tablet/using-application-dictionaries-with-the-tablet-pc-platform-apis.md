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
# <a name="using-application-dictionaries-with-the-tablet-pc-platform-apis"></a>Utilisation de dictionnaires d’applications avec les API de plateforme Tablet PC

Pour utiliser un dictionnaire d’applications avec l’API Tablet PC, vous devez d’abord créer un fichier avec la liste de mots pour votre dictionnaire d’applications.

La solution la plus simple consiste à utiliser un fichier texte qui contient une liste de mots. Lorsque votre application se charge, elle lit le fichier texte et crée [**un objet liste de mots à**](inkwordlist-class.md) partir de la liste des mots du fichier. Pour chaque [**RecognizerContext**](inkrecognizercontext-class.md) associé au dictionnaire d’applications, définissez la propriété liste de [**mots**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) de l’objet **RecognizerContext** sur la liste de mots du fichier texte.

L’exemple suivant montre comment créer un objet de la collection de [**mots**](inkwordlist-class.md) à partir d’une collection [StringCollection](/dotnet/api/system.collections.specialized.stringcollection?view=netcore-3.1) . Cet exemple suppose que vous avez déjà chargé la liste des mots à partir du disque et créé une collection StringCollection à partir de ces mots.


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
> La propriété [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) de l’objet [**RecognizerContext**](inkrecognizercontext-class.md) doit être vide avant de définir la propriété de la propriété [**de la propriété**](inkwordlist-class.md) . Si la propriété [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) n’est pas vide, une exception est levée. En outre, les mots ne doivent jamais être ajoutés à une liste de mots une fois qu’elle a été affectée à un objet **RecognizerContext** . Les mots qui sont ajoutés à la liste de mots une fois qu’elle est assignée à l’objet **RecognizerContext** ne sont pas mis à jour dans le module de reconnaissance. Pour mettre à jour la liste de mots, vous devez réassigner **l’objet liste de mots à** [**la propriété liste de mots de**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) l’objet **RecognizerContext** .

 

Pour une précision de reconnaissance maximale, combinez Factoids avec votre dictionnaire d’applications dans une relation avantageuse. Pour plus d’informations sur la relation entre les Factoids et les dictionnaires d’application, consultez [Présentation des listes de mots, du contexte de reconnaissance et de Factoids](understanding-wordlists--the-recognizercontext--and-factoids.md).

Pour obtenir un exemple d’utilisation de dictionnaires d’application avec le contrôle [InkEdit](inkedit-control-reference.md) , consultez [utilisation d’un dictionnaire d’applications avec InkEdit](using-an-application-dictionary-with-inkedit.md).

 

 
