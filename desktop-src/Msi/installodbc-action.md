---
description: L’action InstallODBC installe les pilotes, les traducteurs et les sources de données dans la table ODBCDriver, la table ODBCTranslator et la table ODBCDataSource.
ms.assetid: fbcf1fdc-5aef-4431-93fe-3ed02748b5ff
title: Action InstallODBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac9becd2a528646805f4201cfb415a6bc61bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521953"
---
# <a name="installodbc-action"></a>Action InstallODBC

L’action InstallODBC installe les pilotes, les traducteurs et les sources de données dans la table [ODBCDriver](odbcdriver-table.md), la table [ODBCTranslator](odbctranslator-table.md)et la [table ODBCDataSource](odbcdatasource-table.md). S’il existe déjà un pilote ou un convertisseur, l’action InstallODBC effectue les appels SQL nécessaires à l’installation.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action InstallODBC ne copie pas et ne supprime pas les fichiers, et doit se trouver après les actions qui copient ou suppriment des fichiers.

## <a name="actiondata-messages"></a>Messages ActionData

Le tableau suivant identifie les messages ActionData pour chaque pilote installé.



| Champ       | Description                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Description du pilote. Clé du pilote ODBC.                                 |
| \[2\]       | ComponentID.                                                             |
| \[3\]       | Dossier.                                                                  |
| \[4, 5,...\] | Paires attribut/valeur de [ODBCAttribute](odbcattribute-table.md). |



 

Le tableau suivant identifie les messages ActionData pour chaque traducteur installé.



| Champ       | Description                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Description du pilote. Clé du pilote ODBC.                                 |
| \[2\]       | ComponentID.                                                             |
| \[3\]       | Dossier.                                                                  |
| \[4, 5,...\] | Paires attribut/valeur de [ODBCAttribute](odbcattribute-table.md). |



 

Le tableau suivant identifie les messages ActionData pour chaque source de données installée.



| Champ       | Description                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Description du pilote. Clé du pilote ODBC.                                 |
| \[2\]       | ComponentID.                                                             |
| \[3\]       | Inscription : ODBC \_ Add \_ DSN ou ODBC \_ Add \_ sys \_ DSN.                     |
| \[4, 5,...\] | Paires attribut/valeur de [ODBCAttribute](odbcattribute-table.md). |



 

## <a name="remarks"></a>Notes

Le gestionnaire de pilotes ODBC doit être créé dans le package Microsoft installer et un composant nommé ODBCDriverManager doit être inclus. Le gestionnaire est installé si nécessaire.

Pour renommer le composant, définissez une propriété nommée ODBCDriverManager sur le nouveau nom du composant. Si un gestionnaire de pilotes ODBC 64 bits doit être installé, le composant qui le contient doit être nommé ODBCDriverManager64.

-   L’action InstallODBC interroge la [table ODBCDataSource](odbcdatasource-table.md) et la [table ODBCSourceAttribute](odbcsourceattribute-table.md) pour chaque source de données à installer, ainsi que les attributs de la source de données.
-   L’action InstallODBC interroge la [table ODBCDriver](odbcdriver-table.md) et la [table ODBCTranslator](odbctranslator-table.md) pour chaque pilote et traducteur sélectionné pour l’installation.
-   L’action InstallODBC interroge la [table ODBCAttribute](odbcattribute-table.md) pour obtenir les attributs des pilotes et des traducteurs.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de Windows Installer](windows-installer-examples.md)
</dt> </dl>

 

 



