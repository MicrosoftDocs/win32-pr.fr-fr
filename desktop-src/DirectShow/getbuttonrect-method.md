---
description: La méthode GetButtonRect récupère le rectangle pour le bouton spécifié, dans les coordonnées de la fenêtre.
ms.assetid: 359e9483-d7ba-45b0-882b-5a4c56dc0350
title: Méthode GetButtonRect
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ba62c70d0cd061e7aec01da286f49c79e19a3b63dfdd9e2c3de8230339be478
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118000234"
---
# <a name="getbuttonrect-method"></a>Méthode GetButtonRect

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `GetButtonRect` méthode récupère le rectangle pour le bouton spécifié, en coordonnées de fenêtre.

``` syntax
[ oButton = ] MSWebDVD.GetButtonRect(iButton)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*
</dt> <dd>

Spécifie le numéro de bouton sous la forme d’un entier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne un objet [DVDRect](dvdrect-object.md) qui définit le rectangle.

## <a name="remarks"></a>Remarques

Utilisez cette méthode lors de l’implémentation de la gestion de souris personnalisée après avoir défini [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) sur **true**.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ButtonsAvailable**](buttonsavailable-property.md)
</dt> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



