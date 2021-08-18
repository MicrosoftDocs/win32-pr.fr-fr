---
description: Un module de reconnaissance peut trouver plusieurs façons de diviser un échantillon d’encre en segments de reconnaissance. Pour cette raison, le nombre de remplaçants de reconnaissance peut être échelonné, même pour un petit échantillon d’encre.
ms.assetid: 7ecffe3f-cbe4-4e65-a1cc-9b08534b26c9
title: Segments d’encre et alternatives
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 702c2da4984afd22490827acdf65962abc789d7ad9f0ddab3e602bc688ac6542
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883989"
---
# <a name="ink-segments-and-alternates"></a>Segments d’encre et alternatives

Un module de reconnaissance peut trouver plusieurs façons de diviser un échantillon d’encre en segments de reconnaissance. Pour cette raison, le nombre de remplaçants de reconnaissance peut être échelonné, même pour un petit échantillon d’encre.

Par exemple, « t o g e t h e r » peut générer les résultats suivants :

-   « pour l’obtenir » (plus de remplacements pour chaque mot)
-   « pour rassembler » (plus de remplacements pour chaque mot)
-   « TOG Ether » (plus de remplacements pour chaque mot)
-   « TOG » (plus de remplacements pour chaque mot)
-   « ensemble » (plus des alternatives pour le mot)

L’objet [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) prend en charge le stockage efficace des résultats de reconnaissance complets au sein de l’objet [**Ink**](inkdisp-class.md) . L’objet **Ink** mappe la reconnaissance alternative aux traits de l’objet **Ink** et peut également contenir d’autres informations telles que la position de ligne de base, les index de ligne et les plages de langue.

 

 



