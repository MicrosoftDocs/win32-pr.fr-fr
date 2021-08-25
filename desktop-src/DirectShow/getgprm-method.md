---
description: La méthode GetGPRM récupère le registre de paramètres généraux spécifié.
ms.assetid: 66afd2a5-6aa1-4280-93cf-dd3cfed2499d
title: Méthode GetGPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c46307f1cbec49b4916cdbd528c2b22cfb42bf89a06285c5c779339786599d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812559"
---
# <a name="getgprm-method"></a>Méthode GetGPRM

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `GetGPRM` méthode récupère le registre de paramètres généraux spécifié.

``` syntax
[ iGPRM = ] MSWebDVD.GetGPRM(iIndex)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Spécifie le registre à récupérer sous la forme d’un entier. La valeur doit être comprise entre 0 et 15.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière représentant le registre spécifié.

## <a name="remarks"></a>Remarques

Cette méthode n’est pas requise pour les fonctionnalités de navigation ou de lecture de DVD à l’aide de l’objet **mswebdvd** . Il est fourni pour ceux qui ont une compréhension approfondie de la spécification du DVD qui souhaite implémenter des fonctionnalités avancées. GPRMs peut être utilisé pour stocker toutes les valeurs, de sorte qu’elles puissent être définies et lues librement. Toutefois, étant donné que les GPRMs sont utilisés pour stocker également les commandes de disque, la modification de leurs valeurs à l’aide de [**SetGPRM**](setgprm-method.md) peut entraîner un comportement imprévisible.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SetGPRM**](setgprm-method.md)
</dt> </dl>

 

 



