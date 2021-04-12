---
description: La méthode DVDAdm. GetParentalLevel récupère le niveau parental qui a été enregistré pour la dernière fois dans le registre.
ms.assetid: 2aadcf41-2c65-4f3a-8ce8-0fc9aa580ad9
title: Méthode GetParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdfa2c2193a9d02249076b2be2225fc50cd1edd5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385564"
---
# <a name="getparentallevel-method"></a>Méthode GetParentalLevel

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DVDAdm.GetParentalLevel` méthode récupère le niveau parental précédemment enregistré dans le registre.

``` syntax
[ iParentalLevel = ] DVD.DVDAdm.GetParentalLevel()
```

## <a name="return-value"></a>Valeur renvoyée

Retourne un entier compris entre 1 et 8 indiquant le niveau parental par défaut.

## <a name="remarks"></a>Notes

Le niveau parental récupéré par cette méthode n’est pas nécessairement le même que celui qui est actuellement stocké dans le contrôle MSWebDVD. pour récupérer le niveau actuellement stocké dans le contrôle, appelez la méthode [**GetPlayerParentalLevel**](getplayerparentallevel-method.md) . La valeur-1 indique que la gestion parentale est désactivée.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objet MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



