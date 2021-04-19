---
description: Récupère le nombre d’objets qualificateurs dans la collection.
ms.assetid: 9dafb83a-ff7f-4317-8ed4-2a46dcebf409
title: Qualifiers. Count, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ffb79941a78602bfda8f5287b0f4df7205d4d86
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545674"
---
# <a name="qualifierscount-property"></a><span data-ttu-id="efeef-103">Qualifiers. Count, propriété</span><span class="sxs-lookup"><span data-stu-id="efeef-103">Qualifiers.Count property</span></span>

<span data-ttu-id="efeef-104">\[La propriété **Count** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="efeef-104">\[The **Count** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="efeef-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour traiter les qualificateurs qui font partie des informations de stratégie dans l’extension des stratégies de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="efeef-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="efeef-106">La propriété **Count** récupère le nombre d’objets [**qualificateurs**](qualifier.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="efeef-106">The **Count** property retrieves the number of [**Qualifier**](qualifier.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="efeef-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efeef-107">Syntax</span></span>


```VB
Qualifiers.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="efeef-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="efeef-108">Property value</span></span>

<span data-ttu-id="efeef-109">Nombre d’objets [**qualificateurs**](qualifier.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="efeef-109">Number of [**Qualifier**](qualifier.md) objects in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="efeef-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="efeef-110">Requirements</span></span>



| <span data-ttu-id="efeef-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="efeef-111">Requirement</span></span> | <span data-ttu-id="efeef-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="efeef-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="efeef-113">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="efeef-113">Redistributable</span></span><br/> | <span data-ttu-id="efeef-114">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="efeef-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="efeef-115">DLL</span><span class="sxs-lookup"><span data-stu-id="efeef-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="efeef-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efeef-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efeef-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efeef-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efeef-118">**Qualificateurs**</span><span class="sxs-lookup"><span data-stu-id="efeef-118">**Qualifiers**</span></span>](qualifiers.md)
</dt> </dl>

 

 
