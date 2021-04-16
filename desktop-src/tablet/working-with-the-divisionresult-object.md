---
description: L’objet DivisionResult représente un instantané de l’analyse de la disposition des traits contenus dans l’objet diviseur. Il contient la classification des traits et les informations de regroupement de l’analyse de la disposition.
ms.assetid: 2bcf5223-7bf4-420c-8f04-a972f04f262d
title: Utilisation de l’objet DivisionResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0b9874f4a9d2e6bc4390d98803c2344308fc3e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526889"
---
# <a name="working-with-the-divisionresult-object"></a>Utilisation de l’objet DivisionResult

L’objet **DivisionResult** représente un instantané de l’analyse de la disposition des traits contenus dans l’objet **diviseur** . Il contient la classification des traits et les informations de regroupement de l’analyse de la disposition.

Vous pouvez récupérer des informations à partir de l’objet **DivisionResult** par type d’élément structurel, tel que le dessin ou les lignes d’écriture manuscrite. L’objet **DivisionResult** peut être conservé après la destruction de l’objet **diviseur** . Dans Automation, cet objet est appelé objet d' [**interface IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .

La propriété [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) de l’objet **DivisionResult** contient une copie de la collection **Strokes** dans l’objet **diviseur** au moment de la création de l’objet **DivisionResult** .

L’énumération [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) définit les types d’éléments structurels reconnus par l’analyse de la disposition.

La méthode [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) de l’objet **DivisionResult** retourne une collection **DivisionUnits** qui contient tous les éléments structurels d’un type donné. Un élément structurel individuel est représenté par un objet **DivisionUnit** . Chaque fois que vous appelez la méthode **ResultByType** , l’objet **DivisionResult** crée une collection **DivisionUnits** . Pour plus d’informations sur l’objet **DivisionUnit** , consultez [utilisation de l’objet DivisionUnit](working-with-the-divisionunit-object.md).

 

 
