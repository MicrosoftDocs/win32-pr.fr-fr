---
description: Implémenté par le Shell pour aider le script et Microsoft Visual Basic les développeurs utilisent certaines des fonctionnalités disponibles dans l’interpréteur de commandes. L’objet ShellUIHelper n’a pas de propriétés ou d’événements. Des méthodes sont fournies pour ajouter des éléments à l’interpréteur de commandes.
title: Objet ShellUIHelper (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9fffebc8-29b9-4064-b60c-c8c63690a79e
ms.openlocfilehash: b77d618c4c772859a9009f3cca761c59df83257a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842430"
---
# <a name="shelluihelper-object"></a><span data-ttu-id="e6f0d-105">Objet ShellUIHelper</span><span class="sxs-lookup"><span data-stu-id="e6f0d-105">ShellUIHelper object</span></span>

<span data-ttu-id="e6f0d-106">Implémenté par le Shell pour aider le script et Microsoft Visual Basic les développeurs utilisent certaines des fonctionnalités disponibles dans l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="e6f0d-106">Implemented by the Shell to help script and Microsoft Visual Basic developers use some of the features available in the Shell.</span></span> <span data-ttu-id="e6f0d-107">L’objet **ShellUIHelper** n’a pas de propriétés ou d’événements.</span><span class="sxs-lookup"><span data-stu-id="e6f0d-107">The **ShellUIHelper** object does not have any properties or events.</span></span> <span data-ttu-id="e6f0d-108">Des méthodes sont fournies pour ajouter des éléments à l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="e6f0d-108">Methods are provided to add items to the Shell.</span></span>

## <a name="members"></a><span data-ttu-id="e6f0d-109">Membres</span><span class="sxs-lookup"><span data-stu-id="e6f0d-109">Members</span></span>

<span data-ttu-id="e6f0d-110">L’objet **ShellUIHelper** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e6f0d-110">The **ShellUIHelper** object has these types of members:</span></span>

-   [<span data-ttu-id="e6f0d-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e6f0d-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e6f0d-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e6f0d-112">Methods</span></span>

<span data-ttu-id="e6f0d-113">L’objet **ShellUIHelper** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e6f0d-113">The **ShellUIHelper** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="e6f0d-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="e6f0d-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="e6f0d-115">Description</span><span class="sxs-lookup"><span data-stu-id="e6f0d-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e6f0d-116"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6f0d-116"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e6f0d-117">Ajoute un nouveau canal à la liste de canaux dans le menu <strong>favoris</strong> d’Internet Explorer et à la barre de <strong>canaux</strong> sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="e6f0d-117">Adds a new channel to the list of channels in the Internet Explorer <strong>Favorites</strong> menu and to the <strong>Channel</strong> bar on the desktop.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e6f0d-118">Cette méthode n’est plus prise en charge sous Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e6f0d-118">This method is no longer supported under Windows Vista.</span></span> <span data-ttu-id="e6f0d-119">Sous ce système d’exploitation, il retourne E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="e6f0d-119">Under that operating system, it returns E_NOTIMPL.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e6f0d-120"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6f0d-120"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e6f0d-121">Ajoute un élément à Active Desktop.</span><span class="sxs-lookup"><span data-stu-id="e6f0d-121">Adds an item to the Active Desktop.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e6f0d-122"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6f0d-122"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e6f0d-123">Affiche l’interface utilisateur par défaut pour la création d’un élément favori.</span><span class="sxs-lookup"><span data-stu-id="e6f0d-123">Displays the default user interface for creating a favorite item.</span></span> <span data-ttu-id="e6f0d-124">L’interface utilisateur est initialisée avec les paramètres spécifiés.</span><span class="sxs-lookup"><span data-stu-id="e6f0d-124">The user interface is initialized to the specified parameters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e6f0d-125"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></span><span class="sxs-lookup"><span data-stu-id="e6f0d-125"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e6f0d-126">Indique si une URL spécifiée est abonnée à.</span><span class="sxs-lookup"><span data-stu-id="e6f0d-126">Indicates whether a specified URL is subscribed to.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="e6f0d-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e6f0d-127">Requirements</span></span>



| <span data-ttu-id="e6f0d-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6f0d-128">Requirement</span></span> | <span data-ttu-id="e6f0d-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6f0d-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6f0d-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6f0d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e6f0d-131">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6f0d-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e6f0d-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6f0d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e6f0d-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6f0d-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e6f0d-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6f0d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6f0d-135"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6f0d-135"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="e6f0d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e6f0d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6f0d-137"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="e6f0d-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




