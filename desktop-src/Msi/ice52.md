---
description: ICE52 vérifie les propriétés privées dans la table AppSearch. Consultez à propos des propriétés.
ms.assetid: 18d1489e-666a-488d-ae12-5dbe60885a2e
title: ICE52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96f514f38e44a802b092acff53ac14f10c5e5d32c03888b7d45540443d34be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044039"
---
# <a name="ice52"></a>ICE52

ICE52 vérifie les propriétés privées dans la [table AppSearch](appsearch-table.md). Consultez [à propos des propriétés](about-properties.md).

quand vous utilisez Windows 2000 toutes les propriétés définies dans la colonne propriété de la table AppSearch doivent être des propriétés publiques.

## <a name="result"></a>Résultat

ICE52 publie un avertissement s’il existe une propriété privée dans la table AppSearch.

## <a name="example"></a>Exemple

ICE52 publie l’avertissement suivant pour l’exemple indiqué.

``` syntax
Property 'Property2' in AppSearch row 'Property2'.'Signature2' 
    is not public. It should be all uppercase.
```

[Table AppSearch](appsearch-table.md)



| Propriété  | Signature  |
|-----------|------------|
| PROPERTY1 | Signature1 |
| Property2 | Signature2 |



 

Pour corriger cet avertissement, passez à la propriété publique personnalisée : PROPERTY2.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



