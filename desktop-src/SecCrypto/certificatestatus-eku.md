---
description: Retourne l’objet EKU utilisé pour générer l’objet de chaîne.
ms.assetid: d02f1614-6a4f-4c60-b406-ce174a99e9a5
title: Méthode CertificateStatus. EKU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d386251c6d7f674d3850de275559bcb87ea6d61e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523885"
---
# <a name="certificatestatuseku-method"></a><span data-ttu-id="c8175-103">Méthode CertificateStatus. EKU</span><span class="sxs-lookup"><span data-stu-id="c8175-103">CertificateStatus.EKU method</span></span>

<span data-ttu-id="c8175-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c8175-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c8175-105">Utilisez plutôt la [**structure X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="c8175-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c8175-106">La méthode **EKU** retourne l’objet [**EKU**](eku.md) utilisé pour créer l’objet de [**chaîne**](chain.md) .</span><span class="sxs-lookup"><span data-stu-id="c8175-106">The **EKU** method returns the [**EKU**](eku.md) object used to build the [**Chain**](chain.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8175-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8175-107">Syntax</span></span>


```VB
CertificateStatus.EKU()
```



## <a name="parameters"></a><span data-ttu-id="c8175-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8175-108">Parameters</span></span>

<span data-ttu-id="c8175-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c8175-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c8175-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c8175-110">Return value</span></span>

<span data-ttu-id="c8175-111">Cette méthode retourne un objet [**EKU**](eku.md) qui indique le paramètre d’utilisation de la clé étendue du [*certificat*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c8175-111">This method returns an [**EKU**](eku.md) object that indicates the extended key usage setting of the [*certificate*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="c8175-112">Le paramètre EKU établit l’utilisation valide d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="c8175-112">The EKU setting establishes a certificate's valid use.</span></span> <span data-ttu-id="c8175-113">Un seul objet **EKU** peut être défini pour chaque certificat.</span><span class="sxs-lookup"><span data-stu-id="c8175-113">Only a single **EKU** object can be set for each certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8175-114">Notes</span><span class="sxs-lookup"><span data-stu-id="c8175-114">Remarks</span></span>

<span data-ttu-id="c8175-115">La méthode [**CertificateStatus. ApplicationPolicies**](certificatestatus-applicationpolicies.md) fournit les mêmes fonctionnalités que cette méthode, mais permet de spécifier un grand nombre de paramètres au lieu d’un seul.</span><span class="sxs-lookup"><span data-stu-id="c8175-115">The [**CertificateStatus.ApplicationPolicies**](certificatestatus-applicationpolicies.md) method provides the same functionality as this method but allows many settings to be specified instead of only one.</span></span> <span data-ttu-id="c8175-116">Si la collection d' [**OID**](oids.md) retournée par la méthode **ApplicationPolicies** contient un ou plusieurs objets [**OID**](oid.md) , l’objet [**EKU**](eku.md) retourné par cette méthode est ignoré.</span><span class="sxs-lookup"><span data-stu-id="c8175-116">If the [**OIDs**](oids.md) collection returned by the **ApplicationPolicies** method contains one or more [**OID**](oid.md) objects, the [**EKU**](eku.md) object returned by this method is ignored.</span></span> <span data-ttu-id="c8175-117">Utilisez la méthode **ApplicationPolicies** à la place de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c8175-117">Use the **ApplicationPolicies** method instead of this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8175-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8175-118">Requirements</span></span>



| <span data-ttu-id="c8175-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8175-119">Requirement</span></span> | <span data-ttu-id="c8175-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8175-120">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8175-121">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="c8175-121">End of client support</span></span><br/> | <span data-ttu-id="c8175-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8175-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c8175-123">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="c8175-123">End of server support</span></span><br/> | <span data-ttu-id="c8175-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8175-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c8175-125">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="c8175-125">Redistributable</span></span><br/>       | <span data-ttu-id="c8175-126">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="c8175-126">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c8175-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c8175-127">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c8175-128"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8175-128"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8175-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8175-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8175-130">**CertificateStatus**</span><span class="sxs-lookup"><span data-stu-id="c8175-130">**CertificateStatus**</span></span>](certificatestatus.md)
</dt> <dt>

[<span data-ttu-id="c8175-131">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="c8175-131">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="c8175-132">**EKU**</span><span class="sxs-lookup"><span data-stu-id="c8175-132">**EKU**</span></span>](eku.md)
</dt> </dl>

 

 
