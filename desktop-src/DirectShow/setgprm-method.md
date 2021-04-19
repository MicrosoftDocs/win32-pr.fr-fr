---
description: La méthode SetGPRM définit le registre de paramètres généraux spécifié sur la valeur spécifiée.
ms.assetid: ded28f2a-5e40-4f76-9ed4-de10296529e1
title: Méthode SetGPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e7492c599cde4c074c1a806f897edf3a8fe0a4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513887"
---
# <a name="setgprm-method"></a>Méthode SetGPRM

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `SetGPRM` méthode définit le registre de paramètres généraux spécifié sur la valeur spécifiée.

``` syntax
MSWebDVD.SetGPRM(iIndex, nValue)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Spécifie le registre de paramètres général à définir en tant qu’entier. La valeur entière doit être comprise entre 0 et 15.

</dd> <dt>

<span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*nValeur*
</dt> <dd>

Spécifie la nouvelle valeur du Registre sous la forme d’un entier.

</dd> </dl>

## <a name="remarks"></a>Notes

Les registres de paramètres généraux, ou GPRMs, sont des registres 16 bits que chaque disque peut utiliser de manière unique pour le stockage de données temporaire. Une application de lecteur n’a pas besoin d’accéder à ces registres pour un contrôle de lecture ou de navigation standard à l’aide de l’objet **mswebdvd** . Cette méthode est fournie pour les applications de lecteur qui implémentent des fonctionnalités avancées. N’essayez pas de modifier le GPRMs directement à moins d’avoir une connaissance approfondie de la spécification DVD et de la façon dont les GPRMs sont utilisés sur le disque en question pour être lu. La modification de ces valeurs peut entraîner un comportement imprévisible.

 

 



