---
description: L’interface IAMErrorLog fournit une méthode de rappel pour la journalisation des erreurs dans les services de modification DirectShow (DES). DES n’implémente pas cette interface.
ms.assetid: d5366072-2de7-437c-b198-cbc4d8623c45
title: Interface IAMErrorLog (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 48a1515ebf3e7c829a3e23772f1f84ee76c36ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537452"
---
# <a name="iamerrorlog-interface"></a><span data-ttu-id="f1aef-103">Interface IAMErrorLog</span><span class="sxs-lookup"><span data-stu-id="f1aef-103">IAMErrorLog interface</span></span>

> [!Note]  
> <span data-ttu-id="f1aef-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="f1aef-104">\[Deprecated.</span></span> <span data-ttu-id="f1aef-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f1aef-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f1aef-106">L' `IAMErrorLog` interface fournit une méthode de rappel pour la journalisation des erreurs dans les [services de modification DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="f1aef-106">The `IAMErrorLog` interface provides a callback method for error logging in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="f1aef-107">DES n’implémente pas cette interface.</span><span class="sxs-lookup"><span data-stu-id="f1aef-107">DES does not implement this interface.</span></span> <span data-ttu-id="f1aef-108">Pour effectuer la journalisation des erreurs, implémentez cette interface dans votre application et appelez [**IAMSetErrorLog ::p ut \_ ErrorLog**](iamseterrorlog-put-errorlog.md) sur la chronologie.</span><span class="sxs-lookup"><span data-stu-id="f1aef-108">To perform error logging, implement this interface in your application and call [**IAMSetErrorLog::put\_ErrorLog**](iamseterrorlog-put-errorlog.md) on the timeline.</span></span> <span data-ttu-id="f1aef-109">Si une erreur se produit lors du rendu du projet, les appellent la méthode [**IAMErrorLog :: LogError**](iamerrorlog-logerror.md) implémentée par votre application.</span><span class="sxs-lookup"><span data-stu-id="f1aef-109">If an error occurs when you render the project, DES will call the [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) method implemented by your application.</span></span>

<span data-ttu-id="f1aef-110">DES enregistre les erreurs uniquement lorsque vous affichez un projet à l’aide de l’interface [**IRenderEngine**](irenderengine.md) .</span><span class="sxs-lookup"><span data-stu-id="f1aef-110">DES logs errors only when you render a project using the [**IRenderEngine**](irenderengine.md) interface.</span></span> <span data-ttu-id="f1aef-111">Par exemple, si vous enregistrez un projet sous la forme d’un graphique de filtre DirectShow (format. GRF) et que vous lisez le fichier de graphique, il n’y a pas de journalisation des erreurs.</span><span class="sxs-lookup"><span data-stu-id="f1aef-111">For example, if you save a project as a DirectShow filter graph (.grf format) and play the graph file, there is no error logging.</span></span> <span data-ttu-id="f1aef-112">Pour plus d’informations sur l’utilisation de cette interface, consultez [journalisation des erreurs](logging-errors.md).</span><span class="sxs-lookup"><span data-stu-id="f1aef-112">For more information on using this interface, see [Logging Errors](logging-errors.md).</span></span>

## <a name="members"></a><span data-ttu-id="f1aef-113">Membres</span><span class="sxs-lookup"><span data-stu-id="f1aef-113">Members</span></span>

<span data-ttu-id="f1aef-114">L’interface **IAMErrorLog** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f1aef-114">The **IAMErrorLog** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f1aef-115">**IAMErrorLog** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f1aef-115">**IAMErrorLog** also has these types of members:</span></span>

-   [<span data-ttu-id="f1aef-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f1aef-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f1aef-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f1aef-117">Methods</span></span>

<span data-ttu-id="f1aef-118">L’interface **IAMErrorLog** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="f1aef-118">The **IAMErrorLog** interface has these methods.</span></span>



| <span data-ttu-id="f1aef-119">Méthode</span><span class="sxs-lookup"><span data-stu-id="f1aef-119">Method</span></span>                                   | <span data-ttu-id="f1aef-120">Description</span><span class="sxs-lookup"><span data-stu-id="f1aef-120">Description</span></span>               |
|:-----------------------------------------|:--------------------------|
| [<span data-ttu-id="f1aef-121">**LogError**</span><span class="sxs-lookup"><span data-stu-id="f1aef-121">**LogError**</span></span>](iamerrorlog-logerror.md) | <span data-ttu-id="f1aef-122">Enregistre une erreur.</span><span class="sxs-lookup"><span data-stu-id="f1aef-122">Logs an error.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f1aef-123">Notes</span><span class="sxs-lookup"><span data-stu-id="f1aef-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f1aef-124">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="f1aef-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f1aef-125">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f1aef-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f1aef-126">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f1aef-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f1aef-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1aef-127">Requirements</span></span>



| <span data-ttu-id="f1aef-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1aef-128">Requirement</span></span> | <span data-ttu-id="f1aef-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1aef-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1aef-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="f1aef-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f1aef-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1aef-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f1aef-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f1aef-132">Library</span></span><br/> | <dl> <span data-ttu-id="f1aef-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1aef-133"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
