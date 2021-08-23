---
description: La propriété CurrentDomain récupère le domaine DVD dans lequel se trouve l’objet MSWebDVD.
ms.assetid: 9d545438-9a3d-4c57-a3df-5e75af2e4d1b
title: CurrentDomain, propriété
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf022d44cc3580a4d5208c5bc96413dfa445b0f2fcbf74eeb938ee77fa0677bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953388"
---
# <a name="currentdomain-property"></a>CurrentDomain, propriété

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `CurrentDomain` propriété récupère le domaine DVD dans lequel se trouve l’objet mswebdvd.

``` syntax
[ iDomain = ] MSWebDVD.CurrentDomain
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant le domaine actuel.

## <a name="remarks"></a>Remarques

Les valeurs possibles de la propriété sont les suivantes :



| Valeur | Description          |
|-------|----------------------|
| 1     | Première lecture           |
| 2     | Menu du gestionnaire de vidéos   |
| 3     | Menu de l’ensemble de titres vidéo |
| 4     | Titre                |
| 5     | Arrêter                 |



 

Appelez cette méthode pour vérifier que le navigateur DVD est dans un domaine valide pour la méthode que vous allez appeler. Par exemple, avant d’appeler [**PlayTitle**](playtitle-method.md), vérifiez la `CurrentDomain` propriété pour vous assurer que le navigateur DVD n’est pas dans le domaine Stop ou First Play.

 

 



