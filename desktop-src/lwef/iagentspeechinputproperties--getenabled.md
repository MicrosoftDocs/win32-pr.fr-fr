---
title: IAgentSpeechInputProperties GetEnabled
description: IAgentSpeechInputProperties GetEnabled
ms.assetid: 5731f9ad-eb2e-4a79-a724-b3c263235c8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c95613398bf79b2446d2bc572864f69ad1ad92ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103670870"
---
# <a name="iagentspeechinputpropertiesgetenabled"></a><span data-ttu-id="4ec1e-103">IAgentSpeechInputProperties :: GetEnabled</span><span class="sxs-lookup"><span data-stu-id="4ec1e-103">IAgentSpeechInputProperties::GetEnabled</span></span>

<span data-ttu-id="4ec1e-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4ec1e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
   long * pbEnabled  // address of variable for speech recognition engine 
);                   // Enabled setting
```

<span data-ttu-id="4ec1e-105">Récupère une valeur indiquant si le moteur de reconnaissance vocale installé est activé.</span><span class="sxs-lookup"><span data-stu-id="4ec1e-105">Retrieves a value indicating whether the installed speech recognition engine is enabled.</span></span>

-   <span data-ttu-id="4ec1e-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="4ec1e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4ec1e-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span><span class="sxs-lookup"><span data-stu-id="4ec1e-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="4ec1e-108">Adresse d’une variable qui reçoit la **valeur true** si le moteur de reconnaissance vocale est actuellement activé et **false** s’il est désactivé.</span><span class="sxs-lookup"><span data-stu-id="4ec1e-108">Address of a variable that receives **True** if the speech engine is currently enabled and **False** if disabled.</span></span>

</dd> </dl>

 

 




