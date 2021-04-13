---
title: Interface IMsRdpPreferredRedirectionInfo
description: Fournit une propriété pour contrôler à l’aide d’un serveur de redirection.
ms.assetid: 1EAD9B15-4A84-4179-8A92-F0736B04B4F1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpPreferredRedirectionInfo
- Services Bureau à distance de l’interface IMsRdpPreferredRedirectionInfo, Description
topic_type:
- apiref
api_name:
- IMsRdpPreferredRedirectionInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8ea28c36ca06548128954298e35c0cc20de5b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464575"
---
# <a name="imsrdppreferredredirectioninfo-interface"></a><span data-ttu-id="05ccf-105">Interface IMsRdpPreferredRedirectionInfo</span><span class="sxs-lookup"><span data-stu-id="05ccf-105">IMsRdpPreferredRedirectionInfo interface</span></span>

<span data-ttu-id="05ccf-106">Fournit une propriété pour contrôler à l’aide d’un serveur de redirection.</span><span class="sxs-lookup"><span data-stu-id="05ccf-106">Provides a property to control using a redirection server.</span></span>

## <a name="members"></a><span data-ttu-id="05ccf-107">Membres</span><span class="sxs-lookup"><span data-stu-id="05ccf-107">Members</span></span>

<span data-ttu-id="05ccf-108">L’interface **IMsRdpPreferredRedirectionInfo** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="05ccf-108">The **IMsRdpPreferredRedirectionInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="05ccf-109">**IMsRdpPreferredRedirectionInfo** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="05ccf-109">**IMsRdpPreferredRedirectionInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="05ccf-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="05ccf-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="05ccf-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="05ccf-111">Properties</span></span>

<span data-ttu-id="05ccf-112">L’interface **IMsRdpPreferredRedirectionInfo** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="05ccf-112">The **IMsRdpPreferredRedirectionInfo** interface has these properties.</span></span>



| <span data-ttu-id="05ccf-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="05ccf-113">Property</span></span>                                                                                               | <span data-ttu-id="05ccf-114">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="05ccf-114">Access type</span></span>           | <span data-ttu-id="05ccf-115">Description</span><span class="sxs-lookup"><span data-stu-id="05ccf-115">Description</span></span>                                                          |
|:-------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="05ccf-116">**UseRedirectionServerName**</span><span class="sxs-lookup"><span data-stu-id="05ccf-116">**UseRedirectionServerName**</span></span>](imsrdppreferredredirectioninfo-useredirectionservername.md)<br/> | <span data-ttu-id="05ccf-117">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="05ccf-117">Read/write</span></span><br/> | <span data-ttu-id="05ccf-118">Obtient et définit s’il faut utiliser le nom du serveur de redirection.</span><span class="sxs-lookup"><span data-stu-id="05ccf-118">Gets and sets whether to use the redirection server name.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="05ccf-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05ccf-119">Requirements</span></span>



| <span data-ttu-id="05ccf-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05ccf-120">Requirement</span></span> | <span data-ttu-id="05ccf-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="05ccf-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05ccf-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05ccf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="05ccf-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="05ccf-123">Windows 8</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="05ccf-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05ccf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="05ccf-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="05ccf-125">Windows Server 2012</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="05ccf-126">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="05ccf-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="05ccf-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05ccf-127"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="05ccf-128">DLL</span><span class="sxs-lookup"><span data-stu-id="05ccf-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05ccf-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05ccf-129"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="05ccf-130">CLSID</span><span class="sxs-lookup"><span data-stu-id="05ccf-130">CLSID</span></span><br/>                    | <span data-ttu-id="05ccf-131">Le CLSID \_ MsRdpClient10 est défini en tant que C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24</span><span class="sxs-lookup"><span data-stu-id="05ccf-131">CLSID\_MsRdpClient10 is defined as C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24</span></span><br/> <span data-ttu-id="05ccf-132">Le CLSID \_ MsRdpClient10NotSafeForScripting est défini en tant que A0C63C30-F08D-4AB4-907C-34905D770C7D</span><span class="sxs-lookup"><span data-stu-id="05ccf-132">CLSID\_MsRdpClient10NotSafeForScripting is defined as A0C63C30-F08D-4AB4-907C-34905D770C7D</span></span><br/> <span data-ttu-id="05ccf-133">Le CLSID \_ MsRdpClient7 est défini en tant que A9D7038D-B5ED-472E-9C47-94BEA90A5910</span><span class="sxs-lookup"><span data-stu-id="05ccf-133">CLSID\_MsRdpClient7 is defined as A9D7038D-B5ED-472E-9C47-94BEA90A5910</span></span><br/> <span data-ttu-id="05ccf-134">Le CLSID \_ MsRdpClient7NotSafeForScripting est défini en tant que 54D38BF7-B1EF-4479-9674-1BD6EA465258</span><span class="sxs-lookup"><span data-stu-id="05ccf-134">CLSID\_MsRdpClient7NotSafeForScripting is defined as 54D38BF7-B1EF-4479-9674-1BD6EA465258</span></span><br/> <span data-ttu-id="05ccf-135">Le CLSID \_ MsRdpClient8 est défini en tant que 5F681803-2900-4C43-A1CC-CF405404A676</span><span class="sxs-lookup"><span data-stu-id="05ccf-135">CLSID\_MsRdpClient8 is defined as 5F681803-2900-4C43-A1CC-CF405404A676</span></span><br/> <span data-ttu-id="05ccf-136">Le CLSID \_ MsRdpClient8NotSafeForScripting est défini en tant que A3BC03A0-041D-42E3-AD22-882B7865C9C5</span><span class="sxs-lookup"><span data-stu-id="05ccf-136">CLSID\_MsRdpClient8NotSafeForScripting is defined as A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span><br/> <span data-ttu-id="05ccf-137">Le CLSID \_ MsRdpClient9 est défini en tant que 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="05ccf-137">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="05ccf-138">Le CLSID \_ MsRdpClient9NotSafeForScripting est défini en tant que 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="05ccf-138">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> |
| <span data-ttu-id="05ccf-139">IID</span><span class="sxs-lookup"><span data-stu-id="05ccf-139">IID</span></span><br/>                      | <span data-ttu-id="05ccf-140">IID \_ IMsRdpPreferredRedirectionInfo est défini en tant que FDD029F9-9574-4def-8529-64B521CCCAA4</span><span class="sxs-lookup"><span data-stu-id="05ccf-140">IID\_IMsRdpPreferredRedirectionInfo is defined as FDD029F9-9574-4DEF-8529-64B521CCCAA4</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

