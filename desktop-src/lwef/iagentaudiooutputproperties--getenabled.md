---
title: IAgentAudioOutputProperties GetEnabled
description: IAgentAudioOutputProperties GetEnabled
ms.assetid: a1e555e1-98f1-4a3d-b6ba-4cd35348db2b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e86b82c720971ae1e14ee294e6d097fd35ca80a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029168"
---
# <a name="iagentaudiooutputpropertiesgetenabled"></a><span data-ttu-id="a1fac-103">IAgentAudioOutputProperties :: GetEnabled</span><span class="sxs-lookup"><span data-stu-id="a1fac-103">IAgentAudioOutputProperties::GetEnabled</span></span>

<span data-ttu-id="a1fac-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a1fac-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
long * pbEnabled  // address of variable for audio output Enabled setting 
);                      
```

<span data-ttu-id="a1fac-105">Récupère une valeur indiquant si la sortie vocale des caractères est activée.</span><span class="sxs-lookup"><span data-stu-id="a1fac-105">Retrieves a value indicating whether character speech output is enabled.</span></span>

-   <span data-ttu-id="a1fac-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="a1fac-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a1fac-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span><span class="sxs-lookup"><span data-stu-id="a1fac-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="a1fac-108">Adresse d’une variable qui reçoit la **valeur true** si la sortie vocale est actuellement activée et **false** si elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="a1fac-108">Address of a variable that receives **True** if the speech output is currently enabled and **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="a1fac-109">Étant donné que ce paramètre affecte la sortie orale (TTS et fichier audio) pour tous les caractères, seul l’utilisateur peut modifier cette propriété dans la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a1fac-109">Because this setting affects spoken output (TTS and sound file) for all characters, only the user can change this property in the Microsoft Agent property sheet.</span></span>

 

 




