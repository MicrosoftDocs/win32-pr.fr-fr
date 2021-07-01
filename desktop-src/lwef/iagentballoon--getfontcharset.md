---
title: IAgentBalloon GetFontCharSet
description: IAgentBalloon GetFontCharSet
ms.assetid: 1ab5767a-31e3-449c-b242-f20b11336ca0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f809fbd83e44259c96184c9f364a85151ec9ddde
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120404"
---
# <a name="iagentballoongetfontcharset"></a><span data-ttu-id="879d8-103">IAgentBalloon::GetFontCharSet</span><span class="sxs-lookup"><span data-stu-id="879d8-103">IAgentBalloon::GetFontCharSet</span></span>

<span data-ttu-id="879d8-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="879d8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontCharSet(
   short * psFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="879d8-105">Indique le jeu de caractères de la police affichée dans une bulle de mot.</span><span class="sxs-lookup"><span data-stu-id="879d8-105">Indicates the character set of the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="879d8-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="879d8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="879d8-107"><span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*</span><span class="sxs-lookup"><span data-stu-id="879d8-107"><span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="879d8-108">Adresse d’une valeur qui reçoit le jeu de caractères de la police.</span><span class="sxs-lookup"><span data-stu-id="879d8-108">The address of a value that receives the font's character set.</span></span> <span data-ttu-id="879d8-109">Voici quelques paramètres courants pour la valeur :</span><span class="sxs-lookup"><span data-stu-id="879d8-109">The following are some common settings for value:</span></span>



| <span data-ttu-id="879d8-110">Value</span><span class="sxs-lookup"><span data-stu-id="879d8-110">Value</span></span>    | <span data-ttu-id="879d8-111">Jeu de caractères</span><span class="sxs-lookup"><span data-stu-id="879d8-111">Character set</span></span>                                                                                       |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="879d8-112">0</span><span class="sxs-lookup"><span data-stu-id="879d8-112">0</span></span>   | <span data-ttu-id="879d8-113">Caractères Windows standard (ANSI).</span><span class="sxs-lookup"><span data-stu-id="879d8-113">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="879d8-114">1</span><span class="sxs-lookup"><span data-stu-id="879d8-114">1</span></span>   | <span data-ttu-id="879d8-115">Jeu de caractères par défaut.</span><span class="sxs-lookup"><span data-stu-id="879d8-115">Default character set.</span></span>                                                                 |
| <span data-ttu-id="879d8-116">2</span><span class="sxs-lookup"><span data-stu-id="879d8-116">2</span></span>   | <span data-ttu-id="879d8-117">Jeu de caractères de symbole.</span><span class="sxs-lookup"><span data-stu-id="879d8-117">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="879d8-118">128</span><span class="sxs-lookup"><span data-stu-id="879d8-118">128</span></span> | <span data-ttu-id="879d8-119">Jeu de caractères codés sur deux octets (DBCS) propre à la version japonaise de Windows.</span><span class="sxs-lookup"><span data-stu-id="879d8-119">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="879d8-120">129</span><span class="sxs-lookup"><span data-stu-id="879d8-120">129</span></span> | <span data-ttu-id="879d8-121">Jeu de caractères codés sur deux octets (DBCS) propre à la version coréenne de Windows.</span><span class="sxs-lookup"><span data-stu-id="879d8-121">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="879d8-122">134</span><span class="sxs-lookup"><span data-stu-id="879d8-122">134</span></span> | <span data-ttu-id="879d8-123">Jeu de caractères codés sur deux octets (DBCS) propre à la version de Windows en chinois simplifié.</span><span class="sxs-lookup"><span data-stu-id="879d8-123">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="879d8-124">136</span><span class="sxs-lookup"><span data-stu-id="879d8-124">136</span></span> | <span data-ttu-id="879d8-125">Jeu de caractères codés sur deux octets (DBCS) propre à la version de Windows en chinois traditionnel.</span><span class="sxs-lookup"><span data-stu-id="879d8-125">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="879d8-126">255</span><span class="sxs-lookup"><span data-stu-id="879d8-126">255</span></span> | <span data-ttu-id="879d8-127">Les caractères étendus sont généralement affichés par les applications MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="879d8-127">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="879d8-128">Pour les autres valeurs de jeu de caractères, consultez la documentation du kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="879d8-128">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="879d8-129">Le jeu de caractères par défaut utilisé dans la bulle de texte d’un caractère est défini dans l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="879d8-129">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="879d8-130">Vous pouvez le modifier à l’aide de [**IAgentBalloon :: SetFontCharSet**](iagentballoon--setfontcharset.md).</span><span class="sxs-lookup"><span data-stu-id="879d8-130">You can change it using [**IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md).</span></span> <span data-ttu-id="879d8-131">Toutefois, l’utilisateur peut remplacer le paramètre de jeu de caractères pour tous les caractères à l’aide de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="879d8-131">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="879d8-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="879d8-132">See Also</span></span>

[<span data-ttu-id="879d8-133">**IAgentBalloon::SetFontCharSet**</span><span class="sxs-lookup"><span data-stu-id="879d8-133">**IAgentBalloon::SetFontCharSet**</span></span>](iagentballoon--setfontcharset.md)


 

 




