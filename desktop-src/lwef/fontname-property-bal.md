---
title: Propriété FontName (objet Balloon)
description: FontName, propriété
ms.assetid: a84a19a4-9e0e-4736-b401-286e6618bc19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead06323b36e86dce36163769b329140279f240d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102733"
---
# <a name="fontname-property-balloon-object"></a><span data-ttu-id="9ec8a-103">Propriété FontName (objet Balloon)</span><span class="sxs-lookup"><span data-stu-id="9ec8a-103">FontName Property (Balloon Object)</span></span>

<span data-ttu-id="9ec8a-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9ec8a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9ec8a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="9ec8a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9ec8a-106">Retourne ou définit la police utilisée dans le mot-bulle pour le caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="9ec8a-106">Returns or sets the font used in the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="9ec8a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="9ec8a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9ec8a-108">\*agents. \***caractères («**_CharacterID_\*_»). Police Balloon. FontName_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="9ec8a-108">*agent.\***Characters("**_CharacterID_*_").Balloon.FontName_\* \[ = *font*\]</span></span>



| <span data-ttu-id="9ec8a-109">Partie</span><span class="sxs-lookup"><span data-stu-id="9ec8a-109">Part</span></span>   | <span data-ttu-id="9ec8a-110">Description</span><span class="sxs-lookup"><span data-stu-id="9ec8a-110">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="9ec8a-111">*son*</span><span class="sxs-lookup"><span data-stu-id="9ec8a-111">*font*</span></span> | <span data-ttu-id="9ec8a-112">Valeur de chaîne correspondant au nom de la police.</span><span class="sxs-lookup"><span data-stu-id="9ec8a-112">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ec8a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9ec8a-113">Remarks</span></span>

<span data-ttu-id="9ec8a-114">La propriété [**FontName**](fontname-property.md) définit la police utilisée pour afficher le texte de la fenêtre de la bulle de texte d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="9ec8a-114">The [**FontName**](fontname-property.md) property defines the font used to display text in the word balloon window of a string.</span></span> <span data-ttu-id="9ec8a-115">La valeur par défaut des paramètres de police de la bulle de texte d’un caractère est définie dans l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="9ec8a-115">The default value for the font settings of a character's word balloon are set in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="9ec8a-116">En outre, l’utilisateur peut remplacer les paramètres de police pour tous les caractères de la feuille de propriétés de l’agent Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9ec8a-116">In addition, the user can override font settings for all characters in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="9ec8a-117">Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="9ec8a-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="9ec8a-118">Si vous utilisez un caractère que vous n’avez pas compilé, vérifiez les propriétés [**FontName**](fontname-property.md) et [**FontCharSet**](fontcharset-property.md) pour déterminer s’ils sont appropriés pour vos paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="9ec8a-118">If you are using a character that you did not compile, check the [**FontName**](fontname-property.md) and [**FontCharSet**](fontcharset-property.md) properties for the character to determine whether they are appropriate for your locale.</span></span> <span data-ttu-id="9ec8a-119">Vous devrez peut-être définir ces valeurs avant d’utiliser la méthode [**Speak**](speak-method.md) pour garantir l’affichage du texte approprié dans la bulle.</span><span class="sxs-lookup"><span data-stu-id="9ec8a-119">You may need to set these values before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

 

 




