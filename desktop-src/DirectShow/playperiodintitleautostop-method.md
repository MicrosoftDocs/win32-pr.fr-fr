---
description: La méthode PlayPeriodInTitleAutoStop démarre la lecture à l’heure spécifiée dans le titre spécifié jusqu’à l’heure d’arrêt spécifiée.
ms.assetid: 0c4df76d-3991-4a6c-a8e5-5fd713eeffc2
title: Méthode PlayPeriodInTitleAutoStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05899b66b7f1a11f8f5b177d311b9634a52595b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846145"
---
# <a name="playperiodintitleautostop-method"></a>Méthode PlayPeriodInTitleAutoStop

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `PlayPeriodInTitleAutoStop` méthode démarre la lecture à l’heure spécifiée dans le titre spécifié jusqu’à l’heure d’arrêt spécifiée.

``` syntax
MSWebDVD.PlayPeriodInTitleAutoStop(iTitle, sStartTime, sEndTime)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Spécifie le titre sous la forme d’un entier.

</dd> <dt>

<span id="sStartTime"></span><span id="sstarttime"></span><span id="SSTARTTIME"></span>*sStartTime*
</dt> <dd>

Spécifie l’heure de début sous la forme d’une chaîne au format « hh : mm : SS : FF » (en spécifiant les heures, les minutes, les secondes, les frames).

</dd> <dt>

<span id="sEndTime"></span><span id="sendtime"></span><span id="SENDTIME"></span>*sEndTime*
</dt> <dd>

Spécifie l’heure de fin sous la forme d’une chaîne au format « hh : mm : SS : FF ».

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PlayChaptersAutoStop**](playchaptersautostop-method.md)
</dt> </dl>

 

 



