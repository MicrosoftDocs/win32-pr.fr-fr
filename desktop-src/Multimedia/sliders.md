---
title: Curseurs (Windows Multimedia)
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
ms.openlocfilehash: 4d1d7644255e2fa9ee6384cbb5102df81c2a1eb0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383631"
---
# <a name="sliders-windows-multimedia"></a>Curseurs (Windows Multimedia)

Les contrôles Slider sont généralement des contrôles horizontaux qui peuvent être ajustés à gauche ou à droite. Ces contrôles utilisent la [**structure \_ signée MIXERCONTROLDETAILS**](/previous-versions//dd757297(v=vs.85)) pour récupérer et définir des propriétés de contrôle. Le tableau suivant décrit les types de curseurs.



| Contrôler    | Description                                                                                                               |
|------------|---------------------------------------------------------------------------------------------------------------------------|
| Curseur     | A une plage comprise entre – 32 768 et 32 767. Le pilote de mixage définit les limites de ce contrôle.                               |
| Panoramique        | A une plage comprise entre – 32 768 et 32 767. Le pilote de mixage définit les limites de ce contrôle, 0 étant la valeur de milieu de gamme. |
| Panoramique QSound | Fournit un contrôle du son développé via QSound. Ce contrôle a une plage comprise entre – 15 et 15.                               |



 

 

 
