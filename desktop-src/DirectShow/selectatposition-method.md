---
description: La méthode SelectAtPosition sélectionne le bouton de menu aux coordonnées spécifiées du pointeur de la souris.
ms.assetid: 005ec550-e04c-4dae-aa5d-d79afefe48ed
title: Méthode SelectAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97bc9feaa4855baac75fca0e776a26a6975b235a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746252"
---
# <a name="selectatposition-method"></a>Méthode SelectAtPosition

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `SelectAtPosition` méthode sélectionne le bouton de menu aux coordonnées spécifiées du pointeur de la souris.

``` syntax
MSWebDVD.SelectAtPosition(xPos, yPos)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

Spécifie la coordonnée x sous la forme d’un entier.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*PosY*
</dt> <dd>

Spécifie la coordonnée y sous la forme d’un entier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Utilisez cette méthode lors de l’implémentation de la gestion de souris personnalisée après avoir défini [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) sur **true**.

Sélectionnez simplement le bouton. Pour envoyer la commande associée à un bouton qui a été sélectionné, appelez [**ActivateButton**](activatebutton-method.md).

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
</dt> </dl>

 

 



