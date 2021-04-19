---
description: Récupère le contenu de l’avis de l’utilisateur.
ms.assetid: dcf73357-253d-4160-be4e-f826296f5eaa
title: Qualifier. ExplicitText, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.ExplicitText
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7d2ba5e6bbf6bb46e28c5dbb6fa9754c72b66dd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535949"
---
# <a name="qualifierexplicittext-property"></a><span data-ttu-id="08123-103">Qualifier. ExplicitText, propriété</span><span class="sxs-lookup"><span data-stu-id="08123-103">Qualifier.ExplicitText property</span></span>

<span data-ttu-id="08123-104">\[La propriété **ExplicitText** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="08123-104">\[The **ExplicitText** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="08123-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour traiter les qualificateurs qui font partie des informations de stratégie dans l’extension des stratégies de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="08123-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="08123-106">La propriété **ExplicitText** récupère le contenu de l’avis de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="08123-106">The **ExplicitText** property retrieves the content of the user notice.</span></span> <span data-ttu-id="08123-107">Cette propriété peut être vide.</span><span class="sxs-lookup"><span data-stu-id="08123-107">This property may be empty.</span></span>

## <a name="syntax"></a><span data-ttu-id="08123-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08123-108">Syntax</span></span>


```VB
Qualifier.ExplicitText As String
```



## <a name="property-value"></a><span data-ttu-id="08123-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="08123-109">Property value</span></span>

<span data-ttu-id="08123-110">Contenu de l’avis de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="08123-110">The content of the user notice.</span></span>

## <a name="requirements"></a><span data-ttu-id="08123-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08123-111">Requirements</span></span>



| <span data-ttu-id="08123-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08123-112">Requirement</span></span> | <span data-ttu-id="08123-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="08123-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08123-114">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="08123-114">Redistributable</span></span><br/> | <span data-ttu-id="08123-115">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="08123-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="08123-116">DLL</span><span class="sxs-lookup"><span data-stu-id="08123-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="08123-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08123-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08123-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08123-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08123-119">**Qualificateur**</span><span class="sxs-lookup"><span data-stu-id="08123-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
