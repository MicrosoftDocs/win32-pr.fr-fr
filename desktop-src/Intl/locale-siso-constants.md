---
description: Paramètres régionaux \_ SIOS \* constantes
ms.assetid: c830e9e9-b58a-4d31-929a-ed699bc08d9f
title: Constantes LOCALE_SISO *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16a3d7583bc920daa2edc85b641f191b016bbbd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952121"
---
# <a name="locale_siso-constants"></a><span data-ttu-id="1dae6-103">Paramètres régionaux \_ SIOS \* constantes</span><span class="sxs-lookup"><span data-stu-id="1dae6-103">LOCALE\_SISO\* Constants</span></span>

<span data-ttu-id="1dae6-104">Cette rubrique définit les \_ \* constantes SIOS des paramètres régionaux utilisés par nls.</span><span class="sxs-lookup"><span data-stu-id="1dae6-104">This topic defines the LOCALE\_SISO\* constants used by NLS.</span></span>



| <span data-ttu-id="1dae6-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="1dae6-105">Value</span></span>                     | <span data-ttu-id="1dae6-106">Signification</span><span class="sxs-lookup"><span data-stu-id="1dae6-106">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dae6-107">Paramètres régionaux \_ SISO3166CTRYNAME</span><span class="sxs-lookup"><span data-stu-id="1dae6-107">LOCALE\_SISO3166CTRYNAME</span></span>  | <span data-ttu-id="1dae6-108">**Windows Me/98, Windows NT 4,0 :** Nom de pays/région, basé sur la norme ISO 3166, par exemple « États-Unis » pour le États-Unis.</span><span class="sxs-lookup"><span data-stu-id="1dae6-108">**Windows Me/98, Windows NT 4.0:** Country/region name, based on ISO Standard 3166, such as "US" for the United States.</span></span> <span data-ttu-id="1dae6-109">Cela peut également retourner un nombre, tel que « 029 » pour les Caraïbes.</span><span class="sxs-lookup"><span data-stu-id="1dae6-109">This can also return a number, such as "029" for Caribbean.</span></span> <span data-ttu-id="1dae6-110">Le nombre maximal de caractères autorisés pour cette chaîne est neuf, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="1dae6-110">The maximum number of characters allowed for this string is nine, including a terminating null character.</span></span>                                                                                        |
| <span data-ttu-id="1dae6-111">Paramètres régionaux \_ SISO3166CTRYNAME2</span><span class="sxs-lookup"><span data-stu-id="1dae6-111">LOCALE\_SISO3166CTRYNAME2</span></span> | <span data-ttu-id="1dae6-112">**Windows Vista et versions ultérieures :** Nom de la région ISO à trois lettres (code ISO 3166 3 lettres pour le pays ou la région), par exemple « USA » pour le États-Unis.</span><span class="sxs-lookup"><span data-stu-id="1dae6-112">**Windows Vista and later:** Three-letter ISO region name (ISO 3166 three-letter code for the country/region), such as "USA" for the United States.</span></span> <span data-ttu-id="1dae6-113">Cela peut également retourner un nombre, tel que « 029 » pour les Caraïbes.</span><span class="sxs-lookup"><span data-stu-id="1dae6-113">This can also return a number, such as "029" for Caribbean.</span></span> <span data-ttu-id="1dae6-114">Le nombre maximal de caractères autorisés pour cette chaîne est neuf, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="1dae6-114">The maximum number of characters allowed for this string is nine, including a terminating null character.</span></span>                                                            |
| <span data-ttu-id="1dae6-115">Paramètres régionaux \_ SISO639LANGNAME</span><span class="sxs-lookup"><span data-stu-id="1dae6-115">LOCALE\_SISO639LANGNAME</span></span>   | <span data-ttu-id="1dae6-116">**Windows Me/98, Windows NT 4,0 :** Nom abrégé du langage basé entièrement sur les valeurs 639 standard ISO, en minuscules, telles que « en » pour l’anglais.</span><span class="sxs-lookup"><span data-stu-id="1dae6-116">**Windows Me/98, Windows NT 4.0:** The abbreviated name of the language based entirely on the ISO Standard 639 values, in lowercase form, such as "en" for English.</span></span> <span data-ttu-id="1dae6-117">Il peut s’agir d’un code à trois lettres pour les langues qui n’ont pas de code à deux lettres, par exemple « Haw » pour Hawaii.</span><span class="sxs-lookup"><span data-stu-id="1dae6-117">This can be a 3-letter code for languages that don't have a 2-letter code, such as "haw" for Hawaiian.</span></span> <span data-ttu-id="1dae6-118">Le nombre maximal de caractères autorisés pour cette chaîne est neuf, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="1dae6-118">The maximum number of characters allowed for this string is nine, including a terminating null character.</span></span> |
| <span data-ttu-id="1dae6-119">Paramètres régionaux \_ SISO639LANGNAME2</span><span class="sxs-lookup"><span data-stu-id="1dae6-119">LOCALE\_SISO639LANGNAME2</span></span>  | <span data-ttu-id="1dae6-120">**Windows Vista et versions ultérieures :** Nom de langue ISO à trois lettres, en minuscules (code ISO 639-2 de trois lettres pour la langue), par exemple « eng » pour l’anglais.</span><span class="sxs-lookup"><span data-stu-id="1dae6-120">**Windows Vista and later:** Three-letter ISO language name, in lowercase form (ISO 639-2 three-letter code for the language), such as "eng" for English.</span></span> <span data-ttu-id="1dae6-121">Le nombre maximal de caractères autorisés pour cette chaîne est neuf, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="1dae6-121">The maximum number of characters allowed for this string is nine, including a terminating null character.</span></span>                                                                                                                  |



 

 

 



