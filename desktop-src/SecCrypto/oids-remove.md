---
description: Supprime l’objet OID spécifié de la collection.
ms.assetid: c5eb6831-b195-4dc1-a6bd-d4245f9b0213
title: Méthode OID. Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 000310e0034d413dea16a45f79647c3e0f7cf52d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525977"
---
# <a name="oidsremove-method"></a><span data-ttu-id="88e6d-103">Méthode OID. Remove</span><span class="sxs-lookup"><span data-stu-id="88e6d-103">OIDs.Remove method</span></span>

<span data-ttu-id="88e6d-104">\[La méthode **Remove** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="88e6d-104">\[The **Remove** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="88e6d-105">Utilisez plutôt la [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="88e6d-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="88e6d-106">La méthode **Remove** supprime l’objet [**OID**](oid.md) spécifié de la collection.</span><span class="sxs-lookup"><span data-stu-id="88e6d-106">The **Remove** method removes the specified [**OID**](oid.md) object from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="88e6d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88e6d-107">Syntax</span></span>


```VB
OIDs.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="88e6d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88e6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88e6d-109">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="88e6d-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88e6d-110">Index de l’objet [**OID**](oid.md) à supprimer.</span><span class="sxs-lookup"><span data-stu-id="88e6d-110">Index of the [**OID**](oid.md) object to be removed.</span></span> <span data-ttu-id="88e6d-111">Il peut s’agir d’un index dans la collection ou de la valeur en pointillés de l’OID.</span><span class="sxs-lookup"><span data-stu-id="88e6d-111">This can be either an index into the collection or the dotted value of the OID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88e6d-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="88e6d-112">Return value</span></span>

<span data-ttu-id="88e6d-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="88e6d-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="88e6d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88e6d-114">Requirements</span></span>



| <span data-ttu-id="88e6d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88e6d-115">Requirement</span></span> | <span data-ttu-id="88e6d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="88e6d-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="88e6d-117">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="88e6d-117">Redistributable</span></span><br/> | <span data-ttu-id="88e6d-118">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="88e6d-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="88e6d-119">DLL</span><span class="sxs-lookup"><span data-stu-id="88e6d-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="88e6d-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88e6d-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
