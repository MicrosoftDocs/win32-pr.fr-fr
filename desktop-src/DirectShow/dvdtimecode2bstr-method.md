---
description: La méthode DVDTimeCode2bstr récupère une chaîne indiquant l’heure actuelle sur le disque.
ms.assetid: 0a477274-ac56-4f46-8461-53411362b33e
title: Méthode DVDTimeCode2bstr
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042c6889fd2d5ee76aa42fc4e92f1c2754a5c95d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513097"
---
# <a name="dvdtimecode2bstr-method"></a>Méthode DVDTimeCode2bstr

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DVDTimeCode2bstr` méthode récupère une chaîne indiquant l’heure actuelle sur le disque.

``` syntax
[ sTimeCode = ] MSWebDVD.DVDTimeCode2bstr(nTimeCode)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*sTimeCode*
</dt> <dd>

Spécifie l’heure actuelle sur le disque par rapport au début du titre sous la forme d’un nombre obtenu par le biais de l’événement [**\_ HMSF de \_ \_ \_ temps actuel du DVD**](ec-dvd-current-hmsf-time.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une chaîne de 11 caractères au format "HH : mm : SS : FF" représentant les heures, les minutes, les secondes et les frames qui définissent l’heure actuelle.

## <a name="remarks"></a>Notes

Cette méthode est en lecture seule.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestion des notifications d’événements DVD](handling-dvd-event-notifications.md)
</dt> </dl>

 

 



