---
description: Ajoute l’objet OID spécifié à la collection.
ms.assetid: 0ae087d6-768a-4538-b834-0f936680de05
title: Méthode OID. Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d2fa007798a0657991ec8e37a7dddc9fb4c95b2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536054"
---
# <a name="oidsadd-method"></a><span data-ttu-id="341fe-103">Méthode OID. Add</span><span class="sxs-lookup"><span data-stu-id="341fe-103">OIDs.Add method</span></span>

<span data-ttu-id="341fe-104">\[La méthode **Add** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="341fe-104">\[The **Add** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="341fe-105">Utilisez plutôt la [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="341fe-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="341fe-106">La méthode **Add** ajoute l’objet [**OID**](oid.md) spécifié à la collection.</span><span class="sxs-lookup"><span data-stu-id="341fe-106">The **Add** method adds the specified [**OID**](oid.md) object to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="341fe-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="341fe-107">Syntax</span></span>


```VB
OIDs.Add( _
  ByVal OID _
)
```



## <a name="parameters"></a><span data-ttu-id="341fe-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="341fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="341fe-109">*OID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="341fe-109">*OID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="341fe-110">Objet [**OID**](oid.md) à ajouter à la collection.</span><span class="sxs-lookup"><span data-stu-id="341fe-110">The [**OID**](oid.md) object to be added to the collection.</span></span> <span data-ttu-id="341fe-111">L’objet **OID** est ajouté dans l’ordre trié en fonction de sa valeur en pointillés.</span><span class="sxs-lookup"><span data-stu-id="341fe-111">The **OID** object is added in sorted order based on its dotted value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="341fe-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="341fe-112">Return value</span></span>

<span data-ttu-id="341fe-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="341fe-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="341fe-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="341fe-114">Requirements</span></span>



| <span data-ttu-id="341fe-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="341fe-115">Requirement</span></span> | <span data-ttu-id="341fe-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="341fe-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="341fe-117">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="341fe-117">Redistributable</span></span><br/> | <span data-ttu-id="341fe-118">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="341fe-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="341fe-119">DLL</span><span class="sxs-lookup"><span data-stu-id="341fe-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="341fe-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="341fe-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
