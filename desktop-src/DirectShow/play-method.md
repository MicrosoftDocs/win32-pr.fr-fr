---
description: La méthode Play lit le titre du DVD actuel.
ms.assetid: fe9dc266-5b12-479d-85cb-50cc6bb9d580
title: Play, méthode (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62323c9c86be476a35977dadf554bbfca3bca91
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521295"
---
# <a name="play-method-directshow"></a>Play, méthode (DirectShow)

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `Play` méthode lit le titre du DVD actuel.

``` syntax
MSWebDVD.Play()
```

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Si la lecture est suspendue ou arrêtée et que [**EnableResetOnStop**](enableresetonstop-property.md) a la valeur true, l’appel de **Play** reprendra la lecture à la vitesse normale à l’emplacement actuel. Si la lecture est arrêtée et que **EnableResetOnStop** a la valeur false, l’appel de **Play** entraîne la lecture du disque au début du premier titre.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Sort**](resume-method.md)
</dt> </dl>

 

 



