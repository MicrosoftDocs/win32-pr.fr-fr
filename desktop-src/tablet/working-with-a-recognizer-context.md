---
description: L’objet diviseur utilise un RecognizerContext pour améliorer son analyse des segments de reconnaissance et pour générer un texte de reconnaissance pour les éléments d’écriture manuscrite.
ms.assetid: 33d9abc4-151e-47b4-b66f-ff6adfe21222
title: Utilisation d’un contexte de module de reconnaissance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d99020e97170f0b68b1459abdc4b85f81ebc3fbba426233c2c13b5e042f28ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715097"
---
# <a name="working-with-a-recognizer-context"></a>Utilisation d’un contexte de module de reconnaissance

L’objet [**diviseur**](inkdivider-class.md) utilise un [**RecognizerContext**](inkrecognizercontext-class.md) pour améliorer son analyse des segments de reconnaissance et pour générer un texte de reconnaissance pour les éléments d’écriture manuscrite.

Vous pouvez définir le contexte de module de reconnaissance à l’aide de la propriété [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) de l’objet [**diviseur**](inkdivider-class.md) ou en fournissant le contexte de module de reconnaissance dans l’appel au constructeur de [diviseur](/previous-versions/ms839465(v=msdn.10)) (en code managé). Si un contexte de module de reconnaissance pour un module de reconnaissance sans écriture manuscrite ou pour un module de reconnaissance qui ne prend pas en charge la fonctionnalité d’entrée libre est assigné à la propriété **RecognizerContext** , une exception est levée.

Si les identifiants ne sont pas installés ou si un contexte de module de reconnaissance n’est pas assigné à l’objet de [**séparateur**](inkdivider-class.md) , l’objet de **séparateur** n’utilise pas de contexte de module de reconnaissance. Dans ce cas, la fonction d’analyse de la disposition effectue la Division du segment, et aucun texte n’est associé à l’objet [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .

> [!Note]  
> La propriété [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) ne peut pas être modifiée une fois que les traits ont été assignés à l’objet [**diviseur**](inkdivider-class.md) . L’objet **diviseur** utilise les valeurs de propriété par défaut de l’objet [**RecognizerContext**](inkrecognizercontext-class.md) .

 

L’objet [**diviseur**](inkdivider-class.md) applique le contexte du module de reconnaissance aux éléments d’écriture manuscrite lors de l’analyse de la disposition. Tous les traits que vous attribuez directement au contexte de module de reconnaissance sont ignorés par l’objet de **séparateur** . Pour plus d’informations sur la reconnaissance de texte, consultez à propos de la reconnaissance de l' [écriture manuscrite](about-handwriting-recognition.md).

 

 
