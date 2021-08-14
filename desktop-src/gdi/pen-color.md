---
description: L’attribut Color spécifie la couleur du stylet.
ms.assetid: ce775359-65fc-40d0-8725-b392cc0464a6
title: Couleur du stylet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e88d73fc80f6fe02a6d9e1de1d33568c94e05768f113c8bee0754c5d8afb418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117886204"
---
# <a name="pen-color"></a>Couleur du stylet

L’attribut Color spécifie la couleur du stylet. Une application peut créer un stylet cosmétique avec une couleur unique à l’aide de la macro [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) pour stocker l’triplet rouge, vert et bleu qui spécifie la couleur souhaitée dans une structure [COLORREF](colorref.md) et transmettant l’adresse de cette structure à la fonction [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)ou [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) . (Les plumes d’action sont limitées en noir, blanc et invisible.) Pour plus d’informations sur les triplets et la couleur RVB, consultez [couleurs](colors.md).

 

 



