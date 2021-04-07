---
description: La méthode SetClipVideoRect fait un zoom de l’affichage vidéo sur le sous-rectangle spécifié.
ms.assetid: 3940a382-8d53-4ff9-b024-38de1aa00f54
title: Méthode SetClipVideoRect
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7f4b003ef20b82f1e783ebf074e8bbd5cc793
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746293"
---
# <a name="setclipvideorect-method"></a>Méthode SetClipVideoRect

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `SetClipVideoRect` méthode effectue un zoom de l’affichage vidéo sur le sous-rectangle spécifié.

``` syntax
MSWebDVD.SetClipVideoRect(oRect)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*oRect*
</dt> <dd>

Spécifie un objet [DVDRect](dvdrect-object.md) , qui contient le rectangle de découpage.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Lorsque vous définissez un nouveau rectangle de découpage, l’objet agrandit cette zone pour s’ajuster aux dimensions d’affichage globales de l’application. Cela crée l’effet de zoom avant sur une zone particulière de l’écran. Pour spécifier le rectangle, créez un nouvel objet [DVDRect](dvdrect-object.md) et renseignez ses propriétés.

Le rectangle le plus courant pour l’affichage vidéo est 720 x 540.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetClipVideoRect**](getclipvideorect-method.md)
</dt> </dl>

 

 



