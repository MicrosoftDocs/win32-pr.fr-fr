---
description: L’interface IWiaErrorHandler fournit des méthodes pour gérer les erreurs qui peuvent se produire lorsqu’une application demande des données d’image, qu’il s’agisse d’un aperçu ou de bits finaux.
ms.assetid: 33d8ccc5-6856-4a54-b1f0-d015933d63ab
title: Interface IWiaErrorHandler (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 7b3ea9f5556f1f919336e4abb4085f9e0c32d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113895"
---
# <a name="iwiaerrorhandler-interface"></a><span data-ttu-id="81de5-103">Interface IWiaErrorHandler</span><span class="sxs-lookup"><span data-stu-id="81de5-103">IWiaErrorHandler interface</span></span>

<span data-ttu-id="81de5-104">L’interface **IWiaErrorHandler** fournit des méthodes pour gérer les erreurs qui peuvent se produire lorsqu’une application demande des données d’image, qu’il s’agisse d’un aperçu ou de bits finaux.</span><span class="sxs-lookup"><span data-stu-id="81de5-104">The **IWiaErrorHandler** interface provides methods to handle errors that may occur when an application requests image data, whether for preview or final bits.</span></span>

## <a name="members"></a><span data-ttu-id="81de5-105">Membres</span><span class="sxs-lookup"><span data-stu-id="81de5-105">Members</span></span>

<span data-ttu-id="81de5-106">L’interface **IWiaErrorHandler** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="81de5-106">The **IWiaErrorHandler** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="81de5-107">**IWiaErrorHandler** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="81de5-107">**IWiaErrorHandler** also has these types of members:</span></span>

-   [<span data-ttu-id="81de5-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="81de5-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="81de5-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="81de5-109">Methods</span></span>

<span data-ttu-id="81de5-110">L’interface **IWiaErrorHandler** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="81de5-110">The **IWiaErrorHandler** interface has these methods.</span></span>



| <span data-ttu-id="81de5-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="81de5-111">Method</span></span>                                                                     | <span data-ttu-id="81de5-112">Description</span><span class="sxs-lookup"><span data-stu-id="81de5-112">Description</span></span>                                                                                             |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81de5-113">**GetStatusDescription**</span><span class="sxs-lookup"><span data-stu-id="81de5-113">**GetStatusDescription**</span></span>](-wia-iwiaerrorhandler-getstatusdescription.md) | <span data-ttu-id="81de5-114">Retourne une chaîne qui décrit le code d’État.</span><span class="sxs-lookup"><span data-stu-id="81de5-114">Returns a string that describes the status code.</span></span><br/>                                             |
| [<span data-ttu-id="81de5-115">**ReportStatus**</span><span class="sxs-lookup"><span data-stu-id="81de5-115">**ReportStatus**</span></span>](-wia-iwiaerrorhandler-reportstatus.md)                 | <span data-ttu-id="81de5-116">Gère les messages d’État et d’erreur pendant les transferts de données d’image et les affiche à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="81de5-116">Handles status and error messages during image data transfers and displays them to the user.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="81de5-117">Notes</span><span class="sxs-lookup"><span data-stu-id="81de5-117">Remarks</span></span>

<span data-ttu-id="81de5-118">L’objet de rappel d’application peut implémenter **IWiaErrorHandler**.</span><span class="sxs-lookup"><span data-stu-id="81de5-118">The application callback object can implement **IWiaErrorHandler**.</span></span>

<span data-ttu-id="81de5-119">Cette interface n’est pas conçue pour gérer les erreurs rencontrées en dehors des transferts de données d’image, par exemple, les erreurs d’obtention ou de définition des propriétés d’appareil ou les rappels non renvoyés dans un pilote.</span><span class="sxs-lookup"><span data-stu-id="81de5-119">This interface is not designed to handle errors encountered outside of image data transfers, for example, errors in getting or setting device properties or unreturned callbacks into a driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="81de5-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81de5-120">Requirements</span></span>



| <span data-ttu-id="81de5-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81de5-121">Requirement</span></span> | <span data-ttu-id="81de5-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="81de5-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81de5-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81de5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="81de5-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81de5-124">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="81de5-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81de5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="81de5-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81de5-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="81de5-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="81de5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="81de5-128"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="81de5-128"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="81de5-129">MIDL</span><span class="sxs-lookup"><span data-stu-id="81de5-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="81de5-130"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="81de5-130"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="81de5-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="81de5-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="81de5-132"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81de5-132"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
