---
description: ICE98 vérifie le champ de description de la table ODBCDataSource pour une source de données ODBC. Elle utilise la fonction SQLValidDSN pour vérifier que seuls les caractères valides sont utilisés et que la description ne dépasse pas la longueur maximale autorisée.
ms.assetid: ed78db96-10a1-4e42-9147-2309c9ca9c6e
title: ICE98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23f8a627b057e6c235fdb57a4f2d5d2b2cf6274e528ef4945c6a6323e1888427
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894689"
---
# <a name="ice98"></a>ICE98

ICE98 vérifie le champ de description de la [table ODBCDataSource](odbcdatasource-table.md) pour une source de données ODBC. Elle utilise la fonction **SQLValidDSN** pour vérifier que seuls les caractères valides sont utilisés et que la description ne dépasse pas la longueur maximale autorisée.

## <a name="result"></a>Résultat

ICE98 publie les avertissements suivants.



| AVERTISSEMENT ICE98                    | Description                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Le nom de la source de données n’est pas valide. | la valeur dans la colonne Description de la [Table ODBCDataSource](odbcdatasource-table.md) contient des caractères non valides ou est trop longue, ce qui signifie qu’elle dépasse la SQL \_ \_ longueur maximale \_ de DSN de 32. |



 

## <a name="example"></a>Exemple

ICE98 signale les avertissements suivants pour l’exemple :

``` syntax
The data source name is invalid: !
The data source name is invalid: <String of length > 32>
```

[Table ODBCDataSource](odbcdatasource-table.md) (partielle)



| DataSource | Description                      |
|------------|----------------------------------|
| BadChar    | !                                |
| TooLong    | <String of length > 32> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> <dt>

[Table ODBCDataSource](odbcdatasource-table.md)
</dt> </dl>

 

 



