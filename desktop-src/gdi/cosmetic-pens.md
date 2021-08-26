---
description: Les dimensions d’un stylet cosmétique sont spécifiées en unités de périphérique.
ms.assetid: d4386681-3523-4872-b048-2a5cfbf7d039
title: Plumes cosmétiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65f875ce5873b5f53cba19b5440751b8ac7683df99765ea7e8e6eec813ef73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966069"
---
# <a name="cosmetic-pens"></a>Plumes cosmétiques

Les dimensions d’un stylet cosmétique sont spécifiées en unités de périphérique. Par conséquent, les lignes dessinées avec un stylet cosmétique ont toujours une largeur fixe. Les lignes dessinées avec un stylet cosmétique sont généralement tracées 3 à 10 fois plus rapidement que les lignes dessinées avec un stylet géométrique. Les plumes cosmétiques ont trois attributs : la largeur, le style et la couleur. Pour plus d’informations sur ces attributs, consultez [Pen Attributes](pen-attributes.md).

Pour créer un stylet cosmétique, utilisez la fonction [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)ou [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) . Pour récupérer l’un des trois plumes cosmétiques de l’action géré par le système, utilisez la fonction [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) .

Une fois que vous avez créé un stylet (ou obtenu un handle vers l’un des plumes d’inventaire), sélectionnez le stylet dans le contexte de périphérique (DC) de l’application à l’aide de la fonction [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) . À partir de ce point, l’application utilise ce stylet pour toutes les opérations de dessin de lignes dans sa zone cliente.

 

 



