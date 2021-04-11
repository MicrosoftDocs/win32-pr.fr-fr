---
description: ICE98 vérifie le champ de description de la table ODBCDataSource pour une source de données ODBC. Elle utilise la fonction SQLValidDSN pour vérifier que seuls les caractères valides sont utilisés et que la description ne dépasse pas la longueur maximale autorisée.
ms.assetid: ed78db96-10a1-4e42-9147-2309c9ca9c6e
title: ICE98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf06e97341bd8f15502b1ea1fe43a975dc9cde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203406"
---
# <a name="ice98"></a>ICE98

ICE98 vérifie le champ de description de la [table ODBCDataSource](odbcdatasource-table.md) pour une source de données ODBC. Elle utilise la fonction **SQLValidDSN** pour vérifier que seuls les caractères valides sont utilisés et que la description ne dépasse pas la longueur maximale autorisée.

## <a name="result"></a>Résultats

ICE98 publie les avertissements suivants.



| AVERTISSEMENT ICE98                    | Description                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Le nom de la source de données n’est pas valide. | La valeur dans la colonne Description de la [table ODBCDataSource](odbcdatasource-table.md) contient des caractères non valides ou est trop longue, ce qui signifie qu’elle dépasse la \_ \_ \_ longueur de DSN max. de 32. |



 

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

 

 



