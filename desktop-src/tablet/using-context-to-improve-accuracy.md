---
description: Un moteur de reconnaissance de l’écriture manuscrite, ou module de reconnaissance, est un logiciel qui traite l’encre et convertit cette entrée manuscrite en texte.
ms.assetid: b64f6856-453c-4080-84e0-0a9e69e79de7
title: Utilisation du contexte pour améliorer la précision
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd5c807804c1855e0be56b09f08448e3dc2967d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515643"
---
# <a name="using-context-to-improve-accuracy"></a><span data-ttu-id="06198-103">Utilisation du contexte pour améliorer la précision</span><span class="sxs-lookup"><span data-stu-id="06198-103">Using Context to Improve Accuracy</span></span>

<span data-ttu-id="06198-104">Un moteur de reconnaissance de l’écriture manuscrite, ou module de reconnaissance, est un logiciel qui traite l’encre et convertit cette entrée manuscrite en texte.</span><span class="sxs-lookup"><span data-stu-id="06198-104">A handwriting recognition engine, or recognizer, is software that processes ink and converts that ink into text.</span></span> <span data-ttu-id="06198-105">Un contexte est pertinent pour les informations spécifiques à l’application que vous fournissez à un module de reconnaissance pour améliorer la précision de la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="06198-105">A context is relevant, application-specific information that you provide to a recognizer to improve recognition accuracy.</span></span> <span data-ttu-id="06198-106">En d’autres termes, le contexte est une information sur l’entrée qui aide le module de reconnaissance à traiter avec précision l’encre dans un champ.</span><span class="sxs-lookup"><span data-stu-id="06198-106">In other words, context is any piece of information about input that aids the recognizer in accurately processing the ink in a field.</span></span>

<span data-ttu-id="06198-107">Cette section décrit les différentes façons dont vous pouvez tirer parti du contexte dans votre application Tablet PC, en mettant l’accent sur la technique de programmation par défaut pour les applications qui ne sont pas activées pour l’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="06198-107">This section describes the different ways you can take advantage of context in your Tablet PC application, placing emphasis on the preferred programmatic technique for applications that are not ink enabled.</span></span>

> [!Note]  
> <span data-ttu-id="06198-108">Les sections de la technologie Tablet PC du kit de développement logiciel (SDK) de Windows Vista permettent d’utiliser le terme « contexte » en ce qui concerne l’objet [**RecognizerContext**](inkrecognizercontext-class.md) et ses propriétés [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) et [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) .</span><span class="sxs-lookup"><span data-stu-id="06198-108">There are places in the Tablet PC Technology sections of the Windows Vista Software Development Kit (SDK) where the term "context" is used in regard to the [**RecognizerContext**](inkrecognizercontext-class.md) object and its [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) and [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) properties.</span></span> <span data-ttu-id="06198-109">Ne confondez pas ces autres utilisations de « context » avec la définition de cette section.</span><span class="sxs-lookup"><span data-stu-id="06198-109">Do not confuse these other usages of "context" with the definition in this section.</span></span>

 

 

 



