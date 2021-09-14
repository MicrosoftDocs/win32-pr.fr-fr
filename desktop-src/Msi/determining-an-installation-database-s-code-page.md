---
description: Pour déterminer la page de codes d’une base de données, appelez MsiDatabaseExport avec hDatabase défini sur le descripteur de la base de données et szTableName défini sur \_ ForceCodepage.
ms.assetid: afa3fbd9-9f54-4f72-ab5d-cb0dbbd9946c
title: Détermination de la page de codes d’une base de données d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212978cbce0e73ae495a0ed10ea9070cce6bd374
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091614"
---
# <a name="determining-an-installation-databases-code-page"></a>Détermination de la page de codes d’une base de données d’installation

Pour déterminer la page de codes d’une base de données, appelez [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) avec *hDatabase* défini sur le descripteur de la base de données et *szTableName* défini sur \_ ForceCodepage. Cela exporte un fichier texte avec une extension. IDT. Les deux premières lignes de ce fichier sont vides. La troisième ligne est le numéro de page de codes ANSI, suivi d’un onglet, suivi du nom \_ ForceCodepage. Voir aussi [gestion des pages de codes des tables importées et exportées](code-page-handling-of-imported-and-exported-tables.md).

un exemple de détermination de la page de codes à l’aide de la [**méthode Export**](database-export.md) est fourni dans le kit de développement logiciel (SDK) Windows Installer dans le cadre de l’utilitaire WiLangId.vbs. Pour plus d’informations sur l’utilisation de WiLangId.vbs consultez la rubrique [gérer la langue et la page de codes](manage-language-and-codepage.md).

 

 



