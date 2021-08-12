---
description: Le stylet d’un Tablet PC peut avoir plusieurs extrémités pouvant interagir avec le digitaliseur.
ms.assetid: c1aa0d65-cfea-4720-ad09-7add724e03c7
title: Fonctionnalités multiples avec un stylet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22cbba4c95ef215b8ae1e0c94cbe1d43eaceb966fd775284c57a365bbba2f7fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449670"
---
# <a name="multiple-functionality-with-one-pen"></a>Fonctionnalités multiples avec un stylet

Le stylet d’un Tablet PC peut avoir plusieurs extrémités pouvant interagir avec le digitaliseur. Si les deux extrémités du stylet peuvent générer des événements, une extrémité peut être utilisée pour définir l’encre, sélectionner et pointer, et l’autre extrémité peut être utilisée pour d’autres fonctions telles que l’effacement.

Pour implémenter cette fonctionnalité, votre application doit être en mesure de déterminer la fin du stylet qui est utilisée et, par conséquent, de modifier l’apparence du curseur. Pour ce faire, il peut Rechercher l’état de la propriété [**inversée**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) sur l’objet [**curseur**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .

Pour plus d’informations sur l’utilisation de l’arrière du stylet pour l’effacement, consultez [effacement de l’encre avec le stylet](erasing-ink-with-the-pen.md). En outre, l' [exemple d’effacement d’encre](ink-erasing-sample.md) montre comment utiliser l’arrière du stylet pour effacer l’encre.

 

 



