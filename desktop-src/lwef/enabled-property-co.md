---
title: Propriété Enabled (objet Command)
description: Propriété activée
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5999e396f61fbcc820bc1cec7deb0c603eb948e4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106509490"
---
# <a name="enabled-property-command-object"></a><span data-ttu-id="c1e60-103">Propriété Enabled (objet Command)</span><span class="sxs-lookup"><span data-stu-id="c1e60-103">Enabled Property (Command Object)</span></span>

<span data-ttu-id="c1e60-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c1e60-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c1e60-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="c1e60-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c1e60-106">Retourne ou définit une valeur indiquant si la **commande** est activée dans le menu contextuel du caractère spécifié.</span><span class="sxs-lookup"><span data-stu-id="c1e60-106">Returns or sets whether the **Command** is enabled in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="c1e60-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="c1e60-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c1e60-108">\*agent \***. Caractères («**_CharacterID_*_»). Commandes («_*_nom_\*_»)._ \*  \[  =  *Valeur booléenne* activée\]</span><span class="sxs-lookup"><span data-stu-id="c1e60-108">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Enabled_\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="c1e60-109">Partie</span><span class="sxs-lookup"><span data-stu-id="c1e60-109">Part</span></span>      | <span data-ttu-id="c1e60-110">Description</span><span class="sxs-lookup"><span data-stu-id="c1e60-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1e60-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="c1e60-111">*boolean*</span></span> | <span data-ttu-id="c1e60-112">Expression booléenne spécifiant si la **commande** est activée.</span><span class="sxs-lookup"><span data-stu-id="c1e60-112">A Boolean expression specifying whether the **Command** is enabled.</span></span><br/> <dl> <span data-ttu-id="c1e60-113"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**Vrai**</dt></span><span class="sxs-lookup"><span data-stu-id="c1e60-113"><dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt></span></span> <dd> <span data-ttu-id="c1e60-114">La **commande** est activée.</span><span class="sxs-lookup"><span data-stu-id="c1e60-114">The **Command** is enabled.</span></span><br/> </dd> <span data-ttu-id="c1e60-115"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**Faux**</dt></span><span class="sxs-lookup"><span data-stu-id="c1e60-115"><dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</dt></span></span> <dd> <span data-ttu-id="c1e60-116">La **commande** est désactivée.</span><span class="sxs-lookup"><span data-stu-id="c1e60-116">The **Command** is disabled.</span></span><br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1e60-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c1e60-117">Remarks</span></span>

<span data-ttu-id="c1e60-118">Si la propriété [**Enabled**](enabled-property.md) a la valeur **true**, la légende de l’objet de [**commande**](/windows/desktop/lwef/the-command-object) apparaît comme texte normal dans le menu contextuel du caractère lorsque l’application cliente est en entrée-active.</span><span class="sxs-lookup"><span data-stu-id="c1e60-118">If the [**Enabled**](enabled-property.md) property is set to **True**, the [**Command**](/windows/desktop/lwef/the-command-object) objects's caption appears as normal text in the character's pop-up menu when the client application is input-active.</span></span> <span data-ttu-id="c1e60-119">Si la propriété **Enabled** a la **valeur false**, la légende apparaît comme texte non disponible (désactivé).</span><span class="sxs-lookup"><span data-stu-id="c1e60-119">If the **Enabled** property is **False**, the caption appears as unavailable (disabled) text.</span></span> <span data-ttu-id="c1e60-120">Une **commande** désactivée n’est pas non plus accessible pour une entrée vocale.</span><span class="sxs-lookup"><span data-stu-id="c1e60-120">A disabled **Command** is also not accessible for voice input.</span></span>

 

