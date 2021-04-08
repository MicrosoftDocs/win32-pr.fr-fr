---
description: Le qualificateur dynamique indique une classe dont les instances sont créées dynamiquement. La valeur de ce qualificateur doit être définie sur TRUE.
ms.assetid: 63286687-abbf-49f0-8061-3b47fba75806
ms.tgt_platform: multiple
title: Qualificateur dynamique
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dynamic
api_type:
- NA
api_location: ''
ms.openlocfilehash: f6530942859c8c3de571ba9ddb94e9b1ce78cc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864022"
---
# <a name="dynamic-qualifier"></a>Qualificateur dynamique

Le qualificateur **dynamique** indique une classe dont les instances sont créées dynamiquement. La valeur de ce qualificateur doit être définie sur **true**.

Le qualificateur **dynamique** doit être spécifié sur toutes les classes qui contiennent des données et pour lesquelles les instances sont créées dynamiquement. Le qualificateur du [**fournisseur**](/windows/desktop/api/Provider/nl-provider-provider) est généralement spécifié pour identifier le fournisseur chargé de fournir les données.

Les classes qui contiennent uniquement des méthodes nécessitant une implémentation ne requièrent pas le qualificateur **dynamique** . Seul le qualificateur du [**fournisseur**](/windows/desktop/api/Provider/nl-provider-provider) est requis pour spécifier le nom du fournisseur pour fournir l’implémentation.

Toutes les classes dérivées d’une classe dynamique doivent être dynamiques. Vous ne pouvez pas dériver une classe statique à partir d’une classe dynamique.

Quand **Dynamic** est spécifié sur une propriété d’une instance, le qualificateur **PropertyContext** doit également être spécifié.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Qualificateurs WMI standard**](standard-wmi-qualifiers.md)
</dt> <dt>

[Qualificateurs WMI](wmi-qualifiers.md)
</dt> <dt>

[Ajout d’un qualificateur](adding-a-qualifier.md)
</dt> </dl>

 

 




