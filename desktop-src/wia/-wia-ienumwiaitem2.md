---
description: Utilisé par les applications pour énumérer les objets IWiaItem2 dans le dossier actif de l’arborescence d’éléments.
ms.assetid: a82298e0-fbe7-4ef5-99c5-18ff60538e03
title: Interface IEnumWiaItem2 (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: f6e41b3172793f696a9ea3c2d319bdee6ca3d691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517550"
---
# <a name="ienumwiaitem2-interface"></a><span data-ttu-id="4a953-103">Interface IEnumWiaItem2</span><span class="sxs-lookup"><span data-stu-id="4a953-103">IEnumWiaItem2 interface</span></span>

<span data-ttu-id="4a953-104">Utilisé par les applications pour énumérer les objets [**IWiaItem2**](-wia-iwiaitem2.md) dans le dossier actif de l’arborescence d’éléments.</span><span class="sxs-lookup"><span data-stu-id="4a953-104">Used by applications to enumerate [**IWiaItem2**](-wia-iwiaitem2.md) objects in the item tree's current folder.</span></span>

## <a name="members"></a><span data-ttu-id="4a953-105">Membres</span><span class="sxs-lookup"><span data-stu-id="4a953-105">Members</span></span>

<span data-ttu-id="4a953-106">L’interface **IEnumWiaItem2** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4a953-106">The **IEnumWiaItem2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4a953-107">**IEnumWiaItem2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4a953-107">**IEnumWiaItem2** also has these types of members:</span></span>

-   [<span data-ttu-id="4a953-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4a953-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4a953-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4a953-109">Methods</span></span>

<span data-ttu-id="4a953-110">L’interface **IEnumWiaItem2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4a953-110">The **IEnumWiaItem2** interface has these methods.</span></span>



| <span data-ttu-id="4a953-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="4a953-111">Method</span></span>                                          | <span data-ttu-id="4a953-112">Description</span><span class="sxs-lookup"><span data-stu-id="4a953-112">Description</span></span>                                                                                                                    |
|:------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a953-113">**Répliqué**</span><span class="sxs-lookup"><span data-stu-id="4a953-113">**Clone**</span></span>](-wia-ienumwiaitem2-clone.md)       | <span data-ttu-id="4a953-114">Crée une instance supplémentaire de l’interface **IEnumWiaItem2** et retourne un pointeur vers celui-ci.</span><span class="sxs-lookup"><span data-stu-id="4a953-114">Creates an additional instance of the **IEnumWiaItem2** interface and sends back a pointer to it.</span></span> <br/>                  |
| [<span data-ttu-id="4a953-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="4a953-115">**GetCount**</span></span>](-wia-ienumwiaitem2-getcount.md) | <span data-ttu-id="4a953-116">Retourne le nombre d’éléments stockés par cet énumérateur.</span><span class="sxs-lookup"><span data-stu-id="4a953-116">Returns the number of elements stored by this enumerator.</span></span> <br/>                                                          |
| [<span data-ttu-id="4a953-117">**Suivant**</span><span class="sxs-lookup"><span data-stu-id="4a953-117">**Next**</span></span>](-wia-ienumwiaitem2-next.md)         | <span data-ttu-id="4a953-118">Remplit un tableau de pointeurs vers des interfaces [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="4a953-118">Fills an array of pointers to [**IWiaItem2**](-wia-iwiaitem2.md) interfaces.</span></span><br/>                                       |
| [<span data-ttu-id="4a953-119">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="4a953-119">**Reset**</span></span>](-wia-ienumwiaitem2-reset.md)       | <span data-ttu-id="4a953-120">Réinitialise la référence d’énumération au premier objet [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="4a953-120">Resets the enumeration reference to the first [**IWiaItem2**](-wia-iwiaitem2.md) object.</span></span> <br/>                          |
| [<span data-ttu-id="4a953-121">**Saut**</span><span class="sxs-lookup"><span data-stu-id="4a953-121">**Skip**</span></span>](-wia-ienumwiaitem2-skip.md)         | <span data-ttu-id="4a953-122">Ignore le nombre spécifié d’éléments au cours d’une énumération des objets [**IWiaItem2**](-wia-iwiaitem2.md) disponibles.</span><span class="sxs-lookup"><span data-stu-id="4a953-122">Skips the specified number of items during an enumeration of available [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4a953-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a953-123">Requirements</span></span>



| <span data-ttu-id="4a953-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a953-124">Requirement</span></span> | <span data-ttu-id="4a953-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a953-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4a953-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a953-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4a953-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a953-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4a953-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a953-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4a953-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a953-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4a953-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a953-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a953-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a953-131"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a953-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="4a953-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4a953-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4a953-133"><dt>Wia.idl</dt></span></span> </dl> |



 

 
