---
description: La propriété EnableResetOnStop définit ou récupère une valeur qui détermine le mode de reprise de la lecture lorsque le graphique de filtre effectue une transition à partir de l’état arrêté.
ms.assetid: ff2e2756-e3f3-4ddb-b99d-5fa65ec67f6b
title: Propriété EnableResetOnStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9449d8dd3e2e5ab0e1f008cba3e4cb2aabaa78c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012219"
---
# <a name="enableresetonstop-property"></a>Propriété EnableResetOnStop

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `EnableResetOnStop` propriété définit ou récupère une valeur qui détermine le mode de reprise de la lecture lorsque le graphique de filtre effectue une transition à partir de l’état arrêté.

``` syntax
[ bEnableReset = ] MSWebDVD.EnableResetOnStop
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur booléenne indiquant où l’objet MSWebDVD recommence à s’exécuter après l’arrêt du graphique de filtre.

## <a name="remarks"></a>Notes

Cette propriété est en lecture/écriture.

Les valeurs possibles de cette propriété sont : avec la valeur par défaut true.



| Valeur | Description                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| true  | Le navigateur DVD est réinitialisé et démarre la lecture à partir du début du disque. Il s’agit de la valeur par défaut |
| false | Le navigateur DVD reprend la lecture là où il s’est arrêté.                                                 |



 

 

 



