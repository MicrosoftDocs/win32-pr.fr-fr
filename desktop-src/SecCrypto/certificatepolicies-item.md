---
description: Récupère l’objet PolicyInformation qui représente la stratégie indexée. Il s’agit de la propriété par défaut.
ms.assetid: 0143629a-97cf-43f4-8f96-774f0f5cfeca
title: CertificatePolicies. Item, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4a41cfb88f5f3ad59a8dbf62c85eca2a13c69f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535394"
---
# <a name="certificatepoliciesitem-property"></a><span data-ttu-id="70a61-104">CertificatePolicies. Item, propriété</span><span class="sxs-lookup"><span data-stu-id="70a61-104">CertificatePolicies.Item property</span></span>

<span data-ttu-id="70a61-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="70a61-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="70a61-106">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour récupérer les stratégies de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="70a61-106">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="70a61-107">La propriété **Item** récupère l’objet [**PolicyInformation**](policyinformation.md) qui représente la stratégie indexée.</span><span class="sxs-lookup"><span data-stu-id="70a61-107">The **Item** property retrieves the [**PolicyInformation**](policyinformation.md) object that represents the indexed policy.</span></span> <span data-ttu-id="70a61-108">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="70a61-108">This is the default property.</span></span>

<span data-ttu-id="70a61-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="70a61-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="70a61-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70a61-110">Syntax</span></span>


```VB
CertificatePolicies.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="70a61-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="70a61-111">Property value</span></span>

<span data-ttu-id="70a61-112">Objet [**PolicyInformation**](policyinformation.md) qui représente la stratégie indexée.</span><span class="sxs-lookup"><span data-stu-id="70a61-112">A [**PolicyInformation**](policyinformation.md) object that represents the indexed policy.</span></span>

## <a name="requirements"></a><span data-ttu-id="70a61-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70a61-113">Requirements</span></span>



| <span data-ttu-id="70a61-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70a61-114">Requirement</span></span> | <span data-ttu-id="70a61-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="70a61-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70a61-116">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="70a61-116">End of client support</span></span><br/> | <span data-ttu-id="70a61-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70a61-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="70a61-118">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="70a61-118">End of server support</span></span><br/> | <span data-ttu-id="70a61-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70a61-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="70a61-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="70a61-120">Redistributable</span></span><br/>       | <span data-ttu-id="70a61-121">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="70a61-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="70a61-122">DLL</span><span class="sxs-lookup"><span data-stu-id="70a61-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="70a61-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70a61-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
