---
title: Propriété tonale
description: Propriété tonale
ms.assetid: 98b2ada3-93c6-4fa1-bf12-353eb229c30c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 998ee4bcf77878062425086d67066040f5d58421
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380395"
---
# <a name="pitch-property"></a><span data-ttu-id="f267a-103">Propriété tonale</span><span class="sxs-lookup"><span data-stu-id="f267a-103">Pitch Property</span></span>

<span data-ttu-id="f267a-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f267a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f267a-105"><span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="f267a-105"><span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Description**</span></span> 
</dt> <dd>

<span data-ttu-id="f267a-106">Retourne un entier long pour le paramètre de hauteur de la sortie vocale (TTS) du caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="f267a-106">Returns a Long integer for the specified character's speech output (TTS) pitch setting.</span></span>

</dd> <dt>

<span data-ttu-id="f267a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="f267a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f267a-108">*agent ***. Caractères («*** CharacterID \* \* * »). Donn**</span><span class="sxs-lookup"><span data-stu-id="f267a-108">*agent ***.Characters ("*** CharacterID\*\*\*").Pitch*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f267a-109">Notes</span><span class="sxs-lookup"><span data-stu-id="f267a-109">Remarks</span></span>

<span data-ttu-id="f267a-110">Cette propriété s’applique uniquement aux caractères configurés pour la sortie TTS.</span><span class="sxs-lookup"><span data-stu-id="f267a-110">This property applies only to characters configured for TTS output.</span></span> <span data-ttu-id="f267a-111">Si le caractère ne prend pas en charge la sortie TTS, cette propriété retourne la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="f267a-111">If the character does not support TTS output, this property returns zero (0).</span></span>

<span data-ttu-id="f267a-112">Bien que votre application ne puisse pas écrire cette valeur, vous pouvez inclure dans votre texte de sortie des balises **Pit** qui augmenteront temporairement le pas pour une énoncé particulière.</span><span class="sxs-lookup"><span data-stu-id="f267a-112">Although your application cannot write this value, you can include **Pit** (pitch) tags in your output text that will temporarily increase the pitch for a particular utterance.</span></span> <span data-ttu-id="f267a-113">Toutefois, l’utilisation de la balise **Pit** pour changer le pas de valeur ne modifie pas le paramètre **de propriété de** pas.</span><span class="sxs-lookup"><span data-stu-id="f267a-113">However, using the **Pit** tag to change the pitch will not change the **Pitch** property setting.</span></span> <span data-ttu-id="f267a-114">Pour plus d’informations, consultez [balises de sortie vocale](pit-tag.md).</span><span class="sxs-lookup"><span data-stu-id="f267a-114">For further information, see [Speech Output Tags](pit-tag.md).</span></span>

 

 




