---
title: IMsRdpClientNonScriptable6, interface
description: Fournit l’accès aux propriétés non scriptables de la session à distance d’un client sur le contrôle ActiveX Bureau à distance. Dérive de l’interface IMsRdpClientNonScriptable5.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable6
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable6, Description
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 0d6793452ebf59f1974831aef0fa10f2469d8e92
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104385487"
---
# <a name="imsrdpclientnonscriptable6-interface"></a><span data-ttu-id="65577-106">IMsRdpClientNonScriptable6, interface</span><span class="sxs-lookup"><span data-stu-id="65577-106">IMsRdpClientNonScriptable6 interface</span></span>

<span data-ttu-id="65577-107">Fournit l’accès aux propriétés non scriptables de la session à distance d’un client sur le contrôle ActiveX Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="65577-107">Provides access to the nonscriptable properties of a client's remote session on the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="65577-108">Dérive de l’interface [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md) .</span><span class="sxs-lookup"><span data-stu-id="65577-108">Derives from the [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md) interface.</span></span> <span data-ttu-id="65577-109">Les méthodes de cette interface sont accessibles uniquement par le biais de la vtable ; ils ne peuvent pas être utilisés pour des clients scriptables.</span><span class="sxs-lookup"><span data-stu-id="65577-109">Methods of this interface can only be accessed through the vtable; they are not available for use to scriptable clients.</span></span>

<span data-ttu-id="65577-110">Une instance de cette interface est obtenue en appelant [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur l’objet [**IMsTscAx**](imstscax-interface.md) , en passant **IID \_ IMsRdpClientNonScriptable6**.</span><span class="sxs-lookup"><span data-stu-id="65577-110">An instance of this interface is obtained by calling [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the [**IMsTscAx**](imstscax-interface.md) object, passing **IID\_IMsRdpClientNonScriptable6**.</span></span>

## <a name="members"></a><span data-ttu-id="65577-111">Membres</span><span class="sxs-lookup"><span data-stu-id="65577-111">Members</span></span>

<span data-ttu-id="65577-112">L’interface **IMsRdpClientNonScriptable6** hérite de [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md).</span><span class="sxs-lookup"><span data-stu-id="65577-112">The **IMsRdpClientNonScriptable6** interface inherits from [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md).</span></span> <span data-ttu-id="65577-113">**IMsRdpClientNonScriptable6** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="65577-113">**IMsRdpClientNonScriptable6** also has these types of members:</span></span>

- [<span data-ttu-id="65577-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="65577-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="65577-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="65577-115">Methods</span></span>

<span data-ttu-id="65577-116">L’interface **IMsRdpClientNonScriptable6** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="65577-116">The **IMsRdpClientNonScriptable6** interface has these methods.</span></span>


| <span data-ttu-id="65577-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="65577-117">Method</span></span>            | <span data-ttu-id="65577-118">Description</span><span class="sxs-lookup"><span data-stu-id="65577-118">Description</span></span>                   |
|:-----------------------------|:-----------------|
| [<span data-ttu-id="65577-119">**SendLocation2D**</span><span class="sxs-lookup"><span data-stu-id="65577-119">**SendLocation2D**</span></span>](imsrdpclientnonscriptable6-sendlocation2d.md)     |  <span data-ttu-id="65577-120">Envoie une valeur de latitude et de longitude au serveur afin que l’emplacement géographique du client puisse être reflété dans la session à distance.</span><span class="sxs-lookup"><span data-stu-id="65577-120">Sends a latitude and longitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>                   |
| [<span data-ttu-id="65577-121">**SendLocation3D**</span><span class="sxs-lookup"><span data-stu-id="65577-121">**SendLocation3D**</span></span>](imsrdpclientnonscriptable6-sendlocation3d.md)     | <span data-ttu-id="65577-122">Envoie une valeur de latitude, de longitude et d’altitude au serveur afin que l’emplacement géographique du client puisse être reflété dans la session à distance.</span><span class="sxs-lookup"><span data-stu-id="65577-122">Sends a latitude, longitude and altitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>                 |

## <a name="requirements"></a><span data-ttu-id="65577-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65577-123">Requirements</span></span>

| <span data-ttu-id="65577-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65577-124">Requirement</span></span> | <span data-ttu-id="65577-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="65577-125">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="65577-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65577-126">Minimum supported client</span></span>| <span data-ttu-id="65577-127">Windows 10, version 1709 (build 16299)</span><span class="sxs-lookup"><span data-stu-id="65577-127">Windows 10, version 1709 (build 16299)</span></span>      |
| <span data-ttu-id="65577-128">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="65577-128">Type library</span></span>            | <span data-ttu-id="65577-129">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="65577-129">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="65577-130">DLL</span><span class="sxs-lookup"><span data-stu-id="65577-130">DLL</span></span>                  | <span data-ttu-id="65577-131">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="65577-131">MsTscAx.dll</span></span>     |
| <span data-ttu-id="65577-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="65577-132">CLSID</span></span>                    | <span data-ttu-id="65577-133">Le CLSID \_ MsRdpClient12 est défini en tant que 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span><span class="sxs-lookup"><span data-stu-id="65577-133">CLSID\_MsRdpClient12 is defined as 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span></span><br/> <span data-ttu-id="65577-134">Le CLSID \_ MsRdpClient12NotSafeForScripting est défini en tant que 3BB805C2-D9E2-4174-8A1E-C87D69563662</span><span class="sxs-lookup"><span data-stu-id="65577-134">CLSID\_MsRdpClient12NotSafeForScripting is defined as 3BB805C2-D9E2-4174-8A1E-C87D69563662</span></span><br/> <span data-ttu-id="65577-135">Le CLSID \_ MsRdpClient11 est défini en tant que 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span><span class="sxs-lookup"><span data-stu-id="65577-135">CLSID\_MsRdpClient11 is defined as 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span></span><br/> <span data-ttu-id="65577-136">Le CLSID \_ MsRdpClient11NotSafeForScripting est défini en tant que 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span><span class="sxs-lookup"><span data-stu-id="65577-136">CLSID\_MsRdpClient11NotSafeForScripting is defined as 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span></span><br/>  |
| <span data-ttu-id="65577-137">IID</span><span class="sxs-lookup"><span data-stu-id="65577-137">IID</span></span>                      | <span data-ttu-id="65577-138">IID \_ IMsRdpClientNonScriptable6 est défini comme 05293249-B28B-4db8-BE64-1B2F496B910E</span><span class="sxs-lookup"><span data-stu-id="65577-138">IID\_IMsRdpClientNonScriptable6 is defined as 05293249-B28B-4DB8-BE64-1B2F496B910E</span></span>            |

## <a name="see-also"></a><span data-ttu-id="65577-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65577-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65577-140">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="65577-140">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>
