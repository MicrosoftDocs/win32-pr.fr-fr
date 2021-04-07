---
description: Le qualificateur de clé indique si la propriété fait partie du handle d’espace de noms.
ms.assetid: 838d295f-e812-4e46-99a4-d2714a0ae8dc
ms.tgt_platform: multiple
title: Qualificateur de clé
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Key
api_type:
- NA
api_location: ''
ms.openlocfilehash: affc9f4be594723700a65c9c92f8ae37ffead265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758325"
---
# <a name="key-qualifier"></a>Qualificateur de clé

Le qualificateur de **clé** indique si la propriété fait partie du handle d’espace de noms. Si plusieurs propriétés ont le qualificateur de **clé** , toutes ces propriétés forment collectivement la clé (une clé composée). Lorsqu’elles sont prises en compte, les propriétés de clé doivent fournir une référence unique pour chaque instance de classe. Si ce qualificateur est placé sur une propriété, seule la valeur **true** est autorisée.

Vous pouvez utiliser n’importe quel type de propriété, à l’exception des éléments suivants :

-   Tableaux
-   Nombres réels et à virgule flottante
-   Objets incorporés
-   Caractères inférieurs à ASCII 32 (autrement dit, les caractères d’espace blanc)
-   Les chaînes de caractères de type **char16** ou les chaînes de caractères définies en tant que clés doivent contenir des valeurs supérieures à U + 0020. Cela est dû au fait que WMI utilise des valeurs de clés dans les chemins d’accès aux objets et que vous ne pouvez pas utiliser de caractères non imprimables dans un chemin d’accès à un objet.

Quand une classe parente spécifie une clé, toutes les classes dérivées de la classe parente héritent de cette clé. Les classes dérivées ne peuvent pas modifier la clé héritée ou définir une nouvelle propriété de clé. Toutefois, lorsque vous dérivez une sous-classe d’une classe abstraite sans clé, vous pouvez introduire une clé dans la sous-classe.

Toutes les classes qui définissent plus d’une instance doivent spécifier une clé. Étant donné que les classes abstraites ne définissent pas d’instances, elles n’ont pas besoin de spécifier des clés. Étant donné que les classes Singleton ne définissent qu’une seule instance, elles ne peuvent pas spécifier de clés.

Les clés sont écrites une fois à l’instanciation de l’objet et ne doivent pas être modifiées ultérieurement. Il n’est pas judicieux d’appliquer une valeur par défaut à une propriété qualifiée de clé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



 

 




