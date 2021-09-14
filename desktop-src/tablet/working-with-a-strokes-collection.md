---
description: La collection Strokes analysée par l’objet diviseur est conservée dans la propriété Strokes de l’objet diviseur.
ms.assetid: c2def964-6f2d-4b79-bfbf-a6719baf3c13
title: Utilisation d’une collection Strokes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdeb03ce8168cec489dfed954a091f50f8d846d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196223"
---
# <a name="working-with-a-strokes-collection"></a>Utilisation d’une collection Strokes

La collection [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) analysée par l’objet [**diviseur**](inkdivider-class.md) est conservée dans la propriété [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) de l’objet **diviseur** . Comme une collection **Strokes** est une référence aux données d’entrée manuscrite et n’est pas les données proprement dites, les modifications apportées à l’objet [**Ink**](inkdisp-class.md) parent de la collection **Strokes** peuvent invalider la collection **Strokes** . Pour plus d’informations sur les données d’entrée manuscrite, consultez [données manuscrites](ink-data.md). Pour plus d’informations sur la collecte d’encres, consultez [collection d’encres](ink-collection.md).

Pour maintenir la propriété [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) de l’objet [**diviseur**](inkdivider-class.md) synchronisée avec un objet [**Ink**](inkdisp-class.md) , utilisez les événements [**InkAdded**](inkdisp-inkadded.md) et [**InkDeleted**](inkdisp-inkdeleted.md) de l’objet **Ink** pour écouter les traits qui doivent être ajoutés ou supprimés de l’objet **diviseur** . Cela couvre les cas où les traits sont ajoutés, supprimés de, découpés ou fractionnés dans l’objet **Ink** . Le déplacement, la mise à l’échelle ou d’autres transformations sur les traits de l’objet **Ink** ne génèrent pas d’événements **InkAdded** ou **InkDeleted** . Pour refléter une transformation de ce type dans la propriété **Strokes** de l’objet **diviseur** , effectuez la même transformation sur les traits de l’objet **diviseur** .

La propriété [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) de l’objet [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) contient une copie des traits dans l’objet [**diviseur**](inkdivider-class.md) au moment de la création de l’objet **DivisionResult** . Vous pouvez comparer les propriétés des **traits** de deux objets **DivisionResult** pour déterminer si les traits ont changé entre les deux fois que la méthode de [**Division**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide) a été appelée.

La propriété [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_strokes) de l’objet [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) contient le sous-ensemble des traits de l’objet [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) qui correspondent à cet élément. Vous pouvez passer ces traits à un [**RecognizerContext**](inkrecognizercontext-class.md) distinct pour obtenir un résultat de reconnaissance pour l’élément. Étant donné que les éléments d’écriture manuscrite existent à différents niveaux de détail, les collections de [**traits**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) pour les différents éléments peuvent se chevaucher. Par exemple, la collection **Strokes** pour un élément de segment de reconnaissance est un sous-ensemble de la collection **Strokes** pour l’élément Line dont le segment de reconnaissance fait partie.

 

 
