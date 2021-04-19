---
description: Définit ou récupère le \_ \_ contexte de chaîne PCCERT d’un certificat.
ms.assetid: 1b33ecd5-88c9-4654-9d2d-95a0be4283c6
title: 'IChainContext :: ChainContext, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.ChainContext
- IChainContext.get_ChainContext
- IChainContext.put_ChainContext
- ChainContext.ChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36b2f6f5811c844e4e43544f5b56b8de66cb3bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525353"
---
# <a name="ichaincontextchaincontext-property"></a><span data-ttu-id="21ca4-103">IChainContext :: ChainContext, propriété</span><span class="sxs-lookup"><span data-stu-id="21ca4-103">IChainContext::ChainContext property</span></span>

<span data-ttu-id="21ca4-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="21ca4-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="21ca4-105">La propriété **chainContext** définit ou récupère le \_ \_ contexte de chaîne PCCERT d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="21ca4-105">The **ChainContext** property sets or retrieves the PCCERT\_CHAIN\_CONTEXT of a certificate.</span></span>

<span data-ttu-id="21ca4-106">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="21ca4-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="21ca4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21ca4-107">Syntax</span></span>


```VB
' Data type: Long

ChainContext.ChainContext As Long
```



## <a name="property-value"></a><span data-ttu-id="21ca4-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="21ca4-108">Property value</span></span>

<span data-ttu-id="21ca4-109">\_Contexte de la chaîne PCCERT \_ du certificat.</span><span class="sxs-lookup"><span data-stu-id="21ca4-109">The PCCERT\_CHAIN\_CONTEXT of the certificate.</span></span>

## <a name="error-codes"></a><span data-ttu-id="21ca4-110">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="21ca4-110">Error codes</span></span>

<span data-ttu-id="21ca4-111">Si les méthodes d’accès aux propriétés **placent \_ chainContext** et **obtiennent \_ chainContext** , elles retournent la réponse \_ OK.</span><span class="sxs-lookup"><span data-stu-id="21ca4-111">If the property access methods **put\_ChainContext** and **get\_ChainContext** succeed, they return S\_OK.</span></span>

<span data-ttu-id="21ca4-112">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="21ca4-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="21ca4-113">Notes</span><span class="sxs-lookup"><span data-stu-id="21ca4-113">Remarks</span></span>

<span data-ttu-id="21ca4-114">Vous devez appeler la méthode [**FreeContext**](ichaincontext-freecontext.md) ou la fonction [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) pour libérer le contexte.</span><span class="sxs-lookup"><span data-stu-id="21ca4-114">You must call either the [**FreeContext**](ichaincontext-freecontext.md) method or the [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) function to free the context.</span></span>

<span data-ttu-id="21ca4-115">Si vous définissez la propriété **chainContext** , l’état de la totalité de l’objet [**chaîne**](chain.md) est réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="21ca4-115">If you set the **ChainContext** property, the state of the entire [**Chain**](chain.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="21ca4-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21ca4-116">Requirements</span></span>



| <span data-ttu-id="21ca4-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21ca4-117">Requirement</span></span> | <span data-ttu-id="21ca4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="21ca4-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21ca4-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="21ca4-119">Redistributable</span></span><br/> | <span data-ttu-id="21ca4-120">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="21ca4-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="21ca4-121">DLL</span><span class="sxs-lookup"><span data-stu-id="21ca4-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="21ca4-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21ca4-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21ca4-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21ca4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21ca4-124">**IChainContext**</span><span class="sxs-lookup"><span data-stu-id="21ca4-124">**IChainContext**</span></span>](ichaincontext.md)
</dt> </dl>

 

 




