---
description: Libère un \_ contexte de chaîne PCCERT \_ acquis par le biais de la propriété chainContext.
ms.assetid: fa9a6171-58ff-400f-bdcc-ba32a0ae0441
title: 'IChainContext :: FreeContext, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.FreeContext
- ChainContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 413b119f250bfbd061301391fee7741362979f65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530558"
---
# <a name="ichaincontextfreecontext-method"></a><span data-ttu-id="8d67c-103">IChainContext :: FreeContext, méthode</span><span class="sxs-lookup"><span data-stu-id="8d67c-103">IChainContext::FreeContext method</span></span>

<span data-ttu-id="8d67c-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="8d67c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="8d67c-105">La méthode **FreeContext** libère un \_ contexte de chaîne PCCERT \_ acquis par le biais de la propriété [**chainContext**](ichaincontext-chaincontext.md) .</span><span class="sxs-lookup"><span data-stu-id="8d67c-105">The **FreeContext** method releases a PCCERT\_CHAIN\_CONTEXT acquired through the [**ChainContext**](ichaincontext-chaincontext.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d67c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d67c-106">Syntax</span></span>


```VB
ChainContext.FreeContext()
```



## <a name="parameters"></a><span data-ttu-id="8d67c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d67c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d67c-108">*pChainContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d67c-108">*pChainContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d67c-109">\_Contexte de la chaîne PCCERT \_ à libérer.</span><span class="sxs-lookup"><span data-stu-id="8d67c-109">The PCCERT\_CHAIN\_CONTEXT to be released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d67c-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8d67c-110">Return value</span></span>

<span data-ttu-id="8d67c-111">La valeur de retour est un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8d67c-111">The return value is an **HRESULT**.</span></span> <span data-ttu-id="8d67c-112">La valeur S \_ OK indique la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="8d67c-112">A value of S\_OK indicates success.</span></span> <span data-ttu-id="8d67c-113">Toute autre valeur indique que l’opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="8d67c-113">Any other value indicates that the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d67c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="8d67c-114">Remarks</span></span>

<span data-ttu-id="8d67c-115">Cette méthode ne libère pas le \_ contexte de chaîne PCCERT \_ contenu dans un objet [**chaîne**](chain.md) .</span><span class="sxs-lookup"><span data-stu-id="8d67c-115">This method does not release the PCCERT\_CHAIN\_CONTEXT contained within a [**Chain**](chain.md) object.</span></span> <span data-ttu-id="8d67c-116">Elle doit être utilisée uniquement pour libérer un \_ contexte de chaîne PCCERT \_ acquis par le biais de la propriété [**chainContext**](ichaincontext-chaincontext.md) .</span><span class="sxs-lookup"><span data-stu-id="8d67c-116">It should be used only to release a PCCERT\_CHAIN\_CONTEXT acquired through the [**ChainContext**](ichaincontext-chaincontext.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d67c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d67c-117">Requirements</span></span>



| <span data-ttu-id="8d67c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d67c-118">Requirement</span></span> | <span data-ttu-id="8d67c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d67c-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d67c-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="8d67c-120">Redistributable</span></span><br/> | <span data-ttu-id="8d67c-121">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="8d67c-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8d67c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="8d67c-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="8d67c-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d67c-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d67c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d67c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d67c-125">**IChainContext**</span><span class="sxs-lookup"><span data-stu-id="8d67c-125">**IChainContext**</span></span>](ichaincontext.md)
</dt> </dl>

 

 




