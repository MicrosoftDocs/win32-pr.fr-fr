---
description: Pour déterminer la page de codes d’une base de données, appelez MsiDatabaseExport avec hDatabase défini sur le descripteur de la base de données et szTableName défini sur \_ ForceCodepage.
ms.assetid: afa3fbd9-9f54-4f72-ab5d-cb0dbbd9946c
title: Détermination de la page de codes d’une base de données d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212978cbce0e73ae495a0ed10ea9070cce6bd374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866349"
---
# <a name="determining-an-installation-databases-code-page"></a><span data-ttu-id="89599-103">Détermination de la page de codes d’une base de données d’installation</span><span class="sxs-lookup"><span data-stu-id="89599-103">Determining an Installation Database's Code Page</span></span>

<span data-ttu-id="89599-104">Pour déterminer la page de codes d’une base de données, appelez [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) avec *hDatabase* défini sur le descripteur de la base de données et *szTableName* défini sur \_ ForceCodepage.</span><span class="sxs-lookup"><span data-stu-id="89599-104">To determine the code page of a database, call [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) with *hDatabase* set to the handle of the database and *szTableName* set to \_ForceCodepage.</span></span> <span data-ttu-id="89599-105">Cela exporte un fichier texte avec une extension. IDT.</span><span class="sxs-lookup"><span data-stu-id="89599-105">This exports a text file with an .idt extension.</span></span> <span data-ttu-id="89599-106">Les deux premières lignes de ce fichier sont vides.</span><span class="sxs-lookup"><span data-stu-id="89599-106">The first two lines of this file are blank.</span></span> <span data-ttu-id="89599-107">La troisième ligne est le numéro de page de codes ANSI, suivi d’un onglet, suivi du nom \_ ForceCodepage.</span><span class="sxs-lookup"><span data-stu-id="89599-107">The third line is the ANSI code page number, followed by a tab, followed by the name \_ForceCodepage.</span></span> <span data-ttu-id="89599-108">Voir aussi [gestion des pages de codes des tables importées et exportées](code-page-handling-of-imported-and-exported-tables.md).</span><span class="sxs-lookup"><span data-stu-id="89599-108">See also [Code Page Handling of Imported and Exported Tables](code-page-handling-of-imported-and-exported-tables.md).</span></span>

<span data-ttu-id="89599-109">Un exemple de détermination de la page de codes à l’aide de la [**méthode Export**](database-export.md) est fourni dans le kit de développement logiciel (SDK) Windows Installer dans le cadre de l’utilitaire WiLangId.vbs.</span><span class="sxs-lookup"><span data-stu-id="89599-109">An example of determining the code page by using the [**Export method**](database-export.md) is provided in the Windows Installer SDK as a part of the utility WiLangId.vbs.</span></span> <span data-ttu-id="89599-110">Pour plus d’informations sur l’utilisation de WiLangId.vbs consultez la rubrique [gérer la langue et la page de codes](manage-language-and-codepage.md).</span><span class="sxs-lookup"><span data-stu-id="89599-110">For more information about using WiLangId.vbs see the topic: [Manage Language and Codepage](manage-language-and-codepage.md).</span></span>

 

 



