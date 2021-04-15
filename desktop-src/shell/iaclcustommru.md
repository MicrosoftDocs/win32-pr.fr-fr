---
description: Expose les méthodes utilisées pour initialiser une liste des derniers fichiers utilisés pour un objet de saisie semi-automatique.
title: Interface IACLCustomMRU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU
api_type:
- COM
api_location: ''
ms.assetid: 6ebf64da-9eba-4ea7-91aa-242474097be1
ms.openlocfilehash: 54cda8d6cc3c7f1c46d6bce7736160b0da67a4c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991536"
---
# <a name="iaclcustommru-interface"></a><span data-ttu-id="5d188-103">Interface IACLCustomMRU</span><span class="sxs-lookup"><span data-stu-id="5d188-103">IACLCustomMRU interface</span></span>

<span data-ttu-id="5d188-104">Expose les méthodes utilisées pour initialiser une liste des derniers fichiers utilisés pour un objet de saisie semi-automatique.</span><span class="sxs-lookup"><span data-stu-id="5d188-104">Exposes methods that are used to initialize a most recently used (MRU) list for an autocompletion object.</span></span>

## <a name="members"></a><span data-ttu-id="5d188-105">Membres</span><span class="sxs-lookup"><span data-stu-id="5d188-105">Members</span></span>

<span data-ttu-id="5d188-106">L’interface **IACLCustomMRU** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5d188-106">The **IACLCustomMRU** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5d188-107">**IACLCustomMRU** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5d188-107">**IACLCustomMRU** also has these types of members:</span></span>

-   [<span data-ttu-id="5d188-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5d188-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5d188-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5d188-109">Methods</span></span>

<span data-ttu-id="5d188-110">L’interface **IACLCustomMRU** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5d188-110">The **IACLCustomMRU** interface has these methods.</span></span>



| <span data-ttu-id="5d188-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="5d188-111">Method</span></span>                                             | <span data-ttu-id="5d188-112">Description</span><span class="sxs-lookup"><span data-stu-id="5d188-112">Description</span></span>                                                             |
|:---------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="5d188-113">**AddMRUString**</span><span class="sxs-lookup"><span data-stu-id="5d188-113">**AddMRUString**</span></span>](iaclcustommru-addmrustring.md) | <span data-ttu-id="5d188-114">Ajoute une entrée à la liste MRU.</span><span class="sxs-lookup"><span data-stu-id="5d188-114">Adds an entry to the MRU list.</span></span><br/>                               |
| [<span data-ttu-id="5d188-115">**Initialiser**</span><span class="sxs-lookup"><span data-stu-id="5d188-115">**Initialize**</span></span>](iaclcustommru-initialize.md)     | <span data-ttu-id="5d188-116">Charge une liste de chaînes dans la liste MRU à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="5d188-116">Loads a list of strings into the MRU list from the registry.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5d188-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5d188-117">Requirements</span></span>



| <span data-ttu-id="5d188-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d188-118">Requirement</span></span> | <span data-ttu-id="5d188-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d188-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5d188-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d188-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5d188-121">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d188-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="5d188-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d188-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5d188-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d188-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
