---
title: Visible, propriété (objet Balloon)
description: En savoir plus sur la propriété visible de l’objet Balloon, qui retourne ou définit le paramètre visible pour le mot-bulle pour le caractère spécifié.
ms.assetid: cbda7f69-889a-45a0-9549-d27eddfcec57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ac587fa649f2a8ccb5ea83ddc077050a8548d2
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396324"
---
# <a name="visible-property-balloon-object"></a><span data-ttu-id="3d545-103">Visible, propriété (objet Balloon)</span><span class="sxs-lookup"><span data-stu-id="3d545-103">Visible Property (Balloon Object)</span></span>

<span data-ttu-id="3d545-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3d545-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3d545-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="3d545-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3d545-106">Retourne ou définit le paramètre visible pour le mot-bulle pour le caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="3d545-106">Returns or sets the visible setting for the word balloon for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="3d545-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="3d545-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="3d545-108">\*agent \***. Caractères (**"\* CharacterID \*" \* *).* \*  \[  =  *Valeur booléenne* Balloon. visible\]</span><span class="sxs-lookup"><span data-stu-id="3d545-108">*agent\***.Characters(**"* CharacterID *"\*\*).Balloon.Visible*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="3d545-109">Partie</span><span class="sxs-lookup"><span data-stu-id="3d545-109">Part</span></span>      | <span data-ttu-id="3d545-110">Description</span><span class="sxs-lookup"><span data-stu-id="3d545-110">Description</span></span>                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d545-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="3d545-111">*boolean*</span></span> | <span data-ttu-id="3d545-112">Expression booléenne spécifiant si la bulle de texte est visible.</span><span class="sxs-lookup"><span data-stu-id="3d545-112">A Boolean expression specifying whether the word balloon is visible.</span></span><br/> <span data-ttu-id="3d545-113">**True** La bulle est visible.</span><span class="sxs-lookup"><span data-stu-id="3d545-113">**True** The balloon is visible.</span></span><br/> <span data-ttu-id="3d545-114">**Valeur false** La bulle est masquée.</span><span class="sxs-lookup"><span data-stu-id="3d545-114">**False** The balloon is hidden.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d545-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="3d545-115">Remarks</span></span>

<span data-ttu-id="3d545-116">Si vous suivez un appel [**Speak**](speak-method.md) ou [**Song**](think-method.md) avec une instruction pour tenter de modifier la propriété de l’info-bulle, cela peut ne pas affecter l’état visible de l’info-bulle, car l’appel **Speak** ou **Song** est mis en file d’attente, mais pas l’appel de la définition de l’état visible de l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="3d545-116">If you follow a [**Speak**](speak-method.md) or [**Think**](think-method.md) call with a statement to attempt to change the balloon's property, it may not affect the balloon's Visible state because the **Speak** or **Think** call gets queued, but the call setting the balloon's visible state does not.</span></span> <span data-ttu-id="3d545-117">Par conséquent, définissez cette valeur uniquement quand aucun appel **Speak** ou **Song** n’est présent dans la file d’attente du caractère.</span><span class="sxs-lookup"><span data-stu-id="3d545-117">Therefore, only set this value when no **Speak** or **Think** calls are in the character's queue.</span></span>

<span data-ttu-id="3d545-118">Si vous tentez de définir cette propriété alors que le caractère parle, bouge ou est glissé, le paramètre de la propriété ne prend pas effet tant que l’opération précédente n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="3d545-118">If you attempt to set this property while the character is speaking, moving, or being dragged, the property setting does not take effect until the preceding operation is completed.</span></span>

<span data-ttu-id="3d545-119">L’appel des méthodes [**Speak**](speak-method.md) et [**Song**](think-method.md) rend automatiquement la bulle visible, en affectant la **valeur true** à la propriété [**visible**](visible-property.md) .</span><span class="sxs-lookup"><span data-stu-id="3d545-119">Calling the [**Speak**](speak-method.md) and [**Think**](think-method.md) methods automatically makes the balloon visible, setting the [**Visible**](visible-property.md) property to **True**.</span></span> <span data-ttu-id="3d545-120">Si la propriété de masquage automatique de l’info-bulle du caractère est activée, l’info-bulle est automatiquement masquée une fois que le texte de sortie est prononcé.</span><span class="sxs-lookup"><span data-stu-id="3d545-120">If the character's balloon AutoHide property is enabled, the balloon is automatically hidden after the output text is spoken.</span></span> <span data-ttu-id="3d545-121">Le fait de cliquer ou de faire glisser un caractère qui n’est pas en train de parler masque également automatiquement l’info-bulle, même si son paramètre Masquer automatiquement est désactivé.</span><span class="sxs-lookup"><span data-stu-id="3d545-121">Clicking or dragging a character that is not currently speaking also automatically hides the balloon even if its AutoHide setting is disabled.</span></span> <span data-ttu-id="3d545-122">Vous pouvez modifier le paramètre de masquage automatique du caractère à l’aide de la propriété [**style**](style-property.md) de l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="3d545-122">You can change the character's AutoHide setting using the balloon's [**Style**](style-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="3d545-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d545-123">See Also</span></span>

[<span data-ttu-id="3d545-124">**Propriété style**</span><span class="sxs-lookup"><span data-stu-id="3d545-124">**Style property**</span></span>](style-property.md)


 

 





