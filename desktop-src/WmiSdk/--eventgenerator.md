---
description: Sert de classe parente pour les classes qui contrôlent la génération d’événements, tels que les événements de minuterie.
ms.assetid: 381b06e7-2857-4932-9f52-f1d62efa8b79
ms.tgt_platform: multiple
title: Classe __EventGenerator
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventGenerator
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b40524405c3b284e7ec61414e36448cb37afeab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210905"
---
# <a name="__eventgenerator-class"></a>\_\_EventGenerator, classe

La classe système **\_ \_ EventGenerator** est une classe de base abstraite qui sert de classe parente pour les classes qui contrôlent la génération d’événements, tels que les [événements de minuterie](receiving-a-timed-or-repeating-event.md).

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[abstract]
class __EventGenerator : __IndicationRelated
{
};
```

## <a name="members"></a>Membres

La classe **\_ \_ EventGenerator** ne définit aucun membre.

## <a name="remarks"></a>Notes

La classe **\_ \_ EventGenerator** est dérivée de [**\_ \_ IndicationRelated**](--indicationrelated.md), qui n’a pas de propriétés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_IndicationRelated**](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> </dl>

 

