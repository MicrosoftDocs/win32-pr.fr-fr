---
description: La méthode TakePicture de l’objet Item fait qu’un appareil photo numérique prend une image et retourne un objet Item qui représente l’image résultante. Cette méthode s’applique uniquement aux appareils photo numériques.
ms.assetid: d181048e-21ef-4fcc-a50a-5ba44bbde72e
title: Item. TakePicture, méthode (wiavideo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.TakePicture
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: e7d2e67876cd32b1db2181aba491090d44679756f5503c078d1edff495afc1cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440587"
---
# <a name="itemtakepicture-method"></a>Item. TakePicture, méthode

La méthode **TakePicture** de l’objet [**Item**](-wia-item.md) fait qu’un appareil photo numérique prend une image et retourne un objet **Item** qui représente l’image résultante. Cette méthode s’applique uniquement aux appareils photo numériques.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = Item.TakePicture()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **IWiaDispatchItem**

Objet d' [**élément**](-wia-item.md) qui représente l’image créée par cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wiavideo. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




