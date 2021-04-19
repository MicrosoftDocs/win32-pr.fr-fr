---
title: IAgentBalloon SetFontCharSet
description: IAgentBalloon SetFontCharSet
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6202aa144d13c3c7435be03721a3f8fd4878b93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106517975"
---
# <a name="iagentballoonsetfontcharset"></a><span data-ttu-id="ae571-103">IAgentBalloon::SetFontCharSet</span><span class="sxs-lookup"><span data-stu-id="ae571-103">IAgentBalloon::SetFontCharSet</span></span>

<span data-ttu-id="ae571-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ae571-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontCharSet(
   short sFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="ae571-105">Définit le jeu de caractères de la police affichée dans la bulle de mot.</span><span class="sxs-lookup"><span data-stu-id="ae571-105">Sets the character set of the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="ae571-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="ae571-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ae571-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*</span><span class="sxs-lookup"><span data-stu-id="ae571-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="ae571-108">Jeu de caractères de la police.</span><span class="sxs-lookup"><span data-stu-id="ae571-108">The character set of the font.</span></span> <span data-ttu-id="ae571-109">Voici quelques paramètres courants pour la valeur :</span><span class="sxs-lookup"><span data-stu-id="ae571-109">The following are some common settings for value:</span></span>



|     |                                                                                        |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae571-110">0</span><span class="sxs-lookup"><span data-stu-id="ae571-110">0</span></span>   | <span data-ttu-id="ae571-111">Caractères Windows standard (ANSI).</span><span class="sxs-lookup"><span data-stu-id="ae571-111">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="ae571-112">1</span><span class="sxs-lookup"><span data-stu-id="ae571-112">1</span></span>   | <span data-ttu-id="ae571-113">Jeu de caractères par défaut.</span><span class="sxs-lookup"><span data-stu-id="ae571-113">Default character set.</span></span>                                                                 |
| <span data-ttu-id="ae571-114">2</span><span class="sxs-lookup"><span data-stu-id="ae571-114">2</span></span>   | <span data-ttu-id="ae571-115">Jeu de caractères de symbole.</span><span class="sxs-lookup"><span data-stu-id="ae571-115">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="ae571-116">128</span><span class="sxs-lookup"><span data-stu-id="ae571-116">128</span></span> | <span data-ttu-id="ae571-117">Jeu de caractères codés sur deux octets (DBCS) propre à la version japonaise de Windows.</span><span class="sxs-lookup"><span data-stu-id="ae571-117">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="ae571-118">129</span><span class="sxs-lookup"><span data-stu-id="ae571-118">129</span></span> | <span data-ttu-id="ae571-119">Jeu de caractères codés sur deux octets (DBCS) propre à la version coréenne de Windows.</span><span class="sxs-lookup"><span data-stu-id="ae571-119">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="ae571-120">134</span><span class="sxs-lookup"><span data-stu-id="ae571-120">134</span></span> | <span data-ttu-id="ae571-121">Jeu de caractères codés sur deux octets (DBCS) propre à la version de Windows en chinois simplifié.</span><span class="sxs-lookup"><span data-stu-id="ae571-121">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="ae571-122">136</span><span class="sxs-lookup"><span data-stu-id="ae571-122">136</span></span> | <span data-ttu-id="ae571-123">Jeu de caractères codés sur deux octets (DBCS) propre à la version de Windows en chinois traditionnel.</span><span class="sxs-lookup"><span data-stu-id="ae571-123">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="ae571-124">255</span><span class="sxs-lookup"><span data-stu-id="ae571-124">255</span></span> | <span data-ttu-id="ae571-125">Les caractères étendus sont généralement affichés par les applications MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="ae571-125">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="ae571-126">Pour les autres valeurs de jeu de caractères, consultez la documentation du kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="ae571-126">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="ae571-127">Le jeu de caractères par défaut utilisé dans la bulle de texte d’un caractère est défini dans l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="ae571-127">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="ae571-128">Vous pouvez le modifier avec [**IAgentBalloon :: SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**).</span><span class="sxs-lookup"><span data-stu-id="ae571-128">You can change it with [**IAgentBalloon::SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**).</span></span> <span data-ttu-id="ae571-129">Toutefois, l’utilisateur peut remplacer le paramètre de jeu de caractères pour tous les caractères à l’aide de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ae571-129">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="ae571-130">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="ae571-130">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae571-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae571-131">See Also</span></span>

[<span data-ttu-id="ae571-132">**IAgentBalloon::GetFontCharSet**</span><span class="sxs-lookup"><span data-stu-id="ae571-132">**IAgentBalloon::GetFontCharSet**</span></span>](iagentballoon--getfontcharset.md)


 

 




