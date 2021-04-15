---
title: Type de données IVgAdjustments VML
description: Type de données IVgAdjustments VML
ms.assetid: d605632b-3ee2-44fd-8122-f38b1f91e965
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29f85f93218db098ca247fa66b1f493e9c622a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463303"
---
# <a name="vml-ivgadjustments-data-type"></a>Type de données IVgAdjustments VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Collection d’ajustements d’une forme qui peut être utilisée dans les formules. Les ajustements peuvent être utilisés en tant qu’espaces réservés temporaires ou pour une raison quelconque, vous pouvez utiliser des variables. La collection ne contient que 8 ajustements.



| Attributs | Description                                                                                                                                                                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Longueur     | **Integer**. Nombre d’ajustements. Ne peut pas être supérieur à 8.                                                                                                                                                                                                                                                                          |
| Élément       | **Long**. Tableau d’ajustements indexés de 0 à 7. Notez que les ajustements peuvent être spécifiés pour SPARC. autrement dit, les valeurs de tableau intermédiaire ne peuvent pas toujours être remplies. Par exemple, les éléments 1, 3 et 5 peuvent avoir des valeurs pour une longueur de 3, avec l’élément (0), l’élément (2) et l’élément (4) spécifiés. Pour voir si un élément existe, utilisez l’attribut exists. |
| Exists     | **IVgTriState**. Détermine si un ajustement spécifié existe. Notez qu’un index doit être utilisé ; en d’autres cas, Exists (Item) doit être utilisé pour récupérer l’existence d’un élément.                                                                                                                                                           |
| Valeur      | **Chaîne**. Représentation textuelle des valeurs numériques, avec des virgules entre chaque nombre.                                                                                                                                                                                                                                                    |



 

 

 