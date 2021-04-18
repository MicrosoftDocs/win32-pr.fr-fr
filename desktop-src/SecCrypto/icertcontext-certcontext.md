---
description: Définit ou récupère le contexte PCCERT \_ d’un certificat.
ms.assetid: aedd219d-43fa-4722-9af4-36172d2c18b0
title: 'ICertContext :: CertContext, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.CertContext
- ICertContext.get_CertContext
- ICertContext.put_CertContext
- CertContext.CertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 38bd1c704ca709fc1e4b6072bb68c2105dc5db9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540519"
---
# <a name="icertcontextcertcontext-property"></a><span data-ttu-id="25294-103">ICertContext :: CertContext, propriété</span><span class="sxs-lookup"><span data-stu-id="25294-103">ICertContext::CertContext property</span></span>

<span data-ttu-id="25294-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="25294-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="25294-105">La propriété **CertContext** définit ou récupère le contexte PCCERT \_ d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="25294-105">The **CertContext** property sets or retrieves the PCCERT\_CONTEXT of a certificate.</span></span>

<span data-ttu-id="25294-106">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="25294-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="25294-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25294-107">Syntax</span></span>


```VB
CertContext.CertContext As Long
```



## <a name="property-value"></a><span data-ttu-id="25294-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="25294-108">Property value</span></span>

<span data-ttu-id="25294-109">Contexte PCCERT \_ du certificat.</span><span class="sxs-lookup"><span data-stu-id="25294-109">The PCCERT\_CONTEXT of the certificate.</span></span>

## <a name="error-codes"></a><span data-ttu-id="25294-110">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="25294-110">Error codes</span></span>

<span data-ttu-id="25294-111">Si les méthodes d’accès aux propriétés **placent \_ CertContext** et **obtiennent \_ CertContext** , elles retournent la réponse \_ OK.</span><span class="sxs-lookup"><span data-stu-id="25294-111">If the property access methods **put\_CertContext** and **get\_CertContext** succeed, they return S\_OK.</span></span>

<span data-ttu-id="25294-112">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="25294-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="25294-113">Notes</span><span class="sxs-lookup"><span data-stu-id="25294-113">Remarks</span></span>

<span data-ttu-id="25294-114">Vous devez appeler la méthode [**FreeContext**](icertcontext-freecontext.md) ou la fonction [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) pour libérer le contexte.</span><span class="sxs-lookup"><span data-stu-id="25294-114">You must call either the [**FreeContext**](icertcontext-freecontext.md) method or the [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) function to free the context.</span></span>

<span data-ttu-id="25294-115">Si vous définissez la propriété **CertContext** , l’état de l’intégralité de l’objet de [**certificat**](certificate.md) est réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="25294-115">If you set the **CertContext** property, the state of the entire [**Certificate**](certificate.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="25294-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25294-116">Requirements</span></span>



| <span data-ttu-id="25294-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25294-117">Requirement</span></span> | <span data-ttu-id="25294-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="25294-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25294-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="25294-119">Redistributable</span></span><br/> | <span data-ttu-id="25294-120">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="25294-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="25294-121">DLL</span><span class="sxs-lookup"><span data-stu-id="25294-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="25294-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25294-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25294-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25294-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25294-124">**ICertContext**</span><span class="sxs-lookup"><span data-stu-id="25294-124">**ICertContext**</span></span>](icertcontext.md)
</dt> </dl>

 

 




