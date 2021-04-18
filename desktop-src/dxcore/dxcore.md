---
title: DXCore
description: DXCore est une API d’énumération d’adaptateur pour les appareils DirectX.
ms.localizationpriority: high
ms.topic: article
ms.date: 06/20/2019
ms.openlocfilehash: 80e93ac7440629a809cb01b4d1d4fa2e73b7ee91
ms.sourcegitcommit: aa021b23d7e8bba2e1df9de93a1c315a17681810
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/10/2020
ms.locfileid: "106512347"
---
# <a name="dxcore"></a><span data-ttu-id="c0dcf-103">DXCore</span><span class="sxs-lookup"><span data-stu-id="c0dcf-103">DXCore</span></span>

<span data-ttu-id="c0dcf-104">DXCore est une API d’énumération d’adaptateur pour les graphiques et les appareils de calcul, de sorte que certaines de ses fonctionnalités se chevauchent avec celles de [dxgi](../direct3ddxgi/dx-graphics-dxgi.md).</span><span class="sxs-lookup"><span data-stu-id="c0dcf-104">DXCore is an adapter enumeration API for graphics and compute devices, so some of its facilities overlap with those of [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).</span></span> <span data-ttu-id="c0dcf-105">DXCore est utilisé par Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="c0dcf-105">DXCore is used by Direct3D 12.</span></span>

<span data-ttu-id="c0dcf-106">Cet ensemble de documentation contient des informations sur la programmation avec DXCore, ainsi que sur la référence DXCore.</span><span class="sxs-lookup"><span data-stu-id="c0dcf-106">This documentation set contains information about programming with DXCore, as well as the DXCore reference.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0dcf-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0dcf-107">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c0dcf-108">**Environnements d’exécution pris en charge**</span><span class="sxs-lookup"><span data-stu-id="c0dcf-108">**Supported runtime environments**</span></span> | <span data-ttu-id="c0dcf-109">Windows/C++</span><span class="sxs-lookup"><span data-stu-id="c0dcf-109">Windows/C++</span></span> |
| <span data-ttu-id="c0dcf-110">**Langages de programmation recommandés**</span><span class="sxs-lookup"><span data-stu-id="c0dcf-110">**Recommended programming languages**</span></span> | <span data-ttu-id="c0dcf-111">C++</span><span class="sxs-lookup"><span data-stu-id="c0dcf-111">C++</span></span> |
| <span data-ttu-id="c0dcf-112">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="c0dcf-112">**Minimum supported client**</span></span> | <span data-ttu-id="c0dcf-113">Windows 10, version 2004 (10,0 ; Build 19041)</span><span class="sxs-lookup"><span data-stu-id="c0dcf-113">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="c0dcf-114">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="c0dcf-114">**Header**</span></span> | <span data-ttu-id="c0dcf-115">dxcore. h et dxcore_interface. h</span><span class="sxs-lookup"><span data-stu-id="c0dcf-115">dxcore.h and dxcore_interface.h</span></span> |
| <span data-ttu-id="c0dcf-116">**Bibliothèque**</span><span class="sxs-lookup"><span data-stu-id="c0dcf-116">**Library**</span></span> | <span data-ttu-id="c0dcf-117">dxcore. lib</span><span class="sxs-lookup"><span data-stu-id="c0dcf-117">dxcore.lib</span></span> |
| <span data-ttu-id="c0dcf-118">**DLL**</span><span class="sxs-lookup"><span data-stu-id="c0dcf-118">**DLL**</span></span> | <span data-ttu-id="c0dcf-119">dxcore.dll</span><span class="sxs-lookup"><span data-stu-id="c0dcf-119">dxcore.dll</span></span> |

## <a name="in-this-section"></a><span data-ttu-id="c0dcf-120">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="c0dcf-120">In this section</span></span>

| <span data-ttu-id="c0dcf-121">Rubrique</span><span class="sxs-lookup"><span data-stu-id="c0dcf-121">Topic</span></span> | <span data-ttu-id="c0dcf-122">Description</span><span class="sxs-lookup"><span data-stu-id="c0dcf-122">Description</span></span> |
|-|-|
| [<span data-ttu-id="c0dcf-123">Guide de programmation DXCore</span><span class="sxs-lookup"><span data-stu-id="c0dcf-123">DXCore programming guide</span></span>](dxcore-programming-guide.md) | <span data-ttu-id="c0dcf-124">Aide pour la programmation avec DXCore.</span><span class="sxs-lookup"><span data-stu-id="c0dcf-124">Guidance for programming with DXCore.</span></span> |
| [<span data-ttu-id="c0dcf-125">Informations de référence sur DXCore</span><span class="sxs-lookup"><span data-stu-id="c0dcf-125">DXCore reference</span></span>](dxcore-reference.md) | <span data-ttu-id="c0dcf-126">Cette section traite des API DXCore déclarées dans dxcore. h et dxcore_interface. h.</span><span class="sxs-lookup"><span data-stu-id="c0dcf-126">This section covers DXCore APIs declared in dxcore.h and dxcore_interface.h.</span></span> |
