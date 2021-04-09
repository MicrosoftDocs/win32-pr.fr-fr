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
ms.openlocfilehash: fd07f7ccd4f2c65c2d911dabdd0ca829dc241765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952067"
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
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wiavideo. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




