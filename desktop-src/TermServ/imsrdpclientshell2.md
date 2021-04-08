---
title: Interface IMsRdpClientShell2
description: Expose les propriétés qui lancent le client Connexion Bureau à distance à partir d’Bureau à distance Accès web (RD Accès web) ou d’autres portails Web.
ms.assetid: cc8ef78f-b7d6-42cd-bb67-8a8e1f33be08
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientShell2
- Services Bureau à distance de l’interface IMsRdpClientShell2, Description
topic_type:
- apiref
api_name:
- IMsRdpClientShell2
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb93fd938602b195f60877be884dbe0bd458a598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740549"
---
# <a name="imsrdpclientshell2-interface"></a><span data-ttu-id="26bdd-105">Interface IMsRdpClientShell2</span><span class="sxs-lookup"><span data-stu-id="26bdd-105">IMsRdpClientShell2 interface</span></span>

<span data-ttu-id="26bdd-106">Expose les propriétés qui lancent le client Connexion Bureau à distance à partir d’Bureau à distance Accès web (RD Accès web) ou d’autres portails Web.</span><span class="sxs-lookup"><span data-stu-id="26bdd-106">Exposes properties that launch the Remote Desktop Connection client from Remote Desktop Web Access (RD Web Access) or from other web portals.</span></span>

<span data-ttu-id="26bdd-107">Cette interface est implémentée par le contrôle Services Bureau à distance Accès web, qui est un wrapper autour du client Connexion Bureau à distance (MsTscAx.dll) et du proxy d’exécution des connexions aux programmes RemoteApp et aux services Bureau à reconnexion (Tswbprxy.exe).</span><span class="sxs-lookup"><span data-stu-id="26bdd-107">This interface is implemented by the Remote Desktop Services Web Access Control, which is a wrapper around the Remote Desktop Connection client (MsTscAx.dll) and the RemoteApp and Desktop Connections runtime proxy (Tswbprxy.exe).</span></span>

## <a name="members"></a><span data-ttu-id="26bdd-108">Membres</span><span class="sxs-lookup"><span data-stu-id="26bdd-108">Members</span></span>

<span data-ttu-id="26bdd-109">L’interface **IMsRdpClientShell2** hérite de **IMsRdpClientShell**.</span><span class="sxs-lookup"><span data-stu-id="26bdd-109">The **IMsRdpClientShell2** interface inherits from **IMsRdpClientShell**.</span></span> <span data-ttu-id="26bdd-110">**IMsRdpClientShell2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="26bdd-110">**IMsRdpClientShell2** also has these types of members:</span></span>

-   [<span data-ttu-id="26bdd-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="26bdd-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26bdd-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="26bdd-112">Properties</span></span>

<span data-ttu-id="26bdd-113">L’interface **IMsRdpClientShell2** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="26bdd-113">The **IMsRdpClientShell2** interface has these properties.</span></span>



| <span data-ttu-id="26bdd-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="26bdd-114">Property</span></span>                                                                               | <span data-ttu-id="26bdd-115">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="26bdd-115">Access type</span></span>          | <span data-ttu-id="26bdd-116">Description</span><span class="sxs-lookup"><span data-stu-id="26bdd-116">Description</span></span>                                                                                                                                                                       |
|:---------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26bdd-117">**MsRdpWorkspace**</span><span class="sxs-lookup"><span data-stu-id="26bdd-117">**MsRdpWorkspace**</span></span>](imsrdpclientshell2-msrdpworkspace.md)<br/>                 | <span data-ttu-id="26bdd-118">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26bdd-118">Read-only</span></span><br/> | <span data-ttu-id="26bdd-119">Récupère un pointeur vers l’interface [**IMsRdpWorkspace**](imsrdpworkspace.md) , qui est utilisée pour gérer les informations d’identification et les connexions de connexions aux programmes RemoteApp et aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="26bdd-119">Retrieves a pointer to the [**IMsRdpWorkspace**](imsrdpworkspace.md) interface, which is used to manage RemoteApp and Desktop Connection credentials and connections.</span></span><br/> |
| [<span data-ttu-id="26bdd-120">**SecuredSettingsEnabled**</span><span class="sxs-lookup"><span data-stu-id="26bdd-120">**SecuredSettingsEnabled**</span></span>](imsrdpclientshell2-securedsettingsenabled.md)<br/> | <span data-ttu-id="26bdd-121">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26bdd-121">Read-only</span></span><br/> | <span data-ttu-id="26bdd-122">Récupère une valeur qui indique si la page Web active se trouve dans une zone de sécurité d’URL Internet Explorer approuvée.</span><span class="sxs-lookup"><span data-stu-id="26bdd-122">Retrieves a value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.</span></span><br/>                                                      |



 

## <a name="requirements"></a><span data-ttu-id="26bdd-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26bdd-123">Requirements</span></span>



| <span data-ttu-id="26bdd-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26bdd-124">Requirement</span></span> | <span data-ttu-id="26bdd-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="26bdd-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="26bdd-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26bdd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="26bdd-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="26bdd-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="26bdd-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26bdd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="26bdd-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="26bdd-129">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="26bdd-130">DLL</span><span class="sxs-lookup"><span data-stu-id="26bdd-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26bdd-131"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26bdd-131"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26bdd-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26bdd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26bdd-133">**IMsRdpWorkspace**</span><span class="sxs-lookup"><span data-stu-id="26bdd-133">**IMsRdpWorkspace**</span></span>](imsrdpworkspace.md)
</dt> </dl>

 

 





