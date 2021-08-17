---
description: vous pouvez ajouter des informations de localisation à une base de données d’installation à l’aide d’un éditeur de tables de base de données comme Orca fourni avec le kit de développement logiciel (SDK) Windows Installer, ou en appelant les fonctions de base de données à partir d’une application.
ms.assetid: cc1eb336-5dec-40cc-8aa5-564cd167855d
title: Gestion des pages de codes des chaînes de paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37555b905c60cb8f4727ccb723435d28b24d41d3aca1fc7026e34b799e25414a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328338"
---
# <a name="code-page-handling-of-parameter-strings"></a>Gestion des pages de codes des chaînes de paramètres

vous pouvez ajouter des informations de localisation à une base de données d’installation à l’aide d’un éditeur de tables de base de données comme Orca fourni avec le kit de développement logiciel (SDK) Windows Installer, ou en appelant les [fonctions de base de données](database-functions.md) à partir d’une application. Veillez à passer uniquement des paramètres de chaîne qui utilisent la page de codes de la base de données localisée. Si un paramètre de chaîne contient des caractères qui ne peuvent pas être représentés par la page de codes de la base de données, le programme d’installation retourne une erreur lors de l’appel de [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Pour obtenir la liste des pages de codes numériques, consultez [localisation des tables Error et ActionText](localizing-the-error-and-actiontext-tables.md).

Pour plus d’informations, consultez [la page détermination de la page de codes d’une base de données d’installation](determining-an-installation-database-s-code-page.md).

## <a name="adding-localization-information-to-a-database"></a>Ajout d’informations de localisation à une base de données

Lorsque vous ajoutez des informations de localisation à une base de données, la page de codes de la base de données doit être prise en charge par le système d’exploitation. Il n’est pas nécessaire qu’il s’agit de la page de codes actuelle du système. [**IsValidCodePage**](/windows/desktop/api/winnls/nf-winnls-isvalidcodepage) doit retourner la **valeur true** pour la page de codes de la base de données. Étant donné que le système convertit les chaînes ANSI en Unicode, il existe une erreur si la page de codes de l’utilisateur actuel n’est pas la même que la page de codes de la base de données.

l’appel de la version ANSI de l’API Windows Installer convertit la chaîne localisée en Unicode à l’aide de la page de codes système actuelle. Lorsque la base de données est validée, la chaîne Unicode est convertie en ANSI à l’aide de la page de codes de la base de données. Si la page de codes système actuelle diffère de la page de codes de la chaîne localisée, le résultat peut être une perte de données et une conversion de chaîne incorrecte.

La procédure suivante vous montre comment stocker les données de localisation.

**Pour stocker les données de localisation**

1.  Définissez la page de codes de la base de données sur la page de codes de la chaîne localisée.
2.  Convertissez la chaîne ANSI en Unicode à l’aide de la fonction [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) , puis spécifiez la page de codes des données localisées.
3.  appelez la version unicode de l’API Windows Installer à l’aide de la chaîne unicode pour ajouter les données localisées.
4.  Validez les modifications apportées à la localisation dans la base de données à l’aide de [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).

Vous pouvez également ajouter des informations de localisation à une base de données d’installation en important et en exportant des fichiers d’archive de texte ASCII. Pour plus d’informations, consultez [gestion des pages de codes des tables importées et exportées](code-page-handling-of-imported-and-exported-tables.md).

 

 
