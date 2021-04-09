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
# <a name="custom-input-scopes-with-regular-expressions"></a>Étendues d’entrée personnalisées avec des expressions régulières

Vous pouvez définir des étendues d’entrée personnalisées à l’aide de modèles de langage composés d’expressions régulières pour l’écriture manuscrite et leur affectation à des champs.

Par exemple, si vous créez une application de base de données pour des composants d’entrepôt et que vous souhaitez que les utilisateurs puissent entrer des numéros de référence à l’aide du bloc d’écriture du panneau de saisie Tablet PC. Si la syntaxe du numéro de référence se compose de trois lettres suivies de quatre chiffres suivis d’une autre lettre (par exemple, ABC1234D), la reconnaissance de l’écriture manuscrite aurait du mal à reconnaître une telle entrée, car elle n’est pas définie dans le modèle de langage. Il n’existe aucun Factoid prédéfini qui correspond à une telle syntaxe, et Microsoft ne peut pas inclure la syntaxe pour chaque champ possible qu’une application peut avoir besoin. L’écriture d’expressions régulières d’écriture permet aux applications de définir facilement leur propre modèle de langage pour un champ particulier à usage spécial.

> [!Note]  
> Lorsque vous travaillez dans une application compatible avec l’écriture manuscrite qui utilise la propriété [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) de l’objet [**RecognizerContext**](inkrecognizercontext-class.md) , vous ne pouvez pas utiliser la version 1 Factoids dans une expression régulière.

 

 

 



