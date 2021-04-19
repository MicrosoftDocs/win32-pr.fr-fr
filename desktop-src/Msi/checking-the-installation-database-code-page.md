---
description: Une page de codes est une table interne que le système d’exploitation utilise pour mapper des symboles (lettres, chiffres et signes de ponctuation) à un nombre de caractères.
ms.assetid: e11193a2-2c72-43a9-8d35-fa524044e306
title: Vérification de la page de codes de la base de données d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ea9513ec80413e00a9f3f4c1232a06704f83e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517031"
---
# <a name="checking-the-installation-database-code-page"></a><span data-ttu-id="3efe6-103">Vérification de la page de codes de la base de données d’installation</span><span class="sxs-lookup"><span data-stu-id="3efe6-103">Checking the Installation Database Code Page</span></span>

<span data-ttu-id="3efe6-104">Une *page de codes* est une table interne que le système d’exploitation utilise pour mapper des symboles (lettres, chiffres et signes de ponctuation) à un nombre de caractères.</span><span class="sxs-lookup"><span data-stu-id="3efe6-104">A *code page* is an internal table that the operating system uses to map symbols (letters, numerals, and punctuation characters) to a character number.</span></span> <span data-ttu-id="3efe6-105">Différentes pages de codes assurent la prise en charge des jeux de caractères utilisés dans différents pays ou régions.</span><span class="sxs-lookup"><span data-stu-id="3efe6-105">Different code pages provide support for the character sets used in different countries or regions.</span></span> <span data-ttu-id="3efe6-106">Les pages de codes sont référencées par nombre ; par exemple, la page de codes 932 représente le jeu de caractères japonais, et la page de codes 950 représente l’un des jeux de caractères chinois.</span><span class="sxs-lookup"><span data-stu-id="3efe6-106">Code pages are referred to by number; for example, code page 932 represents the Japanese character set, and code page 950 represents one of the Chinese character sets.</span></span> <span data-ttu-id="3efe6-107">Consultez [localisation des tables Error et ActionText](localizing-the-error-and-actiontext-tables.md) pour obtenir la liste des pages de codes ASCII.</span><span class="sxs-lookup"><span data-stu-id="3efe6-107">See [Localizing the Error and ActionText Tables](localizing-the-error-and-actiontext-tables.md) for a list of ASCII code pages.</span></span>

<span data-ttu-id="3efe6-108">La même page de codes ASCII, 1252, peut être utilisée pour l’anglais et le français.</span><span class="sxs-lookup"><span data-stu-id="3efe6-108">The same ASCII code page, 1252, may be used for English and French.</span></span> <span data-ttu-id="3efe6-109">Par conséquent, la page de codes de la MNP2000.msi de base de données (anglais) n’a pas besoin d’être réinitialisée pour modifier l’installation en français.</span><span class="sxs-lookup"><span data-stu-id="3efe6-109">Therefore the code page for the database MNP2000.msi (English) does not need to be reset to change the installation to French.</span></span>

<span data-ttu-id="3efe6-110">Pour plus d’informations sur la définition de la page de codes [, consultez Gestion des pages de codes (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="3efe6-110">For more information about setting the code page see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>

[<span data-ttu-id="3efe6-111">Continuer</span><span class="sxs-lookup"><span data-stu-id="3efe6-111">Continue</span></span>](importing-localized-error-and-actiontext-tables.md)

 

 



