---
description: La bibliothèque DirectXMath est basée sur la bibliothèque XNA Math C++ SIMD version 2. x. Ici, nous décrivons comment DirectXMath diffère de XNA Math et comment les versions de DirectXMath diffèrent.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: Nouveautés (DirectXMath)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df1e7f25789ca6f58205ce9f45482e0a49540d1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827625"
---
# <a name="whats-new-directxmath"></a><span data-ttu-id="4ab16-104">Nouveautés (DirectXMath)</span><span class="sxs-lookup"><span data-stu-id="4ab16-104">What's New (DirectXMath)</span></span>

<span data-ttu-id="4ab16-105">La bibliothèque DirectXMath est basée sur la [bibliothèque XNA Math C++ SIMD version 2,04](https://walbourn.github.io/xna-math-version-2-04/).</span><span class="sxs-lookup"><span data-stu-id="4ab16-105">The DirectXMath library is based on the [XNA Math C++ SIMD library version 2.04](https://walbourn.github.io/xna-math-version-2-04/).</span></span> <span data-ttu-id="4ab16-106">Ici, nous décrivons comment DirectXMath diffère de XNA Math et comment les versions de DirectXMath diffèrent.</span><span class="sxs-lookup"><span data-stu-id="4ab16-106">Here we describe how DirectXMath differs from XNA Math and how DirectXMath versions differ.</span></span>

-   [<span data-ttu-id="4ab16-107">Historique Rlease</span><span class="sxs-lookup"><span data-stu-id="4ab16-107">Rlease history</span></span>](#release-history)
-   [<span data-ttu-id="4ab16-108">DirectXMath les différences par rapport à XNA Math</span><span class="sxs-lookup"><span data-stu-id="4ab16-108">DirectXMath differences from XNA Math</span></span>](#directxmath-differences-from-xna-math)
-   [<span data-ttu-id="4ab16-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4ab16-109">Related topics</span></span>](#related-topics)

## <a name="release-history"></a><span data-ttu-id="4ab16-110">Historique des mises en production</span><span class="sxs-lookup"><span data-stu-id="4ab16-110">Release history</span></span>

<table>
 <tr>
  <td><span data-ttu-id="4ab16-111">SDK Windows 10 (20348), version 2104</span><span class="sxs-lookup"><span data-stu-id="4ab16-111">Windows 10 SDK (20348), version 2104</span></span></td><td><span data-ttu-id="4ab16-112">DirectXMath 3,16</span><span class="sxs-lookup"><span data-stu-id="4ab16-112">DirectXMath 3.16</span></span></td>
 </td>
 <tr>
  <td><span data-ttu-id="4ab16-113">Kit de développement logiciel de mise à jour Windows 10 2020</span><span class="sxs-lookup"><span data-stu-id="4ab16-113">Windows 10 May 2020 Update SDK</span></span></td><td><span data-ttu-id="4ab16-114">DirectXMath 3,14</span><span class="sxs-lookup"><span data-stu-id="4ab16-114">DirectXMath 3.14</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4ab16-115">SDK de mise à jour de Windows 10 octobre 2018</span><span class="sxs-lookup"><span data-stu-id="4ab16-115">Windows 10 October 2018 Update SDK</span></span></td><td><span data-ttu-id="4ab16-116">DirectXMath 3,13</span><span class="sxs-lookup"><span data-stu-id="4ab16-116">DirectXMath 3.13</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4ab16-117">Kit de mise à jour de Windows 10 avril 2018</span><span class="sxs-lookup"><span data-stu-id="4ab16-117">Windows 10 April 2018 Update SDK</span></span><br /><span data-ttu-id="4ab16-118">SDK de la mise à jour des créateurs Windows 10 automne</span><span class="sxs-lookup"><span data-stu-id="4ab16-118">Windows 10 Fall Creators Update SDK</span></span></td><td><span data-ttu-id="4ab16-119">DirectXMath 3,11</span><span class="sxs-lookup"><span data-stu-id="4ab16-119">DirectXMath 3.11</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4ab16-120">SDK Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="4ab16-120">Windows 10 Creators Update SDK</span></span></td><td><span data-ttu-id="4ab16-121">DirectXMath 3,10</span><span class="sxs-lookup"><span data-stu-id="4ab16-121">DirectXMath 3.10</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4ab16-122">SDK Windows 10 anniversaire</span><span class="sxs-lookup"><span data-stu-id="4ab16-122">Windows 10 Anniversary SDK</span></span></td><td><span data-ttu-id="4ab16-123">DirectXMath 3,09</span><span class="sxs-lookup"><span data-stu-id="4ab16-123">DirectXMath 3.09</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4ab16-124">SDK Windows 10 (2015 novembre)</span><span class="sxs-lookup"><span data-stu-id="4ab16-124">Windows 10 SDK (November 2015)</span></span></td><td><span data-ttu-id="4ab16-125">DirectXMath 3,08</span><span class="sxs-lookup"><span data-stu-id="4ab16-125">DirectXMath 3.08</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4ab16-126">SDK Windows pour Windows 8.1 (Spring 2015)</span><span class="sxs-lookup"><span data-stu-id="4ab16-126">Windows SDK for Windows 8.1 (Spring 2015)</span></span></td><td><span data-ttu-id="4ab16-127">DirectXMath 3,07</span><span class="sxs-lookup"><span data-stu-id="4ab16-127">DirectXMath 3.07</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4ab16-128">Kit de développement logiciel (SDK) Windows pour Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4ab16-128">Windows SDK for Windows 8.1</span></span></td><td><span data-ttu-id="4ab16-129">DirectXMath 3,06</span><span class="sxs-lookup"><span data-stu-id="4ab16-129">DirectXMath 3.06</span></span></td>
 </tr>
 <tr>
  <td><span data-ttu-id="4ab16-130">SDK Windows pour Windows 8</span><span class="sxs-lookup"><span data-stu-id="4ab16-130">Windows SDK for Windows 8</span></span></td><td><span data-ttu-id="4ab16-131">DirectXMath 3,03</span><span class="sxs-lookup"><span data-stu-id="4ab16-131">DirectXMath 3.03</span></span></td>
 </tr>
</table>

<span data-ttu-id="4ab16-132">Pour plus d’informations, consultez [versions DirectXMath](https://github.com/Microsoft/DirectXMath/releases) .</span><span class="sxs-lookup"><span data-stu-id="4ab16-132">See [DirectXMath releases](https://github.com/Microsoft/DirectXMath/releases) for more information.</span></span>

## <a name="directxmath-differences-from-xna-math"></a><span data-ttu-id="4ab16-133">DirectXMath les différences par rapport à XNA Math</span><span class="sxs-lookup"><span data-stu-id="4ab16-133">DirectXMath differences from XNA Math</span></span>

<span data-ttu-id="4ab16-134">Voici comment la bibliothèque DirectXMath diffère principalement de la bibliothèque XNA Math :</span><span class="sxs-lookup"><span data-stu-id="4ab16-134">Here is how the DirectXMath library primarily differs from the XNA Math library:</span></span>

-   <span data-ttu-id="4ab16-135">DirectXMath est uniquement en C++ (espaces de noms, surcharges, nouveaux modèles, etc.).</span><span class="sxs-lookup"><span data-stu-id="4ab16-135">DirectXMath is C++ only (namespaces, overloads, new templates, and so on).</span></span>
-   <span data-ttu-id="4ab16-136">Requiert la prise en charge de la bibliothèque standard C++ 11 (c’est-à-dire, stdint. h, etc.).</span><span class="sxs-lookup"><span data-stu-id="4ab16-136">Requires C++11 standard library support (that is, stdint.h, and so on).</span></span>
-   <span data-ttu-id="4ab16-137">Prise en charge des intrinsèques ARM-néon pour la plateforme Windows RT.</span><span class="sxs-lookup"><span data-stu-id="4ab16-137">ARM-NEON intrinsics support for the Windows RT platform.</span></span>
-   <span data-ttu-id="4ab16-138">Nouvelles fonctionnalités de couleur (conversions d’espace colorimétrique, constantes de couleur .NET).</span><span class="sxs-lookup"><span data-stu-id="4ab16-138">New color functionality (color space conversions, .NET color constants).</span></span>
-   <span data-ttu-id="4ab16-139">Délimitation des types de volumes (version de qui était précédemment dans l’en-tête XNACollision dans l’exemple de collision du kit de développement logiciel (SDK) DirectX).</span><span class="sxs-lookup"><span data-stu-id="4ab16-139">Bounding volume types (a version of which was previously in the XNACollision header in the DirectX SDK Collision sample).</span></span>
-   <span data-ttu-id="4ab16-140">Aucune version Xbox 360 n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="4ab16-140">No Xbox 360 version is available.</span></span> <span data-ttu-id="4ab16-141">La Xbox 360 XDK continue à expédier XNAMath v2. x ; suppression des types de données et des variantes de fonction spécifiques à Xbox 360.</span><span class="sxs-lookup"><span data-stu-id="4ab16-141">The Xbox 360 XDK continues to ship XNAMath v2.x; removal of Xbox 360 specific data types and function variants.</span></span>
-   <span data-ttu-id="4ab16-142">[**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) retravaillé pour améliorer l’optimisation des intrinsèques SSE et ARM-néon.</span><span class="sxs-lookup"><span data-stu-id="4ab16-142">Reworked [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) for improved optimization for SSE and ARM-NEON intrinsics.</span></span>
-   <span data-ttu-id="4ab16-143">Le type [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) est entièrement opaque.</span><span class="sxs-lookup"><span data-stu-id="4ab16-143">The [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) type is fully opaque.</span></span> <span data-ttu-id="4ab16-144">Pour accéder à des éléments individuels de **XMMATRIX**, utilisez d’autres types tels que [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span><span class="sxs-lookup"><span data-stu-id="4ab16-144">To access individual elements of **XMMATRIX**, use other types such as [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ab16-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4ab16-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ab16-146">Guide de programmation DirectXMath</span><span class="sxs-lookup"><span data-stu-id="4ab16-146">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> <dt>

[<span data-ttu-id="4ab16-147">Versions de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="4ab16-147">DirectXMath releases</span></span>](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
