---
description: La propriété DVDAdm. DisableScreenSaver active ou désactive l’économiseur d’écran du système.
ms.assetid: 78a0512f-456a-45b6-8717-13593461a765
title: Propriété DisableScreenSaver
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bc714dbbdc3e9b144f2d49cb54871cdf09baad5df39f8e18b962d7fc415d44a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821127"
---
# <a name="disablescreensaver-property"></a>Propriété DisableScreenSaver

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DVDAdm.DisableScreenSaver` propriété active ou désactive l’économiseur d’écran système.

``` syntax
[ bDisabled = ] DVD.DVDAdm.DisableScreenSaver
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur booléenne indiquant si les paramètres d’économiseur d’écran du système sont désactivés pour l’application de lecteur de DVD ; true signifie que les paramètres sont désactivés.

## <a name="remarks"></a>Remarques

Cette propriété est en lecture/écriture et sa valeur par défaut est true. Lorsque vous affichez un disque DVD-Video, un utilisateur n’utilise généralement pas la souris ou le clavier pendant des périodes prolongées. par conséquent, le contrôle MSWebDVD ActiveX® désactive par défaut l’économiseur d’écran système. Object

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RestoreScreenSaver**](restorescreensaver-method.md)
</dt> <dt>

[Objet MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



