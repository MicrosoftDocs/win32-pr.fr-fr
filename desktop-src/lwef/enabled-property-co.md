---
title: Propriété Enabled (objet Command)
description: En savoir plus sur la propriété de l’objet de commande activé. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc0c65d5cfa0438fe9d61eac0c59e916731e057
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407332"
---
# <a name="enabled-property-command-object"></a><span data-ttu-id="2d62e-104">Propriété Enabled (objet Command)</span><span class="sxs-lookup"><span data-stu-id="2d62e-104">Enabled Property (Command Object)</span></span>

<span data-ttu-id="2d62e-105">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2d62e-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2d62e-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="2d62e-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2d62e-107">Retourne ou définit une valeur indiquant si la **commande** est activée dans le menu contextuel du caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="2d62e-107">Returns or sets whether the **Command** is enabled in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="2d62e-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="2d62e-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2d62e-109">\*agent \***. Caractères («**_CharacterID_*_»). Commandes («_*_nom_\*_»)._ \*  \[  =  *Valeur booléenne* activée\]</span><span class="sxs-lookup"><span data-stu-id="2d62e-109">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Enabled_\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="2d62e-110">Partie</span><span class="sxs-lookup"><span data-stu-id="2d62e-110">Part</span></span>      | <span data-ttu-id="2d62e-111">Description</span><span class="sxs-lookup"><span data-stu-id="2d62e-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d62e-112">*boolean*</span><span class="sxs-lookup"><span data-stu-id="2d62e-112">*boolean*</span></span> | <span data-ttu-id="2d62e-113">Expression booléenne spécifiant si la **commande** est activée.</span><span class="sxs-lookup"><span data-stu-id="2d62e-113">A Boolean expression specifying whether the **Command** is enabled.</span></span><br/> <dl> <span data-ttu-id="2d62e-114"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt></span><span class="sxs-lookup"><span data-stu-id="2d62e-114"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt></span></span> <dd> <span data-ttu-id="2d62e-115">La **commande** est activée.</span><span class="sxs-lookup"><span data-stu-id="2d62e-115">The **Command** is enabled.</span></span><br/> </dd> <span data-ttu-id="2d62e-116"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**Fausses**</dt></span><span class="sxs-lookup"><span data-stu-id="2d62e-116"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</dt></span></span> <dd> <span data-ttu-id="2d62e-117">La **commande** est désactivée.</span><span class="sxs-lookup"><span data-stu-id="2d62e-117">The **Command** is disabled.</span></span><br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d62e-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="2d62e-118">Remarks</span></span>

<span data-ttu-id="2d62e-119">Si la propriété [**Enabled**](enabled-property.md) a la valeur **true**, la légende de l’objet de [**commande**](/windows/desktop/lwef/the-command-object) apparaît comme texte normal dans le menu contextuel du caractère lorsque l’application cliente est en entrée-active.</span><span class="sxs-lookup"><span data-stu-id="2d62e-119">If the [**Enabled**](enabled-property.md) property is set to **True**, the [**Command**](/windows/desktop/lwef/the-command-object) objects's caption appears as normal text in the character's pop-up menu when the client application is input-active.</span></span> <span data-ttu-id="2d62e-120">Si la propriété **Enabled** a la **valeur false**, la légende apparaît comme texte non disponible (désactivé).</span><span class="sxs-lookup"><span data-stu-id="2d62e-120">If the **Enabled** property is **False**, the caption appears as unavailable (disabled) text.</span></span> <span data-ttu-id="2d62e-121">Une **commande** désactivée n’est pas non plus accessible pour une entrée vocale.</span><span class="sxs-lookup"><span data-stu-id="2d62e-121">A disabled **Command** is also not accessible for voice input.</span></span>

 

