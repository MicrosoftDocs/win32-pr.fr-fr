---
title: Interface IMsRdpClientShell
description: Les paramètres client Connexion Bureau à distance (RDC) utilisés pour lancer le client à partir d’Bureau à distance Accès web (RD Accès web) ou d’autres portails Web.
ms.assetid: 05ca2e90-656a-40a3-a438-29d7985e9feb
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientShell
- Services Bureau à distance de l’interface IMsRdpClientShell, Description
topic_type:
- apiref
api_name:
- IMsRdpClientShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b529ed1819864e5fc6106472b33ddd00312560c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466002"
---
# <a name="imsrdpclientshell-interface"></a><span data-ttu-id="b874c-105">Interface IMsRdpClientShell</span><span class="sxs-lookup"><span data-stu-id="b874c-105">IMsRdpClientShell interface</span></span>

<span data-ttu-id="b874c-106">Les paramètres client Connexion Bureau à distance (RDC) utilisés pour lancer le client à partir d’Bureau à distance Accès web (RD Accès web) ou d’autres portails Web.</span><span class="sxs-lookup"><span data-stu-id="b874c-106">Remote Desktop Connection (RDC) client settings that are used to launch the client from Remote Desktop Web Access (RD Web Access) or from other web portals.</span></span>

## <a name="members"></a><span data-ttu-id="b874c-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b874c-107">Members</span></span>

<span data-ttu-id="b874c-108">L’interface **IMsRdpClientShell** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="b874c-108">The **IMsRdpClientShell** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="b874c-109">**IMsRdpClientShell** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b874c-109">**IMsRdpClientShell** also has these types of members:</span></span>

-   [<span data-ttu-id="b874c-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b874c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="b874c-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b874c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b874c-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b874c-112">Methods</span></span>

<span data-ttu-id="b874c-113">L’interface **IMsRdpClientShell** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b874c-113">The **IMsRdpClientShell** interface has these methods.</span></span>



| <span data-ttu-id="b874c-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="b874c-114">Method</span></span>                                                     | <span data-ttu-id="b874c-115">Description</span><span class="sxs-lookup"><span data-stu-id="b874c-115">Description</span></span>                                                  |
|:-----------------------------------------------------------|:-------------------------------------------------------------|
| <span data-ttu-id="b874c-116">[**GetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381303(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b874c-116">[**GetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381303(v=vs.85))</span></span> | <span data-ttu-id="b874c-117">Récupère une propriété RDP unique.</span><span class="sxs-lookup"><span data-stu-id="b874c-117">Retrieves a single RDP property.</span></span><br/>                  |
| [<span data-ttu-id="b874c-118">**Lancer**</span><span class="sxs-lookup"><span data-stu-id="b874c-118">**Launch**</span></span>](imsrdpclientshell-launch.md)                 | <span data-ttu-id="b874c-119">Lance le contenu du fichier distant à partir du portail Web.</span><span class="sxs-lookup"><span data-stu-id="b874c-119">Launches remote file content from the web portal.</span></span><br/> |
| <span data-ttu-id="b874c-120">[**SetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381312(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b874c-120">[**SetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381312(v=vs.85))</span></span> | <span data-ttu-id="b874c-121">Définit une propriété RDP unique.</span><span class="sxs-lookup"><span data-stu-id="b874c-121">Sets a single RDP property.</span></span><br/>                       |



 

### <a name="properties"></a><span data-ttu-id="b874c-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b874c-122">Properties</span></span>

<span data-ttu-id="b874c-123">L’interface **IMsRdpClientShell** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b874c-123">The **IMsRdpClientShell** interface has these properties.</span></span>



| <span data-ttu-id="b874c-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="b874c-124">Property</span></span>                                                                                              | <span data-ttu-id="b874c-125">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="b874c-125">Access type</span></span>           | <span data-ttu-id="b874c-126">Description</span><span class="sxs-lookup"><span data-stu-id="b874c-126">Description</span></span>                                                                                               |
|:------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b874c-127">**IsRemoteProgramClientInstalled**</span><span class="sxs-lookup"><span data-stu-id="b874c-127">**IsRemoteProgramClientInstalled**</span></span>](imsrdpclientshell-isremoteprogramclientinstalled.md)<br/> | <span data-ttu-id="b874c-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b874c-128">Read-only</span></span><br/>  | <span data-ttu-id="b874c-129">Récupère si le client Connexion Bureau à distance (RDC) prend en charge les fonctionnalités RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b874c-129">Retrieves whether the Remote Desktop Connection (RDC) client supports RemoteApp functionality.</span></span><br/> |
| [<span data-ttu-id="b874c-130">**PublicMode**</span><span class="sxs-lookup"><span data-stu-id="b874c-130">**PublicMode**</span></span>](imsrdpclientshell-publicmode.md)<br/>                                         | <span data-ttu-id="b874c-131">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b874c-131">Read/write</span></span><br/> | <span data-ttu-id="b874c-132">Récupère si le mode public est activé.</span><span class="sxs-lookup"><span data-stu-id="b874c-132">Retrieves whether public mode is enabled.</span></span><br/>                                                      |
| [<span data-ttu-id="b874c-133">**RdpFileContents**</span><span class="sxs-lookup"><span data-stu-id="b874c-133">**RdpFileContents**</span></span>](imsrdpclientshell-rdpfilecontents.md)<br/>                               | <span data-ttu-id="b874c-134">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b874c-134">Read/write</span></span><br/> | <span data-ttu-id="b874c-135">Version de flux du fichier de configuration RDP.</span><span class="sxs-lookup"><span data-stu-id="b874c-135">Stream version of the RDP configuration file.</span></span><br/>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="b874c-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b874c-136">Requirements</span></span>



| <span data-ttu-id="b874c-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b874c-137">Requirement</span></span> | <span data-ttu-id="b874c-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="b874c-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b874c-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b874c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="b874c-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b874c-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b874c-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b874c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="b874c-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b874c-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b874c-143">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b874c-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="b874c-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b874c-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b874c-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b874c-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b874c-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b874c-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b874c-147">IID</span><span class="sxs-lookup"><span data-stu-id="b874c-147">IID</span></span><br/>                      | <span data-ttu-id="b874c-148">IID \_ IMsRdpClientShell est défini en tant que d012ae6d-C19A-4bfe-b367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="b874c-148">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="b874c-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b874c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b874c-150">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="b874c-150">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="b874c-151">Référence Connexion Bureau à distance par le Web</span><span class="sxs-lookup"><span data-stu-id="b874c-151">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

