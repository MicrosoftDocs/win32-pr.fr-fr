---
description: Cette rubrique fournit des informations sur le codec ICO natif disponible via WIC (Windows Imaging Component).
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Vue d’ensemble du format ICO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329a53a3b5d386c5e5386141162c608dc9db1ec0
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444469"
---
# <a name="ico-format-overview"></a><span data-ttu-id="ab411-103">Vue d’ensemble du format ICO</span><span class="sxs-lookup"><span data-stu-id="ab411-103">ICO Format Overview</span></span>

<span data-ttu-id="ab411-104">Cette rubrique fournit des informations sur le codec ICO natif disponible via WIC (Windows Imaging Component).</span><span class="sxs-lookup"><span data-stu-id="ab411-104">This topic provides information about the native ICO codec available through Windows Imaging Component (WIC).</span></span>

## <a name="codec-identity"></a><span data-ttu-id="ab411-105">Identité du codec</span><span class="sxs-lookup"><span data-stu-id="ab411-105">Codec Identity</span></span>

<span data-ttu-id="ab411-106">Le tableau suivant fournit des informations d’identification du codec.</span><span class="sxs-lookup"><span data-stu-id="ab411-106">The following table provides codec identification information.</span></span>



|   <span data-ttu-id="ab411-107">Composant</span><span class="sxs-lookup"><span data-stu-id="ab411-107">Component</span></span>            | <span data-ttu-id="ab411-108">Description</span><span class="sxs-lookup"><span data-stu-id="ab411-108">Description</span></span>       |
|------------------------|-------------------|
| <span data-ttu-id="ab411-109">Nom (s) formel (s)</span><span class="sxs-lookup"><span data-stu-id="ab411-109">Formal Name(s)</span></span>         | <span data-ttu-id="ab411-110">Format d’icône (ICO)</span><span class="sxs-lookup"><span data-stu-id="ab411-110">Icon Format (ICO)</span></span> |
| <span data-ttu-id="ab411-111">Extension (s) de nom de fichier</span><span class="sxs-lookup"><span data-stu-id="ab411-111">File Name Extension(s)</span></span> | <span data-ttu-id="ab411-112">ICO</span><span class="sxs-lookup"><span data-stu-id="ab411-112">ico</span></span>               |
| <span data-ttu-id="ab411-113">type MIME</span><span class="sxs-lookup"><span data-stu-id="ab411-113">MIME type</span></span>              | <span data-ttu-id="ab411-114">image/ico</span><span class="sxs-lookup"><span data-stu-id="ab411-114">image/ico</span></span>         |
| <span data-ttu-id="ab411-115">Prise en charge des spécifications</span><span class="sxs-lookup"><span data-stu-id="ab411-115">Specification Support</span></span>  |                   |



 

<span data-ttu-id="ab411-116">Le tableau suivant répertorie les GUID utilisés pour identifier les composants du codec ICO natifs.</span><span class="sxs-lookup"><span data-stu-id="ab411-116">The following table lists the GUIDs used to identify the native ICO codec components.</span></span>



| <span data-ttu-id="ab411-117">Composant</span><span class="sxs-lookup"><span data-stu-id="ab411-117">Component</span></span>        | <span data-ttu-id="ab411-118">Nom convivial</span><span class="sxs-lookup"><span data-stu-id="ab411-118">Friendly Name</span></span>            | <span data-ttu-id="ab411-119">GUID</span><span class="sxs-lookup"><span data-stu-id="ab411-119">GUID</span></span>                                |
|------------------|--------------------------|-------------------------------------|
| <span data-ttu-id="ab411-120">Format de conteneur</span><span class="sxs-lookup"><span data-stu-id="ab411-120">Container Format</span></span> | <span data-ttu-id="ab411-121">GUID \_ ContainerFormatIco</span><span class="sxs-lookup"><span data-stu-id="ab411-121">GUID\_ContainerFormatIco</span></span> | <span data-ttu-id="ab411-122">a3a860c4-338f-4c17-919afba4b5628f21</span><span class="sxs-lookup"><span data-stu-id="ab411-122">a3a860c4-338f-4c17-919afba4b5628f21</span></span> |
| <span data-ttu-id="ab411-123">Décodeur</span><span class="sxs-lookup"><span data-stu-id="ab411-123">Decoder</span></span>          | <span data-ttu-id="ab411-124">CLSID \_ WICIcoDecoder</span><span class="sxs-lookup"><span data-stu-id="ab411-124">CLSID\_WICIcoDecoder</span></span>     | <span data-ttu-id="ab411-125">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span><span class="sxs-lookup"><span data-stu-id="ab411-125">c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe</span></span> |
| <span data-ttu-id="ab411-126">Encodeur</span><span class="sxs-lookup"><span data-stu-id="ab411-126">Encoder</span></span>          | <span data-ttu-id="ab411-127">NON DISPONIBLE</span><span class="sxs-lookup"><span data-stu-id="ab411-127">NOT AVAILABLE</span></span>            | <span data-ttu-id="ab411-128">NON DISPONIBLE</span><span class="sxs-lookup"><span data-stu-id="ab411-128">NOT AVAILABLE</span></span>                       |



 

## <a name="encoding"></a><span data-ttu-id="ab411-129">Encodage</span><span class="sxs-lookup"><span data-stu-id="ab411-129">Encoding</span></span>

<span data-ttu-id="ab411-130">WIC ne fournit pas d’encodeur d’image ICO natif.</span><span class="sxs-lookup"><span data-stu-id="ab411-130">WIC does not provide a native ICO image encoder.</span></span>

## <a name="decoding"></a><span data-ttu-id="ab411-131">Décodage</span><span class="sxs-lookup"><span data-stu-id="ab411-131">Decoding</span></span>

<span data-ttu-id="ab411-132">L’API de décodage WIC est conçue pour être indépendante du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique.</span><span class="sxs-lookup"><span data-stu-id="ab411-132">The WIC decoding API are designed to be codec-independent and image decoding for WIC-enabled codecs is essentially the same.</span></span> <span data-ttu-id="ab411-133">Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="ab411-133">For more information about image decoding, see the [Decoding Overview](-wic-creating-decoder.md).</span></span> <span data-ttu-id="ab411-134">Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).</span><span class="sxs-lookup"><span data-stu-id="ab411-134">For more information about using decoded image data, see the [Bitmap Sources Overview](-wic-bitmapsources.md).</span></span>

 

 



