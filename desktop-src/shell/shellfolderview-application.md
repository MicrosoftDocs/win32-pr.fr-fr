---
description: Contient l’objet d’application de l’objet.
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
ms.openlocfilehash: ba57c407183179f580b5b616ad039c22e6fea66c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973587"
---
# <a name="shellfolderviewapplication-property"></a><span data-ttu-id="845e0-103">ShellFolderView. application, propriété</span><span class="sxs-lookup"><span data-stu-id="845e0-103">ShellFolderView.Application property</span></span>

<span data-ttu-id="845e0-104">Contient l’objet d’application de l’objet.</span><span class="sxs-lookup"><span data-stu-id="845e0-104">Contains the object's Application object.</span></span>

<span data-ttu-id="845e0-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="845e0-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="845e0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="845e0-106">Syntax</span></span>


```JScript
objApplication = ShellFolderView.Application
```



## <a name="property-value"></a><span data-ttu-id="845e0-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="845e0-107">Property value</span></span>

<span data-ttu-id="845e0-108">Variable de type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui reçoit l’objet application.</span><span class="sxs-lookup"><span data-stu-id="845e0-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="845e0-109">Notes</span><span class="sxs-lookup"><span data-stu-id="845e0-109">Remarks</span></span>

<span data-ttu-id="845e0-110">La propriété d' **application** retourne l’objet Automation pris en charge par l’application qui contient le contrôle WebBrowser, si cet objet est accessible.</span><span class="sxs-lookup"><span data-stu-id="845e0-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="845e0-111">Sinon, cette propriété retourne l’objet Automation du contrôle WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="845e0-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="845e0-112">Utilisez cette propriété avec les commandes **Set** et **CreateObject** ou à l’aide de la commande **GetObject** pour créer et manipuler une instance de l’application Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="845e0-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="845e0-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="845e0-113">Requirements</span></span>



| <span data-ttu-id="845e0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="845e0-114">Requirement</span></span> | <span data-ttu-id="845e0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="845e0-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="845e0-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="845e0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="845e0-117">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="845e0-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="845e0-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="845e0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="845e0-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="845e0-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="845e0-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="845e0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="845e0-121"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="845e0-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="845e0-122">MIDL</span><span class="sxs-lookup"><span data-stu-id="845e0-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="845e0-123"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="845e0-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="845e0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="845e0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="845e0-125"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="845e0-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
