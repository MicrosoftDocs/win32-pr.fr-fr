---
description: Définit ou récupère l’emplacement du magasin CAPICOM \_ \_ d’un magasin de certificats.
ms.assetid: 2bb76f51-f092-4dbe-93e9-1fdc185c7c50
title: 'ICertStore :: StoreLocation, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreLocation
- ICertStore.get_StoreLocation
- ICertStore.put_StoreLocation
- CertStore.StoreLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 97bca7ed9dae20c129d202910b40f7c26d54a576
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537524"
---
# <a name="icertstorestorelocation-property"></a><span data-ttu-id="c3f24-103">ICertStore :: StoreLocation, propriété</span><span class="sxs-lookup"><span data-stu-id="c3f24-103">ICertStore::StoreLocation property</span></span>

<span data-ttu-id="c3f24-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="c3f24-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="c3f24-105">La propriété **StoreLocation** définit ou récupère l' [**\_ \_ emplacement du magasin CAPICOM**](capicom-store-location.md) d’un magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="c3f24-105">The **StoreLocation** property sets or retrieves the [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) of a certificate store.</span></span>

<span data-ttu-id="c3f24-106">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c3f24-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3f24-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3f24-107">Syntax</span></span>


```VB
CertStore.StoreLocation As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a><span data-ttu-id="c3f24-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c3f24-108">Property value</span></span>

<span data-ttu-id="c3f24-109">Emplacement du magasin de certificats</span><span class="sxs-lookup"><span data-stu-id="c3f24-109">The location of the certificate store.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c3f24-110">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="c3f24-110">Error codes</span></span>

<span data-ttu-id="c3f24-111">Si les méthodes d’accès aux propriétés **placent \_ StoreLocation** et **obtiennent \_ StoreLocation** , elles retournent la réponse \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c3f24-111">If the property access methods **put\_StoreLocation** and **get\_StoreLocation** succeed, they return S\_OK.</span></span>

<span data-ttu-id="c3f24-112">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="c3f24-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3f24-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3f24-113">Requirements</span></span>



| <span data-ttu-id="c3f24-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3f24-114">Requirement</span></span> | <span data-ttu-id="c3f24-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3f24-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3f24-116">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="c3f24-116">Redistributable</span></span><br/> | <span data-ttu-id="c3f24-117">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="c3f24-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c3f24-118">DLL</span><span class="sxs-lookup"><span data-stu-id="c3f24-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="c3f24-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3f24-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3f24-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3f24-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3f24-121">**ICertStore**</span><span class="sxs-lookup"><span data-stu-id="c3f24-121">**ICertStore**</span></span>](icertstore.md)
</dt> </dl>

 

 




