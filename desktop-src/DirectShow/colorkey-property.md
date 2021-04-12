---
description: La propriété ColorKey définit ou récupère la clé de couleur utilisée dans le sous-titrage.
ms.assetid: 4d4b38e6-bd29-4e16-8f82-a5da9312d272
title: Propriété ColorKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75620be88a861e02915c27324978382feefc5835
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481177"
---
# <a name="colorkey-property"></a>Propriété ColorKey

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `ColorKey` propriété définit ou récupère la clé de couleur utilisée dans le sous-titrage.

``` syntax
[ iColorKey = ] MSWebDVD.ColorKey
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant la couleur à utiliser comme arrière-plan transparent pour le texte de légende fermée. La valeur par défaut dans les couleurs 256 est magenta, et non noir dans toute autre profondeur de couleur.

## <a name="remarks"></a>Notes

Cette propriété est en lecture/écriture. Cette propriété s’applique uniquement aux légendes fermées, le cas échéant, et non au flux de sous-image.

 

 



