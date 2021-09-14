---
description: La méthode ActivateAtPosition active le bouton de menu à la position spécifiée.
ms.assetid: eddc4880-dd78-4d96-8bff-c5c883a19927
title: Méthode ActivateAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64a83e7fcbc00990c7be7d1a99638a1b4a3de14b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112361"
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

## <a name="remarks"></a>Notes

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

 

 



