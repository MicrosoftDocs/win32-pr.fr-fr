---
description: Récupère une collection des qualificateurs de la stratégie.
ms.assetid: aa5e2225-0a39-40bc-868c-d96f5953edaa
title: PolicyInformation. Qualifiers, propriété (IADs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 89f24e21acd24cbcaa021f7c668fc8c208102c0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537333"
---
# <a name="policyinformationqualifiers-property"></a><span data-ttu-id="7d521-103">PolicyInformation. Qualifiers, propriété</span><span class="sxs-lookup"><span data-stu-id="7d521-103">PolicyInformation.Qualifiers property</span></span>

<span data-ttu-id="7d521-104">\[La propriété **qualificateurs** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="7d521-104">\[The **Qualifiers** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7d521-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour traiter les informations de stratégie dans l’extension des stratégies de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="7d521-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process policy information in the Certificate policies extension.\]</span></span>

<span data-ttu-id="7d521-106">La propriété **Qualifiers** récupère une collection des qualificateurs de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="7d521-106">The **Qualifiers** property retrieves a collection of the policy's qualifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d521-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d521-107">Syntax</span></span>


```VB
PolicyInformation.Qualifiers As Qualifiers
```



## <a name="property-value"></a><span data-ttu-id="7d521-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7d521-108">Property value</span></span>

<span data-ttu-id="7d521-109">Le pointeur CPS (certification Practice Statement) de la stratégie ou les qualificateurs d’avis utilisateur, en tant qu’objet [**qualificateurs**](qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="7d521-109">The policy's Certification Practice Statement (CPS) pointer or user notice qualifiers, as a [**Qualifiers**](qualifiers.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d521-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d521-110">Requirements</span></span>



| <span data-ttu-id="7d521-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d521-111">Requirement</span></span> | <span data-ttu-id="7d521-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d521-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d521-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="7d521-113">Redistributable</span></span><br/> | <span data-ttu-id="7d521-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="7d521-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7d521-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="7d521-115">Header</span></span><br/>          | <dl> <span data-ttu-id="7d521-116"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d521-116"><dt>Iads.h</dt></span></span> </dl>      |
| <span data-ttu-id="7d521-117">DLL</span><span class="sxs-lookup"><span data-stu-id="7d521-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="7d521-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d521-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d521-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d521-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d521-120">**PolicyInformation**</span><span class="sxs-lookup"><span data-stu-id="7d521-120">**PolicyInformation**</span></span>](policyinformation.md)
</dt> </dl>

 

 
