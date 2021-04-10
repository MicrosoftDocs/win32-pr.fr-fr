---
description: L’événement ShowMenu est envoyé lorsque le disque active ou désactive l’émission d’un menu.
ms.assetid: 78fd0b80-baec-4174-9c55-f061627c3599
title: ShowMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b78c2751a270b56f95bac223ab80b2e2143b04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950209"
---
# <a name="showmenu"></a>ShowMenu

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

L' `ShowMenu` événement est envoyé lorsque le disque active ou désactive l’émission d’un menu.

``` syntax
ShowMenu(DVDMenuIDConstants, bEnabled)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*DVDMenuIDConstants*
</dt> <dd>

Spécifie le menu qui a été activé ou désactivé en tant que valeur numérique.



| Valeur | Description |
|-------|-------------|
| 2     | Intitulé       |
| 3     | Root        |
| 4     | Sous-titres  |
| 5     | Audio       |
| 6     | Angle       |
| 7     | Chapitre     |



 

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Spécifie si l’opération est activée ou désactivée en tant que valeur booléenne.

</dd> </dl>

 

 



