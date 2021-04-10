---
description: Msimerg.exe est un utilitaire de ligne de commande qui utilise MsiDatabaseMerge pour fusionner une base de données de référence dans une base de données de base.
ms.assetid: db0c9ae5-a8e8-4eff-ae14-67dcce352483
title: Msimerg.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0555aa7bd762b92ed67d0bac1487159fadb73a6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952807"
---
# <a name="msimergexe"></a><span data-ttu-id="75072-103">Msimerg.exe</span><span class="sxs-lookup"><span data-stu-id="75072-103">Msimerg.exe</span></span>

<span data-ttu-id="75072-104">Msimerg.exe est un utilitaire de ligne de commande qui utilise [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) pour [fusionner](merges-and-transforms.md) une base de données de référence dans une base de données de base.</span><span class="sxs-lookup"><span data-stu-id="75072-104">Msimerg.exe is a command line utility that uses [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) to [merge](merges-and-transforms.md) a reference database into a base database.</span></span>

<span data-ttu-id="75072-105">Cet outil est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="75072-105">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="75072-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75072-106">Syntax</span></span>

<span data-ttu-id="75072-107">**Msimerg** *{base de données de base} {base de données de référence}*</span><span class="sxs-lookup"><span data-stu-id="75072-107">**Msimerg** *{base database}{reference database}*</span></span>

<span data-ttu-id="75072-108">En cas de conflit de fusion entre les deux bases de données, les informations sur les conflits sont placées dans la \_ table MergeErrors.</span><span class="sxs-lookup"><span data-stu-id="75072-108">If there is a merge conflict between the two databases, the conflict information is placed in the \_MergeErrors table.</span></span>

## <a name="command-line-options"></a><span data-ttu-id="75072-109">Options de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="75072-109">Command Line Options</span></span>

<span data-ttu-id="75072-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="75072-110">None.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75072-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="75072-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75072-112">Outils de développement Windows Installer</span><span class="sxs-lookup"><span data-stu-id="75072-112">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="75072-113">Versions, outils et redistribuables publiés</span><span class="sxs-lookup"><span data-stu-id="75072-113">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



