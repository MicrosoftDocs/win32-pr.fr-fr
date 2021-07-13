---
description: Implémente l’interface IInkDesktopHost.
ms.assetid: 7a577536-405b-400d-89bc-c3b3894b448d
title: InkDesktopHost, classe
ms.topic: language-reference
ms.date: 02/03/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDesktopHost
api_type:
- COM
api_location:
- InkPresenterDesktop.idl
ms.openlocfilehash: 74eebdbdfdbe3a4018d63b1f2161687152ebb5cc
ms.sourcegitcommit: 1f917afc149b5cc449a4a25a87de311e4842734b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/13/2021
ms.locfileid: "113689222"
---
# <a name="inkdesktophost-class"></a><span data-ttu-id="b7a20-103">InkDesktopHost, classe</span><span class="sxs-lookup"><span data-stu-id="b7a20-103">InkDesktopHost class</span></span>

<span data-ttu-id="b7a20-104">Implémente l’interface [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) .</span><span class="sxs-lookup"><span data-stu-id="b7a20-104">Implements the [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) interface.</span></span>

<span data-ttu-id="b7a20-105">Un objet [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) permet l’entrée d’encre, le traitement et le rendu via la création d’un thread d’application pour héberger un objet [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) et l’insérer dans l’arborescence d’éléments visuels [DirectComposition](../directcomp/directcomposition-portal.md) de l’application.</span><span class="sxs-lookup"><span data-stu-id="b7a20-105">An [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) object enables ink input, processing, and rendering through the creation of an app thread to host an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object and insert it into the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span>

## <a name="members"></a><span data-ttu-id="b7a20-106">Membres</span><span class="sxs-lookup"><span data-stu-id="b7a20-106">Members</span></span>

<span data-ttu-id="b7a20-107">La classe **InkDesktopHost** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b7a20-107">The **InkDesktopHost** class inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b7a20-108">**InkDesktopHost** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b7a20-108">**InkDesktopHost** also has these types of members:</span></span>

- [<span data-ttu-id="b7a20-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b7a20-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b7a20-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b7a20-110">Methods</span></span>

<span data-ttu-id="b7a20-111">La classe **InkDesktopHost** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b7a20-111">The **InkDesktopHost** class has these methods.</span></span>

| <span data-ttu-id="b7a20-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="b7a20-112">Method</span></span> | <span data-ttu-id="b7a20-113">Description</span><span class="sxs-lookup"><span data-stu-id="b7a20-113">Description</span></span> |
|---|---|
| [<span data-ttu-id="b7a20-114">**CreateAndInitializeInkPresenter**</span><span class="sxs-lookup"><span data-stu-id="b7a20-114">**CreateAndInitializeInkPresenter**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createandinitializeinkpresenter) | <span data-ttu-id="b7a20-115">Crée un objet [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) sur un thread d’application, le connecte à l’arborescence d’éléments visuels [DirectComposition](../directcomp/directcomposition-portal.md) de l’application et définit la taille de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b7a20-115">Creates an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object on an application thread, connects it to the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree, and sets the size of the object.</span></span><br/> |
| [<span data-ttu-id="b7a20-116">**CreateInkPresenter**</span><span class="sxs-lookup"><span data-stu-id="b7a20-116">**CreateInkPresenter**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createinkpresenter) | <span data-ttu-id="b7a20-117">Crée un objet [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) sur un thread d’application.</span><span class="sxs-lookup"><span data-stu-id="b7a20-117">Creates an [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) object on an application thread.</span></span><br/> |
| [<span data-ttu-id="b7a20-118">**QueueWorkItem**</span><span class="sxs-lookup"><span data-stu-id="b7a20-118">**QueueWorkItem**</span></span>](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-queueworkitem) | <span data-ttu-id="b7a20-119">Ajoutez une opération d’écriture manuscrite à une file d’attente de travail pour l’exécuter sur le thread **InkDesktopHost** .</span><span class="sxs-lookup"><span data-stu-id="b7a20-119">Add an ink operation to a work queue for execution on the **InkDesktopHost** thread.</span></span><br/> |

## <a name="creationaccess-functions"></a><span data-ttu-id="b7a20-120">Fonctions d’accès de création \\</span><span class="sxs-lookup"><span data-stu-id="b7a20-120">Creation\\Access Functions</span></span>

<span data-ttu-id="b7a20-121">Appelez [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) avec l’identificateur de classe <strong>InkDesktopHost</strong> pour récupérer une référence à l’objet.</span><span class="sxs-lookup"><span data-stu-id="b7a20-121">Call [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the class identifier <strong>InkDesktopHost</strong> to retrieve a reference to the object.</span></span>

``` C++
CoCreateInstance(__uuidof(InkDesktopHost), 
  nullptr, 
  CLSCTX_INPROC_SERVER, 
  IID_PPV_ARGS(&_spInkHost));
```

## <a name="requirements"></a><span data-ttu-id="b7a20-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7a20-122">Requirements</span></span>

| <span data-ttu-id="b7a20-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7a20-123">Requirement</span></span> | <span data-ttu-id="b7a20-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7a20-124">Value</span></span> |
|---|---|
| <span data-ttu-id="b7a20-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7a20-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b7a20-126">Windows 10 \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7a20-126">Windows 10 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b7a20-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7a20-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b7a20-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7a20-128">None supported</span></span><br/> |
| <span data-ttu-id="b7a20-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7a20-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7a20-130"><dt>InkPresenterDesktop. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7a20-130"><dt>InkPresenterDesktop.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7a20-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="b7a20-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b7a20-132"><dt>InkPresenterDesktop. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b7a20-132"><dt>InkPresenterDesktop.idl</dt></span></span> </dl> |
| <span data-ttu-id="b7a20-133">IID</span><span class="sxs-lookup"><span data-stu-id="b7a20-133">IID</span></span><br/>                      | <span data-ttu-id="b7a20-134">IID \_ IInkDesktopHost est défini en tant que 4ce7d875-A981-4140-a1ff-ad93258e8d59</span><span class="sxs-lookup"><span data-stu-id="b7a20-134">IID\_IInkDesktopHost is defined as 4ce7d875-a981-4140-a1ff-ad93258e8d59</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="b7a20-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7a20-135">Related topics</span></span>

<span data-ttu-id="b7a20-136">[Classes de présentateur d’encre](ink-presenter-classes.md), [interactions de stylet et](/windows/uwp/design/input/pen-and-stylus-interactions)de stylet, [exemple d’analyse](/samples/microsoft/windows-universal-samples/inkanalysis/)de l’encre, exemple d' [encrage simple](/samples/microsoft/windows-universal-samples/simpleink/), [exemple d’écriture](/samples/microsoft/windows-universal-samples/complexink/) manuscrite complexe</span><span class="sxs-lookup"><span data-stu-id="b7a20-136">[Ink presenter classes](ink-presenter-classes.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
