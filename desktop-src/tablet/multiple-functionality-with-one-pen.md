---
description: Le stylet d’un Tablet PC peut avoir plusieurs extrémités pouvant interagir avec le digitaliseur.
ms.assetid: c1aa0d65-cfea-4720-ad09-7add724e03c7
title: Fonctionnalités multiples avec un stylet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8313e6a13cb48900e0c0d31c2e1e590e07df6c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525313"
---
# <a name="multiple-functionality-with-one-pen"></a>Fonctionnalités multiples avec un stylet

Le stylet d’un Tablet PC peut avoir plusieurs extrémités pouvant interagir avec le digitaliseur. Si les deux extrémités du stylet peuvent générer des événements, une extrémité peut être utilisée pour définir l’encre, sélectionner et pointer, et l’autre extrémité peut être utilisée pour d’autres fonctions telles que l’effacement.

Pour implémenter cette fonctionnalité, votre application doit être en mesure de déterminer la fin du stylet qui est utilisée et, par conséquent, de modifier l’apparence du curseur. Pour ce faire, il peut Rechercher l’état de la propriété [**inversée**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) sur l’objet [**curseur**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .

Pour plus d’informations sur l’utilisation de l’arrière du stylet pour l’effacement, consultez [effacement de l’encre avec le stylet](erasing-ink-with-the-pen.md). En outre, l' [exemple d’effacement d’encre](ink-erasing-sample.md) montre comment utiliser l’arrière du stylet pour effacer l’encre.

 

 



