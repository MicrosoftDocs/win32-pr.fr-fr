---
description: Pour obtenir des informations générales sur la localisation, consultez Services de globalisation.
ms.assetid: 734961f6-de0a-4c54-9866-ade994c41c7e
title: Localisation d’un package Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b325b211302fba632f454f30eefbcb688f30d819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113566"
---
# <a name="localizing-a-windows-installer-package"></a>Localisation d’un package Windows Installer

Pour obtenir des informations générales sur la localisation, consultez [services de globalisation](../intl/globalization-services.md). La localisation d’un package de Windows Installer nécessite de modifier les chaînes affichées par l’interface utilisateur et peut également nécessiter l’ajout ou la modification de ressources de produit. Par exemple, la localisation peut inclure l’ajout de dll internationales et de fichiers localisés au produit.

**Pour localiser un package de Windows Installer**

1.  Préparez la localisation lors de la création du package d’installation d’origine. Concevez la disposition des fichiers localisés de sorte que les différentes versions de langue puissent coexister en toute sécurité lorsqu’elles sont installées sur l’ordinateur de l’utilisateur. Organisez les fichiers nécessitant une localisation dans des composants distincts et installez ces fichiers dans des répertoires distincts. Créer une base de données d’installation de base avec une page de contrôle neutre. Consultez [préparation d’un package de Windows Installer pour la localisation](preparing-a-windows-installer-package-for-localization.md).
2.  Définissez toujours la page de codes de la base de données qui est localisée avant d’ajouter des données localisées. Si la page de codes de la base de données localisée est neutre, consultez [définition de la page de codes d’une base de données](setting-the-code-page-of-a-database.md). Pour déterminer la page de codes, consultez [déterminer la page de codes d’une base de données d’installation](determining-an-installation-database-s-code-page.md).
3.  Importez une [table d’erreurs](error-table.md) localisée et une [table ActionText](actiontext-table.md) dans la base de données. Pour plus d’informations, consultez [localisation des tables Error et ActionText](localizing-the-error-and-actiontext-tables.md) pour obtenir une liste des langues prises en charge par le kit de développement logiciel (SDK) Microsoft Windows. Vous pouvez importer ces tables à l’aide de Msidb.exe ou [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta).
4.  Modifiez les autres colonnes localisables dans la base de données à l’aide d’un éditeur de table ou de requêtes SQL. Pour les fonctions d’accès SQL, consultez [utilisation des requêtes](working-with-queries.md). Les rubriques relatives aux tables de base de données identifient les colonnes de base de données qui peuvent être localisées. Pour plus d’informations, consultez la liste des tables dans les [tables de base de données](database-tables.md).
5.  Définissez la propriété [**ProductLanguage**](productlanguage.md) dans la [table de propriétés](property-table.md) sur l’ID de langue de la base de données. Lorsque vous créez un package en tant que langue neutre, affectez la valeur 0 à la propriété ProductLanguage et utilisez la police MS Shell Dlg comme style de texte pour toutes les boîtes de dialogue créées. Étant donné que certaines polices ne prennent pas en charge tous les jeux de caractères, vous pouvez vous assurer que le texte s’affiche correctement sur toutes les versions localisées du système d’exploitation à l’aide de cette police.
6.  Définissez le champ Language de la propriété [**Résumé du modèle**](template-summary.md) pour refléter l’ID de langue de la base de données.
7.  Si les chaînes de texte du [flux d’informations de synthèse](summary-information-stream.md) sont localisées, définissez la propriété Résumé de la page de [**codes**](codepage-summary.md) sur la page de codes.
8.  Définissez la propriété [**ProductCode**](productcode.md) dans la [table de propriétés](property-table.md) et définissez le code du package dans la propriété Résumé du [**numéro de révision**](revision-number-summary.md) sur un nouveau code de package. Un produit localisé est considéré comme un produit différent. Par exemple, les versions allemande et anglaise d’une application sont considérées comme deux produits différents et doivent avoir des codes de produit différents.
9.  La localisation peut nécessiter la modification des ressources qui existent déjà ou l’ajout de nouvelles ressources, telles que des fichiers ou des clés de registre. Vérifiez que le code du composant a été modifié pour chaque composant existant pour lequel une nouvelle ressource a été ajoutée. D’autres modifications peuvent également nécessiter des modifications du code d’un composant. Pour plus d’informations, consultez [modification du code du composant](changing-the-component-code.md).
10. Veillez à enregistrer la localisation et les autres modifications apportées à la base de données en enregistrant le package avec l’outil d’édition ou en appelant [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).

Pour plus d’informations, consultez [un exemple de localisation](a-localization-example.md).

 

 
