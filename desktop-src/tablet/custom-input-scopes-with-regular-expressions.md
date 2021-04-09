---
description: Vous pouvez définir des étendues d’entrée personnalisées à l’aide de modèles de langage composés d’expressions régulières pour l’écriture manuscrite et leur affectation à des champs. Par exemple, si vous créez une application de base de données pour des composants d’entrepôt et que vous souhaitez que les utilisateurs puissent entrer des numéros de référence à l’aide du bloc d’écriture du panneau de saisie Tablet PC. Si la syntaxe du numéro de référence se compose de trois lettres suivies de quatre chiffres suivis d’une autre lettre (par exemple, ABC1234D), la reconnaissance de l’écriture manuscrite aurait du mal à reconnaître une telle entrée, car elle n’est pas définie dans le modèle de langage. Il n’existe aucun Factoid prédéfini qui correspond à une telle syntaxe, et Microsoft ne peut pas inclure la syntaxe pour chaque champ possible qu’une application peut avoir besoin. L’écriture d’expressions régulières d’écriture permet aux applications de définir facilement leur propre modèle de langage pour un champ particulier à usage spécial. Remarque Lorsque vous travaillez dans une application compatible avec l’écriture manuscrite qui utilise la propriété Factoid de l’objet RecognizerContext, vous ne pouvez pas utiliser la version 1 Factoids dans une expression régulière.
ms.assetid: 71f80196-0a36-4a14-a115-712bc909f6d7
title: Étendues d’entrée personnalisées avec des expressions régulières
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bdd7807221aca7b05ed4dc1facf7ddb01470c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033790"
---
# <a name="custom-input-scopes-with-regular-expressions"></a><span data-ttu-id="15a2a-106">Étendues d’entrée personnalisées avec des expressions régulières</span><span class="sxs-lookup"><span data-stu-id="15a2a-106">Custom Input Scopes with Regular Expressions</span></span>

<span data-ttu-id="15a2a-107">Vous pouvez définir des étendues d’entrée personnalisées à l’aide de modèles de langage composés d’expressions régulières pour l’écriture manuscrite et leur affectation à des champs.</span><span class="sxs-lookup"><span data-stu-id="15a2a-107">You can define custom input scopes by using language models composed of regular expressions for handwriting and assigning them to fields.</span></span>

<span data-ttu-id="15a2a-108">Par exemple, si vous créez une application de base de données pour des composants d’entrepôt et que vous souhaitez que les utilisateurs puissent entrer des numéros de référence à l’aide du bloc d’écriture du panneau de saisie Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="15a2a-108">For example, if you are creating a database application for warehouse parts and want users to be able to enter part numbers using the Tablet PC Input Panel's writing pad.</span></span> <span data-ttu-id="15a2a-109">Si la syntaxe du numéro de référence se compose de trois lettres suivies de quatre chiffres suivis d’une autre lettre (par exemple, ABC1234D), la reconnaissance de l’écriture manuscrite aurait du mal à reconnaître une telle entrée, car elle n’est pas définie dans le modèle de langage.</span><span class="sxs-lookup"><span data-stu-id="15a2a-109">If the part number syntax consists of three letters followed by four numbers followed by another letter (for example, ABC1234D), the handwriting recognizer would have a difficult time recognizing such input because it is not defined in the language model.</span></span> <span data-ttu-id="15a2a-110">Il n’existe aucun Factoid prédéfini qui correspond à une telle syntaxe, et Microsoft ne peut pas inclure la syntaxe pour chaque champ possible qu’une application peut avoir besoin.</span><span class="sxs-lookup"><span data-stu-id="15a2a-110">There is no predefined factoid that corresponds to such syntax, nor can Microsoft include the syntax for every possible field an application might need.</span></span> <span data-ttu-id="15a2a-111">L’écriture d’expressions régulières d’écriture permet aux applications de définir facilement leur propre modèle de langage pour un champ particulier à usage spécial.</span><span class="sxs-lookup"><span data-stu-id="15a2a-111">Handwriting regular expressions provide an easy way for applications to define their own language model for a particular special-use field.</span></span>

> [!Note]  
> <span data-ttu-id="15a2a-112">Lorsque vous travaillez dans une application compatible avec l’écriture manuscrite qui utilise la propriété [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) de l’objet [**RecognizerContext**](inkrecognizercontext-class.md) , vous ne pouvez pas utiliser la version 1 Factoids dans une expression régulière.</span><span class="sxs-lookup"><span data-stu-id="15a2a-112">When working in an ink-enabled application that uses the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object, you cannot use version 1 factoids in a regular expression.</span></span>

 

 

 



