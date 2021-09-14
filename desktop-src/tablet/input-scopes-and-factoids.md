---
description: Décrit comment les étendues d’entrée sont utilisées pour la reconnaissance.
ms.assetid: 9faf6d22-b80d-4020-ac74-ee40b31ae9d4
title: Étendues d’entrée et Factoids
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bbb46e21a0524f806daa4eed789fde31e285109
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196264"
---
# <a name="input-scopes-and-factoids"></a>Étendues d’entrée et Factoids

Une étendue d’entrée est un ensemble de mots, de chiffres, de signes de ponctuation et d’ordre syntaxique définis qui sont autorisés dans un modèle de langage donné. Les étendues d’entrée peuvent être utilisées par les applications pour restreindre le modèle de langue utilisé par le module de reconnaissance à un contexte spécifique. Par exemple, l’étendue d’entrée de \_ \_ l’e-mail SMTPEMAILADDRESS influence les résultats de la reconnaissance en indiquant qu’un champ spécifique est une adresse de messagerie. Ainsi, le champ est susceptible de contenir des caractères tels que « @" and " \_ » et il ne peut pas contenir de caractères tels que « \* » et des espaces.

> [!Note]  
> D’autres technologies Microsoft utilisent également des étendues d’entrée. Cet article se concentre sur l’utilisation du contexte pour améliorer la précision des moteurs de reconnaissance de l’écriture manuscrite pour les applications Tablet PC.

 

Les versions précédentes de l’API de technologie Tablet PC utilisaient Factoids pour définir le contexte. Pour des raisons pratiques, un Factoid est la même chose qu’une étendue d’entrée. La version de l’une des plateformes du kit de développement logiciel (SDK) Tablet PC a défini un ensemble de valeurs Factoid dans l’objet [**Factoid**](factoid-constants.md) . Ces valeurs ont été utilisées pour définir le contexte et influencer les résultats de la reconnaissance lors de l’utilisation de l’objet [**RecognizerContext**](inkrecognizercontext-class.md) pour la reconnaissance. pour les identifiants du script Latin commençant par Windows XP édition Tablet PC 2005, vous utilisez toujours la propriété [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) de l’objet **RecognizerContext** pour définir le contexte, mais vous devez passer une étendue d’entrée, une liste d’expressions ou une valeur d’expression régulière d’écriture manuscrite au lieu de l’une des valeurs Factoid de la version. Les Microsoft Recognizers de caractères d’Extrême-Orient ne prennent pas en charge l’utilisation des valeurs énumérées de l’étendue d’entrée. Vous devez continuer à utiliser des valeurs Factoid pour les identificateurs de caractères d’Extrême-Orient.

Les étendues d’entrée et les Factoids sont des restrictions sur les alternatives au niveau du mot ; les caractères alternatifs peuvent se trouver en dehors de l’étendue d’entrée spécifiée, même lorsque l’indicateur de **forçage** est défini.

Lorsque l’indicateur de **forçage** est défini avec un Factoid restrictif, il peut arriver que le module de reconnaissance ne puisse pas produire une réponse qui corresponde à la fois à l’encre et à la Factoid. Un autre scénario où le module de reconnaissance peut ne pas produire de réponse satisfaisante est lorsque la langue du module de reconnaissance ne correspond pas à la langue de l’encre (par exemple, le module de reconnaissance de l’anglais des États-Unis et les caractères d’encre chinoise).

Lorsque le module de reconnaissance de l’écriture manuscrite ne peut pas reconnaître l’encre d’un mot ou d’un caractère donné, il peut retourner une liste alternative vide ou une autre liste où le premier choix est le point de code 0xFFFF (caractère non défini). Cela est particulièrement utile dans les modes de saisie de guide boxed, où chaque boîte avec une encre est supposée avoir une liste non vide d’autres alternatives. L’application peut ensuite afficher ce caractère non défini de la manière choisie (par exemple, «  ??? »).

> [!Note]  
> Les valeurs Factoid continuent de fonctionner avec les module de reconnaissance du script latin pour des raisons de compatibilité descendante.

 

Pour plus d’informations sur Factoids, consultez [définition du contexte pour les contrôles Ink-Enabled](setting-context-for-ink-enabled-controls.md).

Pour plus d’informations sur les Factoids d’Extrême-Orient, consultez [prise en charge de Factoids à partir de la version 1](supported-factoids-from-version-1.md).

 

 



