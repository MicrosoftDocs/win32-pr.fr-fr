---
description: La méthode ActivateButton active le bouton de menu sélectionné.
ms.assetid: 1da486a0-dadc-4c92-b3d3-83aeace01e39
title: Méthode ActivateButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64853a191f688758deb42061e95c91308ff88c00fe9482cce677f8b00926f26f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873519"
---
# <a name="activatebutton-method"></a>Méthode ActivateButton

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La méthode ActivateButton active le bouton de menu sélectionné.

``` syntax
        MSWebDVD.ActivateButton()
```

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Utilisez cette méthode lors de l’implémentation de la gestion de souris personnalisée après avoir défini [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) sur **true**.

Utilisez cette méthode pour activer un bouton qui a été sélectionné par le biais de la méthode [**SelectLeftButton**](selectleftbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md)ou [**SelectRightButton**](selectrightbutton-method.md) .

 

 



