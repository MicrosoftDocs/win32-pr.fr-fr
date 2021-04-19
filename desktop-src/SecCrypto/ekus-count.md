---
description: Récupère le nombre d’objets EKU dans la collection.
ms.assetid: a38ac480-4f9b-4d69-a7e6-fae4993fe2cf
title: EKU. Count, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41e77f3803fa65db1573c6619ebf1265b7418924
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545588"
---
# <a name="ekuscount-property"></a><span data-ttu-id="d7118-103">EKU. Count, propriété</span><span class="sxs-lookup"><span data-stu-id="d7118-103">EKUs.Count property</span></span>

<span data-ttu-id="d7118-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d7118-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d7118-105">Utilisez plutôt la [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="d7118-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d7118-106">La propriété **Count** récupère le nombre d’objets [**EKU**](eku.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="d7118-106">The **Count** property retrieves the number of [**EKU**](eku.md) objects in the collection.</span></span>

<span data-ttu-id="d7118-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d7118-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7118-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7118-108">Syntax</span></span>


```VB
EKUs.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="d7118-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d7118-109">Property value</span></span>

<span data-ttu-id="d7118-110">Nombre d’objets [**EKU**](eku.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="d7118-110">The number of [**EKU**](eku.md) objects in the collection.</span></span> <span data-ttu-id="d7118-111">Chaque objet **EKU** représente une propriété d’utilisation améliorée de la clé (EKU) d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="d7118-111">Each **EKU** object represents a single extended key usage (EKU) property of a certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7118-112">Notes</span><span class="sxs-lookup"><span data-stu-id="d7118-112">Remarks</span></span>

<span data-ttu-id="d7118-113">La propriété **Count** peut être utilisée pour spécifier le dernier objet [**EKU**](eku.md) d’une collection lors de l’extraction d’un objet **EKU** spécifique à l’aide de la propriété [**EKU. Item**](ekus-item.md) .</span><span class="sxs-lookup"><span data-stu-id="d7118-113">The **Count** property can be used to specify the last [**EKU**](eku.md) object in a collection when retrieving a specific **EKU** object using the [**EKUs.Item**](ekus-item.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7118-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7118-114">Requirements</span></span>



| <span data-ttu-id="d7118-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7118-115">Requirement</span></span> | <span data-ttu-id="d7118-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7118-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7118-117">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d7118-117">End of client support</span></span><br/> | <span data-ttu-id="d7118-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d7118-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d7118-119">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="d7118-119">End of server support</span></span><br/> | <span data-ttu-id="d7118-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7118-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d7118-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="d7118-121">Redistributable</span></span><br/>       | <span data-ttu-id="d7118-122">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="d7118-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d7118-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d7118-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d7118-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7118-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
