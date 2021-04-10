---
title: IAgentCharacter Play
description: IAgentCharacter Play
ms.assetid: a0158693-ff62-4da4-8b68-402e8d5b1c2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 996929271156254377f08b9fc41da3932aee9da4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029898"
---
# <a name="iagentcharacterplay"></a><span data-ttu-id="d8d63-103">IAgentCharacter ::P</span><span class="sxs-lookup"><span data-stu-id="d8d63-103">IAgentCharacter::Play</span></span>

<span data-ttu-id="d8d63-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d8d63-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Play(
   BSTR bszAnimation,  // name of an animation
   long * pdwReqID     // address of request ID
);
```

<span data-ttu-id="d8d63-105">Lit l’animation spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d8d63-105">Plays the specified animation.</span></span>

-   <span data-ttu-id="d8d63-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="d8d63-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="d8d63-107">Lorsque la fonction retourne, *pdwReqID* contient l’ID de la demande.</span><span class="sxs-lookup"><span data-stu-id="d8d63-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="d8d63-108"><span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*bszAnimation*</span><span class="sxs-lookup"><span data-stu-id="d8d63-108"><span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*bszAnimation*</span></span>
</dt> <dd>

<span data-ttu-id="d8d63-109">Nom d’une animation.</span><span class="sxs-lookup"><span data-stu-id="d8d63-109">The name of an animation.</span></span>

</dd> <dt>

<span data-ttu-id="d8d63-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="d8d63-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="d8d63-111">Adresse d’une variable qui reçoit l’ID de demande **IAgentCharacter ::P** .</span><span class="sxs-lookup"><span data-stu-id="d8d63-111">Address of a variable that receives the **IAgentCharacter::Play** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="d8d63-112">Le nom d’une animation est défini lorsque le caractère est compilé à l’aide de l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="d8d63-112">An animation's name is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="d8d63-113">Avant de lire l’animation spécifiée, le serveur tente de lire l’animation de **retour** pour l’animation précédente (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="d8d63-113">Before playing the specified animation, the server attempts to play the **Return** animation for the previous animation (if one has been assigned).</span></span>

<span data-ttu-id="d8d63-114">Lorsque les données d’animation d’un caractère sont stockées sur l’ordinateur local de l’utilisateur, vous pouvez utiliser la méthode **IAgentCharacter ::P** et spécifier le nom de l’animation.</span><span class="sxs-lookup"><span data-stu-id="d8d63-114">When a character's animation data is stored on the user's local machine, you can use the **IAgentCharacter::Play** method and specify the name of the animation.</span></span> <span data-ttu-id="d8d63-115">Lorsque vous utilisez le protocole HTTP pour accéder aux données d’animation, utilisez la méthode [**Prepare**](iagentcharacter--prepare.md) pour garantir la disponibilité de l’animation avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="d8d63-115">When using the HTTP protocol to access animation data, use the [**Prepare**](iagentcharacter--prepare.md) method to ensure the availability of the animation before calling this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8d63-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8d63-116">See Also</span></span>

[<span data-ttu-id="d8d63-117">**IAgentCharacter ::P la même parenthèse**</span><span class="sxs-lookup"><span data-stu-id="d8d63-117">**IAgentCharacter::Prepare**</span></span>](iagentcharacter--prepare.md)


 

 




