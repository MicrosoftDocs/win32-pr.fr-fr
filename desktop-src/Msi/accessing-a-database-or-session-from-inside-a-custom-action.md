---
description: Vous ne pouvez pas accéder à une session de programme d’installation à partir d’une action personnalisée qui n’est pas la session d’installation actuelle.
ms.assetid: 8aa0ac17-1341-4399-987e-d26175150874
title: Accès à une base de données ou à une session à partir d’une action personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c653d14bc2fdb361469389c4ee053e5d98b65f8c8265516c4e2c3bd4fc4c96d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046059"
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

 

 



