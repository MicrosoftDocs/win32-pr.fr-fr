---
title: Interfaces principales Direct3D 11
description: Cette section contient des informations sur les interfaces de base.
ms.assetid: e96804db-0987-49ca-b1b1-321f36c13024
keywords:
- interfaces, Direct3D 11 Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c578d84a7a9f223cb81285b69f5b5d1baed4e6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104463850"
---
# <a name="direct3d-11-core-interfaces"></a><span data-ttu-id="aeea8-104">Interfaces principales Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="aeea8-104">Direct3D 11 core interfaces</span></span>

<span data-ttu-id="aeea8-105">Cette section contient des informations sur les interfaces de base.</span><span class="sxs-lookup"><span data-stu-id="aeea8-105">This section contains information about the core interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="aeea8-106">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="aeea8-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aeea8-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="aeea8-107">Topic</span></span></th>
<th><span data-ttu-id="aeea8-108">Description</span><span class="sxs-lookup"><span data-stu-id="aeea8-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aeea8-109"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-109"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-110">Cette interface encapsule les méthodes de récupération des données du GPU de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="aeea8-110">This interface encapsulates methods for retrieving data from the GPU asynchronously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aeea8-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate"><strong>ID3D11BlendState</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate"><strong>ID3D11BlendState</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-112">L’interface d’état de fusion contient une description de l’état de fusion que vous pouvez lier à l' <a href="d3d10-graphics-programming-guide-output-merger-stage.md">étape de fusion de sortie</a>.</span><span class="sxs-lookup"><span data-stu-id="aeea8-112">The blend-state interface holds a description for blending state that you can bind to the <a href="d3d10-graphics-programming-guide-output-merger-stage.md">output-merger stage</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aeea8-113"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11blendstate1"><strong>ID3D11BlendState1</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-113"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11blendstate1"><strong>ID3D11BlendState1</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-114">L’interface d’état de fusion contient une description de l’état de fusion que vous pouvez lier à l' <a href="d3d10-graphics-programming-guide-output-merger-stage.md">étape de fusion de sortie</a>.</span><span class="sxs-lookup"><span data-stu-id="aeea8-114">The blend-state interface holds a description for blending state that you can bind to the <a href="d3d10-graphics-programming-guide-output-merger-stage.md">output-merger stage</a>.</span></span> <span data-ttu-id="aeea8-115">Cette interface d’état de fusion prend en charge les opérations logiques, ainsi que les opérations de fusion.</span><span class="sxs-lookup"><span data-stu-id="aeea8-115">This blend-state interface supports logical operations as well as blending operations.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aeea8-116"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-116"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-117">L’interface <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a> encapsule une liste de commandes Graphics pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="aeea8-117">The <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a> interface encapsulates a list of graphics commands for play back.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aeea8-118"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11counter"><strong>ID3D11Counter</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-118"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11counter"><strong>ID3D11Counter</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-119">Cette interface encapsule des méthodes pour mesurer les performances du GPU.</span><span class="sxs-lookup"><span data-stu-id="aeea8-119">This interface encapsulates methods for measuring GPU performance.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aeea8-120"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate"><strong>ID3D11DepthStencilState</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-120"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate"><strong>ID3D11DepthStencilState</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-121">L’interface Depth-stencil-State contient une description de l’état du gabarit de profondeur que vous pouvez lier à l' <a href="d3d10-graphics-programming-guide-output-merger-stage.md">étape de fusion de sortie</a>.</span><span class="sxs-lookup"><span data-stu-id="aeea8-121">The depth-stencil-state interface holds a description for depth-stencil state that you can bind to the <a href="d3d10-graphics-programming-guide-output-merger-stage.md">output-merger stage</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aeea8-122"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-122"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-123">L’interface d’appareil représente un adaptateur virtuel ; Il est utilisé pour créer des ressources.</span><span class="sxs-lookup"><span data-stu-id="aeea8-123">The device interface represents a virtual adapter; it is used to create resources.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aeea8-124"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-124"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-125">L’interface d’appareil représente un adaptateur virtuel ; Il est utilisé pour créer des ressources.</span><span class="sxs-lookup"><span data-stu-id="aeea8-125">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="aeea8-126"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a> ajoute de nouvelles méthodes à celles de <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="aeea8-126"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aeea8-127"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-127"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-128">L’interface d’appareil représente un adaptateur virtuel ; Il est utilisé pour créer des ressources.</span><span class="sxs-lookup"><span data-stu-id="aeea8-128">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="aeea8-129"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a> ajoute de nouvelles méthodes à celles de <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="aeea8-129"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aeea8-130"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-130"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-131">L’interface d’appareil représente un adaptateur virtuel ; Il est utilisé pour créer des ressources.</span><span class="sxs-lookup"><span data-stu-id="aeea8-131">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="aeea8-132"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a> ajoute de nouvelles méthodes à celles de <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="aeea8-132"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aeea8-133"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-133"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-134">L’interface d’appareil représente un adaptateur virtuel ; Il est utilisé pour créer des ressources.</span><span class="sxs-lookup"><span data-stu-id="aeea8-134">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="aeea8-135"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a> ajoute de nouvelles méthodes à celles de <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a>, telles que <strong>RegisterDeviceRemovedEvent</strong> et <strong>UnregisterDeviceRemoved</strong>.</span><span class="sxs-lookup"><span data-stu-id="aeea8-135"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a>, such as <strong>RegisterDeviceRemovedEvent</strong> and <strong>UnregisterDeviceRemoved</strong>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aeea8-136"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-136"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-137">L’interface d’appareil représente un adaptateur virtuel ; Il est utilisé pour créer des ressources.</span><span class="sxs-lookup"><span data-stu-id="aeea8-137">The device interface represents a virtual adapter; it is used to create resources.</span></span> <span data-ttu-id="aeea8-138"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a> ajoute de nouvelles méthodes à celles de <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="aeea8-138"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a> adds new methods to those in <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aeea8-139"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-139"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-140">Une interface enfant d’appareil accède aux données utilisées par un appareil.</span><span class="sxs-lookup"><span data-stu-id="aeea8-140">A device-child interface accesses data used by a device.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aeea8-141"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-141"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-142">L’interface <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> représente un contexte de périphérique qui génère des commandes de rendu.</span><span class="sxs-lookup"><span data-stu-id="aeea8-142">The <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> interface represents a device context which generates rendering commands.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="aeea8-143">La dernière version de cette interface est <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> introduite dans Windows 10 Creators Update.</span><span class="sxs-lookup"><span data-stu-id="aeea8-143">The latest version of this interface is <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> introduced in the Windows 10 Creators Update.</span></span> <span data-ttu-id="aeea8-144">Les applications ciblant Windows 10 Creators Update doivent utiliser l’interface <strong>ID3D11DeviceContext4</strong> au lieu de <strong>ID3D11Device</strong>.</span><span class="sxs-lookup"><span data-stu-id="aeea8-144">Applications targetting Windows 10 Creators Update should use the <strong>ID3D11DeviceContext4</strong> interface instead of <strong>ID3D11Device</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aeea8-145"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-145"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-146">L’interface de contexte de périphérique représente un contexte de périphérique (Device Context). Il est utilisé pour restituer des commandes.</span><span class="sxs-lookup"><span data-stu-id="aeea8-146">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="aeea8-147"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a> ajoute de nouvelles méthodes à celles de <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="aeea8-147"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aeea8-148"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-148"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-149">L’interface de contexte de périphérique représente un contexte de périphérique (Device Context). Il est utilisé pour restituer des commandes.</span><span class="sxs-lookup"><span data-stu-id="aeea8-149">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="aeea8-150"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a> ajoute de nouvelles méthodes à celles de <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="aeea8-150"><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aeea8-151"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-151"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-152">L’interface de contexte de périphérique représente un contexte de périphérique (Device Context). Il est utilisé pour restituer des commandes.</span><span class="sxs-lookup"><span data-stu-id="aeea8-152">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="aeea8-153"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a> ajoute de nouvelles méthodes à celles de <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="aeea8-153"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a> adds new methods to those in <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aeea8-154"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-154"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-155">L’interface de contexte de périphérique représente un contexte de périphérique (Device Context). Il est utilisé pour restituer des commandes.</span><span class="sxs-lookup"><span data-stu-id="aeea8-155">The device context interface represents a device context; it is used to render commands.</span></span> <span data-ttu-id="aeea8-156"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> ajoute de nouvelles méthodes à celles de <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="aeea8-156"><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> adds new methods to those in <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aeea8-157"><a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-157"><a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-158">L’interface <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a> représente un objet d’état de contexte qui contient les informations sur l’État et le comportement d’un périphérique Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="aeea8-158">The <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a> interface represents a context state object, which holds state and behavior information about a Microsoft Direct3D device.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aeea8-159"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence"><strong>ID3D11Fence</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-159"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence"><strong>ID3D11Fence</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-160">Représente une clôture, un objet utilisé pour la synchronisation de l’UC et un ou plusieurs GPU.</span><span class="sxs-lookup"><span data-stu-id="aeea8-160">Represents a fence, an object used for synchronization of the CPU and one or more GPUs.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aeea8-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout"><strong>ID3D11InputLayout</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout"><strong>ID3D11InputLayout</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-162">Une interface de disposition d’entrée contient une définition de la façon d’alimenter les données de vertex disposées en mémoire dans l' <a href="d3d10-graphics-programming-guide-input-assembler-stage.md">étape assembleur d’entrée</a> du <a href="overviews-direct3d-11-graphics-pipeline.md">pipeline Graphics</a>.</span><span class="sxs-lookup"><span data-stu-id="aeea8-162">An input-layout interface holds a definition of how to feed vertex data that is laid out in memory into the <a href="d3d10-graphics-programming-guide-input-assembler-stage.md">input-assembler stage</a> of the <a href="overviews-direct3d-11-graphics-pipeline.md">graphics pipeline</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aeea8-163"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread"><strong>ID3D11Multithread</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-163"><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread"><strong>ID3D11Multithread</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-164">Fournit une protection de thread pour les sections critiques d’une application multithread.</span><span class="sxs-lookup"><span data-stu-id="aeea8-164">Provides threading protection for critical sections of a multi-threaded application.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aeea8-165"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate"><strong>ID3D11Predicate</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-165"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate"><strong>ID3D11Predicate</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-166">Une interface de prédicat détermine si la géométrie doit être traitée en fonction des résultats d’un appel de dessin précédent.</span><span class="sxs-lookup"><span data-stu-id="aeea8-166">A predicate interface determines whether geometry should be processed depending on the results of a previous draw call.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aeea8-167"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-167"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-168">Une interface de requête interroge les informations du GPU.</span><span class="sxs-lookup"><span data-stu-id="aeea8-168">A query interface queries information from the GPU.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aeea8-169"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11query1"><strong>ID3D11Query1</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-169"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11query1"><strong>ID3D11Query1</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-170">Représente un objet de requête pour interroger des informations à partir de l’unité de traitement graphique (GPU).</span><span class="sxs-lookup"><span data-stu-id="aeea8-170">Represents a query object for querying information from the graphics processing unit (GPU).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aeea8-171"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate"><strong>ID3D11RasterizerState</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-171"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate"><strong>ID3D11RasterizerState</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-172">L’interface d’État du rastériseur contient une description de l’état du rastériseur que vous pouvez lier à l' <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">étape de rastérisation</a>.</span><span class="sxs-lookup"><span data-stu-id="aeea8-172">The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">rasterizer stage</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aeea8-173"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11rasterizerstate1"><strong>ID3D11RasterizerState1</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-173"><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11rasterizerstate1"><strong>ID3D11RasterizerState1</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-174">L’interface d’État du rastériseur contient une description de l’état du rastériseur que vous pouvez lier à l' <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">étape de rastérisation</a>.</span><span class="sxs-lookup"><span data-stu-id="aeea8-174">The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">rasterizer stage</a>.</span></span> <span data-ttu-id="aeea8-175">Cette interface de l’état de rastériseur prend en charge le nombre d’échantillons forcés.</span><span class="sxs-lookup"><span data-stu-id="aeea8-175">This rasterizer-state interface supports forced sample count.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aeea8-176"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rasterizerstate2"><strong>ID3D11RasterizerState2</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-176"><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rasterizerstate2"><strong>ID3D11RasterizerState2</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-177">L’interface d’État du rastériseur contient une description de l’état du rastériseur que vous pouvez lier à l' <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">étape de rastérisation</a>.</span><span class="sxs-lookup"><span data-stu-id="aeea8-177">The rasterizer-state interface holds a description for rasterizer state that you can bind to the <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">rasterizer stage</a>.</span></span> <span data-ttu-id="aeea8-178">Cette interface d’État du rastériseur prend en charge le nombre d’échantillons forcés et le mode de pixellisation conservateur.</span><span class="sxs-lookup"><span data-stu-id="aeea8-178">This rasterizer-state interface supports forced sample count and conservative rasterization mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aeea8-179"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate"><strong>ID3D11SamplerState</strong></a></span><span class="sxs-lookup"><span data-stu-id="aeea8-179"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate"><strong>ID3D11SamplerState</strong></a></span></span><br/></td>
<td><span data-ttu-id="aeea8-180">L’interface d’échantillonnage-état contient une description de l’état de l’échantillonneur que vous pouvez lier à toute étape de nuanceur du <a href="overviews-direct3d-11-graphics-pipeline.md">pipeline</a> pour référencer les opérations d’exemple de texture.</span><span class="sxs-lookup"><span data-stu-id="aeea8-180">The sampler-state interface holds a description for sampler state that you can bind to any shader stage of the <a href="overviews-direct3d-11-graphics-pipeline.md">pipeline</a> for reference by texture sample operations.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="aeea8-181">Direct3D 11 implémente des interfaces pour :</span><span class="sxs-lookup"><span data-stu-id="aeea8-181">Direct3D 11 implements interfaces for:</span></span>

-   [<span data-ttu-id="aeea8-182">Ressources</span><span class="sxs-lookup"><span data-stu-id="aeea8-182">Resources</span></span>](d3d11-graphics-reference-resource-interfaces.md)
-   [<span data-ttu-id="aeea8-183">Nuanceurs</span><span class="sxs-lookup"><span data-stu-id="aeea8-183">Shaders</span></span>](d3d11-graphics-reference-d3d11-shader-interfaces.md)

## <a name="related-topics"></a><span data-ttu-id="aeea8-184">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aeea8-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aeea8-185">Référence principale</span><span class="sxs-lookup"><span data-stu-id="aeea8-185">Core Reference</span></span>](d3d11-graphics-reference-d3d11-core.md)
</dt> </dl>

