---
description: La \_ propriété NewEnum des OID récupère une interface IEnumVARIANT sur un objet qui peut être utilisé pour énumérer la collection. Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).
ms.assetid: 7c09fd11-064b-451e-bd6b-e6c13ab228a0
title: OIDs._NewEnum, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d20856c17dda18a10b85c01453cbe043144742d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528015"
---
# <a name="oids_newenum-property"></a><span data-ttu-id="f4312-104">OID. \_ NewEnum, propriété</span><span class="sxs-lookup"><span data-stu-id="f4312-104">OIDs.\_NewEnum property</span></span>

<span data-ttu-id="f4312-105">\[La propriété **\_ NewEnum** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="f4312-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f4312-106">Utilisez plutôt la [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="f4312-106">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="f4312-107">La propriété **\_ NewEnum** récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="f4312-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="f4312-108">Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="f4312-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="f4312-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4312-109">Syntax</span></span>


```VB
OIDs._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="f4312-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f4312-110">Property value</span></span>

<span data-ttu-id="f4312-111">Une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="f4312-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4312-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f4312-112">Remarks</span></span>

<span data-ttu-id="f4312-113">Cette propriété est utilisée automatiquement en interne quand vous utilisez la `For Each In` construction dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="f4312-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4312-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4312-114">Requirements</span></span>



| <span data-ttu-id="f4312-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4312-115">Requirement</span></span> | <span data-ttu-id="f4312-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4312-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4312-117">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="f4312-117">Redistributable</span></span><br/> | <span data-ttu-id="f4312-118">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="f4312-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f4312-119">DLL</span><span class="sxs-lookup"><span data-stu-id="f4312-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="f4312-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4312-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4312-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4312-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4312-122">**OID**</span><span class="sxs-lookup"><span data-stu-id="f4312-122">**OIDs**</span></span>](oids.md)
</dt> </dl>

 

 
