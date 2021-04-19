---
description: Récupère l’ID d’objet du qualificateur.
ms.assetid: 58ec2af7-f085-43bc-8ea8-926cb840abe9
title: Qualifier. OID, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a86aaf7b60b98811e2d1fbef79c520448f1d47f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532663"
---
# <a name="qualifieroid-property"></a><span data-ttu-id="51ae5-103">Qualifier. OID, propriété</span><span class="sxs-lookup"><span data-stu-id="51ae5-103">Qualifier.OID property</span></span>

<span data-ttu-id="51ae5-104">\[La propriété **OID** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="51ae5-104">\[The **OID** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="51ae5-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour traiter les qualificateurs qui font partie des informations de stratégie dans l’extension des stratégies de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="51ae5-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="51ae5-106">La propriété **OID** récupère l’ID d’objet du qualificateur.</span><span class="sxs-lookup"><span data-stu-id="51ae5-106">The **OID** property retrieves the object ID of the qualifier.</span></span> <span data-ttu-id="51ae5-107">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="51ae5-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="51ae5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51ae5-108">Syntax</span></span>


```VB
Qualifier.OID As OID
```



## <a name="property-value"></a><span data-ttu-id="51ae5-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="51ae5-109">Property value</span></span>

<span data-ttu-id="51ae5-110">Objet [**OID**](oid.md) qui identifie le qualificateur.</span><span class="sxs-lookup"><span data-stu-id="51ae5-110">An [**OID**](oid.md) object that identifies the qualifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="51ae5-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51ae5-111">Requirements</span></span>



| <span data-ttu-id="51ae5-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51ae5-112">Requirement</span></span> | <span data-ttu-id="51ae5-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="51ae5-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="51ae5-114">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="51ae5-114">Redistributable</span></span><br/> | <span data-ttu-id="51ae5-115">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="51ae5-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="51ae5-116">DLL</span><span class="sxs-lookup"><span data-stu-id="51ae5-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="51ae5-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51ae5-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51ae5-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51ae5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51ae5-119">**Qualificateur**</span><span class="sxs-lookup"><span data-stu-id="51ae5-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
