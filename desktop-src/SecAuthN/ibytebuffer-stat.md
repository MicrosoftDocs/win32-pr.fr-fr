---
description: La méthode stat récupère les informations statistiques de l’objet de flux.
ms.assetid: 7dfb59e9-143a-402e-990a-a2b35e6443dd
title: 'IByteBuffer :: stat, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Stat
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bbbf033fc9ad5a25b3bcf5c22028ac1237f46c14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521141"
---
# <a name="ibytebufferstat-method"></a><span data-ttu-id="d1b76-103">IByteBuffer :: stat, méthode</span><span class="sxs-lookup"><span data-stu-id="d1b76-103">IByteBuffer::Stat method</span></span>

<span data-ttu-id="d1b76-104">\[La méthode **Stat** est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="d1b76-104">\[The **Stat** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d1b76-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d1b76-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d1b76-106">L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="d1b76-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="d1b76-107">La méthode **Stat** récupère les informations statistiques de l’objet de flux.</span><span class="sxs-lookup"><span data-stu-id="d1b76-107">The **Stat** method retrieves statistical information from the stream object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1b76-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1b76-108">Syntax</span></span>


```C++
HRESULT Stat(
  [out] LPSTATSTRUCT pstatstg,
  [in]  LONG         grfStatFlag
);
```



## <a name="parameters"></a><span data-ttu-id="d1b76-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1b76-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1b76-110">*pstatstg* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d1b76-110">*pstatstg* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1b76-111">Pointe vers une structure **STATSTRUCT** où cette méthode place des informations sur cet objet de flux.</span><span class="sxs-lookup"><span data-stu-id="d1b76-111">Points to a **STATSTRUCT** structure where this method places information about this stream object.</span></span> <span data-ttu-id="d1b76-112">Ce pointeur est **null** si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="d1b76-112">This pointer is **NULL** if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="d1b76-113">*grfStatFlag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d1b76-113">*grfStatFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1b76-114">Spécifie que cette méthode ne retourne pas certains des champs de la structure **STATSTRUCT** , ce qui entraîne l’enregistrement d’une opération d’allocation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="d1b76-114">Specifies that this method does not return some of the fields in the **STATSTRUCT** structure, thus saving a memory allocation operation.</span></span> <span data-ttu-id="d1b76-115">Les valeurs sont extraites de l’énumération [**StatFlag**](/windows/win32/api/wtypes/ne-wtypes-statflag)</span><span class="sxs-lookup"><span data-stu-id="d1b76-115">Values are taken from the [**STATFLAG**](/windows/win32/api/wtypes/ne-wtypes-statflag) enumeration</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1b76-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1b76-116">Return value</span></span>

<span data-ttu-id="d1b76-117">La valeur de retour est un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d1b76-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="d1b76-118">La valeur S \_ OK indique que l’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="d1b76-118">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1b76-119">Notes</span><span class="sxs-lookup"><span data-stu-id="d1b76-119">Remarks</span></span>

<span data-ttu-id="d1b76-120">La méthode **IByteBuffer :: stat** récupère un pointeur vers la structure **STATSTRUCT** qui contient des informations sur ce flux ouvert.</span><span class="sxs-lookup"><span data-stu-id="d1b76-120">The **IByteBuffer::Stat** method retrieves a pointer to the **STATSTRUCT** structure that contains information about this open stream.</span></span>

## <a name="examples"></a><span data-ttu-id="d1b76-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="d1b76-121">Examples</span></span>

<span data-ttu-id="d1b76-122">L’exemple suivant montre comment récupérer des informations statistiques à partir du flux.</span><span class="sxs-lookup"><span data-stu-id="d1b76-122">The following example shows retrieving statistical information from the stream.</span></span>


```C++
STATSTRUCT  statstr;
HRESULT     hr;

// Retrieve the statistical information.
hr = pIByteBuff->Stat(&statstr,
                      STATFLAG_DEFAULT);
if (FAILED(hr))
  printf("Failed IByteBuffer::Stat\n");
else
  // Use statstr as needed.
```



## <a name="requirements"></a><span data-ttu-id="d1b76-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1b76-123">Requirements</span></span>



| <span data-ttu-id="d1b76-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1b76-124">Requirement</span></span> | <span data-ttu-id="d1b76-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1b76-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1b76-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1b76-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d1b76-127">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1b76-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d1b76-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1b76-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d1b76-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1b76-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d1b76-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d1b76-130">End of client support</span></span><br/>    | <span data-ttu-id="d1b76-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d1b76-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d1b76-132">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="d1b76-132">End of server support</span></span><br/>    | <span data-ttu-id="d1b76-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d1b76-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d1b76-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1b76-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1b76-135"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1b76-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1b76-136">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d1b76-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="d1b76-137"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d1b76-137"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d1b76-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d1b76-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1b76-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1b76-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d1b76-140">IID</span><span class="sxs-lookup"><span data-stu-id="d1b76-140">IID</span></span><br/>                      | <span data-ttu-id="d1b76-141">IID \_ IByteBuffer est défini en tant que E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="d1b76-141">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

