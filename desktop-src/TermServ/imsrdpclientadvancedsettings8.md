---
title: Interface IMsRdpClientAdvancedSettings8
description: Expose des méthodes et des propriétés qui gèrent les paramètres avancés du contrôle ActiveX Bureau à distance.
ms.assetid: 9e1de47d-f194-4d9e-8e47-7c13a0677aaa
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, Description
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings8
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fce32baf792563e64d2f8b8e1ad2bd56a31c5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384183"
---
# <a name="imsrdpclientadvancedsettings8-interface"></a><span data-ttu-id="a6adb-105">Interface IMsRdpClientAdvancedSettings8</span><span class="sxs-lookup"><span data-stu-id="a6adb-105">IMsRdpClientAdvancedSettings8 interface</span></span>

<span data-ttu-id="a6adb-106">Expose des méthodes et des propriétés qui gèrent les paramètres avancés du contrôle ActiveX Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="a6adb-106">Exposes methods and properties that manage advanced settings of the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="a6adb-107">Pour obtenir une instance de cette interface, utilisez la propriété [**IMsRdpClient8 :: AdvancedSettings9**](imsrdpclient8-advancedsettings9.md) .</span><span class="sxs-lookup"><span data-stu-id="a6adb-107">To obtain an instance of this interface, use the [**IMsRdpClient8::AdvancedSettings9**](imsrdpclient8-advancedsettings9.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="a6adb-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a6adb-108">Members</span></span>

<span data-ttu-id="a6adb-109">L’interface **IMsRdpClientAdvancedSettings8** hérite de [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md).</span><span class="sxs-lookup"><span data-stu-id="a6adb-109">The **IMsRdpClientAdvancedSettings8** interface inherits from [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md).</span></span> <span data-ttu-id="a6adb-110">**IMsRdpClientAdvancedSettings8** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a6adb-110">**IMsRdpClientAdvancedSettings8** also has these types of members:</span></span>

-   [<span data-ttu-id="a6adb-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a6adb-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a6adb-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a6adb-112">Properties</span></span>

<span data-ttu-id="a6adb-113">L’interface **IMsRdpClientAdvancedSettings8** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a6adb-113">The **IMsRdpClientAdvancedSettings8** interface has these properties.</span></span>



| <span data-ttu-id="a6adb-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="a6adb-114">Property</span></span>                                                                                  | <span data-ttu-id="a6adb-115">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="a6adb-115">Access type</span></span>           | <span data-ttu-id="a6adb-116">Description</span><span class="sxs-lookup"><span data-stu-id="a6adb-116">Description</span></span>                                                           |
|:------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="a6adb-117">**BandwidthDetection**</span><span class="sxs-lookup"><span data-stu-id="a6adb-117">**BandwidthDetection**</span></span>](imsrdpclientadvancedsettings8-bandwidthdetection.md)<br/> | <span data-ttu-id="a6adb-118">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a6adb-118">Read/write</span></span><br/> | <span data-ttu-id="a6adb-119">Spécifie si les modifications de bande passante sont détectées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="a6adb-119">Specifies if bandwidth changes are automatically detected.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a6adb-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6adb-120">Requirements</span></span>



| <span data-ttu-id="a6adb-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6adb-121">Requirement</span></span> | <span data-ttu-id="a6adb-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6adb-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6adb-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6adb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a6adb-124">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a6adb-124">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="a6adb-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6adb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a6adb-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a6adb-126">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="a6adb-127">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a6adb-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="a6adb-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6adb-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a6adb-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a6adb-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6adb-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6adb-130"><dt>MsTscAx.dll</dt></span></span> </dl> |



 

 





