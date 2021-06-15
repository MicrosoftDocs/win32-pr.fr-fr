---
title: Propriété FontName (objet Balloon)
description: En savoir plus sur la propriété d’objet info-bulle FontName. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: a84a19a4-9e0e-4736-b401-286e6618bc19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c47e14935f913ce81b5faed5a49c3d731a73532f
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068265"
---
# <a name="fontname-property-balloon-object"></a><span data-ttu-id="8b075-104">Propriété FontName (objet Balloon)</span><span class="sxs-lookup"><span data-stu-id="8b075-104">FontName Property (Balloon Object)</span></span>

<span data-ttu-id="8b075-105">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8b075-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8b075-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="8b075-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8b075-107">Retourne ou définit la police utilisée dans le mot-bulle pour le caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="8b075-107">Returns or sets the font used in the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="8b075-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="8b075-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8b075-109">\*agents. \***caractères («**_CharacterID_\*_»). Police Balloon. FontName_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="8b075-109">*agent.\***Characters("**_CharacterID_*_").Balloon.FontName_\* \[ = *font*\]</span></span>



| <span data-ttu-id="8b075-110">Partie</span><span class="sxs-lookup"><span data-stu-id="8b075-110">Part</span></span>   | <span data-ttu-id="8b075-111">Description</span><span class="sxs-lookup"><span data-stu-id="8b075-111">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="8b075-112">*son*</span><span class="sxs-lookup"><span data-stu-id="8b075-112">*font*</span></span> | <span data-ttu-id="8b075-113">Valeur de chaîne correspondant au nom de la police.</span><span class="sxs-lookup"><span data-stu-id="8b075-113">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b075-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8b075-114">Remarks</span></span>

<span data-ttu-id="8b075-115">La propriété [**FontName**](fontname-property.md) définit la police utilisée pour afficher le texte de la fenêtre de la bulle de texte d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="8b075-115">The [**FontName**](fontname-property.md) property defines the font used to display text in the word balloon window of a string.</span></span> <span data-ttu-id="8b075-116">La valeur par défaut des paramètres de police de la bulle de texte d’un caractère est définie dans l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="8b075-116">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="8b075-117">En outre, l’utilisateur peut remplacer les paramètres de police pour tous les caractères de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8b075-117">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="8b075-118">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="8b075-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="8b075-119">Si vous utilisez un caractère que vous n’avez pas compilé, vérifiez les propriétés [**FontName**](fontname-property.md) et [**FontCharSet**](fontcharset-property.md) pour déterminer s’ils sont appropriés pour vos paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="8b075-119">If you are using a character that you did not compile, check the [**FontName**](fontname-property.md) and [**FontCharSet**](fontcharset-property.md) properties for the character to determine whether they are appropriate for your locale.</span></span> <span data-ttu-id="8b075-120">Vous devrez peut-être définir ces valeurs avant d’utiliser la méthode [**Speak**](speak-method.md) pour garantir l’affichage du texte approprié dans la bulle.</span><span class="sxs-lookup"><span data-stu-id="8b075-120">You may need to set these values before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

 

 




