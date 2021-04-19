---
description: La propriété SubpictureOn définit ou récupère l’état de la sous-image actuelle (on ou OFF).
ms.assetid: fa4500bc-48b4-41ed-8b88-0011a0e51c6f
title: Propriété SubpictureOn
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83376793f20468bda88edd8897e8c956094c1a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523412"
---
# <a name="subpictureon-property"></a>Propriété SubpictureOn

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `SubpictureOn` propriété définit ou récupère l’état de la sous-image actuelle (on ou OFF).

``` syntax
[ bState = ] MSWebDVD.SubpictureOn
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur booléenne indiquant si la sous-image est affichée.

## <a name="remarks"></a>Notes

Cette propriété n’a aucune incidence sur l’affichage des sous-titres. Les sous-titres sont incorporés dans le flux vidéo. Les sous-images de DVD sont transportées sur un flux de travail distinct.

Lorsque le flux de sous-image est modifié à l’aide de [**CurrentSubpictureStream**](currentsubpicturestream-property.md), la `SubpictureOn` propriété bascule sur **true**.

Cette propriété est en lecture/écriture et sa valeur par défaut est false.

 

 



