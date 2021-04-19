---
description: Récupère un qualificateur en fonction d’un index spécifié.
ms.assetid: 4d54358d-99de-4a1c-b843-41006f47a279
title: Qualifiers. Item, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 798b1f212aabd5b1ab34a1eefb626be4572b9c1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542700"
---
# <a name="qualifiersitem-property"></a><span data-ttu-id="7fbe0-103">Qualifiers. Item, propriété</span><span class="sxs-lookup"><span data-stu-id="7fbe0-103">Qualifiers.Item property</span></span>

<span data-ttu-id="7fbe0-104">\[La propriété **Item** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="7fbe0-104">\[The **Item** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7fbe0-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour traiter les qualificateurs qui font partie des informations de stratégie dans l’extension des stratégies de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="7fbe0-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="7fbe0-106">La propriété **Item** récupère un qualificateur en fonction d’un index spécifié.</span><span class="sxs-lookup"><span data-stu-id="7fbe0-106">The **Item** property retrieves a qualifier based on a specified index.</span></span> <span data-ttu-id="7fbe0-107">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="7fbe0-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fbe0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7fbe0-108">Syntax</span></span>


```VB
Qualifiers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="7fbe0-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7fbe0-109">Property value</span></span>

<span data-ttu-id="7fbe0-110">Objet [**qualificateur**](qualifier.md) qui représente le qualificateur indexé de la collection.</span><span class="sxs-lookup"><span data-stu-id="7fbe0-110">A [**Qualifier**](qualifier.md) object that represents the indexed qualifier of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fbe0-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7fbe0-111">Requirements</span></span>



| <span data-ttu-id="7fbe0-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7fbe0-112">Requirement</span></span> | <span data-ttu-id="7fbe0-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fbe0-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fbe0-114">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="7fbe0-114">Redistributable</span></span><br/> | <span data-ttu-id="7fbe0-115">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="7fbe0-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7fbe0-116">DLL</span><span class="sxs-lookup"><span data-stu-id="7fbe0-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="7fbe0-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fbe0-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fbe0-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fbe0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fbe0-119">**Qualificateurs**</span><span class="sxs-lookup"><span data-stu-id="7fbe0-119">**Qualifiers**</span></span>](qualifiers.md)
</dt> </dl>

 

 
