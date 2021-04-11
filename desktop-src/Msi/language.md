---
description: Le type de données Language est une chaîne de texte contenant un ou plusieurs ID de langue numériques valides. S’il existe deux ou plusieurs ID de langue, ceux-ci doivent être séparés par des virgules.
ms.assetid: 547fc662-f055-421e-a621-eecdfa0b13f6
title: Language
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc87cb8b88dc3a693eee6890276adb67ad359e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201468"
---
# <a name="language"></a><span data-ttu-id="f0022-104">Language</span><span class="sxs-lookup"><span data-stu-id="f0022-104">Language</span></span>

<span data-ttu-id="f0022-105">Le type de données Language est une chaîne de texte contenant un ou plusieurs ID de langue numériques valides.</span><span class="sxs-lookup"><span data-stu-id="f0022-105">The Language data type is a text string containing one or more valid numeric language IDs.</span></span> <span data-ttu-id="f0022-106">S’il existe deux ou plusieurs ID de langue, ceux-ci doivent être séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="f0022-106">If there are two or more language IDs, they must be separated by commas.</span></span>

<span data-ttu-id="f0022-107">Le type de données Language est une valeur 16 bits qui est la combinaison d’ID numériques primaires et de sous-langage.</span><span class="sxs-lookup"><span data-stu-id="f0022-107">The Language data type is a 16-bit value that is the combination of a primary and sublanguage numeric IDs.</span></span> <span data-ttu-id="f0022-108">Le LANGID principal comprend les bits de 0 à 9, tandis que l’ID de sous-langue est bits 10 à 15.</span><span class="sxs-lookup"><span data-stu-id="f0022-108">The Primary LANGID comprises bits 0 through 9 while the subLanguage ID is bits 10 through 15.</span></span> <span data-ttu-id="f0022-109">Pour obtenir la liste des identificateurs numériques primaires et secondaires, consultez la rubrique relative aux [constantes et aux chaînes](../intl/language-identifier-constants-and-strings.md) de l’identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="f0022-109">For a list of primary and sub language numeric identifiers, see the [Language Identifier Constants and Strings](../intl/language-identifier-constants-and-strings.md) topic.</span></span>

<span data-ttu-id="f0022-110">Pour les ID de langue principaux, la plage 0x200 à 0x3FF est définissable par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f0022-110">For primary language IDs, the range 0x200 to 0x3ff is user definable.</span></span> <span data-ttu-id="f0022-111">La plage 0x000 à 0x1ff est réservée à l’utilisation du système.</span><span class="sxs-lookup"><span data-stu-id="f0022-111">The range 0x000 to 0x1ff is reserved for system use.</span></span> <span data-ttu-id="f0022-112">Pour les ID de sous-langue, la plage 0x20 à 0x3F est définissable par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f0022-112">For sublanguage IDs, the range 0x20 to 0x3f is user definable.</span></span> <span data-ttu-id="f0022-113">La plage 0x00 à 0x1F est réservée à l’utilisation du système.</span><span class="sxs-lookup"><span data-stu-id="f0022-113">The range 0x00 to 0x1f is reserved for system use.</span></span>

 

 
