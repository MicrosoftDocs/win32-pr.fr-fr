---
description: La clé de Registre EUDCCodeRange définit les plages de codes de caractères définis par l’utilisateur final (EUDC) pour diverses pages de codes (jeux de caractères).
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: EUDCCodeRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8619bce02f4ca66fa9b4ce6d25aff0c5a3e66f96
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120674"
---
# <a name="eudccoderange"></a><span data-ttu-id="18840-103">EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="18840-103">EUDCCodeRange</span></span>

<span data-ttu-id="18840-104">La clé de Registre EUDCCodeRange définit les plages de codes de [caractères définis par l’utilisateur final (EUDC)](end-user-defined-characters.md) pour diverses pages de codes (jeux de caractères).</span><span class="sxs-lookup"><span data-stu-id="18840-104">The EUDCCodeRange registry key defines [end-user-defined character (EUDC)](end-user-defined-characters.md) code ranges for various code pages (character sets).</span></span> <span data-ttu-id="18840-105">Elle est utilisée uniquement par les outils qui créent des EUDCs et n’est pas d’une préoccupation directe pour les utilisateurs EUDC.</span><span class="sxs-lookup"><span data-stu-id="18840-105">It is used only by tools that create EUDCs, and is not of direct concern to EUDC users.</span></span> <span data-ttu-id="18840-106">Cette clé de registre a l’emplacement de Registre suivant :</span><span class="sxs-lookup"><span data-stu-id="18840-106">This registry key has the following registry location:</span></span>

<span data-ttu-id="18840-107">HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ contrôler \\ la \\ page de codes nls \\ EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="18840-107">HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\NLS\\CodePage\\EUDCCodeRange</span></span>

<span data-ttu-id="18840-108">Le format est le suivant :</span><span class="sxs-lookup"><span data-stu-id="18840-108">The format is:</span></span>

<span data-ttu-id="18840-109">EUDCCodeRange CodePage = FromTo \[ , FromTo\]</span><span class="sxs-lookup"><span data-stu-id="18840-109">EUDCCodeRange CodePage=FromTo\[,FromTo\]</span></span>

<span data-ttu-id="18840-110">où :</span><span class="sxs-lookup"><span data-stu-id="18840-110">where:</span></span>



| <span data-ttu-id="18840-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="18840-111">Value</span></span>         | <span data-ttu-id="18840-112">Description</span><span class="sxs-lookup"><span data-stu-id="18840-112">Description</span></span>                                                                                                                                                                                                         |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18840-113">CodePage</span><span class="sxs-lookup"><span data-stu-id="18840-113">CodePage</span></span> | <span data-ttu-id="18840-114">L’une des chaînes « 932 » (japonais), « 936 » (chinois simplifié), « 949 » (coréen), « 950 » (chinois traditionnel) ou « Unicode » (Unicode).</span><span class="sxs-lookup"><span data-stu-id="18840-114">One of the strings "932" (Japanese), "936" (Simplified Chinese), "949" (Korean), "950" (Traditional Chinese), or "Unicode" (Unicode).</span></span> <span data-ttu-id="18840-115">Aucune autre valeur n’est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="18840-115">No other values are supported.</span></span>                                     |
| <span data-ttu-id="18840-116">FromTo</span><span class="sxs-lookup"><span data-stu-id="18840-116">FromTo</span></span>   | <span data-ttu-id="18840-117">Valeur de chaîne composée d’une paire de valeurs hexadécimales à 4 chiffres séparés par un trait d’Union (-).</span><span class="sxs-lookup"><span data-stu-id="18840-117">String value consisting of a pair of 4-digit hexadecimal values separated by a hyphen (-).</span></span> <span data-ttu-id="18840-118">Vous pouvez spécifier jusqu’à quatre valeurs FromTo, mais chacune d’elles doit être séparée de la valeur précédente par une virgule (,).</span><span class="sxs-lookup"><span data-stu-id="18840-118">Up to four FromTo values can be specified, but each must be separated from the previous value by a comma (,).</span></span> |



 

<span data-ttu-id="18840-119">Les valeurs suivantes sont correctes pour l’entrée de registre.</span><span class="sxs-lookup"><span data-stu-id="18840-119">The following are the correct values for the registry entry.</span></span>


```C++
932=F040-F9FC
936=A140-A7A0,AAA1-AFFE,F8A1-FEFE
949=C9A1-C9FE,FEA1-FEFE
950=8140-8DFE,8E40-A0FE,C6A1-C8FE,FA40-FEFE
Unicode=E000-F8FF
```



## <a name="related-topics"></a><span data-ttu-id="18840-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="18840-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18840-121">Entrées de Registre EUDC</span><span class="sxs-lookup"><span data-stu-id="18840-121">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="18840-122">EUDC</span><span class="sxs-lookup"><span data-stu-id="18840-122">EUDC</span></span>](eudc.md)
</dt> </dl>

 

 



