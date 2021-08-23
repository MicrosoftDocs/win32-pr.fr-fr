---
description: La méthode CanStep détermine si le décodeur MPEG-2 sur le système local peut effectuer une exécution pas à pas dans une direction spécifiée.
ms.assetid: 21721722-0bf4-4cc7-a0e4-96b353888948
title: Méthode CanStep
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ff6ca29443e059cd5ebfbbb553f67cf50b1cb13e1bc8d7199ac6cfae704cee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017587"
---
# <a name="canstep-method"></a>Méthode CanStep

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `CanStep` méthode détermine si le décodeur MPEG-2 sur le système local peut effectuer un pas à pas détaillé dans une direction spécifiée.

``` syntax
[ bCanStep = ] MSWebDVD.CanStep(bDirection)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bDirection*
</dt> <dd>

Booléen utilisé comme indicateur pour spécifier la direction, l’avant ou l’arrière, de la capacité de l’exécution pas à pas du décodeur.



| Valeur | Description                                          |
|-------|------------------------------------------------------|
| true  | L’étape de décodage peut-elle reculer ?                           |
| false | L’étape de décodage peut-elle progresser ? Il s'agit de la valeur par défaut. |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur booléenne true si le décodeur peut effectuer un pas à pas détaillé dans la direction spécifiée, et false dans le cas contraire.

## <a name="remarks"></a>Remarques

les décodeurs MPEG-2 ne prennent pas tous en charge les nouvelles fonctionnalités d’exécution pas à pas dans DirectShow® 8,0. Cette méthode interroge le décodeur pour ses fonctionnalités de pas à pas de frame. Si le décodeur peut effectuer un pas à pas, une application peut utiliser la méthode [**Step**](step-method.md) pour parcourir les frames. Cette méthode retourne toujours la **valeur true** si un décodeur logiciel est utilisé.

 

 



