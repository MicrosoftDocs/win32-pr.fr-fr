---
description: La méthode GetButtonAtPosition récupère le numéro du bouton aux coordonnées spécifiées sans le sélectionner ou l’activer.
ms.assetid: ac933d0d-db2e-488f-b661-2fdc9f5acb39
title: Méthode GetButtonAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9347929946a6f26cac4652a5357bd6454c80446c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108526"
---
# <a name="getbuttonatposition-method"></a>Méthode GetButtonAtPosition

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `GetButtonAtPosition` méthode récupère le numéro du bouton aux coordonnées spécifiées sans le sélectionner ou l’activer.

``` syntax
[ iButton = ] MSWebDVD.GetButtonAtPosition(xPos, yPos)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

Spécifie la coordonnée x du pointeur de la souris sous la forme d’un entier.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*PosY*
</dt> <dd>

Spécifie la coordonnée y du pointeur de la souris sous la forme d’un entier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière qui spécifie le bouton, le cas échéant, à la position spécifiée.

## <a name="remarks"></a>Notes

Cette méthode retourne zéro si aucun bouton n’est présent aux coordonnées spécifiées. Utilisez cette méthode lors de l’implémentation de la gestion de souris personnalisée après avoir défini [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) sur **true**.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**ButtonsAvailable**](buttonsavailable-property.md)
</dt> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



