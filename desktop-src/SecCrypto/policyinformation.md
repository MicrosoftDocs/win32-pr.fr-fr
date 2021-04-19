---
description: Fournit l’accès aux informations de stratégie d’une extension.
ms.assetid: 03d627b3-2d44-4637-97a4-85cdcaf3e4d3
title: Objet PolicyInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9d0cc89d6f993b72763083e69bb88e848134e8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520799"
---
# <a name="policyinformation-object"></a><span data-ttu-id="bb4fc-103">Objet PolicyInformation</span><span class="sxs-lookup"><span data-stu-id="bb4fc-103">PolicyInformation object</span></span>

<span data-ttu-id="bb4fc-104">\[L’objet **PolicyInformation** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-104">\[The **PolicyInformation** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bb4fc-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour traiter les informations de stratégie dans l’extension des stratégies de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="bb4fc-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process policy information in the Certificate policies extension.\]</span></span>

<span data-ttu-id="bb4fc-106">L’objet **PolicyInformation** fournit l’accès aux informations de stratégie d’une extension.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-106">The **PolicyInformation** object provides access to the policy information of an extension.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="bb4fc-107">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="bb4fc-107">When to use</span></span>

<span data-ttu-id="bb4fc-108">L’objet **PolicyInformation** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="bb4fc-108">The **PolicyInformation** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="bb4fc-109">Récupérez l’OID de stratégie.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-109">Retrieve the policy OID.</span></span>
-   <span data-ttu-id="bb4fc-110">Récupère une collection des qualificateurs de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-110">Retrieve a collection of the policy's qualifiers.</span></span>

## <a name="members"></a><span data-ttu-id="bb4fc-111">Membres</span><span class="sxs-lookup"><span data-stu-id="bb4fc-111">Members</span></span>

<span data-ttu-id="bb4fc-112">L’objet **PolicyInformation** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bb4fc-112">The **PolicyInformation** object has these types of members:</span></span>

-   [<span data-ttu-id="bb4fc-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bb4fc-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bb4fc-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bb4fc-114">Properties</span></span>

<span data-ttu-id="bb4fc-115">L’objet **PolicyInformation** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-115">The **PolicyInformation** object has these properties.</span></span>



| <span data-ttu-id="bb4fc-116">Propriété</span><span class="sxs-lookup"><span data-stu-id="bb4fc-116">Property</span></span>                                                      | <span data-ttu-id="bb4fc-117">Description</span><span class="sxs-lookup"><span data-stu-id="bb4fc-117">Description</span></span>                                                                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb4fc-118">**OID**</span><span class="sxs-lookup"><span data-stu-id="bb4fc-118">**OID**</span></span>](policyinformation-oid.md)<br/>               | <span data-ttu-id="bb4fc-119">Récupère l’OID de la stratégie, sous la forme d’un objet [**OID**](oid.md) .</span><span class="sxs-lookup"><span data-stu-id="bb4fc-119">Retrieves the policy's OID, as an [**OID**](oid.md) object.</span></span> <span data-ttu-id="bb4fc-120">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="bb4fc-120">This is the default property.</span></span><br/>       |
| [<span data-ttu-id="bb4fc-121">**Qualificateurs**</span><span class="sxs-lookup"><span data-stu-id="bb4fc-121">**Qualifiers**</span></span>](policyinformation-qualifiers.md)<br/> | <span data-ttu-id="bb4fc-122">Récupère une collection des qualificateurs de la stratégie, sous la forme d’un objet [**qualificateurs**](qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="bb4fc-122">Retrieves a collection of the policy's qualifiers, as a [**Qualifiers**](qualifiers.md) object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bb4fc-123">Notes</span><span class="sxs-lookup"><span data-stu-id="bb4fc-123">Remarks</span></span>

<span data-ttu-id="bb4fc-124">Impossible de créer l’objet **PolicyInformation** .</span><span class="sxs-lookup"><span data-stu-id="bb4fc-124">The **PolicyInformation** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb4fc-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb4fc-125">Requirements</span></span>



| <span data-ttu-id="bb4fc-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb4fc-126">Requirement</span></span> | <span data-ttu-id="bb4fc-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb4fc-127">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb4fc-128">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="bb4fc-128">Redistributable</span></span><br/> | <span data-ttu-id="bb4fc-129">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="bb4fc-129">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bb4fc-130">DLL</span><span class="sxs-lookup"><span data-stu-id="bb4fc-130">DLL</span></span><br/>             | <dl> <span data-ttu-id="bb4fc-131"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb4fc-131"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
