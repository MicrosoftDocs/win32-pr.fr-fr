---
title: /target, commutateur
description: Le commutateur/target permet au compilateur MIDL d’activer des optimisations disponibles uniquement dans les versions récentes de Windows. Le commutateur/target active automatiquement les commutateurs supplémentaires.
ms.assetid: 8c5aa319-e6a6-4803-99f3-ed8751d565d5
keywords:
- MIDL du commutateur/target
topic_type:
- apiref
api_name:
- /target
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: b1c4292ed3b1fba2d3f3d9bd350c06cee89d2ba569103db1b677bc690be4af15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895779"
---
# <a name="target-switch"></a>/target, commutateur

Le commutateur **/target** permet au compilateur MIDL d’activer des optimisations disponibles uniquement dans les versions récentes de Windows. Le commutateur **/target** active automatiquement les commutateurs supplémentaires.

``` syntax
midl /target level
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*level* 
</dt> <dd>

Spécifie le niveau cible, tel que NT50, NT51, NT60, NT61, NT62 ou NT100.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le commutateur **/target** active automatiquement les commutateurs supplémentaires, selon le système d’exploitation, comme indiqué dans le tableau suivant :



| Système d’exploitation | niveau/target | Commutateurs activés                     |
|------------------|---------------|----------------------------------------|
| Windows 2000     | NT50          | /Oicf/Error tout/Robust               |
| Windows XP       | NT51          | /Oicf/Error All/Protocol All |
| Windows Vista    | NT60          | /Oicf/Error All/Protocol All |
| Windows 7        | NT61          | /Oicf/Error All/Protocol All |
| Windows 8        | NT62          | /Oicf/Error All/Protocol All |
| Windows 10       | NT100         | /Oicf/Error All/Protocol All |
 

pour s’assurer qu’un stub s’exécute sur le système spécifié par le commutateur **/target** , MIDL émet une erreur quand une fonctionnalité disponible uniquement sur une version plus récente de Windows est présente. Le tableau suivant spécifie le niveau minimal de **/target** requis pour activer la fonctionnalité. Les niveaux cibles plus élevés incluent toutes les fonctionnalités des niveaux cibles inférieurs.



| Niveau/Target minimal requis | Fonctionnalités                                                                                                                                                                                          |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NT50                           | /Robust<br/> \[message\]<br/> \[async\]<br/> \[\_UUID asynchrone\]<br/> \[notifier \] en mode/Oicf<br/> \[encoder \] ou \[ décoder \] en mode/Oicf<br/>                   |
| NT51                           | prise en charge de/Protocol 64 bits<br/> \[\_Ignorer partiellement\]<br/> \[forcer l' \_ allocation\]<br/>                                                                                                 |
| NT60                           | Marshaling de structure complexe forcé<br/> Handles de contexte dans un tableau ou une structure<br/> \[\]prise en charge des chaînes non dimensionnées par plage<br/> \[\_handle de \_ contexte \_ strict de type\]<br/> |
| NT61                           | Les appels directs du stub COM pour les interfaces avec moins de 32 méthodes requièrent la liaison des stubs COM avec **OLE32.DLL**.<br/>                                                                          |
| NT62                           | Support ARM<br/> Prise en charge de WinRT<br/>                                                                                                                                                   |
| NT100                          | \[\]support system_handle<br /> |


 

## <a name="examples"></a>Exemples

**MIDL/Target NT50**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>
