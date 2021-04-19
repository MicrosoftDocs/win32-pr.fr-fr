---
description: Pour créer des extensions personnalisées ou encoder une extension complexe, vous pouvez écrire vos propres gestionnaires d’extension qui exportent des interfaces personnalisées.
ms.assetid: a33ac417-b5f9-4ad7-a26e-13cdb1e4ac1b
title: Écriture de gestionnaires d’extensions personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c8c4380b11fd0b0b1a5484ba0a7ab80f69c967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522163"
---
# <a name="writing-custom-extension-handlers"></a><span data-ttu-id="e436d-103">Écriture de gestionnaires d’extensions personnalisés</span><span class="sxs-lookup"><span data-stu-id="e436d-103">Writing Custom Extension Handlers</span></span>

<span data-ttu-id="e436d-104">Pour créer des extensions personnalisées ou encoder une extension complexe, vous pouvez écrire vos propres gestionnaires d’extension qui exportent des interfaces personnalisées.</span><span class="sxs-lookup"><span data-stu-id="e436d-104">To create custom extensions or to encode a complex extension, you can write your own extension handlers that export custom interfaces.</span></span> <span data-ttu-id="e436d-105">Les services de certificats Microsoft sont fournis avec les interfaces suivantes, qui peuvent être utilisées pour encoder différents types de données d’extension : [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname), [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring), [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo), [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray), [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray)et [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray).</span><span class="sxs-lookup"><span data-stu-id="e436d-105">Microsoft Certificate Services ships with the following interfaces which can be used to encode various types of extension data: [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname), [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring), [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo), [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray), [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray), and [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray).</span></span> <span data-ttu-id="e436d-106">Ces interfaces sont contenues dans Certenc.dll.</span><span class="sxs-lookup"><span data-stu-id="e436d-106">These interfaces are contained in Certenc.dll.</span></span> <span data-ttu-id="e436d-107">En outre, les informations de type de ces interfaces sont contenues dans Certencl.dll, qui est contenue dans le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="e436d-107">Additionally, the type information for these interfaces is contained in Certencl.dll, which is contained in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="e436d-108">Pour plus d’informations sur les gestionnaires d’extension, consultez [gestionnaires d’extension](extension-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="e436d-108">For more information about extension handlers, see [Extension Handlers](extension-handlers.md).</span></span>

 

 



