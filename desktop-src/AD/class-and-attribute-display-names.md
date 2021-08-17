---
title: Noms complets des classes et des attributs
description: Cette rubrique contient des informations et des instructions pour les noms d’affichage des classes et des attributs.
ms.assetid: c85905b2-ed8b-4032-8c54-fd4de8b34ecf
ms.tgt_platform: multiple
keywords:
- spécificateurs d’affichage noms d’affichage AD, de classe et d’attribut
- noms complets des classes AD
- noms d’affichage des attributs AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213132acfa6463b1c1e8a7615f5d7f488e53edfcdf9b75f8df5759fcd0e4d398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022590"
---
# <a name="class-and-attribute-display-names"></a>Noms complets des classes et des attributs

Le spécificateur d’affichage d’une classe d’objet contient les attributs suivants qui peuvent être utilisés pour spécifier les noms d’affichage localisés utilisés dans l’interface utilisateur pour les objets de cette classe :

-   L’attribut **classDisplayName** est une chaîne Unicode à valeur unique qui spécifie le nom complet de la classe.
-   L’attribut **attributeDisplayNames** est une propriété à valeurs multiples qui spécifie les noms à utiliser dans l’interface utilisateur pour les attributs de la classe d’objet.

Les valeurs **attributeDisplayNames** sont des chaînes Unicode ; chaque élément se compose d’une paire de noms délimitée par des virgules :


```C++
<attribute name>,<display text>
```



Dans cet exemple, « &lt; nom &gt; d’attribut » est le **lDAPDisplayName** de l’attribut et « &lt; texte affiché &gt; » est le texte à afficher comme nom de cet attribut dans l’interface utilisateur.

## <a name="guidelines-for-class-and-attribute-display-names"></a>Instructions pour les noms d’affichage de classes et d’attributs

Étant donné que de nombreux fournisseurs peuvent étendre des classes avec de nouveaux attributs ou créer des classes entièrement nouvelles, il est important que les noms complets de la classe et de l’attribut ne soient pas ambigus et n’entraînent pas de conflits.

Chaque fournisseur doit préfixer le nom complet de la classe avec un identificateur convivial unique basé sur le nom du fournisseur. Par exemple, si la société fictive Fabrikam Inc., crée une nouvelle classe dérivée de la classe « contact », elle peut avoir un nom d’affichage de classe unique « Fabrikam contact ».

Si un fournisseur étend une classe existante avec de nouveaux attributs, il doit de nouveau identifier de manière unique le nom complet de l’attribut afin qu’aucun conflit ne se produise avec d’autres noms d’affichage d’attribut. Là encore, le fait de préfixer le nom d’affichage de l’attribut avec un identificateur convivial unique basé sur le nom du fournisseur est une bonne pratique. Par exemple, si la société Fabrikam étend la classe utilisateur avec un nouvel attribut RH, elle peut afficher de manière unique l’attribut « informations sur les RH fabrikam ».

en outre, du point de vue de la localisation, chaque fournisseur doit localiser les noms d’affichage des classes et des attributs dans chaque langue prise en charge par Windows 2000.

## <a name="adding-a-value-to-the-attributedisplaynames-attribute"></a>Ajout d’une valeur à l’attribut attributeDisplayNames

**Pour ajouter une valeur de mappage de nom à l’attribut **attributeDisplayNames****

1.  Déterminez si la valeur de mappage de nom de l’attribut existe. Si une valeur de mappage de nom doit être remplacée, supprimez d’abord la valeur existante, à l’aide de la méthode [**IADs ::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) , avec le paramètre *LnControlCode* défini sur **publicités \_ Property \_ Delete** et le paramètre *vProp* défini sur la valeur à supprimer. N’utilisez pas **les \_ Propriétés ad \_ Clear** ou **ADS \_ Property \_ Update** pour *lnControlCode*.
2.  Créez la chaîne qui représente le nom complet de l’attribut. Pour obtenir un exemple, consultez le format ci-dessus.
3.  Utilisez la méthode [**IADs ::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) avec le paramètre *LnControlCode* défini sur **publicité \_ propriété \_ Append** pour ajouter la nouvelle valeur.
4.  Appelez [**IADs :: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) pour valider les modifications apportées au répertoire.

Pour plus d’informations sur l’affectation de noms aux nouvelles classes et attributs, consultez [Naming Attributes and classes](naming-attributes-and-classes.md).

 

 