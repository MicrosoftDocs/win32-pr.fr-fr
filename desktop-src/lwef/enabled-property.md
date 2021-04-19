---
title: Propriété Enabled (objet Balloon)
description: Propriété activée
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07179390b183e98a5eaccb2dfdb4405525d7d26e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106509489"
---
# <a name="enabled-property-balloon-object"></a><span data-ttu-id="fee80-103">Propriété Enabled (objet Balloon)</span><span class="sxs-lookup"><span data-stu-id="fee80-103">Enabled Property (Balloon Object)</span></span>

<span data-ttu-id="fee80-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fee80-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="fee80-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="fee80-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="fee80-106">Retourne une valeur indiquant si la bulle de texte est activée pour le caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="fee80-106">Returns whether the word balloon is enabled for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="fee80-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="fee80-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="fee80-108">\*agent \***. Caractères («**_CharacterID_*_»). Balloon. activé_*</span><span class="sxs-lookup"><span data-stu-id="fee80-108">*agent\***.Characters ("**_CharacterID_*_").Balloon.Enabled_\*</span></span>



| <span data-ttu-id="fee80-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="fee80-109">Value</span></span>     | <span data-ttu-id="fee80-110">Description</span><span class="sxs-lookup"><span data-stu-id="fee80-110">Description</span></span>              |
|-----------|--------------------------|
| <span data-ttu-id="fee80-111">**True**</span><span class="sxs-lookup"><span data-stu-id="fee80-111">**True**</span></span>  | <span data-ttu-id="fee80-112">La bulle est activée.</span><span class="sxs-lookup"><span data-stu-id="fee80-112">The balloon is enabled.</span></span>  |
| <span data-ttu-id="fee80-113">**False**</span><span class="sxs-lookup"><span data-stu-id="fee80-113">**False**</span></span> | <span data-ttu-id="fee80-114">L’info-bulle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="fee80-114">The balloon is disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fee80-115">Notes</span><span class="sxs-lookup"><span data-stu-id="fee80-115">Remarks</span></span>

<span data-ttu-id="fee80-116">La propriété **Enabled** retourne une valeur booléenne qui spécifie si la bulle est activée.</span><span class="sxs-lookup"><span data-stu-id="fee80-116">The **Enabled** property returns a Boolean value specifying whether the balloon is enabled.</span></span> <span data-ttu-id="fee80-117">L’État par défaut de la bulle de texte est défini dans le cadre de la définition d’un caractère lorsque le caractère est compilé dans l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="fee80-117">The word balloon default state is set as part of a character's definition when the character is compiled in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="fee80-118">Si un caractère est défini pour ne pas prendre en charge la bulle de mot, cette propriété aura toujours la **valeur false** pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="fee80-118">If a character is defined to not support the word balloon, this property will always be **False** for the character.</span></span>

 

 




