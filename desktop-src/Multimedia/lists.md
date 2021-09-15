---
title: Listes
description: Listes
ms.assetid: 89fb4457-307a-4693-94d4-57f57c422d1e
keywords:
- mixages audio, contrôles
- mixages audio, listes
- mélangeurs, contrôles
- mélangeurs, listes
- contrôles de liste
- Structure MIXERCONTROLDETAILS_BOOLEAN
- Structure MIXERCONTROLDETAILS_LISTTEXT
- contrôle à sélection unique
- contrôle à sélection multiple
- contrôle mixer
- multiplexeur (multiplexeur)
- MUX (multiplexeur)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d475816d7090ee241a1508cc054b12742c4ab27
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413893"
---
# <a name="lists"></a>Listes

Les contrôles de liste fournissent des États à sélection unique ou à sélection multiple pour les lignes audio complexes. Ces contrôles utilisent la [**structure \_ booléenne MIXERCONTROLDETAILS**](/previous-versions//dd757295(v=vs.85)) pour récupérer et définir des propriétés de contrôle. La structure [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85)) est également utilisée pour récupérer toutes les descriptions textuelles d’un contrôle à plusieurs éléments. Le tableau suivant décrit les types de contrôles de liste.



| Control           | Description                                                                                                                                                                                                                                                                      |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sélection simple     | Limite la sélection de contrôle à un élément à la fois. Contrairement au contrôle multiplexeur, ce contrôle peut être utilisé pour contrôler plus que les lignes de la source audio. Par exemple, vous pouvez utiliser ce contrôle pour sélectionner un filtre à passage faible dans une liste de filtres pris en charge par un appareil de mixage. |
| Multiplexeur (multiplexeur) | Limite la sélection de ligne à une ligne source à la fois.                                                                                                                                                                                                                       |
| Sélection multiple   | Permet à l’utilisateur de sélectionner simultanément plusieurs éléments dans une liste. Contrairement au contrôle mixer, le contrôle à sélection multiple peut être utilisé pour contrôler plus que les lignes de la source audio.                                                                                                  |
| Mixer             | Permet à l’utilisateur de sélectionner des lignes sources dans une liste simultanément.                                                                                                                                                                                                               |



 

 

 