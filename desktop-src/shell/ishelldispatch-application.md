---
description: Contient un objet qui représente une application.
ms.assetid: 61B85691-399D-41c1-9901-825345A38E5A
title: IShellDispatch. application, propriété (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5adeb5663220309310c7cccb323be877de909516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527357"
---
# <a name="ishelldispatchapplication-property"></a><span data-ttu-id="b7126-103">IShellDispatch. application, propriété</span><span class="sxs-lookup"><span data-stu-id="b7126-103">IShellDispatch.Application property</span></span>

<span data-ttu-id="b7126-104">Contient un objet qui représente une application.</span><span class="sxs-lookup"><span data-stu-id="b7126-104">Contains an object that represents an application.</span></span>

<span data-ttu-id="b7126-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b7126-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7126-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7126-106">Syntax</span></span>


```JScript
objApplication = IShellDispatch.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a><span data-ttu-id="b7126-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b7126-107">Property value</span></span>

<span data-ttu-id="b7126-108">Variable de type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui reçoit l’objet application.</span><span class="sxs-lookup"><span data-stu-id="b7126-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7126-109">Notes</span><span class="sxs-lookup"><span data-stu-id="b7126-109">Remarks</span></span>

<span data-ttu-id="b7126-110">Cette propriété est implémentée et accessible via la propriété [**Shell. EjectPC**](shell-ejectpc.md) .</span><span class="sxs-lookup"><span data-stu-id="b7126-110">This property is implemented and accessed through the [**Shell.EjectPC**](shell-ejectpc.md) property.</span></span>

<span data-ttu-id="b7126-111">La propriété d' **application** retourne l’objet Automation pris en charge par l’application qui contient le contrôle WebBrowser, si cet objet est accessible.</span><span class="sxs-lookup"><span data-stu-id="b7126-111">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="b7126-112">Sinon, cette propriété retourne l’objet Automation du contrôle WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="b7126-112">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="b7126-113">Utilisez cette propriété avec les commandes **Set** et **CreateObject** ou à l’aide de la commande **GetObject** pour créer et manipuler une instance de l’application Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b7126-113">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7126-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b7126-114">Requirements</span></span>



| <span data-ttu-id="b7126-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7126-115">Requirement</span></span> | <span data-ttu-id="b7126-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7126-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7126-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7126-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b7126-118">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7126-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b7126-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7126-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b7126-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7126-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b7126-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7126-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7126-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7126-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b7126-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="b7126-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b7126-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b7126-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b7126-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b7126-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7126-126"><dt>Shell32.dll (version 4,71 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="b7126-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
