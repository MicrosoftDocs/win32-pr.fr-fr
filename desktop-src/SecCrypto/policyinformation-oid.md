---
description: Récupère l’OID de la stratégie. Il s’agit de la propriété par défaut.
ms.assetid: c78bbbcb-befd-491c-afbd-80c3ba124d29
title: PolicyInformation. OID, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9acab40130ef6c55bf014058b3e5a6d935ed8a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527998"
---
# <a name="policyinformationoid-property"></a><span data-ttu-id="e32da-104">PolicyInformation. OID, propriété</span><span class="sxs-lookup"><span data-stu-id="e32da-104">PolicyInformation.OID property</span></span>

<span data-ttu-id="e32da-105">\[La propriété **OID** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="e32da-105">\[The **OID** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e32da-106">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour traiter les informations de stratégie dans l’extension des stratégies de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="e32da-106">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process policy information in the Certificate policies extension.\]</span></span>

<span data-ttu-id="e32da-107">La propriété **OID** récupère l’OID de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="e32da-107">The **OID** property retrieves the policy's OID.</span></span> <span data-ttu-id="e32da-108">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="e32da-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="e32da-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e32da-109">Syntax</span></span>


```VB
PolicyInformation.OID As OID
```



## <a name="property-value"></a><span data-ttu-id="e32da-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e32da-110">Property value</span></span>

<span data-ttu-id="e32da-111">Identificateur d’objet de la stratégie en tant qu’objet [**OID**](oid.md) .</span><span class="sxs-lookup"><span data-stu-id="e32da-111">The policy's object identifier as an [**OID**](oid.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="e32da-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e32da-112">Requirements</span></span>



| <span data-ttu-id="e32da-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e32da-113">Requirement</span></span> | <span data-ttu-id="e32da-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="e32da-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e32da-115">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="e32da-115">Redistributable</span></span><br/> | <span data-ttu-id="e32da-116">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="e32da-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e32da-117">DLL</span><span class="sxs-lookup"><span data-stu-id="e32da-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="e32da-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e32da-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e32da-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e32da-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e32da-120">**PolicyInformation**</span><span class="sxs-lookup"><span data-stu-id="e32da-120">**PolicyInformation**</span></span>](policyinformation.md)
</dt> </dl>

 

 
