---
description: Un module de reconnaissance peut trouver plusieurs façons de diviser un échantillon d’encre en segments de reconnaissance. Pour cette raison, le nombre de remplaçants de reconnaissance peut être échelonné, même pour un petit échantillon d’encre.
ms.assetid: 7ecffe3f-cbe4-4e65-a1cc-9b08534b26c9
title: Segments d’encre et alternatives
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91183f6c9628ea798b66d703a59e44b26049e692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033957"
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

 

 



