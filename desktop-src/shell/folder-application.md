---
description: Contient l’objet d’application du dossier.
ms.assetid: 1dba83eb-1af6-42d9-b2c9-ab7767888efe
title: Propriété Folder. application (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Application
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: 13a6a90dd324498c332f7bf580ff5ec987a0c5b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484040"
---
# <a name="folderapplication-property"></a><span data-ttu-id="1306b-103">Folder. application, propriété</span><span class="sxs-lookup"><span data-stu-id="1306b-103">Folder.Application property</span></span>

<span data-ttu-id="1306b-104">Contient l’objet d’application du dossier.</span><span class="sxs-lookup"><span data-stu-id="1306b-104">Contains the folder's Application object.</span></span>

<span data-ttu-id="1306b-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1306b-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1306b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1306b-106">Syntax</span></span>


```JScript
Application = Folder.Application
```



## <a name="property-value"></a><span data-ttu-id="1306b-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1306b-107">Property value</span></span>

<span data-ttu-id="1306b-108">Référence d’objet à l’objet d’application.</span><span class="sxs-lookup"><span data-stu-id="1306b-108">An object reference to the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1306b-109">Notes</span><span class="sxs-lookup"><span data-stu-id="1306b-109">Remarks</span></span>

<span data-ttu-id="1306b-110">La propriété d' **application** retourne l’objet Automation pris en charge par l’application qui contient le contrôle WebBrowser, si cet objet est accessible.</span><span class="sxs-lookup"><span data-stu-id="1306b-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="1306b-111">Sinon, cette propriété retourne l’objet Automation du contrôle WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="1306b-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="1306b-112">Utilisez cette propriété avec les commandes **Set** et **CreateObject** ou à l’aide de la commande **GetObject** pour créer et manipuler une instance de l’application Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="1306b-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Internet Explorer application.</span></span>

> [!Note]  
> <span data-ttu-id="1306b-113">Toutes les méthodes ne sont pas implémentées pour tous les dossiers.</span><span class="sxs-lookup"><span data-stu-id="1306b-113">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="1306b-114">Par exemple, la méthode [**ParseName**](folder-parsename.md) n’est pas implémentée pour le dossier du panneau de configuration ( \_ contrôles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="1306b-114">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="1306b-115">Si vous tentez d’appeler une méthode non implémentée, une erreur 0x800A01BD (Decimal 445) est générée.</span><span class="sxs-lookup"><span data-stu-id="1306b-115">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1306b-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1306b-116">Requirements</span></span>



| <span data-ttu-id="1306b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1306b-117">Requirement</span></span> | <span data-ttu-id="1306b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1306b-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1306b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1306b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1306b-120">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1306b-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                 |
| <span data-ttu-id="1306b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1306b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1306b-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1306b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1306b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1306b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1306b-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1306b-124"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1306b-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="1306b-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1306b-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1306b-126"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




