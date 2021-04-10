---
description: ICE49 recherche les entrées de Registre par défaut qui ne sont pas de type de Registre \_ sz.
ms.assetid: 53d976fe-07d2-4b68-ae21-1dbd00d76942
title: ICE49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edc5ba319380e92fe7d1b7410673c1c688eb337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867294"
---
# <a name="ice49"></a>ICE49

ICE49 recherche les entrées de Registre par défaut qui ne sont pas de type de Registre **\_ SZ** .

## <a name="result"></a>Résultats

ICE49 publie un avertissement s’il existe une entrée de Registre par défaut qui n’est pas un type de Registre **\_ SZ** .

## <a name="example"></a>Exemple

ICE49 signale l’avertissement suivant pour l’exemple indiqué.

``` syntax
Reg Entry 'Reg1' is not of type REG_SZ. Default types must be REG_SZ 
    on Win95 Systems. Make sure the component is conditionalized 
    to never be installed on Win95 machines.
```

La valeur « \# 123 » est une valeur de Registre **DWORD** .

[Table du Registre](registry-table.md) (partielle)



| Registre | Nom | Valeur |
|----------|------|-------|
| Reg1     |      | \#123 |



 

Pour résoudre cet avertissement, remplacez la valeur par tapez **reg \_ SZ**.

Les composants avec des **\_ SZS** non-reg sont valides.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Syntaxe d’instruction conditionnelle](conditional-statement-syntax.md)
</dt> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



