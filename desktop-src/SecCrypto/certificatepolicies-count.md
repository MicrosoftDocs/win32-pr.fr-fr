---
description: Récupère le nombre d’objets PolicyInformation dans la collection.
ms.assetid: d4fb6bd8-4e92-4de8-9430-dd3b6262a806
title: CertificatePolicies. Count (propriété)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0ee51e37b3fd4ac66c4e615eaf068edc98a64807
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533469"
---
# <a name="certificatepoliciescount-property"></a><span data-ttu-id="d317c-103">CertificatePolicies. Count (propriété)</span><span class="sxs-lookup"><span data-stu-id="d317c-103">CertificatePolicies.Count property</span></span>

<span data-ttu-id="d317c-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d317c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d317c-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour récupérer les stratégies de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="d317c-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="d317c-106">La propriété **Count** récupère le nombre d’objets [**PolicyInformation**](policyinformation.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="d317c-106">The **Count** property retrieves the number of [**PolicyInformation**](policyinformation.md) objects in the collection.</span></span>

<span data-ttu-id="d317c-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d317c-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d317c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d317c-108">Syntax</span></span>


```VB
CertificatePolicies.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="d317c-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d317c-109">Property value</span></span>

<span data-ttu-id="d317c-110">Nombre d’objets [**PolicyInformation**](policyinformation.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="d317c-110">The number of [**PolicyInformation**](policyinformation.md) objects in the collection.</span></span> <span data-ttu-id="d317c-111">Chaque objet **PolicyInformation** représente une stratégie de certificat unique dans la collection.</span><span class="sxs-lookup"><span data-stu-id="d317c-111">Each **PolicyInformation** object represents a single certificate policy in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="d317c-112">Notes</span><span class="sxs-lookup"><span data-stu-id="d317c-112">Remarks</span></span>

<span data-ttu-id="d317c-113">La propriété **Count** peut être utilisée pour spécifier le dernier objet [**PolicyInformation**](policyinformation.md) dans la collection lors de l’extraction d’un objet **PolicyInformation** spécifique à l’aide de la propriété [**certificatePolicies. Item**](certificatepolicies-item.md) .</span><span class="sxs-lookup"><span data-stu-id="d317c-113">The **Count** property can be used to specify the last [**PolicyInformation**](policyinformation.md) object in the collection when retrieving a specific **PolicyInformation** object using the [**CertificatePolicies.Item**](certificatepolicies-item.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d317c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d317c-114">Requirements</span></span>



| <span data-ttu-id="d317c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d317c-115">Requirement</span></span> | <span data-ttu-id="d317c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d317c-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d317c-117">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d317c-117">End of client support</span></span><br/> | <span data-ttu-id="d317c-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d317c-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d317c-119">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="d317c-119">End of server support</span></span><br/> | <span data-ttu-id="d317c-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d317c-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d317c-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="d317c-121">Redistributable</span></span><br/>       | <span data-ttu-id="d317c-122">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="d317c-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d317c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d317c-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d317c-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d317c-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
