---
description: La propriété DVDAdm. DisableScreenSaver active ou désactive l’économiseur d’écran du système.
ms.assetid: 78a0512f-456a-45b6-8717-13593461a765
title: Propriété DisableScreenSaver
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d651026f2bf09f872655a0ef58accb3a6173dcb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999664"
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

## <a name="remarks"></a>Notes

Cette propriété est en lecture/écriture et sa valeur par défaut est true. Lorsque vous affichez un disque DVD-Video, un utilisateur n’utilise généralement pas la souris ou le clavier pendant des périodes prolongées. par conséquent, le contrôle MSWebDVD ActiveX® désactive par défaut l’économiseur d’écran système. Object

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RestoreScreenSaver**](restorescreensaver-method.md)
</dt> <dt>

[Objet MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



