---
description: Vous ne pouvez pas accéder à une session de programme d’installation à partir d’une action personnalisée qui n’est pas la session d’installation actuelle.
ms.assetid: 8aa0ac17-1341-4399-987e-d26175150874
title: Accès à une base de données ou à une session à partir d’une action personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839c34fbfcd6cc69c026db455b0c2e3a59a28e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951805"
---
# <a name="accessing-a-database-or-session-from-inside-a-custom-action"></a><span data-ttu-id="46b75-103">Accès à une base de données ou à une session à partir d’une action personnalisée</span><span class="sxs-lookup"><span data-stu-id="46b75-103">Accessing a Database or Session from Inside a Custom Action</span></span>

<span data-ttu-id="46b75-104">Vous ne pouvez pas accéder à une session de programme d’installation à partir d’une action personnalisée qui n’est pas la session d’installation actuelle.</span><span class="sxs-lookup"><span data-stu-id="46b75-104">You cannot access an installer session from a custom action that is not the current installation session.</span></span> <span data-ttu-id="46b75-105">Les actions personnalisées sont limitées à l’utilisation de la base de données active de la session et aucune autre base de données.</span><span class="sxs-lookup"><span data-stu-id="46b75-105">Custom actions are limited to working with only the active database of the session and no other databases.</span></span> <span data-ttu-id="46b75-106">Les [fonctions de base de données](database-functions.md) Windows Installer suivantes ne doivent pas être appelées à partir d’une action personnalisée, car elles nécessitent un handle vers une base de données qui n’est pas la base de données de la session d’installation actuelle :</span><span class="sxs-lookup"><span data-stu-id="46b75-106">The following Windows Installer [Database Functions](database-functions.md) must not be called from a custom action, because they require a handle to a database that is not the database of the current installation session:</span></span>

[<span data-ttu-id="46b75-107">**MsiDatabaseMerge**</span><span class="sxs-lookup"><span data-stu-id="46b75-107">**MsiDatabaseMerge**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)

 

[<span data-ttu-id="46b75-108">**MsiCreateTransformSummaryInfo**</span><span class="sxs-lookup"><span data-stu-id="46b75-108">**MsiCreateTransformSummaryInfo**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)

 

[<span data-ttu-id="46b75-109">**MsiDatabaseApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="46b75-109">**MsiDatabaseApplyTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)

 

[<span data-ttu-id="46b75-110">**MsiDatabaseCommit**</span><span class="sxs-lookup"><span data-stu-id="46b75-110">**MsiDatabaseCommit**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)

 

[<span data-ttu-id="46b75-111">**MsiDatabaseExport**</span><span class="sxs-lookup"><span data-stu-id="46b75-111">**MsiDatabaseExport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)

 

[<span data-ttu-id="46b75-112">**MsiDatabaseGenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="46b75-112">**MsiDatabaseGenerateTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)

 

[<span data-ttu-id="46b75-113">**MsiDatabaseImport**</span><span class="sxs-lookup"><span data-stu-id="46b75-113">**MsiDatabaseImport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)

 

[<span data-ttu-id="46b75-114">**MsiEnableUIPreview**</span><span class="sxs-lookup"><span data-stu-id="46b75-114">**MsiEnableUIPreview**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)

 

[<span data-ttu-id="46b75-115">**MsiGetDatabaseState**</span><span class="sxs-lookup"><span data-stu-id="46b75-115">**MsiGetDatabaseState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)

## <a name="related-topics"></a><span data-ttu-id="46b75-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="46b75-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46b75-117">Accès à la session de programme d’installation actuelle à partir d’une action personnalisée</span><span class="sxs-lookup"><span data-stu-id="46b75-117">Accessing the Current Installer Session from Inside a Custom Action</span></span>](accessing-the-current-installer-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



