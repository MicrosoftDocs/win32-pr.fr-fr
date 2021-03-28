---
description: Étend l’objet ShellLinkObject et prend en charge une propriété supplémentaire.
title: Objet IShellLinkDual2 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellLinkDual2
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 8a63552c-6bce-4583-8df8-a7f7731b35eb
ms.openlocfilehash: 0209b57d621d4335a6ef703dadaef3dd5c307c00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951374"
---
# <a name="ishelllinkdual2-object"></a><span data-ttu-id="9f892-103">Objet IShellLinkDual2</span><span class="sxs-lookup"><span data-stu-id="9f892-103">IShellLinkDual2 object</span></span>

<span data-ttu-id="9f892-104">Étend l’objet [**ShellLinkObject**](shelllinkobject-object.md) et prend en charge une propriété supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="9f892-104">Extends the [**ShellLinkObject**](shelllinkobject-object.md) object and supports one additional property.</span></span>

## <a name="members"></a><span data-ttu-id="9f892-105">Membres</span><span class="sxs-lookup"><span data-stu-id="9f892-105">Members</span></span>

<span data-ttu-id="9f892-106">L’objet **IShellLinkDual2** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9f892-106">The **IShellLinkDual2** object has these types of members:</span></span>

-   [<span data-ttu-id="9f892-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9f892-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f892-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9f892-108">Properties</span></span>

<span data-ttu-id="9f892-109">L’objet **IShellLinkDual2** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="9f892-109">The **IShellLinkDual2** object has these properties.</span></span>



| <span data-ttu-id="9f892-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="9f892-110">Property</span></span>                                            | <span data-ttu-id="9f892-111">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="9f892-111">Access type</span></span>          | <span data-ttu-id="9f892-112">Description</span><span class="sxs-lookup"><span data-stu-id="9f892-112">Description</span></span>                                   |
|:----------------------------------------------------|:---------------------|:----------------------------------------------|
| [<span data-ttu-id="9f892-113">**Cible**</span><span class="sxs-lookup"><span data-stu-id="9f892-113">**Target**</span></span>](ishelllinkdual2-target.md)<br/> | <span data-ttu-id="9f892-114">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9f892-114">Read-only</span></span><br/> | <span data-ttu-id="9f892-115">Contient la cible de l’objet de lien.</span><span class="sxs-lookup"><span data-stu-id="9f892-115">Contains the link object's target.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9f892-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9f892-116">Requirements</span></span>



| <span data-ttu-id="9f892-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f892-117">Requirement</span></span> | <span data-ttu-id="9f892-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f892-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f892-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f892-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9f892-120">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f892-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9f892-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f892-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9f892-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9f892-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9f892-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="9f892-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f892-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f892-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="9f892-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="9f892-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9f892-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9f892-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="9f892-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9f892-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f892-128"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="9f892-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




