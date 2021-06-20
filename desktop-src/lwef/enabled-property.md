---
title: Propriété Enabled (objet Balloon)
description: En savoir plus sur la propriété d’objet Balloon activée. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 602d39a9bef7713a92707d8a43050f04a3577b6d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407302"
---
# <a name="enabled-property-balloon-object"></a><span data-ttu-id="68a0e-104">Propriété Enabled (objet Balloon)</span><span class="sxs-lookup"><span data-stu-id="68a0e-104">Enabled Property (Balloon Object)</span></span>

<span data-ttu-id="68a0e-105">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="68a0e-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="68a0e-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="68a0e-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="68a0e-107">Retourne une valeur indiquant si la bulle de texte est activée pour le caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="68a0e-107">Returns whether the word balloon is enabled for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="68a0e-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="68a0e-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="68a0e-109">\*agent \***. Caractères («**_CharacterID_*_»). Balloon. activé_*</span><span class="sxs-lookup"><span data-stu-id="68a0e-109">*agent\***.Characters ("**_CharacterID_*_").Balloon.Enabled_\*</span></span>



| <span data-ttu-id="68a0e-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="68a0e-110">Value</span></span>     | <span data-ttu-id="68a0e-111">Description</span><span class="sxs-lookup"><span data-stu-id="68a0e-111">Description</span></span>              |
|-----------|--------------------------|
| <span data-ttu-id="68a0e-112">**True**</span><span class="sxs-lookup"><span data-stu-id="68a0e-112">**True**</span></span>  | <span data-ttu-id="68a0e-113">La bulle est activée.</span><span class="sxs-lookup"><span data-stu-id="68a0e-113">The balloon is enabled.</span></span>  |
| <span data-ttu-id="68a0e-114">**False**</span><span class="sxs-lookup"><span data-stu-id="68a0e-114">**False**</span></span> | <span data-ttu-id="68a0e-115">L’info-bulle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="68a0e-115">The balloon is disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68a0e-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="68a0e-116">Remarks</span></span>

<span data-ttu-id="68a0e-117">La propriété **Enabled** retourne une valeur booléenne qui spécifie si la bulle est activée.</span><span class="sxs-lookup"><span data-stu-id="68a0e-117">The **Enabled** property returns a Boolean value specifying whether the balloon is enabled.</span></span> <span data-ttu-id="68a0e-118">L’État par défaut de la bulle de texte est défini dans le cadre de la définition d’un caractère lorsque le caractère est compilé dans l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="68a0e-118">The word balloon default state is set as part of a character's definition when the character is compiled in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="68a0e-119">Si un caractère est défini pour ne pas prendre en charge la bulle de mot, cette propriété aura toujours la **valeur false** pour le caractère.</span><span class="sxs-lookup"><span data-stu-id="68a0e-119">If a character is defined to not support the word balloon, this property will always be **False** for the character.</span></span>

 

 




