---
description: Récupère un objet OID de la collection. Il s’agit de la propriété par défaut.
ms.assetid: af0de567-e520-411d-850d-fbdbcb2ace69
title: OID. Item, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dfdf65f013c5e5e1a031c03c19af9d08b8fc72c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533733"
---
# <a name="oidsitem-property"></a><span data-ttu-id="8a3f6-104">OID. Item, propriété</span><span class="sxs-lookup"><span data-stu-id="8a3f6-104">OIDs.Item property</span></span>

<span data-ttu-id="8a3f6-105">\[La propriété **Item** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="8a3f6-105">\[The **Item** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8a3f6-106">Utilisez plutôt la [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="8a3f6-106">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="8a3f6-107">La propriété **Item** récupère un objet [**OID**](oid.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="8a3f6-107">The **Item** property retrieves an [**OID**](oid.md) object from the collection.</span></span> <span data-ttu-id="8a3f6-108">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="8a3f6-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a3f6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a3f6-109">Syntax</span></span>


```VB
OIDs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="8a3f6-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="8a3f6-110">Property value</span></span>

<span data-ttu-id="8a3f6-111">Objet [**OID**](oid.md) à l’index spécifié, ou objet **OID** avec la valeur en pointillés spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8a3f6-111">The [**OID**](oid.md) object at the specified index, or the **OID** object with the specified dotted value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a3f6-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a3f6-112">Requirements</span></span>



| <span data-ttu-id="8a3f6-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a3f6-113">Requirement</span></span> | <span data-ttu-id="8a3f6-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a3f6-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a3f6-115">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="8a3f6-115">Redistributable</span></span><br/> | <span data-ttu-id="8a3f6-116">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="8a3f6-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8a3f6-117">DLL</span><span class="sxs-lookup"><span data-stu-id="8a3f6-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="8a3f6-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a3f6-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a3f6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a3f6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a3f6-120">**OID**</span><span class="sxs-lookup"><span data-stu-id="8a3f6-120">**OIDs**</span></span>](oids.md)
</dt> </dl>

 

 
