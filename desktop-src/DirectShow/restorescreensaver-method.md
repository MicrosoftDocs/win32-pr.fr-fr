---
description: La méthode DVDAdm. RestoreScreenSaver restaure les paramètres de l’économiseur d’écran système.
ms.assetid: 606ab850-95bf-4c60-b7cf-e3a94ceee7a7
title: Méthode RestoreScreenSaver
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b747aa21815bb37cc7db2296347c9890a06914
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515125"
---
# <a name="restorescreensaver-method"></a>Méthode RestoreScreenSaver

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DVDAdm.RestoreScreenSaver` méthode restaure les paramètres de l’économiseur d’écran système.

``` syntax
DVD.DVDAdm.RestoreScreenSaver()
```

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

En règle générale, une application DVD désactive l’économiseur d’écran du système au démarrage en affectant à la propriété [**DisableScreenSaver**](disablescreensaver-property.md) la valeur true, puis réactive l’économiseur d’écran lorsque l’application DVD est fermée en appelant `RestoreScreenSaver` . Si une application n’utilise pas les paramètres d’économiseur d’écran du système, elle n’a pas à appeler cette méthode ou à définir la propriété **DisableScreenSaver** .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objet MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



