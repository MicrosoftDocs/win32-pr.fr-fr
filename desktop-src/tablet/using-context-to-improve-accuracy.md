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
# <a name="using-context-to-improve-accuracy"></a>Utilisation du contexte pour améliorer la précision

Un moteur de reconnaissance de l’écriture manuscrite, ou module de reconnaissance, est un logiciel qui traite l’encre et convertit cette entrée manuscrite en texte. Un contexte est pertinent pour les informations spécifiques à l’application que vous fournissez à un module de reconnaissance pour améliorer la précision de la reconnaissance. En d’autres termes, le contexte est une information sur l’entrée qui aide le module de reconnaissance à traiter avec précision l’encre dans un champ.

Cette section décrit les différentes façons dont vous pouvez tirer parti du contexte dans votre application Tablet PC, en mettant l’accent sur la technique de programmation par défaut pour les applications qui ne sont pas activées pour l’écriture manuscrite.

> [!Note]  
> Les sections de la technologie Tablet PC du kit de développement logiciel (SDK) de Windows Vista permettent d’utiliser le terme « contexte » en ce qui concerne l’objet [**RecognizerContext**](inkrecognizercontext-class.md) et ses propriétés [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) et [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) . Ne confondez pas ces autres utilisations de « context » avec la définition de cette section.

 

 

 



