---
title: Interface IMsRdpWorkspace2
description: Expose une méthode qui associe Connexions aux programmes RemoteApp et aux services Bureau à distance informations d’identification à une connexion.
ms.assetid: 7E09AF14-2D6C-4D6E-8033-C691D9DC8057
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpWorkspace
- Services Bureau à distance de l’interface IMsRdpWorkspace, Description
topic_type:
- apiref
api_name:
- IMsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d6b5ff193eec393b67029d355a0f0c1bc67c0ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032787"
---
# <a name="imsrdpworkspace2-interface"></a><span data-ttu-id="f68bf-105">Interface IMsRdpWorkspace2</span><span class="sxs-lookup"><span data-stu-id="f68bf-105">IMsRdpWorkspace2 interface</span></span>

<span data-ttu-id="f68bf-106">Expose une méthode qui associe Connexions aux programmes RemoteApp et aux services Bureau à distance informations d’identification à une connexion.</span><span class="sxs-lookup"><span data-stu-id="f68bf-106">Exposes a method that associates RemoteApp and Desktop Connection credentials with a connection.</span></span> <span data-ttu-id="f68bf-107">Cette interface est implémentée par le contrôle Services Bureau à distance Accès web.</span><span class="sxs-lookup"><span data-stu-id="f68bf-107">This interface is implemented by the Remote Desktop Services Web Access Control.</span></span> <span data-ttu-id="f68bf-108">Ce contrôle est un wrapper autour du client Connexion Bureau à distance (MsTscAx.dll) et du proxy d’exécution des connexions aux programmes RemoteApp et aux services Bureau à la connexion (Tswbprxy.exe).</span><span class="sxs-lookup"><span data-stu-id="f68bf-108">This control is a wrapper around the Remote Desktop Connection client (MsTscAx.dll) and the RemoteApp and Desktop Connections runtime proxy (Tswbprxy.exe).</span></span>

## <a name="members"></a><span data-ttu-id="f68bf-109">Membres</span><span class="sxs-lookup"><span data-stu-id="f68bf-109">Members</span></span>

<span data-ttu-id="f68bf-110">L’interface **IMsRdpWorkspace** hérite de [**IMsRdpWorkspace**](imsrdpworkspace.md).</span><span class="sxs-lookup"><span data-stu-id="f68bf-110">The **IMsRdpWorkspace** interface inherits from [**IMsRdpWorkspace**](imsrdpworkspace.md).</span></span> <span data-ttu-id="f68bf-111">**IMsRdpWorkspace2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f68bf-111">**IMsRdpWorkspace2** also has these types of members:</span></span>

-   [<span data-ttu-id="f68bf-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f68bf-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f68bf-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f68bf-113">Methods</span></span>

<span data-ttu-id="f68bf-114">L’interface **IMsRdpWorkspace** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="f68bf-114">The **IMsRdpWorkspace** interface has these methods.</span></span>



| <span data-ttu-id="f68bf-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="f68bf-115">Method</span></span>                                                        | <span data-ttu-id="f68bf-116">Description</span><span class="sxs-lookup"><span data-stu-id="f68bf-116">Description</span></span>                                                                    |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="f68bf-117">[**StartWorkspaceEx**](/previous-versions/windows/desktop/legacy/dn123459(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f68bf-117">[**StartWorkspaceEx**](/previous-versions/windows/desktop/legacy/dn123459(v=vs.85))</span></span> | <span data-ttu-id="f68bf-118">Associe les informations d’identification de l’utilisateur et les certificats à un ID de connexion.</span><span class="sxs-lookup"><span data-stu-id="f68bf-118">Associates user credentials and certificates with a connection ID.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="f68bf-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f68bf-119">Requirements</span></span>



| <span data-ttu-id="f68bf-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f68bf-120">Requirement</span></span> | <span data-ttu-id="f68bf-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f68bf-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f68bf-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f68bf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f68bf-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f68bf-123">Windows 8</span></span><br/>                                                                          |
| <span data-ttu-id="f68bf-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f68bf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f68bf-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f68bf-125">Windows Server 2012</span></span><br/>                                                                |
| <span data-ttu-id="f68bf-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f68bf-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f68bf-127"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f68bf-127"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |
| <span data-ttu-id="f68bf-128">IID</span><span class="sxs-lookup"><span data-stu-id="f68bf-128">IID</span></span><br/>                      | <span data-ttu-id="f68bf-129">IID \_ IMsRdpWorkspace2 est défini en tant que 145D0622-04CF-4FC3-A776-A82A9169CDF8</span><span class="sxs-lookup"><span data-stu-id="f68bf-129">IID\_IMsRdpWorkspace2 is defined as 145D0622-04CF-4FC3-A776-A82A9169CDF8</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="f68bf-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f68bf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f68bf-131">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="f68bf-131">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> <dt>

[<span data-ttu-id="f68bf-132">**IMsRdpWorkspace**</span><span class="sxs-lookup"><span data-stu-id="f68bf-132">**IMsRdpWorkspace**</span></span>](imsrdpworkspace.md)
</dt> </dl>

 

