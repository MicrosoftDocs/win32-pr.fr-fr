---
description: Définissez toujours la page de codes d’une base de données avant d’ajouter des informations de localisation.
ms.assetid: 0d8aee30-989a-4093-8718-1bb90029c0fb
title: Définition de la page de codes d’une base de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c9ac1840b624b821dff6a85bee94607cd9568dcd6bb9b01025cb02f87c5c39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628539"
---
# <a name="setting-the-code-page-of-a-database"></a>Définition de la page de codes d’une base de données

Définissez toujours la page de codes d’une base de données avant d’ajouter des informations de localisation. La tentative de définition de la page de codes après l’entrée de données dans la base de données n’est pas recommandée, car cela peut corrompre des caractères étendus. La localisation peut être facilement facilitée en commençant par une base de données qui est indépendante de la page de codes. Pour plus d’informations, consultez [création d’une base de données avec une page de codes neutre](creating-a-database-with-a-neutral-code-page.md). Vous pouvez déterminer la page de codes actuelle d’une base de données comme décrit dans détermination de la [page de codes d’une base de données d’installation](determining-an-installation-database-s-code-page.md). Consultez [localisation des tables Error et ActionText](localizing-the-error-and-actiontext-tables.md) pour obtenir la liste des pages de codes numériques.

Vous pouvez définir la page de codes d’une base de données vide ou d’une base de données avec une page de codes neutre, en important un fichier d’archive de texte contenant une page de codes non neutre avec [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Cela permet de définir la page de codes de la base de données sur la page de codes du fichier importé. Tous les fichiers d’archive qui sont ensuite importés dans la base de données doivent avoir la même page de codes que le premier fichier. Si un fichier d’archive de texte est exporté à partir d’une base de données, la page de codes du fichier d’archive est la même que la base de données parente. Consultez [gestion des pages de codes des tables importées et exportées](code-page-handling-of-imported-and-exported-tables.md).

La page de codes d’une base de données peut être définie sur une page de codes numérique spécifiée à l’aide de [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) pour importer un fichier d’archive de texte au format suivant : deux lignes vides ; suivi d’une ligne contenant la page de codes numérique, d’un délimiteur de tabulation et de la chaîne exacte : \_ ForceCodepage. notez qu’avec Windows 2000, cela traduit toutes les chaînes dans la base de données en la page de codes de \_ ForceCodepage. Cela peut être prévu lors de la localisation d’une base de données existante et de la conversion de toutes les chaînes non neutres vers la nouvelle page de codes. Toutefois, cela génère une erreur si la base de données contient des chaînes non neutres qui ne doivent pas être traduites.

L’utilitaire WiLangId.vbs fournit un exemple de la façon de définir la page de codes d’un package à l’aide de la [**méthode Import**](database-import.md). une copie de WiLangId.vbs est fournie dans le kit de développement logiciel (SDK) Windows Installer. Vous pouvez utiliser cet utilitaire pour déterminer les versions de langue prises en charge par la base de données (package), la langue utilisée par le programme d’installation pour toutes les chaînes de l’interface utilisateur qui ne sont pas créées dans la base de données (produit) ou la page de codes ANSI unique pour le pool de chaînes (CodePage). Pour plus d’informations sur l’utilisation de WiLangId.vbs consultez la page d’aide : [gérer la langue et la page de codes](manage-language-and-codepage.md).

Pour déterminer les valeurs du produit, du package et de la page de codes, exécutez WiLangId.vbs comme suit.

**cscript wilangid.vbs** *\[ chemin d’accès \] à la base de données*

Pour définir la page de codes du package, exécutez la ligne de commande suivante.

**cscript wilangid.vbs** *\[ chemin d’accès \] à la page* *\[ \]* de **codes** de la base de données

Par exemple, pour définir la page de codes de test.msi sur la valeur de page de codes ANSI numérique 1252, exécutez la ligne de commande suivante.

**cscript wilangid.vbs c : \\ temp \\test.msi CodePage 1252**

 

 



