---
description: Récupère le nom du magasin de certificats que cet objet représente.
ms.assetid: db61b464-0e8e-4b19-be12-04e00d6bba53
title: Propriété Store.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85679bb594bdb59c41773b7f956deea95021381f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541784"
---
# <a name="storename-property"></a><span data-ttu-id="87d42-103">Propriété Store.Name</span><span class="sxs-lookup"><span data-stu-id="87d42-103">Store.Name property</span></span>

<span data-ttu-id="87d42-104">\[La propriété [**nom**](store-location.md) peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="87d42-104">\[The [**Name**](store-location.md) property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="87d42-105">Utilisez plutôt la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="87d42-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="87d42-106">La propriété [**Name**](store-location.md) récupère le nom du magasin de certificats que cet objet représente.</span><span class="sxs-lookup"><span data-stu-id="87d42-106">The [**Name**](store-location.md) property retrieves the name of the certificate store that this object represents.</span></span>

## <a name="syntax"></a><span data-ttu-id="87d42-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87d42-107">Syntax</span></span>


```VB
Store.Name As String
```



## <a name="property-value"></a><span data-ttu-id="87d42-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="87d42-108">Property value</span></span>

<span data-ttu-id="87d42-109">Valeur de **chaîne** qui représente le nom du magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="87d42-109">The **String** value that represents the name of the certificate store.</span></span>

## <a name="remarks"></a><span data-ttu-id="87d42-110">Notes</span><span class="sxs-lookup"><span data-stu-id="87d42-110">Remarks</span></span>

<span data-ttu-id="87d42-111">Voici des exemples de noms de magasins de certificats : My et root.</span><span class="sxs-lookup"><span data-stu-id="87d42-111">Examples of certificate store names include My and Root.</span></span>

<span data-ttu-id="87d42-112">La valeur de la propriété [**Name**](store-location.md) est la même que la valeur fournie pour le paramètre *StoreName* de la méthode [**Open**](store-open.md) lors de l’ouverture du magasin.</span><span class="sxs-lookup"><span data-stu-id="87d42-112">The value of the [**Name**](store-location.md) property is the same as the value supplied for the *StoreName* parameter of the [**Open**](store-open.md) method when the store was opened.</span></span>

## <a name="requirements"></a><span data-ttu-id="87d42-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87d42-113">Requirements</span></span>



| <span data-ttu-id="87d42-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87d42-114">Requirement</span></span> | <span data-ttu-id="87d42-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="87d42-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87d42-116">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="87d42-116">Redistributable</span></span><br/> | <span data-ttu-id="87d42-117">CAPICOM 2,1 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="87d42-117">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="87d42-118">DLL</span><span class="sxs-lookup"><span data-stu-id="87d42-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="87d42-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87d42-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87d42-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87d42-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87d42-121">**Magasin**</span><span class="sxs-lookup"><span data-stu-id="87d42-121">**Store**</span></span>](store.md)
</dt> </dl>

 

 
