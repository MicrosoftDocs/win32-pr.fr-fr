---
description: La propriété ColorKey définit ou récupère la clé de couleur utilisée dans le sous-titrage.
ms.assetid: 4d4b38e6-bd29-4e16-8f82-a5da9312d272
title: Propriété ColorKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abca1dabbdb67f4380dbe32acbf2948862695b7c424dfd08629ec16237bb88c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073733"
---
# <a name="colorkey-property"></a>Propriété ColorKey

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `ColorKey` propriété définit ou récupère la clé de couleur utilisée dans le sous-titrage.

``` syntax
[ iColorKey = ] MSWebDVD.ColorKey
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant la couleur à utiliser comme arrière-plan transparent pour le texte de légende fermée. La valeur par défaut dans les couleurs 256 est magenta, et non noir dans toute autre profondeur de couleur.

## <a name="remarks"></a>Remarques

Cette propriété est en lecture/écriture. Cette propriété s’applique uniquement aux légendes fermées, le cas échéant, et non au flux de sous-image.

 

 



