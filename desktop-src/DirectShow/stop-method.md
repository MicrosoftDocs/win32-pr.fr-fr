---
description: La méthode Stop arrête la lecture.
ms.assetid: e1ebfacc-4f33-4b4d-8e6c-1d1e1f0a22bd
title: Méthode Stop (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8cae45c7f076f2c4e90f1e7f50676bebbd3482
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952644"
---
# <a name="stop-method-directshow"></a>Méthode Stop (DirectShow)

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `Stop` méthode arrête la lecture.

``` syntax
MSWebDVD.Stop()
```

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Si [**EnableResetOnStop**](enableresetonstop-property.md) a la valeur true, l’appel de `Stop` place le navigateur DVD, ainsi que le reste du graphique de filtre, à l’état arrêté, ce qui signifie que la lecture commence au début du disque la prochaine fois que l’utilisateur appuie sur le bouton de **lecture** . Si **EnableResetOnStop** a la valeur true, la lecture reprend là où elle s’est arrêtée lorsque l’utilisateur émet la commande **Play** suivante.

 

 



