---
title: Signet, événement
description: Signet, événement
ms.assetid: 6733cd4e-2ba0-4cff-b68d-abfea284f748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0695ccd04f93eae46eaae66955c84fefb9e0c963
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196612"
---
# <a name="bookmark-event"></a><span data-ttu-id="3c045-103">Signet, événement</span><span class="sxs-lookup"><span data-stu-id="3c045-103">Bookmark Event</span></span>

<span data-ttu-id="3c045-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3c045-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3c045-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="3c045-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3c045-106">Se produit lorsqu’un signet dans une chaîne de texte vocal que votre application a définie est activé.</span><span class="sxs-lookup"><span data-stu-id="3c045-106">Occurs when a bookmark in a speech text string that your application defined is activated.</span></span>

</dd> <dt>

<span data-ttu-id="3c045-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="3c045-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="3c045-108">Signet du **sous-** *agent* \_  **(ByVal** - *BookmarkID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="3c045-108">**Sub** *agent*\_**Bookmark** **(ByVal** *BookmarkID\*\*\*)*\*</span></span>



| <span data-ttu-id="3c045-109">Partie</span><span class="sxs-lookup"><span data-stu-id="3c045-109">Part</span></span>         | <span data-ttu-id="3c045-110">Description</span><span class="sxs-lookup"><span data-stu-id="3c045-110">Description</span></span>                                     |
|--------------|-------------------------------------------------|
| <span data-ttu-id="3c045-111">*BookmarkID*</span><span class="sxs-lookup"><span data-stu-id="3c045-111">*BookmarkID*</span></span> | <span data-ttu-id="3c045-112">Entier long identifiant le numéro de signet.</span><span class="sxs-lookup"><span data-stu-id="3c045-112">A Long integer identifying the bookmark number.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="3c045-113">Notes</span><span class="sxs-lookup"><span data-stu-id="3c045-113">Remarks</span></span>

<span data-ttu-id="3c045-114">Pour spécifier un événement Bookmark, utilisez la méthode [**Speak**](speak-method.md) avec une balise **MRK** dans le texte fourni.</span><span class="sxs-lookup"><span data-stu-id="3c045-114">To specify a bookmark event, use the [**Speak**](speak-method.md) method with a **Mrk** tag in your supplied text.</span></span> <span data-ttu-id="3c045-115">Pour plus d’informations sur les balises, consultez balises de sortie vocale.</span><span class="sxs-lookup"><span data-stu-id="3c045-115">For more information about tags, see Speech Output Tags.</span></span>

 

 




