---
title: Interface ITSRemoteProgram
description: Comprend des méthodes permettant de définir et de récupérer le mode RemoteApp et les paramètres de démarrage d’un programme RemoteApp, comme le chemin d’accès du fichier exécutable et le répertoire de travail.
ms.assetid: c9eec63b-7162-4bf8-b5d5-8cadb971ef98
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface ITSRemoteProgram
- Services Bureau à distance de l’interface ITSRemoteProgram, Description
topic_type:
- apiref
api_name:
- ITSRemoteProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfec99c109dfd3f69e22caf13071b77cd41f61bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033001"
---
# <a name="itsremoteprogram-interface"></a><span data-ttu-id="a864f-105">Interface ITSRemoteProgram</span><span class="sxs-lookup"><span data-stu-id="a864f-105">ITSRemoteProgram interface</span></span>

<span data-ttu-id="a864f-106">Comprend des méthodes permettant de définir et de récupérer le mode RemoteApp et les paramètres de démarrage d’un programme RemoteApp, comme le chemin d’accès du fichier exécutable et le répertoire de travail.</span><span class="sxs-lookup"><span data-stu-id="a864f-106">Includes methods to set and retrieve the RemoteApp mode and the start-up parameters for a RemoteApp program, such as the path of the executable file and the working directory.</span></span>

## <a name="members"></a><span data-ttu-id="a864f-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a864f-107">Members</span></span>

<span data-ttu-id="a864f-108">L’interface **ITSRemoteProgram** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="a864f-108">The **ITSRemoteProgram** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="a864f-109">**ITSRemoteProgram** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a864f-109">**ITSRemoteProgram** also has these types of members:</span></span>

-   [<span data-ttu-id="a864f-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a864f-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="a864f-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a864f-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a864f-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a864f-112">Methods</span></span>

<span data-ttu-id="a864f-113">L’interface **ITSRemoteProgram** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a864f-113">The **ITSRemoteProgram** interface has these methods.</span></span>



| <span data-ttu-id="a864f-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="a864f-114">Method</span></span>                                                            | <span data-ttu-id="a864f-115">Description</span><span class="sxs-lookup"><span data-stu-id="a864f-115">Description</span></span>                                                              |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="a864f-116">**ServerStartProgram**</span><span class="sxs-lookup"><span data-stu-id="a864f-116">**ServerStartProgram**</span></span>](itsremoteprogram-serverstartprogram.md) | <span data-ttu-id="a864f-117">Spécifie un programme RemoteApp à démarrer dans la session à distance.</span><span class="sxs-lookup"><span data-stu-id="a864f-117">Specifies a RemoteApp program to start in the remote session.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a864f-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a864f-118">Properties</span></span>

<span data-ttu-id="a864f-119">L’interface **ITSRemoteProgram** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a864f-119">The **ITSRemoteProgram** interface has these properties.</span></span>



| <span data-ttu-id="a864f-120">Propriété</span><span class="sxs-lookup"><span data-stu-id="a864f-120">Property</span></span>                                                                   | <span data-ttu-id="a864f-121">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="a864f-121">Access type</span></span>           | <span data-ttu-id="a864f-122">Description</span><span class="sxs-lookup"><span data-stu-id="a864f-122">Description</span></span>                    |
|:---------------------------------------------------------------------------|:----------------------|:-------------------------------|
| [<span data-ttu-id="a864f-123">**RemoteProgramMode**</span><span class="sxs-lookup"><span data-stu-id="a864f-123">**RemoteProgramMode**</span></span>](itsremoteprogram-remoteprogrammode.md)<br/> | <span data-ttu-id="a864f-124">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a864f-124">Read/write</span></span><br/> | <span data-ttu-id="a864f-125">Mode RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="a864f-125">The RemoteApp mode.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a864f-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a864f-126">Requirements</span></span>



| <span data-ttu-id="a864f-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a864f-127">Requirement</span></span> | <span data-ttu-id="a864f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="a864f-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a864f-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a864f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a864f-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a864f-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a864f-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a864f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a864f-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a864f-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a864f-133">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a864f-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="a864f-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a864f-134"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a864f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a864f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a864f-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a864f-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a864f-137">IID</span><span class="sxs-lookup"><span data-stu-id="a864f-137">IID</span></span><br/>                      | <span data-ttu-id="a864f-138">IID \_ ITSRemoteProgram est défini en tant que FDD029F9-467A-4c49-8529-64B521DBD1B4</span><span class="sxs-lookup"><span data-stu-id="a864f-138">IID\_ITSRemoteProgram is defined as FDD029F9-467A-4c49-8529-64B521DBD1B4</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="a864f-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a864f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a864f-140">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="a864f-140">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="a864f-141">Référence Connexion Bureau à distance par le Web</span><span class="sxs-lookup"><span data-stu-id="a864f-141">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

