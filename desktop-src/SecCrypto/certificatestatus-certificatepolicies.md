---
description: Retourne une collection d’OID qui représente les stratégies de certificat utilisées pour créer l’objet de chaîne.
ms.assetid: 7fe7d3ea-28fc-4c0a-9b43-a97518ac65db
title: Méthode CertificateStatus. CertificatePolicies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98c9e22c0cad40252cc9eebebf9aa32dc4d89b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532612"
---
# <a name="certificatestatuscertificatepolicies-method"></a><span data-ttu-id="edf2d-103">Méthode CertificateStatus. CertificatePolicies</span><span class="sxs-lookup"><span data-stu-id="edf2d-103">CertificateStatus.CertificatePolicies method</span></span>

<span data-ttu-id="edf2d-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="edf2d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="edf2d-105">Utilisez plutôt la [**structure X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="edf2d-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="edf2d-106">La méthode **certificatePolicies** retourne une collection d' [**OID**](oids.md) qui représente les stratégies de certificat utilisées pour créer l’objet de [**chaîne**](chain.md) .</span><span class="sxs-lookup"><span data-stu-id="edf2d-106">The **CertificatePolicies** method returns an [**OIDs**](oids.md) collection that represents the certificate policies used to create the [**Chain**](chain.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="edf2d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="edf2d-107">Syntax</span></span>


```VB
CertificateStatus.CertificatePolicies()
```



## <a name="parameters"></a><span data-ttu-id="edf2d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="edf2d-108">Parameters</span></span>

<span data-ttu-id="edf2d-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="edf2d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="edf2d-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="edf2d-110">Return value</span></span>

<span data-ttu-id="edf2d-111">Collection d' [**OID**](oids.md) .</span><span class="sxs-lookup"><span data-stu-id="edf2d-111">An [**OIDs**](oids.md) collection.</span></span> <span data-ttu-id="edf2d-112">Chaque objet [**OID**](oid.md) de la collection représente un OID de stratégie de certificat.</span><span class="sxs-lookup"><span data-stu-id="edf2d-112">Each [**OID**](oid.md) object in the collection represents a certificate policy OID.</span></span>

## <a name="remarks"></a><span data-ttu-id="edf2d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="edf2d-113">Remarks</span></span>

<span data-ttu-id="edf2d-114">Ajoutez des OID de stratégie de certificat au regroupement pour spécifier les stratégies de certificat à utiliser pour générer la chaîne d’approbation de certificat.</span><span class="sxs-lookup"><span data-stu-id="edf2d-114">Add certificate policy OIDs to the collection to specify the certificate policies that should be used to build the certificate trust chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="edf2d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="edf2d-115">Requirements</span></span>



| <span data-ttu-id="edf2d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="edf2d-116">Requirement</span></span> | <span data-ttu-id="edf2d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="edf2d-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="edf2d-118">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="edf2d-118">End of client support</span></span><br/> | <span data-ttu-id="edf2d-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="edf2d-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="edf2d-120">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="edf2d-120">End of server support</span></span><br/> | <span data-ttu-id="edf2d-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="edf2d-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="edf2d-122">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="edf2d-122">Redistributable</span></span><br/>       | <span data-ttu-id="edf2d-123">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="edf2d-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="edf2d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="edf2d-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="edf2d-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edf2d-125"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
