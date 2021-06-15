---
title: Propriété FontName (objet Commands)
description: En savoir plus sur la propriété de l’objet Commands FontName. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 739fceae4e73788f408306f6af08713173c99843
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068255"
---
# <a name="fontname-property-commands-object"></a><span data-ttu-id="6f689-104">Propriété FontName (objet Commands)</span><span class="sxs-lookup"><span data-stu-id="6f689-104">FontName Property (Commands Object)</span></span>

<span data-ttu-id="6f689-105">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6f689-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="6f689-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="6f689-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="6f689-107">Retourne ou définit la police utilisée dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="6f689-107">Returns or sets the font used in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="6f689-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="6f689-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="6f689-109">\*agents. \***caractères («**_CharacterID_\*_»). Police Commands. FontName_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="6f689-109">*agent.\***Characters("**_CharacterID_*_").Commands.FontName_\* \[ = *Font*\]</span></span>



| <span data-ttu-id="6f689-110">Partie</span><span class="sxs-lookup"><span data-stu-id="6f689-110">Part</span></span>   | <span data-ttu-id="6f689-111">Description</span><span class="sxs-lookup"><span data-stu-id="6f689-111">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="6f689-112">*Police*</span><span class="sxs-lookup"><span data-stu-id="6f689-112">*Font*</span></span> | <span data-ttu-id="6f689-113">Valeur de chaîne correspondant au nom de la police.</span><span class="sxs-lookup"><span data-stu-id="6f689-113">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f689-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6f689-114">Remarks</span></span>

<span data-ttu-id="6f689-115">La propriété **FontName** définit la police utilisée pour afficher le texte dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="6f689-115">The **FontName** property defines the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="6f689-116">La valeur par défaut du paramètre de police est basée sur le paramètre de police de menu pour le paramètre **LanguageID** du caractère, ou--si ce n’est pas le cas, le paramètre ID de langue par défaut de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6f689-116">The default value for the font setting is based on the menu font setting for the character's **LanguageID** setting, or -- if that's not set -- the user default language ID setting.</span></span>

<span data-ttu-id="6f689-117">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="6f689-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 




