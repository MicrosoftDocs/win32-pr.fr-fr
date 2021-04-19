---
description: Retourne une collection d’OID qui représente les stratégies d’application utilisées pour créer l’objet de chaîne.
ms.assetid: dca0acbf-e369-4216-a4f6-44ed965011d0
title: Méthode CertificateStatus. ApplicationPolicies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.ApplicationPolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b02503590a64c1c14e3f66dc5d07d9d61034bd60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542507"
---
# <a name="certificatestatusapplicationpolicies-method"></a><span data-ttu-id="63390-103">Méthode CertificateStatus. ApplicationPolicies</span><span class="sxs-lookup"><span data-stu-id="63390-103">CertificateStatus.ApplicationPolicies method</span></span>

<span data-ttu-id="63390-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="63390-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="63390-105">Utilisez plutôt la [**structure X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="63390-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="63390-106">La méthode **ApplicationPolicies** retourne une collection d' [**OID**](oids.md) qui représente les stratégies d’application utilisées pour créer l’objet de [**chaîne**](chain.md) .</span><span class="sxs-lookup"><span data-stu-id="63390-106">The **ApplicationPolicies** method returns an [**OIDs**](oids.md) collection that represents the application policies used to create the [**Chain**](chain.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="63390-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63390-107">Syntax</span></span>


```VB
CertificateStatus.ApplicationPolicies()
```



## <a name="parameters"></a><span data-ttu-id="63390-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63390-108">Parameters</span></span>

<span data-ttu-id="63390-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="63390-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="63390-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="63390-110">Return value</span></span>

<span data-ttu-id="63390-111">Collection d' [**OID**](oids.md) .</span><span class="sxs-lookup"><span data-stu-id="63390-111">An [**OIDs**](oids.md) collection.</span></span> <span data-ttu-id="63390-112">Chaque objet [**OID**](oid.md) de la collection représente un OID de stratégie d’application.</span><span class="sxs-lookup"><span data-stu-id="63390-112">Each [**OID**](oid.md) object in the collection represents an application policy OID.</span></span>

## <a name="remarks"></a><span data-ttu-id="63390-113">Notes</span><span class="sxs-lookup"><span data-stu-id="63390-113">Remarks</span></span>

<span data-ttu-id="63390-114">Ajoutez des OID de stratégie d’application au regroupement pour spécifier les stratégies d’application qui doivent être utilisées pour générer la chaîne d’approbation de certificat.</span><span class="sxs-lookup"><span data-stu-id="63390-114">Add application policy OIDs to the collection to specify the application policies that should be used to build the certificate trust chain.</span></span> <span data-ttu-id="63390-115">Si la collection contient au moins un objet [**OID**](oid.md) , l’objet [**EKU**](eku.md) renvoyé par la méthode [**CertificateStatus. EKU**](certificatestatus-eku.md) est ignoré.</span><span class="sxs-lookup"><span data-stu-id="63390-115">If the collection contains at least one [**OID**](oid.md) object, the [**EKU**](eku.md) object returned by the [**CertificateStatus.EKU**](certificatestatus-eku.md) method is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="63390-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63390-116">Requirements</span></span>



| <span data-ttu-id="63390-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63390-117">Requirement</span></span> | <span data-ttu-id="63390-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="63390-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63390-119">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="63390-119">End of client support</span></span><br/> | <span data-ttu-id="63390-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63390-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="63390-121">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="63390-121">End of server support</span></span><br/> | <span data-ttu-id="63390-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63390-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="63390-123">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="63390-123">Redistributable</span></span><br/>       | <span data-ttu-id="63390-124">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="63390-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="63390-125">DLL</span><span class="sxs-lookup"><span data-stu-id="63390-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="63390-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63390-126"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
