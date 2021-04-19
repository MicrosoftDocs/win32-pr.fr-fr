---
description: L’interface IWiaAppErrorHandler permet aux applications d’afficher des fenêtres d’erreur (pendant les transferts de données) à partir desquelles l’utilisateur peut choisir de continuer, d’annuler ou d’abandonner le transfert.
ms.assetid: ac2597e6-2857-4694-bea7-1ea65d63b365
title: Interface IWiaAppErrorHandler (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6ccac7b689055bfaab926a8db46b4632606811d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534279"
---
# <a name="iwiaapperrorhandler-interface"></a><span data-ttu-id="37bac-103">Interface IWiaAppErrorHandler</span><span class="sxs-lookup"><span data-stu-id="37bac-103">IWiaAppErrorHandler interface</span></span>

<span data-ttu-id="37bac-104">L’interface **IWiaAppErrorHandler** permet aux applications d’afficher des fenêtres d’erreur (pendant les transferts de données) à partir desquelles l’utilisateur peut choisir de continuer, d’annuler ou d’abandonner le transfert.</span><span class="sxs-lookup"><span data-stu-id="37bac-104">The **IWiaAppErrorHandler** interface enables applications to display error windows (during data transfers) from which the user can choose whether to continue, cancel, or abort the transfer.</span></span>

## <a name="members"></a><span data-ttu-id="37bac-105">Membres</span><span class="sxs-lookup"><span data-stu-id="37bac-105">Members</span></span>

<span data-ttu-id="37bac-106">L’interface **IWiaAppErrorHandler** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="37bac-106">The **IWiaAppErrorHandler** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="37bac-107">**IWiaAppErrorHandler** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="37bac-107">**IWiaAppErrorHandler** also has these types of members:</span></span>

-   [<span data-ttu-id="37bac-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="37bac-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="37bac-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="37bac-109">Methods</span></span>

<span data-ttu-id="37bac-110">L’interface **IWiaAppErrorHandler** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="37bac-110">The **IWiaAppErrorHandler** interface has these methods.</span></span>



| <span data-ttu-id="37bac-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="37bac-111">Method</span></span>                                                        | <span data-ttu-id="37bac-112">Description</span><span class="sxs-lookup"><span data-stu-id="37bac-112">Description</span></span>                                                                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="37bac-113">**GetWindow**</span><span class="sxs-lookup"><span data-stu-id="37bac-113">**GetWindow**</span></span>](-wia-iwiaapperrorhandler-getwindow.md)       | <span data-ttu-id="37bac-114">Obtient un handle vers la boîte de dialogue qui affiche les messages d’erreur et fournit un ou plusieurs boutons pour continuer, annuler ou abandonner l’application.</span><span class="sxs-lookup"><span data-stu-id="37bac-114">Gets a handle to the dialog box that displays error messages and provides one or more buttons to continue, cancel, or abort the application.</span></span><br/> |
| [<span data-ttu-id="37bac-115">**ReportStatus**</span><span class="sxs-lookup"><span data-stu-id="37bac-115">**ReportStatus**</span></span>](-wia-iwiaapperrorhandler-reportstatus.md) | <span data-ttu-id="37bac-116">Gère l’état des appareils et les messages d’erreur pendant les transferts de données d’image et affiche les messages à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="37bac-116">Handles device status and error messages during image data transfers and displays the messages to the user.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="37bac-117">Notes</span><span class="sxs-lookup"><span data-stu-id="37bac-117">Remarks</span></span>

<span data-ttu-id="37bac-118">L’objet de gestion des erreurs ou de rappel qui implémente cette interface est passé dans [**IWiaTransfer ::D lécharger**](-wia-iwiatransfer-download.md) et [**IWiaTransfer :: upload**](-wia-iwiatransfer-upload.md).</span><span class="sxs-lookup"><span data-stu-id="37bac-118">The error handling, or callback, object that implements this interface is passed into [**IWiaTransfer::Download**](-wia-iwiatransfer-download.md) and [**IWiaTransfer::Upload**](-wia-iwiatransfer-upload.md).</span></span>

<span data-ttu-id="37bac-119">Cette interface n’est pas conçue pour gérer les erreurs rencontrées en dehors des transferts de données d’image, par exemple, les erreurs d’obtention ou de définition des propriétés d’appareil ou les rappels non renvoyés dans un pilote.</span><span class="sxs-lookup"><span data-stu-id="37bac-119">This interface is not designed to handle errors encountered outside of image data transfers, for example, errors in getting or setting device properties or unreturned callbacks into a driver.</span></span>

<span data-ttu-id="37bac-120">Un gestionnaire d’erreurs de pilote doit implémenter [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md)au lieu de **IWiaAppErrorHandler**.</span><span class="sxs-lookup"><span data-stu-id="37bac-120">A driver error handler should implement [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md), instead of **IWiaAppErrorHandler**.</span></span>

<span data-ttu-id="37bac-121">L’objet qui implémente cette interface doit également implémenter [**IWiaTransferCallback**](-wia-iwiatransfercallback.md).</span><span class="sxs-lookup"><span data-stu-id="37bac-121">The object that implements this interface should also implement [**IWiaTransferCallback**](-wia-iwiatransfercallback.md).</span></span>

<span data-ttu-id="37bac-122">Si vous souhaitez qu’un gestionnaire d’erreurs de pilote et un gestionnaire d’erreurs par défaut affichent des fenêtres de message d’erreur, mais que vous ne souhaitez pas créer de gestionnaire d’erreurs complet pour l’application, implémentez cette interface et implémentez également la méthode [**IWiaAppErrorHandler :: ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) pour retourner l' \_ État WIA \_ non \_ géré.</span><span class="sxs-lookup"><span data-stu-id="37bac-122">If you want a driver error handler and default error handler to display error message windows, but you do not want to create a complete error handler for the application, implement this interface and also implement the [**IWiaAppErrorHandler::ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) method to return WIA\_STATUS\_NOT\_HANDLED.</span></span>

## <a name="requirements"></a><span data-ttu-id="37bac-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37bac-123">Requirements</span></span>



| <span data-ttu-id="37bac-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37bac-124">Requirement</span></span> | <span data-ttu-id="37bac-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="37bac-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="37bac-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37bac-126">Minimum supported client</span></span><br/> | <span data-ttu-id="37bac-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37bac-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="37bac-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37bac-128">Minimum supported server</span></span><br/> | <span data-ttu-id="37bac-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37bac-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="37bac-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="37bac-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="37bac-131"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="37bac-131"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="37bac-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="37bac-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="37bac-133"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="37bac-133"><dt>Wia.idl</dt></span></span> </dl> |



 

 
