---
title: Description, propriété (fonctionnalités héritées de l’environnement Windows)
description: Description, propriété
ms.assetid: 81ac4bc7-ef0c-4e7c-b57e-acc4ad315515
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b4fb60b20a57f56a914c7e44ced957d91bf7085
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032192"
---
# <a name="description-property-legacy-windows-environment-features"></a><span data-ttu-id="356c8-103">Description, propriété (fonctionnalités héritées de l’environnement Windows)</span><span class="sxs-lookup"><span data-stu-id="356c8-103">Description Property (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="356c8-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="356c8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="356c8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="356c8-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="356c8-106">Retourne ou définit une chaîne qui spécifie la description du caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="356c8-106">Returns or sets a string that specifies the description for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="356c8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="356c8-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="356c8-108">*agent*. **Caractères («**_CharacterID_*_»)._* \[  =  *Chaîne* de description\]</span><span class="sxs-lookup"><span data-stu-id="356c8-108">*agent*.**Characters("**_CharacterID_*_").Description_* \[ = *string*\]</span></span>



| <span data-ttu-id="356c8-109">Partie</span><span class="sxs-lookup"><span data-stu-id="356c8-109">Part</span></span>     | <span data-ttu-id="356c8-110">Description</span><span class="sxs-lookup"><span data-stu-id="356c8-110">Description</span></span>                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="356c8-111">*string*</span><span class="sxs-lookup"><span data-stu-id="356c8-111">*string*</span></span> | <span data-ttu-id="356c8-112">Valeur de chaîne correspondant à la description du caractère (dans le paramètre de langue actuel).</span><span class="sxs-lookup"><span data-stu-id="356c8-112">A string value corresponding to the character's description (in the current language setting).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="356c8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="356c8-113">Remarks</span></span>

<span data-ttu-id="356c8-114">La **Description** d’un caractère peut dépendre du paramètre **LanguageID** du caractère.</span><span class="sxs-lookup"><span data-stu-id="356c8-114">A character's **Description** may depend on the character's **LanguageID** setting.</span></span> <span data-ttu-id="356c8-115">Le nom d’un caractère dans une langue peut être différent ou utiliser des caractères différents de ceux d’un autre langage.</span><span class="sxs-lookup"><span data-stu-id="356c8-115">A character's name in one language may be different or use different characters than in another.</span></span> <span data-ttu-id="356c8-116">La **Description** par défaut du caractère pour une langue spécifique est définie lorsque le caractère est compilé à l’aide de l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="356c8-116">The character's default **Description** for a specific language is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span>

> [!Note]  
> <span data-ttu-id="356c8-117">Le paramètre de propriété **Description** est facultatif et ne peut pas être fourni pour tous les caractères.</span><span class="sxs-lookup"><span data-stu-id="356c8-117">The **Description** property setting is optional and may not be supplied for all characters.</span></span>

 

 

 




