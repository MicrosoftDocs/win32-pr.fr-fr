---
description: Récupère l’emplacement du magasin de certificats que cet objet représente.
ms.assetid: 756ee7cb-5f9f-4fb2-bf10-79b543895189
title: Store. Location, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Location
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 42afe40dffde5a0375928d355508ec75a4076f17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531120"
---
# <a name="storelocation-property"></a><span data-ttu-id="7ec18-103">Store. Location, propriété</span><span class="sxs-lookup"><span data-stu-id="7ec18-103">Store.Location property</span></span>

<span data-ttu-id="7ec18-104">\[La propriété **emplacement** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="7ec18-104">\[The **Location** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7ec18-105">Utilisez plutôt la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="7ec18-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="7ec18-106">La propriété **location** récupère l’emplacement du magasin de certificats que cet objet représente.</span><span class="sxs-lookup"><span data-stu-id="7ec18-106">The **Location** property retrieves the location of the certificate store that this object represents.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ec18-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ec18-107">Syntax</span></span>


```VB
Store.Location As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a><span data-ttu-id="7ec18-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7ec18-108">Property value</span></span>

<span data-ttu-id="7ec18-109">Valeur d' [**emplacement du \_ magasin \_ CAPICOM**](capicom-store-location.md) qui représente l’emplacement du magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="7ec18-109">The [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) value that represents the location of the certificate store.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ec18-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7ec18-110">Remarks</span></span>

<span data-ttu-id="7ec18-111">La valeur de la propriété **location** est identique à la valeur fournie pour le paramètre *StoreLocation* de la méthode [**Open**](store-open.md) lors de l’ouverture du magasin.</span><span class="sxs-lookup"><span data-stu-id="7ec18-111">The value of the **Location** property is the same as the value supplied for the *StoreLocation* parameter of the [**Open**](store-open.md) method when the store was opened.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ec18-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ec18-112">Requirements</span></span>



| <span data-ttu-id="7ec18-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ec18-113">Requirement</span></span> | <span data-ttu-id="7ec18-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ec18-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ec18-115">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="7ec18-115">Redistributable</span></span><br/> | <span data-ttu-id="7ec18-116">CAPICOM 2,1 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="7ec18-116">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7ec18-117">DLL</span><span class="sxs-lookup"><span data-stu-id="7ec18-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="7ec18-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ec18-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ec18-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ec18-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ec18-120">**Magasin**</span><span class="sxs-lookup"><span data-stu-id="7ec18-120">**Store**</span></span>](store.md)
</dt> </dl>

 

 
