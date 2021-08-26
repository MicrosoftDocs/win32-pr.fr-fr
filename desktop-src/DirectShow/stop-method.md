---
description: La méthode Stop arrête la lecture.
ms.assetid: e1ebfacc-4f33-4b4d-8e6c-1d1e1f0a22bd
title: Méthode Stop (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9eb216c3ad5c98dd1722ff941131198cfe662d025b20c3f71fe9ea758e0a7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050109"
---
# <a name="stop-method-directshow"></a>Méthode Stop (DirectShow)

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `Stop` méthode arrête la lecture.

``` syntax
MSWebDVD.Stop()
```

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Si [**EnableResetOnStop**](enableresetonstop-property.md) a la valeur true, l’appel de `Stop` place le navigateur DVD, ainsi que le reste du graphique de filtre, à l’état arrêté, ce qui signifie que la lecture commence au début du disque la prochaine fois que l’utilisateur appuie sur le bouton de **lecture** . Si **EnableResetOnStop** a la valeur true, la lecture reprend là où elle s’est arrêtée lorsque l’utilisateur émet la commande **Play** suivante.

 

 



