---
description: étant donné que le programme d’installation utilise une base de données relationnelle, il existe des fonctions permettant d’effectuer des requêtes langage SQL (SQL) à la base de données. la procédure suivante décrit comment utiliser SQL pour interroger une base de données.
ms.assetid: 1b8fd935-4964-4875-801b-cc6765b16924
title: Utilisation des requêtes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b6ea5a2f0b962b195fde531216f4b57fd5834162e31c1e34fc9ff1dd3695df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942124"
---
# <a name="working-with-queries"></a>Utilisation des requêtes

étant donné que le programme d’installation utilise une base de données relationnelle, il existe des fonctions permettant d’effectuer des requêtes langage SQL (SQL) à la base de données. la procédure suivante décrit comment utiliser SQL pour interroger une base de données.

**Pour interroger une base de données avec SQL**

1.  ouvrez l’objet de [**vue**](view-object.md) , avec l’instruction SQL appropriée, en appelant la fonction [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) .

    Un objet de [**vue**](view-object.md) est la table logique créée par l’application d’une requête à un ensemble de tables. SQL requêtes doivent respecter la [syntaxe SQL](sql-syntax.md) fournie par le programme d’installation. cette instruction SQL peut contenir des marqueurs de paramètres qui ne sont pas spécifiés tant que l’objet de **vue** n’est pas exécuté.

2.  Exécutez l’objet de [**vue**](view-object.md) en appelant la fonction [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) .
3.  Récupérez l’enregistrement suivant d’un objet de [**vue**](view-object.md) en appelant la fonction [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch) .
4.  Modifiez l’objet de [**vue**](view-object.md) en appelant la fonction [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) .

    Vous pouvez également valider les données avec [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) en passant les indicateurs appropriés. Si **MsiViewModify** retourne \_ des données d’erreur non valides \_ d’une demande de validation, les données sous-jacentes sont endommagées.

5.  Obtenez des informations détaillées sur l’erreur sur l’objet de [**vue**](view-object.md) en appelant la fonction [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) .
6.  Fermez l’objet de [**vue**](view-object.md) en appelant la fonction [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose) .

pour plus d’informations, consultez [exemples de requêtes de base de données à l’aide d’SQL et de Script](examples-of-database-queries-using-sql-and-script.md).

 

 



