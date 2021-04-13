---
description: 'La méthode Revert ignore toutes les modifications apportées à un flux transactionnel depuis le dernier appel de IByteBuffer :: Commit.'
ms.assetid: da3d9810-6511-43d5-af87-03a392f8be75
title: 'IByteBuffer :: Revert, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Revert
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: cf7873407196c98868ca45c73db503568f8259e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201368"
---
# <a name="ibytebufferrevert-method"></a><span data-ttu-id="21f77-103">IByteBuffer :: Revert, méthode</span><span class="sxs-lookup"><span data-stu-id="21f77-103">IByteBuffer::Revert method</span></span>

<span data-ttu-id="21f77-104">\[La méthode **Revert** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="21f77-104">\[The **Revert** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="21f77-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="21f77-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="21f77-106">L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="21f77-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="21f77-107">La méthode **Revert** ignore toutes les modifications apportées à un flux transactionnel depuis le dernier appel de [**IByteBuffer :: Commit**](ibytebuffer-commit.md) .</span><span class="sxs-lookup"><span data-stu-id="21f77-107">The **Revert** method discards all changes that have been made to a transacted stream since the last [**IByteBuffer::Commit**](ibytebuffer-commit.md) call.</span></span>

## <a name="syntax"></a><span data-ttu-id="21f77-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21f77-108">Syntax</span></span>


```C++
HRESULT Revert();
```



## <a name="parameters"></a><span data-ttu-id="21f77-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21f77-109">Parameters</span></span>

<span data-ttu-id="21f77-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="21f77-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="21f77-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="21f77-111">Return value</span></span>

<span data-ttu-id="21f77-112">La valeur de retour est un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="21f77-112">The return value is an **HRESULT**.</span></span> <span data-ttu-id="21f77-113">La valeur S \_ OK indique que l’appel a réussi et que le flux a été rétabli à sa version précédente.</span><span class="sxs-lookup"><span data-stu-id="21f77-113">A value of S\_OK indicates the call was successful and the stream was reverted to its previous version.</span></span>

## <a name="remarks"></a><span data-ttu-id="21f77-114">Notes</span><span class="sxs-lookup"><span data-stu-id="21f77-114">Remarks</span></span>

<span data-ttu-id="21f77-115">Cette méthode ignore les modifications apportées à un flux transactionnel depuis la dernière opération de validation.</span><span class="sxs-lookup"><span data-stu-id="21f77-115">This method discards changes made to a transacted stream since the last commit operation.</span></span>

## <a name="examples"></a><span data-ttu-id="21f77-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="21f77-116">Examples</span></span>

<span data-ttu-id="21f77-117">L’exemple suivant illustre la restauration d’un flux transactionnel avec la dernière opération validée.</span><span class="sxs-lookup"><span data-stu-id="21f77-117">The following example shows reverting a transacted stream to the last-committed operation.</span></span>


```C++
HRESULT  hr;

hr = pIByteBuff->Revert();
if (FAILED(hr))
  printf("Failed IByteBuffer::Revert\n");
```



## <a name="requirements"></a><span data-ttu-id="21f77-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21f77-118">Requirements</span></span>



| <span data-ttu-id="21f77-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21f77-119">Requirement</span></span> | <span data-ttu-id="21f77-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="21f77-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21f77-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21f77-121">Minimum supported client</span></span><br/> | <span data-ttu-id="21f77-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21f77-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="21f77-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21f77-123">Minimum supported server</span></span><br/> | <span data-ttu-id="21f77-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21f77-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="21f77-125">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="21f77-125">End of client support</span></span><br/>    | <span data-ttu-id="21f77-126">Windows XP</span><span class="sxs-lookup"><span data-stu-id="21f77-126">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="21f77-127">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="21f77-127">End of server support</span></span><br/>    | <span data-ttu-id="21f77-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="21f77-128">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="21f77-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="21f77-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="21f77-130"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="21f77-130"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="21f77-131">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="21f77-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="21f77-132"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="21f77-132"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="21f77-133">DLL</span><span class="sxs-lookup"><span data-stu-id="21f77-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21f77-134"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21f77-134"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="21f77-135">IID</span><span class="sxs-lookup"><span data-stu-id="21f77-135">IID</span></span><br/>                      | <span data-ttu-id="21f77-136">IID \_ IByteBuffer est défini en tant que E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="21f77-136">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

