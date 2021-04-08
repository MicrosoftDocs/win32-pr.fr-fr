---
title: Balise MRK
description: Balise MRK
ms.assetid: 1bc04853-f919-4f6f-90c2-21ac836bb1e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805a66b9ce5863bda7b7b95317bcab9cf1d80f32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673206"
---
# <a name="mrk-tag"></a><span data-ttu-id="eb53c-103">Balise MRK</span><span class="sxs-lookup"><span data-stu-id="eb53c-103">Mrk Tag</span></span>

<span data-ttu-id="eb53c-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="eb53c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="eb53c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="eb53c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="eb53c-106">Définit un signet dans le texte parlé.</span><span class="sxs-lookup"><span data-stu-id="eb53c-106">Defines a bookmark in the spoken text.</span></span>

</dd> <dt>

<span data-ttu-id="eb53c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="eb53c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="eb53c-108">**\\MRK =***nombre***\\**</span><span class="sxs-lookup"><span data-stu-id="eb53c-108">**\\Mrk=***number***\\**</span></span>



| <span data-ttu-id="eb53c-109">Partie</span><span class="sxs-lookup"><span data-stu-id="eb53c-109">Part</span></span>     | <span data-ttu-id="eb53c-110">Description</span><span class="sxs-lookup"><span data-stu-id="eb53c-110">Description</span></span>                                        |
|----------|----------------------------------------------------|
| <span data-ttu-id="eb53c-111">*number*</span><span class="sxs-lookup"><span data-stu-id="eb53c-111">*number*</span></span> | <span data-ttu-id="eb53c-112">Valeur entière de type long qui identifie le signet.</span><span class="sxs-lookup"><span data-stu-id="eb53c-112">A Long integer value that identifies the bookmark.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="eb53c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="eb53c-113">Remarks</span></span>

<span data-ttu-id="eb53c-114">Quand le serveur traite un signet, il génère un événement Bookmark.</span><span class="sxs-lookup"><span data-stu-id="eb53c-114">When the server processes a bookmark, it generates a bookmark event.</span></span> <span data-ttu-id="eb53c-115">Vous devez spécifier un nombre supérieur à zéro (0) et différent de 2147483647 ou 2147483646.</span><span class="sxs-lookup"><span data-stu-id="eb53c-115">You must specify a number greater than zero (0) and not equal to 2147483647 or 2147483646.</span></span>

 

 




