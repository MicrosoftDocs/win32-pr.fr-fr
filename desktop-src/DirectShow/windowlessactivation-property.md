---
description: La propriété WindowlessActivation Initialise l’objet MSWebDVD au moment de la conception pour le mode fenêtre ou sans fenêtre.
ms.assetid: 290a9459-154a-4ec7-a013-d696e6b27341
title: Propriété WindowlessActivation
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6915dbf2ddcfe1b8925ccc1dc3c163799563d137e39e6d6260ad75f5496a0b1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982249"
---
# <a name="windowlessactivation-property"></a>Propriété WindowlessActivation

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `WindowlessActivation` propriété Initialise l’objet **mswebdvd** au moment du design pour le mode fenêtre ou sans fenêtre.

``` syntax
[ bWindowless = ] MSWebDVD.WindowlessActivation
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur indiquant si l’objet est en mode fenêtre sous forme de valeur booléenne.

## <a name="remarks"></a>Remarques

Cette propriété est en lecture/écriture et sa valeur par défaut est true. Par conséquent, il vous suffit de définir cette propriété si vous exécutez l’objet **mswebdvd** dans un conteneur en fenêtre. Lorsqu’il est contenu dans une page Web de Microsoft® Internet Explorer, **mswebdvd** est toujours en mode sans fenêtre, et vous n’avez pas besoin de définir cette propriété.

 

 



