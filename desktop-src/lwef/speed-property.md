---
title: Speed, propriété
description: Speed, propriété
ms.assetid: 43d0480b-d3a5-4992-a2a5-80eba37221e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24738ac17d7efac45f2aefe7e4beb5ec018915a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106543402"
---
# <a name="speed-property"></a><span data-ttu-id="525c9-103">Speed, propriété</span><span class="sxs-lookup"><span data-stu-id="525c9-103">Speed Property</span></span>

<span data-ttu-id="525c9-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="525c9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="525c9-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="525c9-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="525c9-106">Retourne un entier long qui spécifie la vitesse actuelle de la sortie vocale du caractère.</span><span class="sxs-lookup"><span data-stu-id="525c9-106">Returns a Long integer that specifies the current speed of the character's speech output.</span></span>

</dd> <dt>

<span data-ttu-id="525c9-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="525c9-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="525c9-108">*agent ***. Caractères («*** CharacterID \* \* * »). Temps**</span><span class="sxs-lookup"><span data-stu-id="525c9-108">*agent ***.Characters ("*** CharacterID\*\*\*").Speed*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="525c9-109">Notes</span><span class="sxs-lookup"><span data-stu-id="525c9-109">Remarks</span></span>

<span data-ttu-id="525c9-110">Cette propriété retourne le paramètre de vitesse de sortie en cours pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="525c9-110">This property returns the current speaking output speed setting for the character.</span></span> <span data-ttu-id="525c9-111">Pour les caractères utilisant la sortie TTS, la propriété retourne le paramètre de sortie TTS réel pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="525c9-111">For characters using TTS output, the property returns the actual TTS output setting for the character.</span></span> <span data-ttu-id="525c9-112">Si TTS n’est pas activé ou que le caractère ne prend pas en charge la sortie TTS, le paramètre reflète le paramètre utilisateur pour la vitesse de sortie.</span><span class="sxs-lookup"><span data-stu-id="525c9-112">If TTS is not enabled or the character does not support TTS output, the setting reflects the user setting for output speed.</span></span>

<span data-ttu-id="525c9-113">Bien que votre application ne puisse pas écrire cette valeur, vous pouvez inclure des balises **SPD** (vitesse) dans votre texte de sortie qui accélèrent temporairement la sortie d’une énoncé particulière.</span><span class="sxs-lookup"><span data-stu-id="525c9-113">Although your application cannot write this value, you can include **Spd** (speed) tags in your output text that will temporarily speed up the output for a particular utterance.</span></span> <span data-ttu-id="525c9-114">Toutefois, l’utilisation de la balise **SPD** pour modifier la sortie orale du caractère n’affecte pas le paramètre de propriété **Speed** .</span><span class="sxs-lookup"><span data-stu-id="525c9-114">However, using the **Spd** tag to change the character's spoken output does not affect the **Speed** property setting.</span></span> <span data-ttu-id="525c9-115">Pour plus d’informations, consultez [balises de sortie vocale](microsoft-agent-speech-output-tags.md).</span><span class="sxs-lookup"><span data-stu-id="525c9-115">For further information, see [Speech Output Tags](microsoft-agent-speech-output-tags.md).</span></span>

 

 




