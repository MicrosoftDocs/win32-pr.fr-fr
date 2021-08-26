---
description: Une application remplit l’intérieur d’une région en appelant la fonction FillRgn et en fournissant un handle qui identifie un pinceau spécifique.
ms.assetid: 6174b2ea-836a-4538-a0ad-e123c88fc6f6
title: Remplissage des régions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d909643155b027f72b4235db366e640d7e53dacd4825b85090f9958aec1c94c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015399"
---
# <a name="filling-regions"></a>Remplissage des régions

Une application remplit l’intérieur d’une région en appelant la fonction [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) et en fournissant un handle qui identifie un pinceau spécifique. Quand une application appelle FillRgn, le système remplit la région avec le pinceau en utilisant le mode de remplissage actuel pour le contexte de périphérique spécifié. Il existe deux modes de remplissage : alternative et enroulement. L’application peut définir le mode de remplissage pour un contexte de périphérique en appelant la fonction [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) . L’application peut récupérer le mode de remplissage actuel pour un contexte de périphérique en appelant la fonction [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) .

L’illustration suivante montre deux régions identiques : l’une remplie à l’aide du mode alternatif et l’autre remplie à l’aide du mode enroulement.

![Illustration montrant des étoiles de 2 5 : une remplie uniquement en points, l’autre remplie entièrement](images/csrgn-03.png)

## <a name="alternate-mode"></a>Mode alternatif

Pour déterminer les pixels que le système met en surbrillance lorsque le mode alternatif est spécifié, effectuez le test suivant :

1.  Sélectionnez un pixel dans l’intérieur de la région.
2.  Dessinez un rayon imaginaire, dans l’axe x positif, de ce pixel vers l’infini.
3.  Chaque fois que le rayon croise une ligne de limite, Incrémentez une valeur de nombre.

Le système met en surbrillance le pixel si la valeur de nombre est un nombre impair.

## <a name="winding-mode"></a>Mode de bobinage

Pour déterminer les pixels que le système met en surbrillance lorsque le mode d’enroulement est spécifié, effectuez le test suivant :

1.  Déterminez la direction dans laquelle chaque ligne de limite est dessinée.
2.  Sélectionnez un pixel dans l’intérieur de la région.
3.  Dessinez un rayon imaginaire, dans l’axe x positif, du pixel vers l’infini.
4.  Chaque fois que le rayon croise une ligne de limite avec un composant y positif, Incrémentez une valeur de nombre. Chaque fois que le rayon croise une ligne de limite avec un composant y négatif, décrémente la valeur du nombre.

Le système met en surbrillance le pixel si la valeur de nombre est différente de zéro.

 

 



