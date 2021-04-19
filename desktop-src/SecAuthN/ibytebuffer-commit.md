---
description: La méthode Commit garantit que toutes les modifications apportées à un objet ouvert en mode transactionnel sont reflétées dans le stockage parent.
ms.assetid: 00986e48-c5b9-4ac9-a204-a0774cb5e03e
title: 'IByteBuffer :: Commit, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Commit
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 066925361d0ee4391bcd1eaafe33e0ae2d4b9120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528269"
---
# <a name="ibytebuffercommit-method"></a><span data-ttu-id="a65c2-103">IByteBuffer :: Commit, méthode</span><span class="sxs-lookup"><span data-stu-id="a65c2-103">IByteBuffer::Commit method</span></span>

<span data-ttu-id="a65c2-104">\[La méthode de **validation** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="a65c2-104">\[The **Commit** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a65c2-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a65c2-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a65c2-106">L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="a65c2-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="a65c2-107">La méthode **Commit** garantit que toutes les modifications apportées à un objet ouvert en mode transactionnel sont reflétées dans le stockage parent.</span><span class="sxs-lookup"><span data-stu-id="a65c2-107">The **Commit** method ensures that any changes made to an object open in transacted mode are reflected in the parent storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="a65c2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a65c2-108">Syntax</span></span>


```C++
HRESULT Commit(
  [in] LONG grfCommitFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a65c2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a65c2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a65c2-110">*grfCommitFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a65c2-110">*grfCommitFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a65c2-111">Contrôle comment les modifications apportées à un objet de flux sont validées.</span><span class="sxs-lookup"><span data-stu-id="a65c2-111">Controls how the changes for the stream object are committed.</span></span> <span data-ttu-id="a65c2-112">Pour obtenir une définition de ces valeurs, consultez l’énumération STGC.</span><span class="sxs-lookup"><span data-stu-id="a65c2-112">For a definition of these values, see the STGC enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a65c2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a65c2-113">Return value</span></span>

<span data-ttu-id="a65c2-114">La valeur de retour est un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a65c2-114">The return value is an **HRESULT**.</span></span> <span data-ttu-id="a65c2-115">La valeur S \_ OK indique que l’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="a65c2-115">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a65c2-116">Notes</span><span class="sxs-lookup"><span data-stu-id="a65c2-116">Remarks</span></span>

<span data-ttu-id="a65c2-117">Cette méthode garantit que les modifications apportées à un objet de flux ouvert en mode traité sont reflétées dans le stockage parent.</span><span class="sxs-lookup"><span data-stu-id="a65c2-117">This method ensures that changes to a stream object opened in transacted mode are reflected in the parent storage.</span></span> <span data-ttu-id="a65c2-118">Les modifications apportées au flux depuis son ouverture ou la dernière validation sont reflétées dans l’objet de stockage parent.</span><span class="sxs-lookup"><span data-stu-id="a65c2-118">Changes that have been made to the stream since it was opened or last committed are reflected to the parent storage object.</span></span> <span data-ttu-id="a65c2-119">Si le parent est ouvert en mode traité, le parent peut toujours revenir ultérieurement à la restauration des modifications apportées à cet objet de flux.</span><span class="sxs-lookup"><span data-stu-id="a65c2-119">If the parent is opened in transacted mode, the parent may still revert at a later time rolling back the changes to this stream object.</span></span> <span data-ttu-id="a65c2-120">L’implémentation de fichier composé ne prend pas en charge l’ouverture de flux en mode traité. cette méthode a donc très peu d’effet que de vider les mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="a65c2-120">The compound file implementation does not support opening streams in transacted mode, so this method has very little effect other than to flush memory buffers.</span></span>

## <a name="examples"></a><span data-ttu-id="a65c2-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="a65c2-121">Examples</span></span>

<span data-ttu-id="a65c2-122">L’exemple suivant illustre la validation des modifications apportées au stockage.</span><span class="sxs-lookup"><span data-stu-id="a65c2-122">The following example shows committing changes to storage.</span></span>


```C++
HRESULT  hr;

// Commit the buffer.
hr = pIByteBuff->Commit(STGC_DEFAULT | STGC_CONSOLIDATE);
if (FAILED(hr))
  printf("Failed IByteBuffer::Commit\n");
```



## <a name="requirements"></a><span data-ttu-id="a65c2-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a65c2-123">Requirements</span></span>



| <span data-ttu-id="a65c2-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a65c2-124">Requirement</span></span> | <span data-ttu-id="a65c2-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="a65c2-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a65c2-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a65c2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a65c2-127">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a65c2-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a65c2-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a65c2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a65c2-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a65c2-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a65c2-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a65c2-130">End of client support</span></span><br/>    | <span data-ttu-id="a65c2-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a65c2-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a65c2-132">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="a65c2-132">End of server support</span></span><br/>    | <span data-ttu-id="a65c2-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a65c2-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a65c2-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="a65c2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a65c2-135"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a65c2-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a65c2-136">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a65c2-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="a65c2-137"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a65c2-137"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a65c2-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a65c2-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a65c2-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a65c2-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a65c2-140">IID</span><span class="sxs-lookup"><span data-stu-id="a65c2-140">IID</span></span><br/>                      | <span data-ttu-id="a65c2-141">IID \_ IByteBuffer est défini en tant que E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="a65c2-141">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

