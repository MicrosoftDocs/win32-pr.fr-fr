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
ms.openlocfilehash: 4d1d7644255e2fa9ee6384cbb5102df81c2a1eb0
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368847"
---
# <a name="sliders-windows-multimedia"></a>curseurs (Windows multimédia)

Les contrôles Slider sont généralement des contrôles horizontaux qui peuvent être ajustés à gauche ou à droite. Ces contrôles utilisent la [**structure \_ signée MIXERCONTROLDETAILS**](/previous-versions//dd757297(v=vs.85)) pour récupérer et définir des propriétés de contrôle. Le tableau suivant décrit les types de curseurs.



| Control    | Description                                                                                                               |
|------------|---------------------------------------------------------------------------------------------------------------------------|
| Curseur     | A une plage comprise entre – 32 768 et 32 767. Le pilote de mixage définit les limites de ce contrôle.                               |
| Panoramique        | A une plage comprise entre – 32 768 et 32 767. Le pilote de mixage définit les limites de ce contrôle, 0 étant la valeur de milieu de gamme. |
| Panoramique QSound | Fournit un contrôle du son développé via QSound. Ce contrôle a une plage comprise entre – 15 et 15.                               |



 

 

 
