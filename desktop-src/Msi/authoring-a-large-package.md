---
description: utilisez cette instruction pour créer un Windows Installer package contenant plus de 32767 fichiers.
ms.assetid: 3145629f-cc0a-4216-8549-76bb61070772
title: Création d’un package volumineux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca09c427336e4ca8a17fd8ebdf803f52ebe6c26
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092522"
---
# <a name="authoring-a-large-package"></a>Création d’un package volumineux

utilisez cette instruction pour créer un Windows Installer package contenant plus de 32767 fichiers.

si votre package Windows Installer contient plus de 32767 fichiers, vous devez modifier le schéma de la base de données pour augmenter la limite des colonnes suivantes :

-   Colonne de séquence de la [table de fichiers](file-table.md).
-   Colonne LastSequence de la [table multimédia](media-table.md).
-   Colonne de séquence de la [table des correctifs](patch-table.md).

Pour plus d’informations, consultez [format de définition de colonne](column-definition-format.md).

**Pour augmenter la limite d’une colonne de base de données**

1.  Exportez la table vers un fichier. IDT. Pour plus d’informations, consultez [Msidb.exe](msidb-exe.md), [exporter des fichiers](export-files.md)et [importation et exportation](importing-and-exporting.md).
2.  Modifiez le fichier. IDT pour remplacer le type de colonne I2 par i4, ou de I2 par I4.
3.  Exportez la table de [ \_ validation](-validation-table.md) dans un fichier. IDT.
4.  Modifiez le fichier. IDT pour modifier les valeurs de la colonne MaxValue du tableau de [ \_ validation](-validation-table.md) afin de prendre en compte les largeurs de colonne accrues.
5.  Importez de nouveau les fichiers. IDT dans la base de données.

Notez que les transformations et les correctifs ne peuvent pas être créés entre deux packages avec des types de colonnes différents.

 

 



