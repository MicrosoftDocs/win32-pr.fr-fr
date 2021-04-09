---
description: L’approche recommandée pour gérer les pages de codes consiste à créer une base de données de base neutre qui contient uniquement des caractères qui peuvent être traduits dans une page de codes.
ms.assetid: 8ded41a6-6e5b-4a39-b783-e2b9f83eaed4
title: Création d’une base de données avec une page de codes neutre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08639b6ab3521f183a2dab46dfd257121b28bae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034656"
---
# <a name="creating-a-database-with-a-neutral-code-page"></a><span data-ttu-id="108c1-103">Création d’une base de données avec une page de codes neutre</span><span class="sxs-lookup"><span data-stu-id="108c1-103">Creating a Database with a Neutral Code Page</span></span>

<span data-ttu-id="108c1-104">L’approche recommandée pour gérer les pages de codes consiste à créer une base de données de base neutre qui contient uniquement des caractères qui peuvent être traduits dans une page de codes.</span><span class="sxs-lookup"><span data-stu-id="108c1-104">The recommended approach for handling code pages is to author a neutral base database that only contains characters that can be translated into any code page.</span></span> <span data-ttu-id="108c1-105">La base de données peut ensuite être définie sur la page de codes de la localisation et les informations de localisation peuvent être ajoutées comme décrit dans [localisation d’un Windows Installer Package](localizing-a-windows-installer-package.md).</span><span class="sxs-lookup"><span data-stu-id="108c1-105">The database may then be set to the code page of the localization and the localization information can be added as described in [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md).</span></span>

<span data-ttu-id="108c1-106">Pour créer une base de données neutre, évitez les caractères étendus qui n’appartiennent pas au jeu de caractères ASCII et nécessitent donc une page de codes spéciale.</span><span class="sxs-lookup"><span data-stu-id="108c1-106">To author a neutral database, avoid extended characters that do not belong to the ASCII character set and therefore require a special code page.</span></span> <span data-ttu-id="108c1-107">Par exemple, le signe de copyright, le © et le signe de marque déposée,, ne sont pas des caractères ASCII et nécessitent une page de codes ANSI spéciale pour un affichage correct.</span><span class="sxs-lookup"><span data-stu-id="108c1-107">For example, the copyright sign, ©, and the registered trademark sign, , are not ASCII characters, and require a special ANSI code page for proper display.</span></span> <span data-ttu-id="108c1-108">Utilisez à la place (c) et (r), car ces caractères peuvent être traduits ou transformés en symboles pour la version en anglais.</span><span class="sxs-lookup"><span data-stu-id="108c1-108">Instead use (c) and (r), because these characters can be translated or transformed to the symbols for the English-language version.</span></span> <span data-ttu-id="108c1-109">Cette base de données neutre peut ensuite être localisée en définissant sa page de codes et en ajoutant des informations de localisation par modification de table ou en important des fichiers d’archive de texte.</span><span class="sxs-lookup"><span data-stu-id="108c1-109">This neutral database can then be localized by setting its code page and adding localization information by table editing or by importing text archive files.</span></span>

 

 



