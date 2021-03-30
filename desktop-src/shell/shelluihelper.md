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
ms.openlocfilehash: f0df3b02624a802c19663b67cbcab508c3e0e487
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973731"
---
# <a name="shelluihelper-object"></a><span data-ttu-id="caf4c-105">Objet ShellUIHelper</span><span class="sxs-lookup"><span data-stu-id="caf4c-105">ShellUIHelper object</span></span>

<span data-ttu-id="caf4c-106">Implémenté par le Shell pour aider le script et Microsoft Visual Basic les développeurs utilisent certaines des fonctionnalités disponibles dans l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="caf4c-106">Implemented by the Shell to help script and Microsoft Visual Basic developers use some of the features available in the Shell.</span></span> <span data-ttu-id="caf4c-107">L’objet **ShellUIHelper** n’a pas de propriétés ou d’événements.</span><span class="sxs-lookup"><span data-stu-id="caf4c-107">The **ShellUIHelper** object does not have any properties or events.</span></span> <span data-ttu-id="caf4c-108">Des méthodes sont fournies pour ajouter des éléments à l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="caf4c-108">Methods are provided to add items to the Shell.</span></span>

## <a name="members"></a><span data-ttu-id="caf4c-109">Membres</span><span class="sxs-lookup"><span data-stu-id="caf4c-109">Members</span></span>

<span data-ttu-id="caf4c-110">L’objet **ShellUIHelper** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="caf4c-110">The **ShellUIHelper** object has these types of members:</span></span>

-   [<span data-ttu-id="caf4c-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="caf4c-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="caf4c-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="caf4c-112">Methods</span></span>

<span data-ttu-id="caf4c-113">L’objet **ShellUIHelper** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="caf4c-113">The **ShellUIHelper** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="caf4c-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="caf4c-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="caf4c-115">Description</span><span class="sxs-lookup"><span data-stu-id="caf4c-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="caf4c-116"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></span><span class="sxs-lookup"><span data-stu-id="caf4c-116"><a href="shelluihelper-addchannel.md"><strong>AddChannel</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="caf4c-117">Ajoute un nouveau canal à la liste de canaux dans le menu <strong>favoris</strong> d’Internet Explorer et à la barre de <strong>canaux</strong> sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="caf4c-117">Adds a new channel to the list of channels in the Internet Explorer <strong>Favorites</strong> menu and to the <strong>Channel</strong> bar on the desktop.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="caf4c-118">Cette méthode n’est plus prise en charge sous Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="caf4c-118">This method is no longer supported under Windows Vista.</span></span> <span data-ttu-id="caf4c-119">Sous ce système d’exploitation, il retourne E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="caf4c-119">Under that operating system, it returns E_NOTIMPL.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="caf4c-120"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></span><span class="sxs-lookup"><span data-stu-id="caf4c-120"><a href="shelluihelper-adddesktopcomponent.md"><strong>AddDesktopComponent</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="caf4c-121">Ajoute un élément à Active Desktop.</span><span class="sxs-lookup"><span data-stu-id="caf4c-121">Adds an item to the Active Desktop.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="caf4c-122"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></span><span class="sxs-lookup"><span data-stu-id="caf4c-122"><a href="shelluihelper-addfavorite.md"><strong>AddFavorite</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="caf4c-123">Affiche l’interface utilisateur par défaut pour la création d’un élément favori.</span><span class="sxs-lookup"><span data-stu-id="caf4c-123">Displays the default user interface for creating a favorite item.</span></span> <span data-ttu-id="caf4c-124">L’interface utilisateur est initialisée avec les paramètres spécifiés.</span><span class="sxs-lookup"><span data-stu-id="caf4c-124">The user interface is initialized to the specified parameters.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="caf4c-125"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></span><span class="sxs-lookup"><span data-stu-id="caf4c-125"><a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="caf4c-126">Indique si une URL spécifiée est abonnée à.</span><span class="sxs-lookup"><span data-stu-id="caf4c-126">Indicates whether a specified URL is subscribed to.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="caf4c-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="caf4c-127">Requirements</span></span>



| <span data-ttu-id="caf4c-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="caf4c-128">Requirement</span></span> | <span data-ttu-id="caf4c-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="caf4c-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caf4c-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="caf4c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="caf4c-131">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="caf4c-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="caf4c-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="caf4c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="caf4c-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="caf4c-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="caf4c-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="caf4c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="caf4c-135"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="caf4c-135"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="caf4c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="caf4c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="caf4c-137"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="caf4c-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




