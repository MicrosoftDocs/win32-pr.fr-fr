---
description: Le service Windows Installer utilise la langue de l’utilisateur actuel dans toutes les boîtes de dialogue jusqu’à l’ouverture d’un package Windows Installer.
ms.assetid: c9902990-7a26-48fd-96ac-4d5a749e34be
title: Localisation de la langue affichée par les boîtes de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042b2b7f9ac256ebad265b75a8756fc422403e37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520592"
---
# <a name="localizing-the-language-displayed-by-dialogs"></a><span data-ttu-id="0da0f-103">Localisation de la langue affichée par les boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="0da0f-103">Localizing the Language Displayed by Dialogs</span></span>

<span data-ttu-id="0da0f-104">Le service Windows Installer utilise la langue de l’utilisateur actuel dans toutes les boîtes de dialogue jusqu’à l’ouverture d’un package Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="0da0f-104">The Windows Installer service uses the current user's language in all dialogs until a Windows Installer package is opened.</span></span> <span data-ttu-id="0da0f-105">Le Windows Installer détermine cela à l’aide de **GetUserDefaultUILanguage**.</span><span class="sxs-lookup"><span data-stu-id="0da0f-105">The Windows Installer determines this by using **GetUserDefaultUILanguage**.</span></span> <span data-ttu-id="0da0f-106">Lors de l’ouverture d’un package Windows Installer, le programme d’installation affiche les boîtes de dialogue à l’aide de la langue du package, comme spécifié par la propriété [**Résumé du modèle**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="0da0f-106">When a Windows Installer package is opened, the installer displays dialogs using the package's language as specified by the [**Template Summary**](template-summary.md) Property.</span></span>

<span data-ttu-id="0da0f-107">Pour plus d’informations sur la localisation du langage d’un package de Windows Installer, consultez également [un exemple de localisation](a-localization-example.md).</span><span class="sxs-lookup"><span data-stu-id="0da0f-107">For more information about localizing the language of a Windows Installer package, see also [A Localization Example](a-localization-example.md).</span></span>

 

 



