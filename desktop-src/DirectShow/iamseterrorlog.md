---
description: L’interface IAMSetErrorLog définit ou récupère un journal des erreurs dans les services de modification DirectShow (DES).
ms.assetid: ce658533-eacf-4b5d-9910-dca918de09e7
title: Interface IAMSetErrorLog (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c0a24d29625bf08bc2f4c728a61f5188e8bec211
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528472"
---
# <a name="iamseterrorlog-interface"></a><span data-ttu-id="f672c-103">Interface IAMSetErrorLog</span><span class="sxs-lookup"><span data-stu-id="f672c-103">IAMSetErrorLog interface</span></span>

> [!Note]  
> <span data-ttu-id="f672c-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="f672c-104">\[Deprecated.</span></span> <span data-ttu-id="f672c-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f672c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f672c-106">L' `IAMSetErrorLog` interface définit ou récupère un journal des erreurs dans les [services de modification DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="f672c-106">The `IAMSetErrorLog` interface sets or retrieves an error log in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="f672c-107">L’objet Timeline implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="f672c-107">The timeline object implements this interface.</span></span> <span data-ttu-id="f672c-108">Les applications peuvent utiliser cette interface pour consigner les erreurs de rendu au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="f672c-108">Applications can use this interface to log rendering errors at run time.</span></span> <span data-ttu-id="f672c-109">Implémentez l’interface [**IAMErrorLog**](iamerrorlog.md) dans votre application, puis appelez la méthode [**IAMSetErrorLog ::p ut \_ ErrorLog**](iamseterrorlog-put-errorlog.md) sur la chronologie.</span><span class="sxs-lookup"><span data-stu-id="f672c-109">Implement the [**IAMErrorLog**](iamerrorlog.md) interface in your application, and then call the [**IAMSetErrorLog::put\_ErrorLog**](iamseterrorlog-put-errorlog.md) method on the timeline.</span></span>

<span data-ttu-id="f672c-110">Pour plus d’informations sur l’utilisation de cette interface, consultez [journalisation des erreurs](logging-errors.md).</span><span class="sxs-lookup"><span data-stu-id="f672c-110">For more information on using this interface, see [Logging Errors](logging-errors.md).</span></span>

## <a name="members"></a><span data-ttu-id="f672c-111">Membres</span><span class="sxs-lookup"><span data-stu-id="f672c-111">Members</span></span>

<span data-ttu-id="f672c-112">L’interface **IAMSetErrorLog** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f672c-112">The **IAMSetErrorLog** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f672c-113">**IAMSetErrorLog** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f672c-113">**IAMSetErrorLog** also has these types of members:</span></span>

-   [<span data-ttu-id="f672c-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f672c-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f672c-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f672c-115">Methods</span></span>

<span data-ttu-id="f672c-116">L’interface **IAMSetErrorLog** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="f672c-116">The **IAMSetErrorLog** interface has these methods.</span></span>



| <span data-ttu-id="f672c-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="f672c-117">Method</span></span>                                               | <span data-ttu-id="f672c-118">Description</span><span class="sxs-lookup"><span data-stu-id="f672c-118">Description</span></span>                                                 |
|:-----------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="f672c-119">**recevoir le \_ Journal des erreurs**</span><span class="sxs-lookup"><span data-stu-id="f672c-119">**get\_ErrorLog**</span></span>](iamseterrorlog-get-errorlog.md) | <span data-ttu-id="f672c-120">Récupère le journal des erreurs actuel de cet objet.</span><span class="sxs-lookup"><span data-stu-id="f672c-120">Retrieves the current error log for this object.</span></span><br/> |
| [<span data-ttu-id="f672c-121">**Placer le \_ Journal des erreurs**</span><span class="sxs-lookup"><span data-stu-id="f672c-121">**put\_ErrorLog**</span></span>](iamseterrorlog-put-errorlog.md) | <span data-ttu-id="f672c-122">Spécifie un journal des erreurs pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="f672c-122">Specifies an error log for the object.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="f672c-123">Notes</span><span class="sxs-lookup"><span data-stu-id="f672c-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f672c-124">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="f672c-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f672c-125">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f672c-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f672c-126">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f672c-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f672c-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f672c-127">Requirements</span></span>



| <span data-ttu-id="f672c-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f672c-128">Requirement</span></span> | <span data-ttu-id="f672c-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="f672c-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f672c-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="f672c-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f672c-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f672c-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f672c-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f672c-132">Library</span></span><br/> | <dl> <span data-ttu-id="f672c-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f672c-133"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
