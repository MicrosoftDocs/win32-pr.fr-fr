---
description: La valeur de la propriété Résumé du numéro de révision dans le flux d’informations de résumé doit être remplacée par une nouvelle valeur unique lors de la localisation d’une base de données, car la base de données d’installation est en cours de modification. Consultez codes de package.
ms.assetid: fce292c5-6702-4948-a13a-2a9ccacbd5c9
title: Mise à jour d’un flux d’informations de synthèse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37c022023f79d8f4d3999db6e11e4cf65b73e1ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393772"
---
# <a name="updating-a-summary-information-stream"></a><span data-ttu-id="685c3-104">Mise à jour d’un flux d’informations de synthèse</span><span class="sxs-lookup"><span data-stu-id="685c3-104">Updating a Summary Information Stream</span></span>

<span data-ttu-id="685c3-105">La valeur de la propriété [**Résumé du numéro de révision**](revision-number-summary.md) dans le flux d’informations de [Résumé](summary-information-stream.md) doit être remplacée par une nouvelle valeur unique lors de la localisation d’une base de données, car la base de données d’installation est en cours de modification.</span><span class="sxs-lookup"><span data-stu-id="685c3-105">The value of the [**Revision Number Summary**](revision-number-summary.md) Property in the [summary information stream](summary-information-stream.md) must be changed to a new, unique value when localizing a database, because the installation database is being changed.</span></span> <span data-ttu-id="685c3-106">Consultez [codes de package](package-codes.md).</span><span class="sxs-lookup"><span data-stu-id="685c3-106">See [Package Codes](package-codes.md).</span></span>

<span data-ttu-id="685c3-107">La valeur de la propriété [**Résumé du modèle**](template-summary.md) dans le flux d’informations de résumé doit être remplacée par l’identificateur de langue numérique (LANGID) du nouveau langage.</span><span class="sxs-lookup"><span data-stu-id="685c3-107">The value of the [**Template Summary**](template-summary.md) Property in the summary information stream must be changed to the numeric language identifier (LANGID) of the new language.</span></span>

<span data-ttu-id="685c3-108">Si les chaînes de texte descriptives dans le flux d’informations de synthèse sont localisées dans la nouvelle langue, la propriété de résumé de la page de [**codes**](codepage-summary.md) doit être définie sur la page de codes appropriée pour la nouvelle langue.</span><span class="sxs-lookup"><span data-stu-id="685c3-108">If the descriptive text strings in the summary information stream are localized to the new language, the [**Codepage Summary**](codepage-summary.md) Property must be set to the correct code page for the new language.</span></span>

<span data-ttu-id="685c3-109">Vous pouvez modifier le flux d’informations de synthèse du package localisé en procédant de la même façon que lors de l' [Ajout d’informations de résumé](adding-summary-information.md).</span><span class="sxs-lookup"><span data-stu-id="685c3-109">You may modify the summary information stream of the localized package by the same procedure as in [Adding Summary Information](adding-summary-information.md).</span></span> <span data-ttu-id="685c3-110">Un exemple illustrant l’utilisation des méthodes d’informations récapitulatives de la base de données est également fourni dans le kit de développement logiciel (SDK) Windows Installer en tant que WiSumInf.vbs de l’utilitaire.</span><span class="sxs-lookup"><span data-stu-id="685c3-110">An example demonstrating the use of the database summary information methods is also provided in the Windows Installer SDK as the utility WiSumInf.vbs.</span></span> <span data-ttu-id="685c3-111">Pour plus d’informations sur la WiSumInf.vbs, consultez [gérer les informations de résumé](manage-summary-information.md).</span><span class="sxs-lookup"><span data-stu-id="685c3-111">For more information about WiSumInf.vbs, see [Manage Summary Information](manage-summary-information.md).</span></span>

[<span data-ttu-id="685c3-112">Continuer</span><span class="sxs-lookup"><span data-stu-id="685c3-112">Continue</span></span>](adding-localized-resources.md)

 

 



