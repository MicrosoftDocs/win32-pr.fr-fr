---
title: Propriétés et attributs ADSI
description: Les attributs sont parfois appelés propriétés. Cela peut entraîner une confusion. Cette documentation utilise les définitions suivantes pour les propriétés et les attributs.
ms.assetid: 8e391d36-5a8d-4960-805a-0caf281cab80
ms.tgt_platform: multiple
keywords:
- Propriétés et attributs ADSI ADSI
- ADSI ADSI, utilisation, accès et manipulation des données, des propriétés et des attributs
- propriétés ADSI
- attributs ADSI
- propriétés ADSI, définition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b05637cada9a62cee129e9645385233b4700cbf2762b9446ba9a871d1897d440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082793"
---
# <a name="adsi-properties-and-attributes"></a>Propriétés et attributs ADSI

Les attributs sont parfois appelés propriétés. Cela peut entraîner une confusion. Cette documentation utilise les définitions suivantes pour les propriétés et les attributs.

Les propriétés sont des valeurs nommées associées à un objet de programmation. Par exemple, l’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) expose des propriétés telles que [**Class**](iads-property-methods.md) et **Name**.

Les attributs sont les données associées aux objets dans un service d’annuaire. Par exemple, un objet utilisateur aura un attribut appelé **CN** qui contient une chaîne qui est le nom unique commun ou relatif de l’objet. Les attributs sont accessibles par le biais de méthodes d’interface ADSI comme [**IADs. obten**](/windows/desktop/api/Iads/nf-iads-iads-get) et [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put).

Pour plus d’informations sur les propriétés et les attributs ADSI, consultez :

-   [Le cache des attributs ADSI](the-adsi-attribute-cache.md)
-   [Attributs Single et multiple value](single-vs--multiple-value-attributes.md)
-   [Active Directory attributs opérationnels](active-directory-operational-attributes.md)

 

 




