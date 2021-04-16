---
title: Limites de téléchargement
description: Pour limiter la taille des chargements, définissez la propriété d’extension IIS BITSMaximumUploadSize.
ms.assetid: 01ad2f32-18be-43a5-a07f-e6f28f7a471b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647aeefe82cf9c3ab035bc3e233c4157f471110b
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104462719"
---
# <a name="upload-limits"></a><span data-ttu-id="3dc1a-103">Limites de téléchargement</span><span class="sxs-lookup"><span data-stu-id="3dc1a-103">Upload Limits</span></span>

<span data-ttu-id="3dc1a-104">Pour limiter la taille des chargements, définissez la propriété d’extension IIS [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="3dc1a-104">To limit the size of uploads, set the [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) IIS extension property.</span></span> <span data-ttu-id="3dc1a-105">Dans IIS 7, vous devrez peut-être également modifier l’attribut **maxAllowedContentLength** .</span><span class="sxs-lookup"><span data-stu-id="3dc1a-105">In IIS 7, you may also have to modify the **maxAllowedContentLength** attribute.</span></span> <span data-ttu-id="3dc1a-106">Par défaut, la limite de téléchargement d’IIS 7 est de 30 millions octets.</span><span class="sxs-lookup"><span data-stu-id="3dc1a-106">By default, the IIS 7 upload limit is 30 million bytes.</span></span> <span data-ttu-id="3dc1a-107">Pour plus d’informations sur la modification de la valeur par défaut IIS, consultez [KB942074](https://support.microsoft.com//kb/942074).</span><span class="sxs-lookup"><span data-stu-id="3dc1a-107">For details and information on changing the IIS default, see [KB942074](https://support.microsoft.com//kb/942074).</span></span>

 

 




