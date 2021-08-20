---
title: Recherche d’une liste d’attributs à interroger
description: Lors de la recherche d’objets d’une classe particulière, les comparaisons dans votre filtre de recherche doivent spécifier des attributs qui existent réellement sur les objets de cette classe.
ms.assetid: 19d52933-e4b0-414f-9785-871e624da07b
ms.tgt_platform: multiple
keywords:
- Recherche d’une liste d’attributs pour interroger Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0edfee59c42a8cf07be05ab31e58c0298f7285c8a02de659257e3b3cd14bfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189189"
---
# <a name="finding-a-list-of-attributes-to-query"></a>Recherche d’une liste d’attributs à interroger

Lors de la recherche d’objets d’une classe particulière, les comparaisons dans votre filtre de recherche doivent spécifier des attributs qui existent réellement sur les objets de cette classe. Pour obtenir les attributs de liste sur un objet d’une classe particulière, établissez une liaison à cette classe dans le schéma abstrait et récupérez les propriétés [**IADsClass. MandatoryProperties**](/windows/desktop/ADSI/iadsclass-property-methods) et **IADsClass. (OptionalProperties)** . Pour plus d’informations, consultez [lecture du schéma abstrait](reading-the-abstract-schema.md).

En outre, tous les objets héritent de la classe abstraite supérieure. Par conséquent, tout attribut en **haut** peut exister, bien qu’il ne soit pas défini, sur un objet.

Si vous recherchez dans le catalogue global, veillez à spécifier des attributs dans le catalogue global. Les attributs inclus dans le catalogue global ont le **isMemberOfPartialAttributeSet** défini sur **true** sur leurs objets **attributeSchema** . N’oubliez pas que ces données ne sont pas disponibles dans le schéma abstrait ; Lisez-le à partir de l’objet **attributeSchema** dans le conteneur de schéma.

Dans le catalogue global, un attribut de lien précédent peut être interrogé uniquement si les deux conditions suivantes sont réunies : tout d’abord, l’attribut est marqué pour être inclus dans le catalogue global. Deuxièmement, le lien suivant est également marqué pour être inclus dans le catalogue global. Cela s’applique aux filtres de requête et aux résultats de la requête. Pour plus d’informations, consultez [attributs liés](linked-attributes.md).

En outre, certains attributs, principalement sur l’objet utilisateur, sont construits. Les filtres de requête ne peuvent pas contenir d’attributs construits. Les attributs construits ne peuvent pas être évalués dans les filtres de requête ; Toutefois, elles peuvent être retournées dans les résultats de la requête. Cela s’applique à tous les contextes d’attribution de noms et au catalogue global. Les attributs construits ont **ADS \_ systemFlags \_ attr \_ est \_ construit** (0x00000004) dans la propriété **systemFlags** sur leurs objets **attributeSchema** .

> [!Note]  
> Pour plus d’informations sur les classes et les attributs prédéfinis inclus dans le système, consultez [Active Directory Domain Services référence](active-directory-domain-services-reference.md). Ces pages répertorient les attributs obligatoires et facultatifs de chaque classe d’objet. Pour les attributs, la page de référence indique si l’attribut est indexé, construit, lié ou dans le catalogue global.

 

 

 