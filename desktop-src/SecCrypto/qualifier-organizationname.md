---
description: Récupère le nom de l’organisation associée au qualificateur.
ms.assetid: 4ceb2c0f-903d-4fcd-8446-abf3175fe8e0
title: Qualifier. OrganizationName, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OrganizationName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b1e1ebb2b948d5a933b59e86c8753b6b68a3a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533097"
---
# <a name="qualifierorganizationname-property"></a><span data-ttu-id="18537-103">Qualifier. OrganizationName, propriété</span><span class="sxs-lookup"><span data-stu-id="18537-103">Qualifier.OrganizationName property</span></span>

<span data-ttu-id="18537-104">\[La propriété **OrganizationName** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="18537-104">\[The **OrganizationName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="18537-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour traiter les qualificateurs qui font partie des informations de stratégie dans l’extension des stratégies de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="18537-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="18537-106">La propriété **OrganizationName** récupère le nom de l’organisation associée au qualificateur.</span><span class="sxs-lookup"><span data-stu-id="18537-106">The **OrganizationName** property retrieves the name of the organization associated with the qualifier.</span></span> <span data-ttu-id="18537-107">Cette propriété peut être vide.</span><span class="sxs-lookup"><span data-stu-id="18537-107">This property may be empty.</span></span>

## <a name="syntax"></a><span data-ttu-id="18537-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18537-108">Syntax</span></span>


```VB
Qualifier.OrganizationName As String
```



## <a name="property-value"></a><span data-ttu-id="18537-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="18537-109">Property value</span></span>

<span data-ttu-id="18537-110">Nom de l’organisation associée au qualificateur.</span><span class="sxs-lookup"><span data-stu-id="18537-110">The name of the organization associated with the qualifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="18537-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18537-111">Requirements</span></span>



| <span data-ttu-id="18537-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18537-112">Requirement</span></span> | <span data-ttu-id="18537-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="18537-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18537-114">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="18537-114">Redistributable</span></span><br/> | <span data-ttu-id="18537-115">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="18537-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="18537-116">DLL</span><span class="sxs-lookup"><span data-stu-id="18537-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="18537-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18537-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18537-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18537-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18537-119">**Qualificateur**</span><span class="sxs-lookup"><span data-stu-id="18537-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
