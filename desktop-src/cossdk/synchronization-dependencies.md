---
description: Les valeurs de synchronisation peuvent être automatiquement déterminées ou restreintes par la configuration d’autres propriétés, telles que les exigences transactionnelles et l’activation juste-à-temps (JIT).
ms.assetid: 16771121-cb10-42b4-babc-59270188495a
title: Dépendances de synchronisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c139d0d6e78288b25e42bd0a84b29432cebb44ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860969"
---
# <a name="synchronization-dependencies"></a>Dépendances de synchronisation

Les valeurs de synchronisation peuvent être automatiquement déterminées ou restreintes par la configuration d’autres propriétés, telles que les exigences transactionnelles et l’activation juste-à-temps (JIT). Par exemple, COM+ applique la synchronisation pour les composants transactionnels et activés par le JIT.

Ces dépendances existent, car les composants qui sont activés juste-à-temps ou qui participent à des transactions doivent avoir une isolation et un comportement d’accès concurrentiel appropriés. Par conséquent, COM+ requiert que l’accès à ces composants soit sérialisé en appliquant la synchronisation. (Pour plus d’informations sur ces dépendances, consultez [activation juste-à-temps de com+](com--just-in-time-activation.md).)

Les tableaux suivants présentent les caractéristiques des valeurs d’attribut de synchronisation COM+.

### <a name="transactional-requirement"></a>Exigence transactionnelle



| Lorsque les transactions sont définies sur | La synchronisation peut être définie sur                    |
|------------------------------|--------------------------------------------------|
| Désactivé<br/>          | Tout, en fonction de l’activation JIT<br/> |
| Non pris en charge<br/>     | Tout, en fonction de l’activation JIT<br/> |
| Pris en charge<br/>         | Obligatoire<br/>                              |
| Obligatoire<br/>          | Obligatoire<br/>                              |
| Nouveau requis<br/>      | Obligatoire ou requiert New<br/>              |



 

### <a name="jit-activation"></a>Activation juste-à-temps



| Lorsque l’activation JIT a la valeur | La synchronisation peut être définie sur       |
|-------------------------------|-------------------------------------|
| activé<br/>            | Obligatoire ou requiert New<br/> |
| Désactivé<br/>           | Rien<br/>                 |



 

Pour plus d’informations sur la façon dont les attributs transaction, activation JIT et synchronisation se comportent, consultez [Configuration des transactions](configuring-transactions.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition de l’attribut de synchronisation](setting-the-synchronization-attribute.md)
</dt> <dt>

[Valeurs d’attribut de synchronisation](synchronization-attribute-values.md)
</dt> </dl>

 

 




