---
description: La méthode ActivateAtPosition active le bouton de menu à la position spécifiée.
ms.assetid: eddc4880-dd78-4d96-8bff-c5c883a19927
title: Méthode ActivateAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fee8b81c10b010132d07ac4418f273be228595bab45e86ec03c7828d78ba74f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873549"
---
# <a name="activateatposition-method"></a>Méthode ActivateAtPosition

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La méthode ActivateAtPosition active le bouton de menu à la position spécifiée.

``` syntax
        MSWebDVD.ActivateAtPosition(xPos, yPos)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

Spécifie la coordonnée x comme un entier.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*PosY*
</dt> <dd>

Spécifie la coordonnée y sous la forme d’un entier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Utilisez cette méthode lors de l’implémentation de la gestion de souris personnalisée après avoir défini [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) sur **true**.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ButtonsAvailable**](buttonsavailable-property.md)
</dt> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**GetButtonAtPosition**](getbuttonatposition-method.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



