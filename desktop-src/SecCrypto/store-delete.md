---
description: Supprime le magasin de certificats représenté par l’objet de magasin actuel.
ms.assetid: 274914ee-27a0-4bd6-8510-af897aab3a2d
title: Store. Delete, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41c6417dae5006eb2ecaf64660fd0007cdf37fd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533503"
---
# <a name="storedelete-method"></a><span data-ttu-id="47305-103">Store. Delete, méthode</span><span class="sxs-lookup"><span data-stu-id="47305-103">Store.Delete method</span></span>

<span data-ttu-id="47305-104">\[La méthode de **suppression** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="47305-104">\[The **Delete** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="47305-105">Utilisez plutôt la [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="47305-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="47305-106">La méthode **Delete** supprime le [*magasin de certificats*](../secgloss/c-gly.md) représenté par l’objet [**Store**](certificate.md) actuel.</span><span class="sxs-lookup"><span data-stu-id="47305-106">The **Delete** method deletes the [*certificate store*](../secgloss/c-gly.md) that is represented by the current [**Store**](certificate.md) object.</span></span> <span data-ttu-id="47305-107">Cette méthode supprime uniquement les magasins qui ne sont pas du système.</span><span class="sxs-lookup"><span data-stu-id="47305-107">This method deletes only nonsystem stores.</span></span>

## <a name="syntax"></a><span data-ttu-id="47305-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47305-108">Syntax</span></span>


```VB
Store.Delete()
```



## <a name="parameters"></a><span data-ttu-id="47305-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47305-109">Parameters</span></span>

<span data-ttu-id="47305-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="47305-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="47305-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="47305-111">Return value</span></span>

<span data-ttu-id="47305-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="47305-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="47305-113">Notes</span><span class="sxs-lookup"><span data-stu-id="47305-113">Remarks</span></span>

<span data-ttu-id="47305-114">Les magasins suivants sont des magasins système qui ne peuvent pas être supprimés :</span><span class="sxs-lookup"><span data-stu-id="47305-114">The following stores are system stores and cannot be deleted:</span></span>

-   <span data-ttu-id="47305-115">My</span><span class="sxs-lookup"><span data-stu-id="47305-115">My</span></span>
-   <span data-ttu-id="47305-116">Root</span><span class="sxs-lookup"><span data-stu-id="47305-116">Root</span></span>
-   <span data-ttu-id="47305-117">Confiance</span><span class="sxs-lookup"><span data-stu-id="47305-117">Trust</span></span>
-   <span data-ttu-id="47305-118">CA</span><span class="sxs-lookup"><span data-stu-id="47305-118">CA</span></span>
-   <span data-ttu-id="47305-119">UserDS</span><span class="sxs-lookup"><span data-stu-id="47305-119">UserDS</span></span>
-   <span data-ttu-id="47305-120">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="47305-120">TrustedPublisher</span></span>
-   <span data-ttu-id="47305-121">Interdit</span><span class="sxs-lookup"><span data-stu-id="47305-121">Disallowed</span></span>
-   <span data-ttu-id="47305-122">AuthRoot</span><span class="sxs-lookup"><span data-stu-id="47305-122">AuthRoot</span></span>
-   <span data-ttu-id="47305-123">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="47305-123">TrustedPeople</span></span>

<span data-ttu-id="47305-124">La méthode **Delete** retourne une erreur si elle est appelée à partir d’un script Web.</span><span class="sxs-lookup"><span data-stu-id="47305-124">The **Delete** method returns an error if called from a web script.</span></span>

## <a name="requirements"></a><span data-ttu-id="47305-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47305-125">Requirements</span></span>



| <span data-ttu-id="47305-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47305-126">Requirement</span></span> | <span data-ttu-id="47305-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="47305-127">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47305-128">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="47305-128">Redistributable</span></span><br/> | <span data-ttu-id="47305-129">CAPICOM 2,1 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="47305-129">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="47305-130">DLL</span><span class="sxs-lookup"><span data-stu-id="47305-130">DLL</span></span><br/>             | <dl> <span data-ttu-id="47305-131"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47305-131"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47305-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47305-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47305-133">**Magasin**</span><span class="sxs-lookup"><span data-stu-id="47305-133">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="47305-134">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="47305-134">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
