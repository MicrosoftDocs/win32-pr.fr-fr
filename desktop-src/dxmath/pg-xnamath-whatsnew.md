---
description: La bibliothèque DirectXMath est basée sur la bibliothèque XNA Math C++ SIMD version 2. x. Ici, nous décrivons comment DirectXMath diffère de XNA Math et comment les versions de DirectXMath diffèrent.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: Nouveautés (DirectXMath)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb9fa8c7ee0600ce0b0fa5eade3a3e111e5edbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527789"
---
# <a name="whats-new-directxmath"></a><span data-ttu-id="66d20-104">Nouveautés (DirectXMath)</span><span class="sxs-lookup"><span data-stu-id="66d20-104">What's New (DirectXMath)</span></span>

<span data-ttu-id="66d20-105">La bibliothèque DirectXMath est basée sur la [bibliothèque XNA Math C++ SIMD version 2,04](https://walbourn.github.io/).</span><span class="sxs-lookup"><span data-stu-id="66d20-105">The DirectXMath library is based on the [XNA Math C++ SIMD library version 2.04](https://walbourn.github.io/).</span></span> <span data-ttu-id="66d20-106">Ici, nous décrivons comment DirectXMath diffère de XNA Math et comment les versions de DirectXMath diffèrent.</span><span class="sxs-lookup"><span data-stu-id="66d20-106">Here we describe how DirectXMath differs from XNA Math and how DirectXMath versions differ.</span></span>

-   [<span data-ttu-id="66d20-107">Historique Rlease</span><span class="sxs-lookup"><span data-stu-id="66d20-107">Rlease history</span></span>](#release-history)
-   [<span data-ttu-id="66d20-108">DirectXMath les différences par rapport à XNA Math</span><span class="sxs-lookup"><span data-stu-id="66d20-108">DirectXMath differences from XNA Math</span></span>](#directxmath-differences-from-xna-math)
-   [<span data-ttu-id="66d20-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="66d20-109">Related topics</span></span>](#related-topics)

## <a name="release-history"></a><span data-ttu-id="66d20-110">Historique des mises en production</span><span class="sxs-lookup"><span data-stu-id="66d20-110">Release history</span></span>

<table>
 <tr>
  <td><span data-ttu-id="66d20-111">Kit de développement logiciel de mise à jour Windows 10 2020</span><span class="sxs-lookup"><span data-stu-id="66d20-111">Windows 10 May 2020 Update SDK</span></span></td><td><span data-ttu-id="66d20-112">DirectXMath 3,14</span><span class="sxs-lookup"><span data-stu-id="66d20-112">DirectXMath 3.14</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="66d20-113">SDK de mise à jour de Windows 10 octobre 2018</span><span class="sxs-lookup"><span data-stu-id="66d20-113">Windows 10 October 2018 Update SDK</span></span></td><td><span data-ttu-id="66d20-114">DirectXMath 3,13</span><span class="sxs-lookup"><span data-stu-id="66d20-114">DirectXMath 3.13</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="66d20-115">Kit de mise à jour de Windows 10 avril 2018</span><span class="sxs-lookup"><span data-stu-id="66d20-115">Windows 10 April 2018 Update SDK</span></span><br /><span data-ttu-id="66d20-116">SDK de la mise à jour des créateurs Windows 10 automne</span><span class="sxs-lookup"><span data-stu-id="66d20-116">Windows 10 Fall Creators Update SDK</span></span></td><td><span data-ttu-id="66d20-117">DirectXMath 3,11</span><span class="sxs-lookup"><span data-stu-id="66d20-117">DirectXMath 3.11</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="66d20-118">SDK Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="66d20-118">Windows 10 Creators Update SDK</span></span></td><td><span data-ttu-id="66d20-119">DirectXMath 3,10</span><span class="sxs-lookup"><span data-stu-id="66d20-119">DirectXMath 3.10</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="66d20-120">SDK Windows 10 anniversaire</span><span class="sxs-lookup"><span data-stu-id="66d20-120">Windows 10 Anniversary SDK</span></span></td><td><span data-ttu-id="66d20-121">DirectXMath 3,09</span><span class="sxs-lookup"><span data-stu-id="66d20-121">DirectXMath 3.09</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="66d20-122">SDK Windows 10 (2015 novembre)</span><span class="sxs-lookup"><span data-stu-id="66d20-122">Windows 10 SDK (November 2015)</span></span></td><td><span data-ttu-id="66d20-123">DirectXMath 3,08</span><span class="sxs-lookup"><span data-stu-id="66d20-123">DirectXMath 3.08</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="66d20-124">SDK Windows pour Windows 8.1 (Spring 2015)</span><span class="sxs-lookup"><span data-stu-id="66d20-124">Windows SDK for Windows 8.1 (Spring 2015)</span></span></td><td><span data-ttu-id="66d20-125">DirectXMath 3,07</span><span class="sxs-lookup"><span data-stu-id="66d20-125">DirectXMath 3.07</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="66d20-126">Kit de développement logiciel (SDK) Windows pour Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="66d20-126">Windows SDK for Windows 8.1</span></span></td><td><span data-ttu-id="66d20-127">DirectXMath 3,06</span><span class="sxs-lookup"><span data-stu-id="66d20-127">DirectXMath 3.06</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="66d20-128">SDK Windows pour Windows 8</span><span class="sxs-lookup"><span data-stu-id="66d20-128">Windows SDK for Windows 8</span></span></td><td><span data-ttu-id="66d20-129">DirectXMath 3,03</span><span class="sxs-lookup"><span data-stu-id="66d20-129">DirectXMath 3.03</span></span></td>
 </tr>
</table>

<span data-ttu-id="66d20-130">Pour plus d’informations, consultez [versions DirectXMath](https://github.com/Microsoft/DirectXMath/releases) .</span><span class="sxs-lookup"><span data-stu-id="66d20-130">See [DirectXMath releases](https://github.com/Microsoft/DirectXMath/releases) for more information.</span></span>

## <a name="directxmath-differences-from-xna-math"></a><span data-ttu-id="66d20-131">DirectXMath les différences par rapport à XNA Math</span><span class="sxs-lookup"><span data-stu-id="66d20-131">DirectXMath differences from XNA Math</span></span>

<span data-ttu-id="66d20-132">Voici comment la bibliothèque DirectXMath diffère principalement de la bibliothèque XNA Math :</span><span class="sxs-lookup"><span data-stu-id="66d20-132">Here is how the DirectXMath library primarily differs from the XNA Math library:</span></span>

-   <span data-ttu-id="66d20-133">DirectXMath est uniquement en C++ (espaces de noms, surcharges, nouveaux modèles, etc.).</span><span class="sxs-lookup"><span data-stu-id="66d20-133">DirectXMath is C++ only (namespaces, overloads, new templates, and so on).</span></span>
-   <span data-ttu-id="66d20-134">Requiert la prise en charge de la bibliothèque standard C++ 11 (c’est-à-dire, stdint. h, etc.).</span><span class="sxs-lookup"><span data-stu-id="66d20-134">Requires C++11 standard library support (that is, stdint.h, and so on).</span></span>
-   <span data-ttu-id="66d20-135">Prise en charge des intrinsèques ARM-néon pour la plateforme Windows RT.</span><span class="sxs-lookup"><span data-stu-id="66d20-135">ARM-NEON intrinsics support for the Windows RT platform.</span></span>
-   <span data-ttu-id="66d20-136">Nouvelles fonctionnalités de couleur (conversions d’espace colorimétrique, constantes de couleur .NET).</span><span class="sxs-lookup"><span data-stu-id="66d20-136">New color functionality (color space conversions, .NET color constants).</span></span>
-   <span data-ttu-id="66d20-137">Délimitation des types de volumes (version de qui était précédemment dans l’en-tête XNACollision dans l’exemple de collision du kit de développement logiciel (SDK) DirectX).</span><span class="sxs-lookup"><span data-stu-id="66d20-137">Bounding volume types (a version of which was previously in the XNACollision header in the DirectX SDK Collision sample).</span></span>
-   <span data-ttu-id="66d20-138">Aucune version Xbox 360 n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="66d20-138">No Xbox 360 version is available.</span></span> <span data-ttu-id="66d20-139">La Xbox 360 XDK continue à expédier XNAMath v2. x ; suppression des types de données et des variantes de fonction spécifiques à Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="66d20-139">The Xbox 360 XDK continues to ship XNAMath v2.x; removal of Xbox 360 specific data types and function variants.</span></span>
-   <span data-ttu-id="66d20-140">[**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) retravaillé pour améliorer l’optimisation des intrinsèques SSE et ARM-néon.</span><span class="sxs-lookup"><span data-stu-id="66d20-140">Reworked [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) for improved optimization for SSE and ARM-NEON intrinsics.</span></span>
-   <span data-ttu-id="66d20-141">Le type [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) est entièrement opaque.</span><span class="sxs-lookup"><span data-stu-id="66d20-141">The [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) type is fully opaque.</span></span> <span data-ttu-id="66d20-142">Pour accéder à des éléments individuels de **XMMATRIX**, utilisez d’autres types tels que [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span><span class="sxs-lookup"><span data-stu-id="66d20-142">To access individual elements of **XMMATRIX**, use other types such as [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span></span>

## <a name="related-topics"></a><span data-ttu-id="66d20-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="66d20-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66d20-144">Guide de programmation DirectXMath</span><span class="sxs-lookup"><span data-stu-id="66d20-144">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> <dt>

[<span data-ttu-id="66d20-145">Versions de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="66d20-145">DirectXMath releases</span></span>](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
