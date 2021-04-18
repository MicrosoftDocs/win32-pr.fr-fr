---
description: Récupère la collection qui contient tous les certificats du magasin.
ms.assetid: 06cfc0e9-8a77-4e10-b559-4d42ac93c01b
title: Store. Certificates, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 979cf31c98286ca5bdd2df709176a27a5abb2321
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533046"
---
# <a name="storecertificates-property"></a><span data-ttu-id="99f42-103">Store. Certificates, propriété</span><span class="sxs-lookup"><span data-stu-id="99f42-103">Store.Certificates property</span></span>

<span data-ttu-id="99f42-104">\[La propriété **certificats** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="99f42-104">\[The **Certificates** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="99f42-105">Utilisez plutôt la [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="99f42-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="99f42-106">La propriété **certificats** récupère la collection qui contient tous les certificats du magasin.</span><span class="sxs-lookup"><span data-stu-id="99f42-106">The **Certificates** property retrieves the collection that includes all of the certificates in the store.</span></span> <span data-ttu-id="99f42-107">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="99f42-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="99f42-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99f42-108">Syntax</span></span>


```VB
Store.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="99f42-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="99f42-109">Property value</span></span>

<span data-ttu-id="99f42-110">Collection de certificats dans le magasin.</span><span class="sxs-lookup"><span data-stu-id="99f42-110">The collection of certificates in the store.</span></span>

## <a name="requirements"></a><span data-ttu-id="99f42-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99f42-111">Requirements</span></span>



| <span data-ttu-id="99f42-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99f42-112">Requirement</span></span> | <span data-ttu-id="99f42-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="99f42-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99f42-114">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="99f42-114">Redistributable</span></span><br/> | <span data-ttu-id="99f42-115">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="99f42-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="99f42-116">DLL</span><span class="sxs-lookup"><span data-stu-id="99f42-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="99f42-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99f42-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99f42-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99f42-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99f42-119">**Magasin**</span><span class="sxs-lookup"><span data-stu-id="99f42-119">**Store**</span></span>](store.md)
</dt> </dl>

 

 
