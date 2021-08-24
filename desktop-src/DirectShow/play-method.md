---
description: La méthode Play lit le titre du DVD actuel.
ms.assetid: fe9dc266-5b12-479d-85cb-50cc6bb9d580
title: Play, méthode (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d4cea7dc53afc6a116ad052da9a4ca0d52c2e8687d99bde854d3f89fa60a9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633559"
---
# <a name="play-method-directshow"></a>Play, méthode (DirectShow)

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `Play` méthode lit le titre du DVD actuel.

``` syntax
MSWebDVD.Play()
```

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Si la lecture est suspendue ou arrêtée et que [**EnableResetOnStop**](enableresetonstop-property.md) a la valeur true, l’appel de **Play** reprendra la lecture à la vitesse normale à l’emplacement actuel. Si la lecture est arrêtée et que **EnableResetOnStop** a la valeur false, l’appel de **Play** entraîne la lecture du disque au début du premier titre.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Reprendre**](resume-method.md)
</dt> </dl>

 

 



