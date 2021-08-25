---
description: La propriété CurrentCCService définit ou récupère le service de sous-titrage en cours.
ms.assetid: 094cf812-3122-4d5f-af8a-afd1c2264a2b
title: Propriété CurrentCCService
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d836e852d1a144abb5422f71d0127eb9c37b8f333dce0723db2c2b3b1889ec50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075959"
---
# <a name="currentccservice-property"></a>Propriété CurrentCCService

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `CurrentCCService` propriété définit ou récupère le service de sous-titrage en cours.

``` syntax
[ iService = ] MSWebDVD.CurrentCCService
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière indiquant le type de service de sous-titrage activé.

## <a name="remarks"></a>Remarques

Les valeurs possibles de cette propriété sont les suivantes :



| Valeur | Description                                                          |
|-------|----------------------------------------------------------------------|
| 0x0   | Aucun service en cours. Il s'agit de la valeur par défaut.                       |
| 0x1   | True Captioning, premier champ. Service par défaut.                       |
| 0x2   | Sous-titrage pour la langue secondaire, deuxième champ. Généralement non utilisé. |



 

Cette propriété est en lecture/écriture.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCActive**](ccactive-property.md)
</dt> </dl>

 

 



