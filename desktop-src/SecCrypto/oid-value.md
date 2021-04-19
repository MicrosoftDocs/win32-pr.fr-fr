---
description: Définit ou récupère la valeur du numéro d’OID en pointillés de l’identificateur.
ms.assetid: bb960e65-776e-4ae8-a557-62254dc10558
title: OID. Propriété Value
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d8c3c59cfd3eadfb8aec56c6814a2af6ce9ff900
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531141"
---
# <a name="oidvalue-property"></a><span data-ttu-id="70511-103">OID. Propriété Value</span><span class="sxs-lookup"><span data-stu-id="70511-103">OID.Value property</span></span>

<span data-ttu-id="70511-104">\[La propriété **valeur** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="70511-104">\[The **Value** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="70511-105">Utilisez plutôt la [**classe OID**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="70511-105">Instead, use the [**Oid Class**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="70511-106">La propriété **value** définit ou récupère la valeur du numéro d’OID en pointillés de l’identificateur.</span><span class="sxs-lookup"><span data-stu-id="70511-106">The **Value** property sets or retrieves the value of the OID dotted number of the identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="70511-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70511-107">Syntax</span></span>


```VB
OID.Value As String
```



## <a name="property-value"></a><span data-ttu-id="70511-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="70511-108">Property value</span></span>

<span data-ttu-id="70511-109">Valeur du numéro d’OID en pointillés de l’identificateur.</span><span class="sxs-lookup"><span data-stu-id="70511-109">The value of the OID dotted number of the identifier.</span></span> <span data-ttu-id="70511-110">Pour connaître les valeurs possibles, consultez Wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="70511-110">For possible values, see Wincrypt.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="70511-111">Notes</span><span class="sxs-lookup"><span data-stu-id="70511-111">Remarks</span></span>

<span data-ttu-id="70511-112">Si la propriété **valeur** est définie, la propriété [**FriendlyName**](oid-friendlyname.md) est définie sur le nom complet correspondant.</span><span class="sxs-lookup"><span data-stu-id="70511-112">If the **Value** property is set, the [**FriendlyName**](oid-friendlyname.md) property is set to the corresponding display name.</span></span> <span data-ttu-id="70511-113">Si la propriété **FriendlyName** est définie, la propriété **value** est définie sur la valeur en pointillé correspondante.</span><span class="sxs-lookup"><span data-stu-id="70511-113">If the **FriendlyName** property is set, the **Value** property is set to the corresponding dotted value.</span></span>

## <a name="requirements"></a><span data-ttu-id="70511-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70511-114">Requirements</span></span>



| <span data-ttu-id="70511-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70511-115">Requirement</span></span> | <span data-ttu-id="70511-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="70511-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70511-117">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="70511-117">Redistributable</span></span><br/> | <span data-ttu-id="70511-118">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="70511-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="70511-119">DLL</span><span class="sxs-lookup"><span data-stu-id="70511-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="70511-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70511-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70511-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70511-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70511-122">**OID**</span><span class="sxs-lookup"><span data-stu-id="70511-122">**OID**</span></span>](oid.md)
</dt> </dl>

 

 
