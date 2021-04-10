---
description: La propriété CurrentCCService définit ou récupère le service de sous-titrage en cours.
ms.assetid: 094cf812-3122-4d5f-af8a-afd1c2264a2b
title: Propriété CurrentCCService
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5c1ddf243b0ec943be1f22930a8802d28d1bda
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846477"
---
# <a name="currentccservice-property"></a>Propriété CurrentCCService

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `CurrentCCService` propriété définit ou récupère le service de sous-titrage en cours.

``` syntax
[ iService = ] MSWebDVD.CurrentCCService
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière indiquant le type de service de sous-titrage activé.

## <a name="remarks"></a>Notes

Les valeurs possibles de cette propriété sont les suivantes :



| Valeur | Description                                                          |
|-------|----------------------------------------------------------------------|
| 0x0   | Aucun service en cours. Il s’agit de la valeur par défaut.                       |
| 0x1   | True Captioning, premier champ. Service par défaut.                       |
| 0x2   | Sous-titrage pour la langue secondaire, deuxième champ. Généralement non utilisé. |



 

Cette propriété est en lecture/écriture.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CCActive**](ccactive-property.md)
</dt> </dl>

 

 



