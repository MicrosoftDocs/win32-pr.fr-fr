---
description: Récupère l’URI qui pointe vers une déclaration CPS (certification Practice Statement) publiée par l’autorité de certification.
ms.assetid: fd030c1c-137c-4036-bf13-ae989a9703cc
title: Qualifier. CPSPointer, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.CPSPointer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: db16e8faa25fc929e884358fcd885943adc17e32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521680"
---
# <a name="qualifiercpspointer-property"></a><span data-ttu-id="da85d-103">Qualifier. CPSPointer, propriété</span><span class="sxs-lookup"><span data-stu-id="da85d-103">Qualifier.CPSPointer property</span></span>

<span data-ttu-id="da85d-104">\[La propriété **CPSPointer** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="da85d-104">\[The **CPSPointer** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="da85d-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour traiter les qualificateurs qui font partie des informations de stratégie dans l’extension des stratégies de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="da85d-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="da85d-106">La propriété **CPSPointer** récupère l’URI qui pointe vers une déclaration CPS (certification Practice Statement) publiée par l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="da85d-106">The **CPSPointer** property retrieves the URI that points to a Certification Practice Statement (CPS) published by the certification authority (CA).</span></span>

## <a name="syntax"></a><span data-ttu-id="da85d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da85d-107">Syntax</span></span>


```VB
Qualifier.CPSPointer As String
```



## <a name="property-value"></a><span data-ttu-id="da85d-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="da85d-108">Property value</span></span>

<span data-ttu-id="da85d-109">URI qui pointe vers un CPS publié par l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="da85d-109">The URI that points to a CPS published by the CA.</span></span>

## <a name="requirements"></a><span data-ttu-id="da85d-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da85d-110">Requirements</span></span>



| <span data-ttu-id="da85d-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da85d-111">Requirement</span></span> | <span data-ttu-id="da85d-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="da85d-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da85d-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="da85d-113">Redistributable</span></span><br/> | <span data-ttu-id="da85d-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="da85d-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="da85d-115">DLL</span><span class="sxs-lookup"><span data-stu-id="da85d-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="da85d-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da85d-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da85d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da85d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da85d-118">**Qualificateur**</span><span class="sxs-lookup"><span data-stu-id="da85d-118">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
