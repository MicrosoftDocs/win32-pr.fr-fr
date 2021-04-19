---
title: IAgentCharacter GetTTSPitch
description: IAgentCharacter GetTTSPitch
ms.assetid: b21ae1f1-daf6-42e5-9c52-f28722180021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dff1bb7999795cf27e29a7d064dd500b47bb419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511046"
---
# <a name="iagentcharactergetttspitch"></a><span data-ttu-id="d36f8-103">IAgentCharacter::GetTTSPitch</span><span class="sxs-lookup"><span data-stu-id="d36f8-103">IAgentCharacter::GetTTSPitch</span></span>

<span data-ttu-id="d36f8-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d36f8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetTTSPitch(
   long * pdwPitch  // address of variable for character TTS pitch
);
```

<span data-ttu-id="d36f8-105">Récupère le paramètre de tonalité de sortie TTS du caractère.</span><span class="sxs-lookup"><span data-stu-id="d36f8-105">Retrieves the character's TTS output pitch setting.</span></span>

-   <span data-ttu-id="d36f8-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="d36f8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d36f8-107"><span id="pdwPitch"></span><span id="pdwpitch"></span><span id="PDWPITCH"></span>*pdwPitch*</span><span class="sxs-lookup"><span data-stu-id="d36f8-107"><span id="pdwPitch"></span><span id="pdwpitch"></span><span id="PDWPITCH"></span>*pdwPitch*</span></span>
</dt> <dd>

<span data-ttu-id="d36f8-108">Adresse d’une variable qui reçoit la valeur actuelle de l’espace de synthèse vocale du caractère en Hertz.</span><span class="sxs-lookup"><span data-stu-id="d36f8-108">Address of a variable that receives the character's current TTS pitch setting in Hertz.</span></span>

</dd> </dl>

<span data-ttu-id="d36f8-109">Bien que votre application ne puisse pas écrire cette valeur, vous pouvez inclure des balises de hauteur dans votre texte de sortie, ce qui augmentera temporairement le pas pour une énoncé particulière.</span><span class="sxs-lookup"><span data-stu-id="d36f8-109">Although your application cannot write this value, you can include pitch tags in your output text that will temporarily increase the pitch for a particular utterance.</span></span> <span data-ttu-id="d36f8-110">Cette méthode s’applique uniquement aux caractères configurés pour la sortie TTS.</span><span class="sxs-lookup"><span data-stu-id="d36f8-110">This method applies only to characters configured for TTS output.</span></span> <span data-ttu-id="d36f8-111">Si le moteur de synthèse vocale (TTS) n’est pas activé (ou installé) ou si le caractère ne prend pas en charge la sortie TTS, cette méthode retourne zéro (0).</span><span class="sxs-lookup"><span data-stu-id="d36f8-111">If the speech synthesis (TTS) engine is not enabled (or installed) or the character does not support TTS output, this method returns zero (0).</span></span>

 

 




