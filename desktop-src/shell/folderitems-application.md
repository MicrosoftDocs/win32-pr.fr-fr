---
description: Contient l’objet application de la collection d’éléments Folder.
ms.assetid: 2cd4243e-a5a6-4de4-b310-f74558ac0fbe
title: FolderItems. application, propriété (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7f073b81106923f889ca5209c0aa492f4c4bbd60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111723"
---
# <a name="folderitemsapplication-property"></a><span data-ttu-id="4cfb3-103">FolderItems. application, propriété</span><span class="sxs-lookup"><span data-stu-id="4cfb3-103">FolderItems.Application property</span></span>

<span data-ttu-id="4cfb3-104">Contient l’objet **application** de la collection d’éléments Folder.</span><span class="sxs-lookup"><span data-stu-id="4cfb3-104">Contains the **Application** object of the folder items collection.</span></span>

<span data-ttu-id="4cfb3-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="4cfb3-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cfb3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4cfb3-106">Syntax</span></span>


```JScript
objApplication = FolderItems.Application
```



## <a name="property-value"></a><span data-ttu-id="4cfb3-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4cfb3-107">Property value</span></span>

<span data-ttu-id="4cfb3-108">Référence d’objet à l’objet d’application.</span><span class="sxs-lookup"><span data-stu-id="4cfb3-108">An object reference to the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cfb3-109">Notes</span><span class="sxs-lookup"><span data-stu-id="4cfb3-109">Remarks</span></span>

<span data-ttu-id="4cfb3-110">La propriété d' **application** retourne l’objet Automation pris en charge par l’application qui contient le contrôle WebBrowser, si cet objet est accessible.</span><span class="sxs-lookup"><span data-stu-id="4cfb3-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="4cfb3-111">Sinon, cette propriété retourne l’objet Automation du contrôle WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="4cfb3-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="4cfb3-112">Utilisez cette propriété avec les commandes **Set** et **CreateObject** ou à l’aide de la commande **GetObject** pour créer et manipuler une instance de l’application Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="4cfb3-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cfb3-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4cfb3-113">Requirements</span></span>



| <span data-ttu-id="4cfb3-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4cfb3-114">Requirement</span></span> | <span data-ttu-id="4cfb3-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cfb3-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cfb3-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4cfb3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4cfb3-117">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4cfb3-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4cfb3-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4cfb3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4cfb3-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4cfb3-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4cfb3-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="4cfb3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cfb3-121"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cfb3-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="4cfb3-122">MIDL</span><span class="sxs-lookup"><span data-stu-id="4cfb3-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4cfb3-123"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4cfb3-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="4cfb3-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4cfb3-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cfb3-125"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="4cfb3-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




