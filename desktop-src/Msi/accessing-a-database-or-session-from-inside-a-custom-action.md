---
description: Vous ne pouvez pas accéder à une session de programme d’installation à partir d’une action personnalisée qui n’est pas la session d’installation actuelle.
ms.assetid: 8aa0ac17-1341-4399-987e-d26175150874
title: Accès à une base de données ou à une session à partir d’une action personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839c34fbfcd6cc69c026db455b0c2e3a59a28e2f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092913"
---
# <a name="accessing-a-database-or-session-from-inside-a-custom-action"></a>Accès à une base de données ou à une session à partir d’une action personnalisée

Vous ne pouvez pas accéder à une session de programme d’installation à partir d’une action personnalisée qui n’est pas la session d’installation actuelle. Les actions personnalisées sont limitées à l’utilisation de la base de données active de la session et aucune autre base de données. les [fonctions de base de données](database-functions.md) Windows Installer suivantes ne doivent pas être appelées à partir d’une action personnalisée, car elles nécessitent un handle vers une base de données qui n’est pas la base de données de la session d’installation actuelle :

[**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)

 

[**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)

 

[**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)

 

[**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)

 

[**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)

 

[**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)

 

[**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)

 

[**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)

 

[**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accès à la session de programme d’installation actuelle à partir d’une action personnalisée](accessing-the-current-installer-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



