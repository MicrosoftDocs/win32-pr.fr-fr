---
title: Propriété Name (objet Characters)
description: Propriété Name
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e7b4a8872952cce0ae68445ec22a5599891674
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464055"
---
# <a name="name-property-characters-object"></a><span data-ttu-id="34ce1-103">Propriété Name (objet Characters)</span><span class="sxs-lookup"><span data-stu-id="34ce1-103">Name Property (Characters Object)</span></span>

<span data-ttu-id="34ce1-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="34ce1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="34ce1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="34ce1-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="34ce1-106">Retourne ou définit une chaîne qui spécifie le nom par défaut du caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="34ce1-106">Returns or sets a string that specifies the default name of the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="34ce1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="34ce1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="34ce1-108">\*agent \***. Caractères («**_CharacterID_\*_»)._ \*  \[  =  *Chaîne* de nom\]</span><span class="sxs-lookup"><span data-stu-id="34ce1-108">*agent\***.Characters ("**_CharacterID_*_").Name_\* \[ = *string*\]</span></span>



| <span data-ttu-id="34ce1-109">Partie</span><span class="sxs-lookup"><span data-stu-id="34ce1-109">Part</span></span>     | <span data-ttu-id="34ce1-110">Description</span><span class="sxs-lookup"><span data-stu-id="34ce1-110">Description</span></span>                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34ce1-111">*string*</span><span class="sxs-lookup"><span data-stu-id="34ce1-111">*string*</span></span> | <span data-ttu-id="34ce1-112">Valeur de chaîne correspondant au nom du caractère (dans le paramètre de langue actuel).</span><span class="sxs-lookup"><span data-stu-id="34ce1-112">A string value corresponding to the character's name (in the current language setting).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34ce1-113">Notes</span><span class="sxs-lookup"><span data-stu-id="34ce1-113">Remarks</span></span>

<span data-ttu-id="34ce1-114">Le **nom** d’un caractère peut dépendre du paramètre [**LanguageID**](languageid-property.md) du caractère.</span><span class="sxs-lookup"><span data-stu-id="34ce1-114">A character's **Name** may depend on the character's [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="34ce1-115">Le nom d’un caractère dans une langue peut être différent ou utiliser des caractères différents de ceux d’un autre langage.</span><span class="sxs-lookup"><span data-stu-id="34ce1-115">A character's name in one language may be different or use different characters than in another.</span></span> <span data-ttu-id="34ce1-116">Le **nom** par défaut du caractère pour une langue spécifique est défini lorsque le caractère est compilé à l’aide de l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="34ce1-116">The character's default **Name** for a specific language is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="34ce1-117">Évitez de renommer un caractère, surtout quand vous l’utilisez dans un scénario où d’autres applications clientes peuvent utiliser le même caractère.</span><span class="sxs-lookup"><span data-stu-id="34ce1-117">Avoid renaming a character, especially when using it in a scenario where other client applications may use the same character.</span></span> <span data-ttu-id="34ce1-118">En outre, l’agent utilise le **nom** du caractère pour créer automatiquement des commandes de masquage et d’indication du caractère.</span><span class="sxs-lookup"><span data-stu-id="34ce1-118">Also, Agent uses the character's **Name** to automatically create commands for hiding and showing the character.</span></span>

 

 




