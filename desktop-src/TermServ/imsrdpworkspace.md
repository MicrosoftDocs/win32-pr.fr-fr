---
title: Interface IMsRdpWorkspace
description: Expose des méthodes qui gèrent les informations d’identification et les connexions de Connexions aux programmes RemoteApp et aux services Bureau à distance.
ms.assetid: cddcdfc2-b30a-4d00-84c2-ad036ab6288f
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
ms.openlocfilehash: 0ba55a02c5d984bc87aa05caffd42b3a3b965c43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941750"
---
# <a name="imsrdpworkspace-interface"></a><span data-ttu-id="8153c-105">Interface IMsRdpWorkspace</span><span class="sxs-lookup"><span data-stu-id="8153c-105">IMsRdpWorkspace interface</span></span>

<span data-ttu-id="8153c-106">Expose des méthodes qui gèrent les informations d’identification et les connexions de Connexions aux programmes RemoteApp et aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="8153c-106">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span> <span data-ttu-id="8153c-107">Cette interface est implémentée par le contrôle Services Bureau à distance Accès web.</span><span class="sxs-lookup"><span data-stu-id="8153c-107">This interface is implemented by the Remote Desktop Services Web Access Control.</span></span> <span data-ttu-id="8153c-108">Ce contrôle est un wrapper autour du client Connexion Bureau à distance (MsTscAx.dll) et du proxy d’exécution des connexions aux programmes RemoteApp et aux services Bureau à la connexion (Tswbprxy.exe).</span><span class="sxs-lookup"><span data-stu-id="8153c-108">This control is a wrapper around the Remote Desktop Connection client (MsTscAx.dll) and the RemoteApp and Desktop Connections runtime proxy (Tswbprxy.exe).</span></span>

## <a name="members"></a><span data-ttu-id="8153c-109">Membres</span><span class="sxs-lookup"><span data-stu-id="8153c-109">Members</span></span>

<span data-ttu-id="8153c-110">L’interface **IMsRdpWorkspace** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="8153c-110">The **IMsRdpWorkspace** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="8153c-111">**IMsRdpWorkspace** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8153c-111">**IMsRdpWorkspace** also has these types of members:</span></span>

-   [<span data-ttu-id="8153c-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8153c-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8153c-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8153c-113">Methods</span></span>

<span data-ttu-id="8153c-114">L’interface **IMsRdpWorkspace** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8153c-114">The **IMsRdpWorkspace** interface has these methods.</span></span>



| <span data-ttu-id="8153c-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="8153c-115">Method</span></span>                                                                                   | <span data-ttu-id="8153c-116">Description</span><span class="sxs-lookup"><span data-stu-id="8153c-116">Description</span></span>                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8153c-117">[**ClearWorkspaceCredential**](/previous-versions/windows/desktop/legacy/ee351596(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8153c-117">[**ClearWorkspaceCredential**](/previous-versions/windows/desktop/legacy/ee351596(v=vs.85))</span></span>             | <span data-ttu-id="8153c-118">Supprime les informations d’identification de l’utilisateur associées à l’ID de connexion spécifié.</span><span class="sxs-lookup"><span data-stu-id="8153c-118">Deletes the user credentials associated with the specified connection ID.</span></span><br/>                                                                                  |
| <span data-ttu-id="8153c-119">[**DisconnectWorkspace**](/previous-versions/windows/desktop/legacy/ee351597(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8153c-119">[**DisconnectWorkspace**](/previous-versions/windows/desktop/legacy/ee351597(v=vs.85))</span></span>                       | <span data-ttu-id="8153c-120">Déconnecte toutes les connexions existantes associées à l’ID de connexion spécifié et supprime les informations d’identification de l’utilisateur correspondant de la Banque d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="8153c-120">Disconnects all existing connections associated with the specified connection ID and deletes the corresponding user credentials from the credential store.</span></span><br/> |
| <span data-ttu-id="8153c-121">[**IsWorkspaceCredentialSpecified**](/previous-versions/windows/desktop/legacy/ee351598(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8153c-121">[**IsWorkspaceCredentialSpecified**](/previous-versions/windows/desktop/legacy/ee351598(v=vs.85))</span></span> | <span data-ttu-id="8153c-122">Détermine si les informations d’identification de l’utilisateur existent pour l’ID de connexion spécifié.</span><span class="sxs-lookup"><span data-stu-id="8153c-122">Determines whether user credentials exist for the specified connection ID.</span></span><br/>                                                                                 |
| <span data-ttu-id="8153c-123">[**IsWorkspaceSSOEnabled**](/previous-versions/windows/desktop/legacy/ee351599(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8153c-123">[**IsWorkspaceSSOEnabled**](/previous-versions/windows/desktop/legacy/ee351599(v=vs.85))</span></span>                   | <span data-ttu-id="8153c-124">Détermine si l’authentification unique (SSO) est activée pour Connexions aux programmes RemoteApp et aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="8153c-124">Determines whether single sign on (SSO) is enabled for RemoteApp and Desktop Connection.</span></span><br/>                                                                   |
| <span data-ttu-id="8153c-125">[**OnAuthenticated**](/previous-versions/windows/desktop/legacy/ee351600(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8153c-125">[**OnAuthenticated**](/previous-versions/windows/desktop/legacy/ee351600(v=vs.85))</span></span>                               | <span data-ttu-id="8153c-126">Marque l’authentification des informations d’identification de l’utilisateur pour l’ID de connexion, puis affiche la notification de connexion dans la zone de notification de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="8153c-126">Marks the authentication of user credentials for the connection ID, and subsequently shows the connect notification in the taskbar notification area.</span></span> <br/>     |
| <span data-ttu-id="8153c-127">[**StartWorkspace**](/previous-versions/windows/desktop/legacy/ee351601(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8153c-127">[**StartWorkspace**](/previous-versions/windows/desktop/legacy/ee351601(v=vs.85))</span></span>                                 | <span data-ttu-id="8153c-128">Associe les informations d’identification de l’utilisateur et les certificats à un ID de connexion.</span><span class="sxs-lookup"><span data-stu-id="8153c-128">Associates user credentials and certificates with a connection ID.</span></span><br/>                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="8153c-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8153c-129">Requirements</span></span>



| <span data-ttu-id="8153c-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8153c-130">Requirement</span></span> | <span data-ttu-id="8153c-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="8153c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8153c-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8153c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8153c-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8153c-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8153c-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8153c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8153c-135">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8153c-135">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="8153c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8153c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8153c-137"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8153c-137"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |
| <span data-ttu-id="8153c-138">IID</span><span class="sxs-lookup"><span data-stu-id="8153c-138">IID</span></span><br/>                      | <span data-ttu-id="8153c-139">IID \_ IMsRdpWorkspace est défini en tant que 145D0621-04CF-4FC2-A766-A81A9069CDF8</span><span class="sxs-lookup"><span data-stu-id="8153c-139">IID\_IMsRdpWorkspace is defined as 145D0621-04CF-4FC2-A766-A81A9069CDF8</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="8153c-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8153c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8153c-141">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="8153c-141">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> </dl>

 

