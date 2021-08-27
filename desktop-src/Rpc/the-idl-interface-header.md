---
title: En-tête d’interface IDL
description: L’en-tête d’interface IDL spécifie des informations sur l’interface dans son ensemble. Contrairement à ACF, l’en-tête d’interface contient des attributs qui sont indépendants de la plateforme.
ms.assetid: 667e5228-3ea7-4910-90b9-999e6fd705e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c176078c370819331405b070ffa832384584a944b65fae771b9a2044a178e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924268"
---
# <a name="the-idl-interface-header"></a>En-tête d’interface IDL

L’en-tête d’interface IDL spécifie des informations sur l’interface dans son ensemble. Contrairement à ACF, l’en-tête d’interface contient des attributs qui sont indépendants de la plateforme.

Les attributs dans l’en-tête d’interface sont globaux pour l’ensemble de l’interface. Autrement dit, ils s’appliquent à l’interface et à toutes ses parties. Ces attributs sont placés entre crochets au début de la définition de l’interface. Un exemple est présenté dans la définition d’interface suivante :

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

Notez que l’en-tête d’interface contient les **\[** attributs [**UUID**](/windows/desktop/Midl/uuid) **\]** et **\[** [**version**](/windows/desktop/Midl/version) **\]** . Étant donné que ceux-ci représentent respectivement l’UUID et le numéro de version de l’interface, il s’agit d’attributs de l’interface entière.

Le corps de l’interface peut également contenir des attributs. Toutefois, ils ne sont pas applicables à l’ensemble de l’interface. Ils font référence à des éléments spécifiques dans l’interface, tels que les paramètres de procédure distante.

Pour une description complète des attributs d’en-tête IDL, consultez [Référence du langage MIDL](/windows/desktop/Midl/midl-language-reference).

 

 