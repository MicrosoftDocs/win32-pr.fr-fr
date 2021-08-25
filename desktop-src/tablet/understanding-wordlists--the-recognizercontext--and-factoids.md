---
description: Tous les dictionnaires d’application sont implémentés à l’aide de l’objet de la demande.
ms.assetid: 805788ec-1672-462a-b188-c680f56c2641
title: Compréhension des listes de mots, du contexte de reconnaissance et des Factoids
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60fbfc7a3a3099a1146307637d20e777cca416789a61f5dd034f9d86911f1a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842809"
---
# <a name="understanding-word-lists-recognizer-context-and-factoids"></a>Compréhension des listes de mots, du contexte de reconnaissance et des Factoids

Tous les dictionnaires d’application sont implémentés [**à l’aide de l’objet de**](inkwordlist-class.md) la demande. L’objet [**RecognizerContext**](inkrecognizercontext-class.md) gère la reconnaissance, en partie [**via la propriété de la référence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) de cet objet. L’objet **RecognizerContext** transmet la liste de mots au module de reconnaissance. Vous pouvez activer un dictionnaire d’applications dans n’importe quel **RecognizerContext** de votre application en définissant **la propriété de la propriété** de la propriété de l’objet **RecognizerContext** . Pour que la liste de mots soit disponible pour l’ensemble de l’application, vous devez définir **la propriété liste de mots de** chaque objet **RecognizerContext** dans l’application.

Au niveau du module de reconnaissance, tous les dictionnaires, à l’exception du dictionnaire système, sont implémentés en tant que listes de mots. Toutefois, le module de reconnaissance ne peut avoir qu’une seule liste de mots actifs à la fois. Cela signifie que vous ne pouvez pas avoir à la fois un dictionnaire d’applications et le dictionnaire utilisateur actifs. En revanche, le dictionnaire système est toujours disponible, sauf si un Factoid est défini pour désactiver le dictionnaire système.

Le dictionnaire utilisateur est la liste des mots que l’utilisateur a ajoutés à son Tablet PC. Si la propriété liste de [**mots**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) de [**RecognizerContext**](inkrecognizercontext-class.md) n’est pas définie, **RecognizerContext** passe le dictionnaire utilisateur en tant que liste de mots au module de reconnaissance. Toutefois, si la propriété liste de **mots** de l’objet **RecognizerContext** est définie, la liste de mots est transmise au module de reconnaissance au lieu du dictionnaire de l’utilisateur.

> [!Note]  
> La propriété [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) de l’objet [**RecognizerContext**](inkrecognizercontext-class.md) doit être vide avant de définir la propriété de la propriété [**de la propriété**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) . Si la propriété **Strokes** n’est pas vide, une exception est levée. Les mots ne doivent jamais être ajoutés à une liste de mots une fois qu’elle a été affectée à un objet **RecognizerContext** .

 

La définition d’un Factoid sur l’objet [**RecognizerContext**](inkrecognizercontext-class.md) affecte également la manière dont le module de reconnaissance utilise les dictionnaires d’applications. Les Factoids qui affectent le comportement des dictionnaires sont les suivants :

-   **Mots**
-   **SystemDictionary**
-   **Aucun**

Jusqu’à présent, la Factoid la plus utile pour les dictionnaires d’applications est **la Factoid.** La liste de **mots** Factoid biaise le module de reconnaissance pour retourner uniquement les mots trouvés dans la liste de mots. Ce Factoid désactive tous les autres dictionnaires, à l’exception de la liste de mots. Si la liste de **mots** Factoid est définie et qu’aucune liste de mots n’est spécifiée dans le contexte du module de reconnaissance, le dictionnaire de l’utilisateur est utilisé comme liste de mots.

Par exemple, si vous concevez une application de parties aériennes avec un champ qui accepte l’un des dix noms de parties spécialisées, vous pouvez créer une liste de mots qui contient uniquement ces noms de parties. La définition **de la** zone de texte Factoid pour le champ améliore considérablement la reconnaissance pour les mots entrés dans ce champ. Le module de reconnaissance n’a pas besoin de choisir entre les mots dans le dictionnaire système et les mots dans la liste de mots.

**SystemDictionary** Factoid active le dictionnaire système uniquement. Le Factoid **None** désactive tous les dictionnaires. Ces deux Factoids sont utilisés pour augmenter la précision de la reconnaissance dans certains cas. Toutefois, étant donné qu’ils désactivent les dictionnaires d’applications, ils sont rarement utilisés conjointement avec les dictionnaires d’applications.

Pour plus d’informations sur la façon dont Factoids affecte la reconnaissance, consultez [utilisation du contexte pour améliorer la précision](using-context-to-improve-accuracy.md).

Pour plus d’informations sur **SystemDictionary** et **None** Factoids, consultez [prise en charge de Factoids à partir de la version 1](supported-factoids-from-version-1.md).

 

 



