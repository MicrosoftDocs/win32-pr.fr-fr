---
description: L’interface IUpdateCollection définit les propriétés suivantes.
ms.assetid: 38420d5e-4d36-4ed7-be06-e1df903929a7
title: Propriétés IUpdateCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aae347885deccb52ac44513bd1138aa18995c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514032"
---
# <a name="iupdatecollection-properties"></a><span data-ttu-id="e23b1-103">Propriétés IUpdateCollection</span><span class="sxs-lookup"><span data-stu-id="e23b1-103">IUpdateCollection Properties</span></span>

<span data-ttu-id="e23b1-104">L’interface [**IUpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection) définit les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e23b1-104">The [**IUpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection) interface defines the following properties.</span></span>



| <span data-ttu-id="e23b1-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="e23b1-105">Property</span></span>                                        | <span data-ttu-id="e23b1-106">Description</span><span class="sxs-lookup"><span data-stu-id="e23b1-106">Description</span></span>                                                                                                              |
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e23b1-107">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="e23b1-107">**\_NewEnum**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get__newenum) | <span data-ttu-id="e23b1-108">Obtient une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) qui peut être utilisée pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="e23b1-108">Gets an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface that can be used to enumerate the collection.</span></span> |
| [<span data-ttu-id="e23b1-109">**Saut**</span><span class="sxs-lookup"><span data-stu-id="e23b1-109">**Count**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_count)        | <span data-ttu-id="e23b1-110">Obtient le nombre d’éléments de la collection.</span><span class="sxs-lookup"><span data-stu-id="e23b1-110">Gets the number of elements in the collection.</span></span>                                                                           |
| [<span data-ttu-id="e23b1-111">**Élément**</span><span class="sxs-lookup"><span data-stu-id="e23b1-111">**Item**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_item)          | <span data-ttu-id="e23b1-112">Obtient ou définit une interface [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) dans une collection.</span><span class="sxs-lookup"><span data-stu-id="e23b1-112">Gets or sets an [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) interface in a collection.</span></span>                                                    |
| [<span data-ttu-id="e23b1-113">**Seulement**</span><span class="sxs-lookup"><span data-stu-id="e23b1-113">**ReadOnly**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_readonly)  | <span data-ttu-id="e23b1-114">Obtient une valeur booléenne qui indique si la collection de mises à jour est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e23b1-114">Gets a Boolean value that indicates whether the update collection is read-only.</span></span>                                          |



 

 

 
