---
description: La méthode SetDelayTime définit le délai d’attente de l’info-bulle associée à l’objet MSWebDVD.
ms.assetid: bb1086e1-57e2-495a-9b7b-2d349a516e72
title: SetDelayTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26ebd119f20977c98aa2664518dc2125b7b5c157b44ff53c3a37740bf40a1677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683739"
---
# <a name="setdelaytime"></a>SetDelayTime

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `SetDelayTime` méthode définit le délai d’attente pour l’info-bulle associée à l’objet **mswebdvd** .

``` syntax
MSWebDVD.SetDelayTime(iDelayType, iNewVal)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*iDelayType*
</dt> <dd>

Spécifie le type de délai sous la forme d’un entier.



| Valeur | Description                                                                                                                                                                                                                                      |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -1    | Pour rétablir la valeur par défaut du délai d’attente de autopop, affectez la valeur-1 à *iNewVal* .                                                                                                                                                                       |
| 0     | Définissez la durée pendant laquelle une fenêtre d’info-bulle reste visible si le pointeur est immobile dans le rectangle englobant d’un outil.                                                                                                                         |
| 1     | Définissez la durée pendant laquelle un pointeur doit rester immobile dans le rectangle englobant d’un outil avant que la fenêtre d’info-bulle ne s’affiche.                                                                                                                    |
| 2     | Définissez le temps nécessaire pour que les fenêtres d’info-bulle suivantes s’affichent lorsque le pointeur se déplace d’un outil à un autre.                                                                                                                          |
| 3     | Définissez tous les délais d’attente sur les proportions par défaut. Le temps de autopop est dix fois l’heure initiale et l’heure de réaffichage est le cinquième de l’heure initiale. Si cet indicateur est défini, utilisez une valeur positive de iNewVal pour spécifier l’heure initiale, en millisecondes. |



 

</dd> <dt>

<span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*iNewVal*
</dt> <dd>

Spécifie le délai, en millisecondes, sous la forme d’un entier.



| Valeur                    | Description                                                   |
|--------------------------|---------------------------------------------------------------|
| -1                       | Définit le délai spécifié dans *iDelayType* à sa valeur par défaut |
| toute autre valeur négative | Définit tous les types de retard à leur valeur par défaut.                  |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

 

 



