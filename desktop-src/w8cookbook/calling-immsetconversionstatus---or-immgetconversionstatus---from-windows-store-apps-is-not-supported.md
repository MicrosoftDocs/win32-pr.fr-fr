---
title: L’appel de ImmSetConversionStatus () ou ImmGetConversionStatus () à partir d’applications du Windows Store n’est pas pris en charge
description: L’appel de ImmSetConversionStatus () ou ImmGetConversionStatus () à partir d’applications du Windows Store n’est pas pris en charge
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b0846b56b1d6c2367c46e4adf82dac011c49fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727693"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a><span data-ttu-id="7453e-103">L’appel de ImmSetConversionStatus () ou ImmGetConversionStatus () à partir d’applications du Windows Store n’est pas pris en charge</span><span class="sxs-lookup"><span data-stu-id="7453e-103">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from Windows Store apps is not supported</span></span>

## <a name="platforms"></a><span data-ttu-id="7453e-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="7453e-104">Platforms</span></span>

<dl> <span data-ttu-id="7453e-105">Clients-Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="7453e-105">Clients - windows 8.1</span></span>  
<span data-ttu-id="7453e-106">Serveurs-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7453e-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="7453e-107">Description</span><span class="sxs-lookup"><span data-stu-id="7453e-107">Description</span></span>

<span data-ttu-id="7453e-108">L’appel de ImmSetConversionStatus () ou ImmGetConversionStatus () à partir d’une application du Windows Store n’est pas pris en charge et peut entraîner des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="7453e-108">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from a Windows Store app is not supported and may cause unexpected results.</span></span>

## <a name="manifestations"></a><span data-ttu-id="7453e-109">Manifestations</span><span class="sxs-lookup"><span data-stu-id="7453e-109">Manifestations</span></span>

<span data-ttu-id="7453e-110">Au démarrage de l’application, le mode IME est défini sur les valeurs par défaut suivantes :</span><span class="sxs-lookup"><span data-stu-id="7453e-110">At application start up, the IME mode is set to the following defaults:</span></span>



|          | <span data-ttu-id="7453e-111">Panneau de saisie du logiciel</span><span class="sxs-lookup"><span data-stu-id="7453e-111">Software input panel</span></span> | <span data-ttu-id="7453e-112">Clavier matériel</span><span class="sxs-lookup"><span data-stu-id="7453e-112">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="7453e-113">KOR, JPN</span><span class="sxs-lookup"><span data-stu-id="7453e-113">KOR, JPN</span></span> | <span data-ttu-id="7453e-114">Il en va</span><span class="sxs-lookup"><span data-stu-id="7453e-114">On</span></span>                   | <span data-ttu-id="7453e-115">Désactivé</span><span class="sxs-lookup"><span data-stu-id="7453e-115">Off</span></span>               |
| <span data-ttu-id="7453e-116">CHS, CHT</span><span class="sxs-lookup"><span data-stu-id="7453e-116">CHS, CHT</span></span> | <span data-ttu-id="7453e-117">Il en va</span><span class="sxs-lookup"><span data-stu-id="7453e-117">On</span></span>                   | <span data-ttu-id="7453e-118">Il en va</span><span class="sxs-lookup"><span data-stu-id="7453e-118">On</span></span>                |



 

## <a name="solution"></a><span data-ttu-id="7453e-119">Solution</span><span class="sxs-lookup"><span data-stu-id="7453e-119">Solution</span></span>

<span data-ttu-id="7453e-120">Les développeurs peuvent contrôler le mode IME par défaut en spécifiant une valeur d’étendue d’entrée pour le champ.</span><span class="sxs-lookup"><span data-stu-id="7453e-120">Developers can control the default IME mode by specifying an input scope value for the field.</span></span>

<span data-ttu-id="7453e-121">Le mode IME pour une étendue d’entrée spécifiée est déterminé par chaque IME.</span><span class="sxs-lookup"><span data-stu-id="7453e-121">The IME mode for a specified input scope is determined by each IME.</span></span> <span data-ttu-id="7453e-122">Les développeurs ne peuvent pas spécifier le mode IME.</span><span class="sxs-lookup"><span data-stu-id="7453e-122">Developers cannot specify the IME mode.</span></span>

## <a name="resources"></a><span data-ttu-id="7453e-123">Ressources</span><span class="sxs-lookup"><span data-stu-id="7453e-123">Resources</span></span>

-   [<span data-ttu-id="7453e-124">Énumération InputScope</span><span class="sxs-lookup"><span data-stu-id="7453e-124">InputScope Enumeration</span></span>](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [<span data-ttu-id="7453e-125">ImmSetConversionStatus</span><span class="sxs-lookup"><span data-stu-id="7453e-125">ImmSetConversionStatus</span></span>](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   <span data-ttu-id="7453e-126">[ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7453e-126">[ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))</span></span>

 

 