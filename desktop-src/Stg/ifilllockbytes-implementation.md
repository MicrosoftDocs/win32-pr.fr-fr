---
title: IFillLockBytes-implémentation
description: Le système fournit une implémentation de IFillLockBytes dans le cadre de l’implémentation de fichiers composés.
ms.assetid: a8aed8c5-3c4c-4cce-b568-68031da0edf5
keywords:
- IFillLockBytes Strctd STG, implémentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58737d02e3e6bc2511670178825aef8cbe2dcc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939933"
---
# <a name="ifilllockbytes---implementation"></a><span data-ttu-id="c2c03-104">IFillLockBytes-implémentation</span><span class="sxs-lookup"><span data-stu-id="c2c03-104">IFillLockBytes - Implementation</span></span>

<span data-ttu-id="c2c03-105">Le système fournit une implémentation de [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) dans le cadre de l’implémentation de fichiers composés.</span><span class="sxs-lookup"><span data-stu-id="c2c03-105">The system provides an [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) implementation as part of the Compound Files implementation.</span></span>

<span data-ttu-id="c2c03-106">Le téléchargement de code peut créer une instance d’un objet de fichier composé asynchrone en appelant [**StgOpenAsyncDocFileOnIFillLockBytes**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes).</span><span class="sxs-lookup"><span data-stu-id="c2c03-106">Downloading code can create an instance of an asynchronous Compound File object by calling [**StgOpenAsyncDocFileOnIFillLockBytes**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes).</span></span> <span data-ttu-id="c2c03-107">Le téléchargement de code peut également créer une instance d’un objet wrapper de tableau d’octets asynchrone sur un fichier ou un tableau d’octets existant en appelant la fonction [**StgGetIFillLockBytesOnFile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) ou la fonction [**StgGetIFillLockBytesOnILockBytes**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes) .</span><span class="sxs-lookup"><span data-stu-id="c2c03-107">Downloading code can also create an instance of an asynchronous byte array wrapper object on an existing file or byte array by calling either the [**StgGetIFillLockBytesOnFile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) function or the [**StgGetIFillLockBytesOnILockBytes**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes) function.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="c2c03-108">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="c2c03-108">When to Use</span></span>

<span data-ttu-id="c2c03-109">Actuellement, les monikers d’URL sont les seuls utilisateurs de l’implémentation de stockage asynchrone COM.</span><span class="sxs-lookup"><span data-stu-id="c2c03-109">Currently, URL monikers are the only users of the COM asynchronous storage implementation.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2c03-110">Notes</span><span class="sxs-lookup"><span data-stu-id="c2c03-110">Remarks</span></span>

<span data-ttu-id="c2c03-111">Voici les quatre méthodes de l’implémentation de [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) .</span><span class="sxs-lookup"><span data-stu-id="c2c03-111">The following are the four methods of the [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) implementation.</span></span>

<dl> <dt>

<span data-ttu-id="c2c03-112"><span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**IFillLockBytes::FillAppend**</span><span class="sxs-lookup"><span data-stu-id="c2c03-112"><span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**IFillLockBytes::FillAppend**</span></span>
</dt> <dd>

<span data-ttu-id="c2c03-113">Écrit un nouveau bloc d’octets à la fin d’un tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="c2c03-113">Writes a new block of bytes to the end of a byte array.</span></span> <span data-ttu-id="c2c03-114">La taille du bloc est spécifiée en tant que paramètre de [**FillAppend**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend).</span><span class="sxs-lookup"><span data-stu-id="c2c03-114">The size of the block is specified as a parameter to [**FillAppend**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend).</span></span>

</dd> <dt>

<span data-ttu-id="c2c03-115"><span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**IFillLockBytes::FillAt**</span><span class="sxs-lookup"><span data-stu-id="c2c03-115"><span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**IFillLockBytes::FillAt**</span></span>
</dt> <dd>

<span data-ttu-id="c2c03-116">Écrit un nouveau bloc de données à un emplacement spécifié dans le tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="c2c03-116">Writes a new block of data to a specified location in the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="c2c03-117"><span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**IFillLockBytes::SetFillSize**</span><span class="sxs-lookup"><span data-stu-id="c2c03-117"><span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**IFillLockBytes::SetFillSize**</span></span>
</dt> <dd>

<span data-ttu-id="c2c03-118">Définit la taille du tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="c2c03-118">Sets the size of the byte array.</span></span> <span data-ttu-id="c2c03-119">Retourne E \_ Fail à partir des appels à [**ILockBytes :: readatum**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat) qui tentent d’accéder aux données au-delà de la limite supérieure spécifiée par la méthode.</span><span class="sxs-lookup"><span data-stu-id="c2c03-119">Returns E\_FAIL from calls to [**ILockBytes::ReadAt**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat) that attempt to access data beyond the upper limit specified by the method.</span></span>

</dd> <dt>

<span data-ttu-id="c2c03-120"><span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**IFillLockBytes :: Terminate**</span><span class="sxs-lookup"><span data-stu-id="c2c03-120"><span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**IFillLockBytes::Terminate**</span></span>
</dt> <dd>

<span data-ttu-id="c2c03-121">Informe le tableau d’octets qu’un téléchargement a été terminé, avec succès ou non.</span><span class="sxs-lookup"><span data-stu-id="c2c03-121">Informs the byte array that a download has been terminated, either successfully or unsuccessfully.</span></span>

</dd> </dl>

 

 




