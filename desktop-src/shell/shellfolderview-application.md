---
description: 'ShellFolderView. application, propriété : contient l’objet application de l’objet.'
ms.assetid: 305766b1-a19f-4743-a9e3-6837b3f8ffe0
title: ShellFolderView. application, propriété (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 95ef542f91235b3b068e1b1b54768b4dd453d9b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083467"
---
# <a name="shellfolderviewapplication-property"></a><span data-ttu-id="9dc26-103">ShellFolderView. application, propriété</span><span class="sxs-lookup"><span data-stu-id="9dc26-103">ShellFolderView.Application property</span></span>

<span data-ttu-id="9dc26-104">Contient l’objet d’application de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9dc26-104">Contains the object's Application object.</span></span>

<span data-ttu-id="9dc26-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9dc26-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dc26-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9dc26-106">Syntax</span></span>


```JScript
objApplication = ShellFolderView.Application
```



## <a name="property-value"></a><span data-ttu-id="9dc26-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9dc26-107">Property value</span></span>

<span data-ttu-id="9dc26-108">Variable de type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui reçoit l’objet application.</span><span class="sxs-lookup"><span data-stu-id="9dc26-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dc26-109">Notes </span><span class="sxs-lookup"><span data-stu-id="9dc26-109">Remarks</span></span>

<span data-ttu-id="9dc26-110">La propriété d' **application** retourne l’objet Automation pris en charge par l’application qui contient le contrôle WebBrowser, si cet objet est accessible.</span><span class="sxs-lookup"><span data-stu-id="9dc26-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="9dc26-111">Sinon, cette propriété retourne l’objet Automation du contrôle WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="9dc26-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="9dc26-112">Utilisez cette propriété avec les commandes **Set** et **CreateObject** ou à l’aide de la commande **GetObject** pour créer et manipuler une instance de l’application Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="9dc26-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dc26-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9dc26-113">Requirements</span></span>



| <span data-ttu-id="9dc26-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9dc26-114">Requirement</span></span> | <span data-ttu-id="9dc26-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="9dc26-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dc26-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9dc26-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9dc26-117">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9dc26-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9dc26-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9dc26-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9dc26-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9dc26-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9dc26-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="9dc26-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dc26-121"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dc26-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="9dc26-122">MIDL</span><span class="sxs-lookup"><span data-stu-id="9dc26-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9dc26-123"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9dc26-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="9dc26-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9dc26-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dc26-125"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="9dc26-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
