---
description: Libère un \_ contexte PCCERT acquis par le biais de la propriété CertContext.
ms.assetid: fcb9e885-d26c-4866-a35d-1c940bfe8162
title: 'ICertContext :: FreeContext, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.FreeContext
- CertContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e1f4c216f6e417726e60d5f2e2bd67387a51d352
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532674"
---
# <a name="icertcontextfreecontext-method"></a><span data-ttu-id="add25-103">ICertContext :: FreeContext, méthode</span><span class="sxs-lookup"><span data-stu-id="add25-103">ICertContext::FreeContext method</span></span>

<span data-ttu-id="add25-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="add25-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="add25-105">La méthode **FreeContext** libère un \_ contexte PCCERT acquis par le biais de la propriété [**CertContext**](icertcontext-certcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="add25-105">The **FreeContext** method releases a PCCERT\_CONTEXT acquired through the [**CertContext**](icertcontext-certcontext.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="add25-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="add25-106">Syntax</span></span>


```VB
CertContext.FreeContext( _
  ByVal pCertContext _
)
```



## <a name="parameters"></a><span data-ttu-id="add25-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="add25-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="add25-108">*pCertContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="add25-108">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="add25-109">Contexte PCCERT \_ à libérer.</span><span class="sxs-lookup"><span data-stu-id="add25-109">The PCCERT\_CONTEXT to be released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="add25-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="add25-110">Return value</span></span>

<span data-ttu-id="add25-111">La valeur de retour est un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="add25-111">The return value is an **HRESULT**.</span></span> <span data-ttu-id="add25-112">La valeur S \_ OK indique la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="add25-112">A value of S\_OK indicates success.</span></span> <span data-ttu-id="add25-113">Toute autre valeur indique que l’opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="add25-113">Any other value indicates that the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="add25-114">Notes</span><span class="sxs-lookup"><span data-stu-id="add25-114">Remarks</span></span>

<span data-ttu-id="add25-115">Cette méthode ne libère pas le \_ contexte PCCERT contenu dans un objet de [**certificat**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="add25-115">This method does not release the PCCERT\_CONTEXT contained within a [**Certificate**](certificate.md) object.</span></span> <span data-ttu-id="add25-116">Elle doit être utilisée uniquement pour libérer un \_ contexte PCCERT acquis par le biais de la propriété [**CertContext**](icertcontext-certcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="add25-116">It should be used only to release a PCCERT\_CONTEXT acquired through the [**CertContext**](icertcontext-certcontext.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="add25-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="add25-117">Requirements</span></span>



| <span data-ttu-id="add25-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="add25-118">Requirement</span></span> | <span data-ttu-id="add25-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="add25-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="add25-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="add25-120">Redistributable</span></span><br/> | <span data-ttu-id="add25-121">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="add25-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="add25-122">DLL</span><span class="sxs-lookup"><span data-stu-id="add25-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="add25-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="add25-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="add25-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="add25-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="add25-125">**ICertContext**</span><span class="sxs-lookup"><span data-stu-id="add25-125">**ICertContext**</span></span>](icertcontext.md)
</dt> </dl>

 

 




