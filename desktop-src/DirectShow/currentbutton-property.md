---
description: La propriété CurrentButton récupère le numéro du bouton de menu sélectionné.
ms.assetid: bd9720bc-068a-4f29-aa2d-1c6b550f789c
title: Propriété CurrentButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d85b246b77283a2632f2feac4c2b374075ef9d9a205bcb71813856b9847df21b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053139"
---
# <a name="currentbutton-property"></a>Propriété CurrentButton

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `CurrentButton` propriété récupère le numéro du bouton de menu sélectionné.

``` syntax
[ iButton = ] MSWebDVD.CurrentButton
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant le bouton.

## <a name="remarks"></a>Remarques

Cette propriété est en lecture seule sans valeur par défaut. Utilisez cette méthode lors de l’implémentation de la gestion de souris personnalisée après avoir défini [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) sur **true**.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**ButtonsAvailable**](buttonsavailable-property.md)
</dt> <dt>

[**GetButtonAtPosition**](getbuttonatposition-method.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



