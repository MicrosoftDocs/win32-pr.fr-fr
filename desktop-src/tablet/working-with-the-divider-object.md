---
description: L’objet diviseur fournit l’accès aux fonctionnalités d’analyse de la disposition du Tablet PC.
ms.assetid: 9fa299fe-3713-4fa8-95c6-be15f144103a
title: Utilisation de l’objet diviseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a31c7ab0c99c0ac4007abe164a887694c8e41fb8c8892dfe2637efaf25b10f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966568"
---
# <a name="working-with-the-divider-object"></a>Utilisation de l’objet diviseur

L’objet [diviseur](/previous-versions/ms583616(v=vs.100)) fournit l’accès aux fonctionnalités d’analyse de la disposition du Tablet PC.

Dans le code managé, l’objet de [séparateur](/previous-versions/ms583616(v=vs.100)) peut être instancié en appelant l’un des constructeurs de [diviseur](/previous-versions/ms839465(v=msdn.10)) . Dans Automation, il s’agit de l’objet [**InkDivider**](inkdivider-class.md) et il peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

Vous pouvez obtenir un instantané du résultat de l’analyse actuelle en appelant la méthode [Divide](/previous-versions/ms839461(v=msdn.10)) de l’objet [diviseur](/previous-versions/ms583616(v=vs.100)) . Le résultat de l’analyse est retourné dans un objet [DivisionResult](/previous-versions/ms839371(v=msdn.10)) . Chaque fois que vous appelez la méthode Divide, l’objet diviseur crée un objet DivisionResult. Pour plus d’informations sur l’objet DivisionResult, consultez [utilisation de l’objet DivisionResult](working-with-the-divisionresult-object.md).

La collection [Strokes](/previous-versions/ms552701(v=vs.100)) analysée par l’objet [diviseur](/previous-versions/ms583616(v=vs.100)) est contenue dans la propriété [Strokes](/previous-versions/ms839422(v=msdn.10)) de l’objet diviseur. L’objet diviseur analyse dynamiquement la collection Strokes à mesure que vous ajoutez ou supprimez la collection. Pour plus d’informations sur la propriété Strokes de l’objet diviseur, consultez [utilisation d’une collection Strokes](working-with-a-strokes-collection.md).

L’objet [diviseur](/previous-versions/ms583616(v=vs.100)) utilise un contexte de module de reconnaissance pour améliorer son analyse des segments de reconnaissance et pour générer un texte de reconnaissance pour les éléments d’écriture manuscrite. Vous pouvez définir le contexte du module de reconnaissance à l’aide de la propriété [RecognizerContext](/previous-versions/ms839415(v=msdn.10)) de l’objet diviseur. La propriété RecognizerContext ne peut pas être modifiée une fois que les traits ont été assignés à l’objet diviseur. Pour plus d’informations sur la propriété RecognizerContext de l’objet diviseur, consultez [utilisation d’un contexte](working-with-a-recognizer-context.md)de module de reconnaissance.

> [!Caution]  
> Dans le code managé, vous devez appeler la méthode [dispose](/previous-versions/ms839450(v=msdn.10)) sur cet objet avant qu’il ne soit hors de portée. Cet objet gère les ressources non managées. Si vous vous fiez à la finalisation de cet objet, vous risquez de provoquer des fuites de mémoire et des exceptions dans votre application.

 

 

 
