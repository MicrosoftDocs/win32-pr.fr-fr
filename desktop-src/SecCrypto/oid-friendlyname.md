---
description: Définit ou récupère le nom complet de l’identificateur.
ms.assetid: 53f84d0d-c189-4fd2-a383-29fd0d22de08
title: OID. FriendlyName, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.FriendlyName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1976980d1a22f4246f0ace686941cc4bcec87c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540036"
---
# <a name="oidfriendlyname-property"></a><span data-ttu-id="e9332-103">OID. FriendlyName, propriété</span><span class="sxs-lookup"><span data-stu-id="e9332-103">OID.FriendlyName property</span></span>

<span data-ttu-id="e9332-104">\[La propriété **FriendlyName** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="e9332-104">\[The **FriendlyName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e9332-105">Utilisez plutôt la [**classe OID**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="e9332-105">Instead, use the [**Oid Class**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="e9332-106">La propriété **FriendlyName** définit ou récupère le nom complet de l’identificateur.</span><span class="sxs-lookup"><span data-stu-id="e9332-106">The **FriendlyName** property sets or retrieves the display name for the identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9332-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9332-107">Syntax</span></span>


```VB
OID.FriendlyName As String
```



## <a name="property-value"></a><span data-ttu-id="e9332-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e9332-108">Property value</span></span>

<span data-ttu-id="e9332-109">Nom complet de l' [**OID**](oid.md).</span><span class="sxs-lookup"><span data-stu-id="e9332-109">The display name for the [**OID**](oid.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e9332-110">Notes</span><span class="sxs-lookup"><span data-stu-id="e9332-110">Remarks</span></span>

<span data-ttu-id="e9332-111">Si la propriété **FriendlyName** est définie, la propriété [**value**](oid-value.md) est définie sur la valeur en pointillé correspondante.</span><span class="sxs-lookup"><span data-stu-id="e9332-111">If the **FriendlyName** property is set, the [**Value**](oid-value.md) property is set to the corresponding dotted value.</span></span> <span data-ttu-id="e9332-112">Si la propriété **valeur** est définie, la propriété **FriendlyName** est définie sur le nom complet correspondant.</span><span class="sxs-lookup"><span data-stu-id="e9332-112">If the **Value** property is set, the **FriendlyName** property is set to the corresponding display name.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9332-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9332-113">Requirements</span></span>



| <span data-ttu-id="e9332-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9332-114">Requirement</span></span> | <span data-ttu-id="e9332-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9332-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9332-116">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="e9332-116">Redistributable</span></span><br/> | <span data-ttu-id="e9332-117">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="e9332-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e9332-118">DLL</span><span class="sxs-lookup"><span data-stu-id="e9332-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="e9332-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9332-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9332-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9332-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9332-121">**OID**</span><span class="sxs-lookup"><span data-stu-id="e9332-121">**OID**</span></span>](oid.md)
</dt> </dl>

 

 
