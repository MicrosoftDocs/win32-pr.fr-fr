---
description: L’objet Microsoft. Windows. ActCtx fait référence aux manifestes et permet aux moteurs de script d’accéder aux assemblys côte à côte. L’objet Microsoft. Windows. ActCtx peut être utilisé pour créer une instance d’un assembly côte à côte avec des composants COM.
ms.assetid: 818e175e-2c58-4c44-87ce-4e97352fc3f3
title: Objet Microsoft. Windows. ActCtx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Microsoft.Windows.ActCtx
api_type:
- COM
api_location: ''
ms.openlocfilehash: 58290ec9d36d8e8428000422d0e1014335870149
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864213"
---
# <a name="microsoftwindowsactctx-object"></a><span data-ttu-id="3310c-104">Objet Microsoft. Windows. ActCtx</span><span class="sxs-lookup"><span data-stu-id="3310c-104">Microsoft.Windows.ActCtx object</span></span>

<span data-ttu-id="3310c-105">L’objet **Microsoft. Windows. ActCtx** fait référence aux manifestes et permet aux moteurs de script d’accéder aux assemblys côte à côte.</span><span class="sxs-lookup"><span data-stu-id="3310c-105">The **Microsoft.Windows.ActCtx** object references manifests and provides a way for scripting engines to access side-by-side assemblies.</span></span> <span data-ttu-id="3310c-106">L’objet **Microsoft. Windows. ActCtx** peut être utilisé pour créer une instance d’un assembly côte à côte avec des composants com.</span><span class="sxs-lookup"><span data-stu-id="3310c-106">The **Microsoft.Windows.ActCtx** object can be used to create an instance of a side-by-side assembly with COM components.</span></span>

<span data-ttu-id="3310c-107">L’objet **Microsoft. Windows. ActCtx** est fourni sous la forme d’un assembly dans Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3310c-107">The **Microsoft.Windows.ActCtx** object comes as an assembly in Windows Server 2003.</span></span> <span data-ttu-id="3310c-108">Il peut également être installé par les applications qui utilisent le Windows Installer pour l’installation et l’inclure en tant que module de fusion dans son package d’installation.</span><span class="sxs-lookup"><span data-stu-id="3310c-108">It can also be installed by applications that use the Windows Installer for setup and include it as a merge module in their installation package.</span></span>

## <a name="members"></a><span data-ttu-id="3310c-109">Membres</span><span class="sxs-lookup"><span data-stu-id="3310c-109">Members</span></span>

<span data-ttu-id="3310c-110">L’objet **Microsoft. Windows. ActCtx** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3310c-110">The **Microsoft.Windows.ActCtx** object has these types of members:</span></span>

-   [<span data-ttu-id="3310c-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3310c-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="3310c-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3310c-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3310c-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3310c-113">Methods</span></span>

<span data-ttu-id="3310c-114">L’objet **Microsoft. Windows. ActCtx** possède les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="3310c-114">The **Microsoft.Windows.ActCtx** object has these methods.</span></span>



| <span data-ttu-id="3310c-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="3310c-115">Method</span></span>                               | <span data-ttu-id="3310c-116">Description</span><span class="sxs-lookup"><span data-stu-id="3310c-116">Description</span></span>                                                                     |
|:-------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="3310c-117">**CreateObject**</span><span class="sxs-lookup"><span data-stu-id="3310c-117">**CreateObject**</span></span>](createobject.md) | <span data-ttu-id="3310c-118">Crée un objet dans le contexte du manifeste actuel.</span><span class="sxs-lookup"><span data-stu-id="3310c-118">Creates an object in the context of the current manifest.</span></span><br/>            |
| [<span data-ttu-id="3310c-119">**GetObject**</span><span class="sxs-lookup"><span data-stu-id="3310c-119">**GetObject**</span></span>](getobject.md)       | <span data-ttu-id="3310c-120">Obtient une instance d’un objet **Microsoft. Windows. ActCtx** existant.</span><span class="sxs-lookup"><span data-stu-id="3310c-120">Gets an instance of an existing **Microsoft.Windows.ActCtx** object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3310c-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3310c-121">Properties</span></span>

<span data-ttu-id="3310c-122">L’objet **Microsoft. Windows. ActCtx** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3310c-122">The **Microsoft.Windows.ActCtx** object has these properties.</span></span>



| <span data-ttu-id="3310c-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="3310c-123">Property</span></span>                                | <span data-ttu-id="3310c-124">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="3310c-124">Access type</span></span>          | <span data-ttu-id="3310c-125">Description</span><span class="sxs-lookup"><span data-stu-id="3310c-125">Description</span></span>                                    |
|:----------------------------------------|:---------------------|:-----------------------------------------------|
| [<span data-ttu-id="3310c-126">**Du**</span><span class="sxs-lookup"><span data-stu-id="3310c-126">**Manifest**</span></span>](manifest.md)<br/> | <span data-ttu-id="3310c-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3310c-127">Read-only</span></span><br/> | <span data-ttu-id="3310c-128">Obtient le contexte d’activation actif.</span><span class="sxs-lookup"><span data-stu-id="3310c-128">Gets the active activation context.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3310c-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3310c-129">Requirements</span></span>



| <span data-ttu-id="3310c-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3310c-130">Requirement</span></span> | <span data-ttu-id="3310c-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="3310c-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3310c-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3310c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3310c-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3310c-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="3310c-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3310c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3310c-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3310c-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




