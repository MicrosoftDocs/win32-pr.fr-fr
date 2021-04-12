---
description: L’interface IWiaTransfer fournit un transfert de données basé sur les flux.
ms.assetid: 7bc6d3b8-9bf0-4b77-aa2b-b7c64c5730c0
title: Interface IWiaTransfer (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 623cc21591289f4c1fff33cabe1d504b3682708c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201489"
---
# <a name="iwiatransfer-interface"></a><span data-ttu-id="53879-103">Interface IWiaTransfer</span><span class="sxs-lookup"><span data-stu-id="53879-103">IWiaTransfer interface</span></span>

<span data-ttu-id="53879-104">L’interface **IWiaTransfer** fournit un transfert de données basé sur les flux.</span><span class="sxs-lookup"><span data-stu-id="53879-104">The **IWiaTransfer** interface provides stream-based transfer of data.</span></span>

## <a name="members"></a><span data-ttu-id="53879-105">Membres</span><span class="sxs-lookup"><span data-stu-id="53879-105">Members</span></span>

<span data-ttu-id="53879-106">L’interface **IWiaTransfer** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="53879-106">The **IWiaTransfer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="53879-107">**IWiaTransfer** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="53879-107">**IWiaTransfer** also has these types of members:</span></span>

-   [<span data-ttu-id="53879-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="53879-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="53879-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="53879-109">Methods</span></span>

<span data-ttu-id="53879-110">L’interface **IWiaTransfer** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="53879-110">The **IWiaTransfer** interface has these methods.</span></span>



| <span data-ttu-id="53879-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="53879-111">Method</span></span>                                                                 | <span data-ttu-id="53879-112">Description</span><span class="sxs-lookup"><span data-stu-id="53879-112">Description</span></span>                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53879-113">**Annuler**</span><span class="sxs-lookup"><span data-stu-id="53879-113">**Cancel**</span></span>](-wia-iwiatransfer-cancel.md)                             | <span data-ttu-id="53879-114">Annule l’opération de transfert en cours.</span><span class="sxs-lookup"><span data-stu-id="53879-114">Cancels the current transfer operation.</span></span> <br/>                                         |
| [<span data-ttu-id="53879-115">**Télécharger**</span><span class="sxs-lookup"><span data-stu-id="53879-115">**Download**</span></span>](-wia-iwiatransfer-download.md)                         | <span data-ttu-id="53879-116">Lance un téléchargement de données vers l’appelant.</span><span class="sxs-lookup"><span data-stu-id="53879-116">Initiates a data download to the caller.</span></span> <br/>                                        |
| [<span data-ttu-id="53879-117">**\_Informations de format EnumWIA \_**</span><span class="sxs-lookup"><span data-stu-id="53879-117">**EnumWIA\_FORMAT\_INFO**</span></span>](-wia-iwiatransfer-enumwia-format-info.md) | <span data-ttu-id="53879-118">Crée un énumérateur pour les formats de transfert pris en charge par l’appareil WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="53879-118">Creates an enumerator for the transfer formats that the WIA 2.0 device supports.</span></span><br/> |
| [<span data-ttu-id="53879-119">**Télécharger**</span><span class="sxs-lookup"><span data-stu-id="53879-119">**Upload**</span></span>](-wia-iwiatransfer-upload.md)                             | <span data-ttu-id="53879-120">Lance un chargement de données d’un élément unique à partir de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="53879-120">Initiates a data upload of a single item from the caller.</span></span> <br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="53879-121">Notes</span><span class="sxs-lookup"><span data-stu-id="53879-121">Remarks</span></span>

<span data-ttu-id="53879-122">L’interface **IWiaTransfer** , comme toutes les interfaces COM (Component Object Model), hérite des méthodes d’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="53879-122">The **IWiaTransfer** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="53879-123">Méthodes IUnknown</span><span class="sxs-lookup"><span data-stu-id="53879-123">IUnknown Methods</span></span>                                        | <span data-ttu-id="53879-124">Description</span><span class="sxs-lookup"><span data-stu-id="53879-124">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="53879-125">[IUnknown :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="53879-125">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="53879-126">Retourne des pointeurs aux interfaces prises en charge.</span><span class="sxs-lookup"><span data-stu-id="53879-126">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="53879-127">IUnknown :: AddRef</span><span class="sxs-lookup"><span data-stu-id="53879-127">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="53879-128">Incrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="53879-128">Increments reference count.</span></span>               |
| [<span data-ttu-id="53879-129">IUnknown :: Release</span><span class="sxs-lookup"><span data-stu-id="53879-129">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="53879-130">Décrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="53879-130">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="53879-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53879-131">Requirements</span></span>



| <span data-ttu-id="53879-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53879-132">Requirement</span></span> | <span data-ttu-id="53879-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="53879-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53879-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53879-134">Minimum supported client</span></span><br/> | <span data-ttu-id="53879-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53879-135">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="53879-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53879-136">Minimum supported server</span></span><br/> | <span data-ttu-id="53879-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53879-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="53879-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="53879-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="53879-139"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="53879-139"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="53879-140">MIDL</span><span class="sxs-lookup"><span data-stu-id="53879-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="53879-141"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="53879-141"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="53879-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="53879-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="53879-143"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53879-143"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
