---
title: IAgentAudioOutputProperties GetUsingSoundEffects
description: IAgentAudioOutputProperties GetUsingSoundEffects
ms.assetid: 3ccf90b1-a2aa-482a-9f96-85d735532c11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e83314acfc67ce8bea4a0f0d305f6d5d490a92e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673293"
---
# <a name="iagentaudiooutputpropertiesgetusingsoundeffects"></a><span data-ttu-id="29901-103">IAgentAudioOutputProperties::GetUsingSoundEffects</span><span class="sxs-lookup"><span data-stu-id="29901-103">IAgentAudioOutputProperties::GetUsingSoundEffects</span></span>

<span data-ttu-id="29901-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="29901-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetUsingSoundEffects(
long * pbUsingSoundEffects  // address of variable sound effects output 
);                          // setting 
```

<span data-ttu-id="29901-105">Récupère une valeur indiquant si la sortie des effets sonores est activée.</span><span class="sxs-lookup"><span data-stu-id="29901-105">Retrieves a value indicating whether sound effects output is enabled.</span></span>

-   <span data-ttu-id="29901-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="29901-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="29901-107"><span id="pbUsingSoundEffects"></span><span id="pbusingsoundeffects"></span><span id="PBUSINGSOUNDEFFECTS"></span>*pbUsingSoundEffects*</span><span class="sxs-lookup"><span data-stu-id="29901-107"><span id="pbUsingSoundEffects"></span><span id="pbusingsoundeffects"></span><span id="PBUSINGSOUNDEFFECTS"></span>*pbUsingSoundEffects*</span></span>
</dt> <dd>

<span data-ttu-id="29901-108">Adresse d’une variable qui reçoit la **valeur true** si la sortie des effets sonores est actuellement activée et **false** si elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="29901-108">Address of a variable that receives **True** if the sound effects output is currently enabled and **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="29901-109">Les effets sonores de l’animation d’un caractère sont attribués dans l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="29901-109">Sound effects for a character's animation are assigned in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="29901-110">Étant donné que ce paramètre affecte la sortie des effets sonores pour tous les caractères, seul l’utilisateur peut modifier cette propriété dans la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="29901-110">Because this setting affects sound effects output for all characters, only the user can change this property in the Microsoft Agent property sheet.</span></span>

 

 




