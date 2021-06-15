---
title: FontSize, propriété (objet Commands)
description: En savoir plus sur la propriété de l’objet FontSize Commands. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: a1113a3a-5da8-4077-8565-168963c503d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d4e32bf57d129e7bf1d7b45f97846a1fe90756
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068206"
---
# <a name="fontsize-property-commands-object"></a><span data-ttu-id="fdc53-104">FontSize, propriété (objet Commands)</span><span class="sxs-lookup"><span data-stu-id="fdc53-104">FontSize Property (Commands Object)</span></span>

<span data-ttu-id="fdc53-105">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fdc53-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="fdc53-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="fdc53-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="fdc53-107">Retourne ou définit la taille de police utilisée dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="fdc53-107">Returns or sets the font size used in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="fdc53-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="fdc53-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="fdc53-109">\*agents. \***caractères («**_CharacterID_\*_»). Points de commande. FontSize_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="fdc53-109">*agent.\***Characters("**_CharacterID_*_").Commands.FontSize_\* \[ = *Points*\]</span></span>



| <span data-ttu-id="fdc53-110">Partie</span><span class="sxs-lookup"><span data-stu-id="fdc53-110">Part</span></span>     | <span data-ttu-id="fdc53-111">Description</span><span class="sxs-lookup"><span data-stu-id="fdc53-111">Description</span></span>                                              |
|----------|----------------------------------------------------------|
| <span data-ttu-id="fdc53-112">*Moments*</span><span class="sxs-lookup"><span data-stu-id="fdc53-112">*Points*</span></span> | <span data-ttu-id="fdc53-113">Valeur entière de type long spécifiant la taille de police en points.</span><span class="sxs-lookup"><span data-stu-id="fdc53-113">A Long integer value specifying the font size in points.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fdc53-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="fdc53-114">Remarks</span></span>

<span data-ttu-id="fdc53-115">La propriété **FontSize** définit la taille en points de la police utilisée pour afficher le texte dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="fdc53-115">The **FontSize** property defines the point size of the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="fdc53-116">La valeur par défaut du paramètre de police est basée sur le paramètre de police de menu du paramètre **LanguageID** du caractère ou, si cela n’est pas défini, le paramètre de langue par défaut de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fdc53-116">The default value for the font setting is based on the menu font setting for the character's **LanguageID** setting, or—if that's not set—the user default language setting.</span></span>

<span data-ttu-id="fdc53-117">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="fdc53-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 




