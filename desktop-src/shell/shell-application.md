---
description: Contient l’objet d’application de l’objet.
ms.assetid: 5335f4dd-ca80-49c8-8953-e32a6e6308e0
title: Shell. application, propriété (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a9f9bd7fa28d2b277adfd8038c10c97efe16f51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868689"
---
# <a name="shellapplication-property"></a><span data-ttu-id="ece4d-103">Shell. application, propriété</span><span class="sxs-lookup"><span data-stu-id="ece4d-103">Shell.Application property</span></span>

<span data-ttu-id="ece4d-104">Contient l’objet d’application de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ece4d-104">Contains the object's Application object.</span></span>

<span data-ttu-id="ece4d-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ece4d-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ece4d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ece4d-106">Syntax</span></span>


```JScript
objApplication = Shell.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a><span data-ttu-id="ece4d-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ece4d-107">Property value</span></span>

<span data-ttu-id="ece4d-108">Variable de type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui reçoit l’objet application.</span><span class="sxs-lookup"><span data-stu-id="ece4d-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ece4d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="ece4d-109">Remarks</span></span>

<span data-ttu-id="ece4d-110">La propriété d' **application** retourne l’objet Automation pris en charge par l’application qui contient le contrôle WebBrowser, si cet objet est accessible.</span><span class="sxs-lookup"><span data-stu-id="ece4d-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="ece4d-111">Sinon, cette propriété retourne l’objet Automation du contrôle WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="ece4d-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="ece4d-112">Utilisez cette propriété avec les commandes **Set** et **CreateObject** ou à l’aide de la commande **GetObject** pour créer et manipuler une instance de l’application Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="ece4d-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="ece4d-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ece4d-113">Requirements</span></span>



| <span data-ttu-id="ece4d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ece4d-114">Requirement</span></span> | <span data-ttu-id="ece4d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ece4d-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece4d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ece4d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ece4d-117">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ece4d-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ece4d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ece4d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ece4d-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ece4d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ece4d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ece4d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ece4d-121"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ece4d-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="ece4d-122">MIDL</span><span class="sxs-lookup"><span data-stu-id="ece4d-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ece4d-123"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ece4d-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="ece4d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ece4d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ece4d-125"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="ece4d-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
