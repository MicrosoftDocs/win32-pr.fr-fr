---
title: IAgentCharacter MoveTo
description: IAgentCharacter MoveTo
ms.assetid: 4e24d2f8-1df2-47ca-a1e9-b9d29708207d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d1ba423dc637895216ff03e2adec2862bbf27d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031115"
---
# <a name="iagentcharactermoveto"></a><span data-ttu-id="4ab08-103">IAgentCharacter :: MoveTo</span><span class="sxs-lookup"><span data-stu-id="4ab08-103">IAgentCharacter::MoveTo</span></span>

<span data-ttu-id="4ab08-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4ab08-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT MoveTo(
   short x,         // x-coordinate of new location
   short y,         // y-coordinate of new location
   long lSpeed,     // speed to move the character
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="4ab08-105">Lit l’animation d’état **mobile** associée et déplace le cadre de caractère vers l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="4ab08-105">Plays the associated **Moving** state animation and moves the character frame to the specified location.</span></span>

-   <span data-ttu-id="4ab08-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="4ab08-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="4ab08-107">Lorsque la fonction retourne, cette variable contient l’ID de la demande.</span><span class="sxs-lookup"><span data-stu-id="4ab08-107">When the function returns, this variable contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="4ab08-108"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="4ab08-108"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="4ab08-109">Coordonnée x de la nouvelle position, en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="4ab08-109">The x-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="4ab08-110">L’emplacement d’un caractère est basé sur l’angle supérieur gauche de son cadre d’animation.</span><span class="sxs-lookup"><span data-stu-id="4ab08-110">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="4ab08-111"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="4ab08-111"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="4ab08-112">Coordonnée y de la nouvelle position, en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="4ab08-112">The y-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="4ab08-113">L’emplacement d’un caractère est basé sur l’angle supérieur gauche de son cadre d’animation.</span><span class="sxs-lookup"><span data-stu-id="4ab08-113">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="4ab08-114"><span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lSpeed*</span><span class="sxs-lookup"><span data-stu-id="4ab08-114"><span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="4ab08-115">Paramètre spécifiant, en millisecondes, la vitesse de déplacement du cadre du caractère.</span><span class="sxs-lookup"><span data-stu-id="4ab08-115">A parameter specifying in milliseconds how quickly the character's frame moves.</span></span> <span data-ttu-id="4ab08-116">La valeur recommandée est 1000.</span><span class="sxs-lookup"><span data-stu-id="4ab08-116">The recommended value is 1000.</span></span> <span data-ttu-id="4ab08-117">Si vous spécifiez zéro (0), le frame est déplacé sans qu’une animation ne soit lue.</span><span class="sxs-lookup"><span data-stu-id="4ab08-117">Specifying zero (0) moves the frame without playing an animation.</span></span>

</dd> <dt>

<span data-ttu-id="4ab08-118"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="4ab08-118"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="4ab08-119">Adresse d’une variable qui reçoit l’ID de requête [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) .</span><span class="sxs-lookup"><span data-stu-id="4ab08-119">Address of a variable that receives the [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="4ab08-120">Lorsque vous utilisez le protocole HTTP pour accéder aux données de caractères et d’animation, utilisez la méthode [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) pour garantir la disponibilité des animations d’état **mobile** avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4ab08-120">When using the HTTP protocol to access character and animation data, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the **Moving** state animations before calling this method.</span></span> <span data-ttu-id="4ab08-121">Même si l’animation n’est pas chargée, le serveur déplace toujours le frame.</span><span class="sxs-lookup"><span data-stu-id="4ab08-121">Even if the animation is not loaded, the server still moves the frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ab08-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ab08-122">See Also</span></span>

[<span data-ttu-id="4ab08-123">**IAgentCharacter :: SetPosition**</span><span class="sxs-lookup"><span data-stu-id="4ab08-123">**IAgentCharacter::SetPosition**</span></span>](iagentcharacter--setposition.md)


 

 