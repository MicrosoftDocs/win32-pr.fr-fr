---
description: La propriété ButtonsAvailable récupère le nombre total de boutons dans le menu actuel.
ms.assetid: 4df3a7e7-1be4-4cc7-ad61-567f7f45811e
title: Propriété ButtonsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cab4afdd9f6e23a376bb72885810b8464f180d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111393"
---
# <a name="buttonsavailable-property"></a>Propriété ButtonsAvailable

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `ButtonsAvailable` propriété récupère le nombre total de boutons dans le menu actuel.

``` syntax
[ iButtons = ] MSWebDVD.ButtonsAvailable
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant le nombre de boutons.

## <a name="remarks"></a>Notes

Cette propriété est en lecture seule sans valeur par défaut. Utilisez cette méthode lors de l’implémentation de la gestion de souris personnalisée après avoir défini [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) sur **true**.

Appelez cette méthode pour récupérer la limite supérieure de la plage de numéros de boutons valides.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

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

 

 



