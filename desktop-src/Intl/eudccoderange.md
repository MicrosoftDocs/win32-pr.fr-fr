---
description: La clé de Registre EUDCCodeRange définit les plages de codes de caractères définis par l’utilisateur final (EUDC) pour diverses pages de codes (jeux de caractères).
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: EUDCCodeRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e68c71751ca5d13cd04c95ff66c84067fd1d46d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536599"
---
# <a name="eudccoderange"></a><span data-ttu-id="82261-103">EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="82261-103">EUDCCodeRange</span></span>

<span data-ttu-id="82261-104">La clé de Registre EUDCCodeRange définit les plages de codes de [caractères définis par l’utilisateur final (EUDC)](end-user-defined-characters.md) pour diverses pages de codes (jeux de caractères).</span><span class="sxs-lookup"><span data-stu-id="82261-104">The EUDCCodeRange registry key defines [end-user-defined character (EUDC)](end-user-defined-characters.md) code ranges for various code pages (character sets).</span></span> <span data-ttu-id="82261-105">Elle est utilisée uniquement par les outils qui créent des EUDCs et n’est pas d’une préoccupation directe pour les utilisateurs EUDC.</span><span class="sxs-lookup"><span data-stu-id="82261-105">It is used only by tools that create EUDCs, and is not of direct concern to EUDC users.</span></span> <span data-ttu-id="82261-106">Cette clé de registre a l’emplacement de Registre suivant :</span><span class="sxs-lookup"><span data-stu-id="82261-106">This registry key has the following registry location:</span></span>

<span data-ttu-id="82261-107">HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ contrôler \\ la \\ page de codes nls \\ EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="82261-107">HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\NLS\\CodePage\\EUDCCodeRange</span></span>

<span data-ttu-id="82261-108">Le format est le suivant :</span><span class="sxs-lookup"><span data-stu-id="82261-108">The format is:</span></span>

<span data-ttu-id="82261-109">EUDCCodeRange CodePage = FromTo \[ , FromTo\]</span><span class="sxs-lookup"><span data-stu-id="82261-109">EUDCCodeRange CodePage=FromTo\[,FromTo\]</span></span>

<span data-ttu-id="82261-110">où :</span><span class="sxs-lookup"><span data-stu-id="82261-110">where:</span></span>



|          |                                                                                                                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82261-111">CodePage</span><span class="sxs-lookup"><span data-stu-id="82261-111">CodePage</span></span> | <span data-ttu-id="82261-112">L’une des chaînes « 932 » (japonais), « 936 » (chinois simplifié), « 949 » (coréen), « 950 » (chinois traditionnel) ou « Unicode » (Unicode).</span><span class="sxs-lookup"><span data-stu-id="82261-112">One of the strings "932" (Japanese), "936" (Simplified Chinese), "949" (Korean), "950" (Traditional Chinese), or "Unicode" (Unicode).</span></span> <span data-ttu-id="82261-113">Aucune autre valeur n’est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="82261-113">No other values are supported.</span></span>                                     |
| <span data-ttu-id="82261-114">FromTo</span><span class="sxs-lookup"><span data-stu-id="82261-114">FromTo</span></span>   | <span data-ttu-id="82261-115">Valeur de chaîne composée d’une paire de valeurs hexadécimales à 4 chiffres séparés par un trait d’Union (-).</span><span class="sxs-lookup"><span data-stu-id="82261-115">String value consisting of a pair of 4-digit hexadecimal values separated by a hyphen (-).</span></span> <span data-ttu-id="82261-116">Vous pouvez spécifier jusqu’à quatre valeurs FromTo, mais chacune d’elles doit être séparée de la valeur précédente par une virgule (,).</span><span class="sxs-lookup"><span data-stu-id="82261-116">Up to four FromTo values can be specified, but each must be separated from the previous value by a comma (,).</span></span> |



 

<span data-ttu-id="82261-117">Les valeurs suivantes sont correctes pour l’entrée de registre.</span><span class="sxs-lookup"><span data-stu-id="82261-117">The following are the correct values for the registry entry.</span></span>


```C++
932=F040-F9FC
936=A140-A7A0,AAA1-AFFE,F8A1-FEFE
949=C9A1-C9FE,FEA1-FEFE
950=8140-8DFE,8E40-A0FE,C6A1-C8FE,FA40-FEFE
Unicode=E000-F8FF
```



## <a name="related-topics"></a><span data-ttu-id="82261-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="82261-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82261-119">Entrées de Registre EUDC</span><span class="sxs-lookup"><span data-stu-id="82261-119">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="82261-120">EUDC</span><span class="sxs-lookup"><span data-stu-id="82261-120">EUDC</span></span>](eudc.md)
</dt> </dl>

 

 



