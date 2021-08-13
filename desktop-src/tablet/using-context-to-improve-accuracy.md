---
description: Un moteur de reconnaissance de l’écriture manuscrite, ou module de reconnaissance, est un logiciel qui traite l’encre et convertit cette entrée manuscrite en texte.
ms.assetid: b64f6856-453c-4080-84e0-0a9e69e79de7
title: Utilisation du contexte pour améliorer la précision
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7564c18ace39c17e8877c3e5edee6464caea0c36d148cffbfcfb3b5ac09f666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715273"
---
# <a name="using-context-to-improve-accuracy"></a>Utilisation du contexte pour améliorer la précision

Un moteur de reconnaissance de l’écriture manuscrite, ou module de reconnaissance, est un logiciel qui traite l’encre et convertit cette entrée manuscrite en texte. Un contexte est pertinent pour les informations spécifiques à l’application que vous fournissez à un module de reconnaissance pour améliorer la précision de la reconnaissance. En d’autres termes, le contexte est une information sur l’entrée qui aide le module de reconnaissance à traiter avec précision l’encre dans un champ.

Cette section décrit les différentes façons dont vous pouvez tirer parti du contexte dans votre application Tablet PC, en mettant l’accent sur la technique de programmation par défaut pour les applications qui ne sont pas activées pour l’écriture manuscrite.

> [!Note]  
> les sections de la technologie Tablet PC de la Windows kit de développement logiciel (SDK) de Vista sont des emplacements où le terme « contexte » est utilisé en ce qui concerne l’objet [**RecognizerContext**](inkrecognizercontext-class.md) et ses propriétés [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) et [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) . Ne confondez pas ces autres utilisations de « context » avec la définition de cette section.

 

 

 



