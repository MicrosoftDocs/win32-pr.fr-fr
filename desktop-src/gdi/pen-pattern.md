---
description: L’attribut pattern spécifie le modèle d’un stylet géométrique.
ms.assetid: 5a330416-3b83-4f0f-825c-80e47903966e
title: Modèle Pen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577b5e2cb31e44a4631760c82e678af069322cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528299"
---
# <a name="pen-pattern"></a>Modèle Pen

L’attribut pattern spécifie le modèle d’un stylet géométrique.

L’illustration suivante montre des lignes dessinées avec différents stylets géométriques. Chaque stylo a été créé à l’aide d’un attribut de modèle différent.

![Illustration montrant quatre lignes, chacune remplie d’un stylet différent](images/cspen-02.png)

La première ligne de l’illustration précédente est dessinée à l’aide de l’un des six modèles de hachures disponibles ; Pour plus d’informations sur les modèles de hachurage, consultez [Pen Hatch](pen-hatch.md). La ligne suivante est dessinée à l’aide du modèle creux, identique au modèle null. La troisième ligne est dessinée à l’aide d’un modèle personnalisé créé à partir d’une bitmap de 8 par 8 pixels. (Pour plus d’informations sur les bitmaps et leur création, consultez [bitmaps](bitmaps.md).) La dernière ligne est dessinée à l’aide d’un modèle Uni. La création d’un pinceau et le passage de son handle à la fonction [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) créent un modèle.

 

 



