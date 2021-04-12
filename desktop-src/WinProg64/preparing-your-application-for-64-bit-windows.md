---
title: Préparation de votre application pour Windows 64 bits
description: Il existe plusieurs fonctionnalités qui facilitent le développement d’applications qui s’exécutent à la fois sur les versions 32 et 64 bits de Windows. La plupart de ces types de données, tels que les nouveaux types de données, sont décrits dans préparation pour Windows 64 bits.
ms.assetid: 6559b0ab-17cf-4bec-bf2d-3a0da0a344d3
keywords:
- 64-bit Toolkit, programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f3b40d2fb22b84abdd4322f476981dc54c7ad3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199348"
---
# <a name="preparing-your-application-for-64-bit-windows"></a><span data-ttu-id="fa363-105">Préparation de votre application pour Windows 64 bits</span><span class="sxs-lookup"><span data-stu-id="fa363-105">Preparing Your Application for 64-bit Windows</span></span>

<span data-ttu-id="fa363-106">Il existe plusieurs fonctionnalités qui facilitent le développement d’applications qui s’exécutent à la fois sur les versions 32 et 64 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="fa363-106">There are several features that make it easier for you to develop applications that will run on both 32- and 64-bit Windows.</span></span> <span data-ttu-id="fa363-107">La plupart de ces types de données, tels que les nouveaux types de données, sont décrits dans [préparation pour Windows 64 bits](getting-ready-for-64-bit-windows.md).</span><span class="sxs-lookup"><span data-stu-id="fa363-107">Most of these, such as the new data types, are described in [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).</span></span>

<span data-ttu-id="fa363-108">La boîte à outils 64 bits fournie avec le SDK Windows inclut un compilateur MIDL 64 bits, Midl.exe, pour générer des stubs 64 bits natifs, ainsi que des stubs 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fa363-108">The 64-bit toolkit that ships with the Windows SDK includes a 64-bit MIDL compiler, Midl.exe, for generating native 64-bit stubs, as well as 32-bit stubs.</span></span> <span data-ttu-id="fa363-109">Utilisez le commutateur **/env Win64** pour générer uniquement des stubs 64 bits.</span><span class="sxs-lookup"><span data-stu-id="fa363-109">Use the **/env win64** switch to generate 64-bit stubs only.</span></span> <span data-ttu-id="fa363-110">La valeur par défaut consiste à générer deux stubs qui s’exécutent sur les deux plateformes.</span><span class="sxs-lookup"><span data-stu-id="fa363-110">The default is to generate dual stubs that run on both platforms.</span></span>

<span data-ttu-id="fa363-111">Notez que le MIDL 64 bits ne prend en charge que les modes d’optimisation [**/Oicf**](/windows/desktop/Midl/-oi) et [**/OS**](/windows/desktop/Midl/-os) .</span><span class="sxs-lookup"><span data-stu-id="fa363-111">Note that the 64-bit MIDL supports the [**/Oicf**](/windows/desktop/Midl/-oi) and [**/Os**](/windows/desktop/Midl/-os) optimization modes only.</span></span>

 

 