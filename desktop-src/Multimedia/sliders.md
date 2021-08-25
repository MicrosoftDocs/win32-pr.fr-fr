---
title: curseurs (Windows multimédia)
description: Curseurs
ms.assetid: cfd82672-5b22-4b59-82b5-15ca68a451fc
keywords:
- mixages audio, contrôles
- mixages audio, curseurs
- mélangeurs, contrôles
- mélangeurs, curseurs
- contrôles Slider
- Structure MIXERCONTROLDETAILS_SIGNED
- contrôle panoramique
- Contrôle PAN QSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e902e3ead0416cb4b2a7d56d289f91779563109cb9494784635affc75069dfe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805349"
---
# <a name="sliders-windows-multimedia"></a>curseurs (Windows multimédia)

Les contrôles Slider sont généralement des contrôles horizontaux qui peuvent être ajustés à gauche ou à droite. Ces contrôles utilisent la [**structure \_ signée MIXERCONTROLDETAILS**](/previous-versions//dd757297(v=vs.85)) pour récupérer et définir des propriétés de contrôle. Le tableau suivant décrit les types de curseurs.



| Contrôler    | Description                                                                                                               |
|------------|---------------------------------------------------------------------------------------------------------------------------|
| Curseur     | A une plage comprise entre – 32 768 et 32 767. Le pilote de mixage définit les limites de ce contrôle.                               |
| Panoramique        | A une plage comprise entre – 32 768 et 32 767. Le pilote de mixage définit les limites de ce contrôle, 0 étant la valeur de milieu de gamme. |
| Panoramique QSound | Fournit un contrôle du son développé via QSound. Ce contrôle a une plage comprise entre – 15 et 15.                               |



 

 

 
