---
description: La \_ propriété NewEnum des attributs récupère une interface IEnumVARIANT sur un objet qui peut être utilisé pour énumérer la collection. Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).
ms.assetid: a90ef28b-3926-4542-bcd2-27f0eda4e339
title: Attributes._NewEnum, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9948c55943a8374665fe5e4883013742188665c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533102"
---
# <a name="attributes_newenum-property"></a><span data-ttu-id="2cfd5-104">Attributs. \_ NewEnum, propriété</span><span class="sxs-lookup"><span data-stu-id="2cfd5-104">Attributes.\_NewEnum property</span></span>

<span data-ttu-id="2cfd5-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2cfd5-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="2cfd5-106">Utilisez plutôt la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="2cfd5-106">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="2cfd5-107">La propriété **\_ NewEnum** récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="2cfd5-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="2cfd5-108">Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="2cfd5-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="2cfd5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2cfd5-109">Syntax</span></span>


```VB
Attributes._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="2cfd5-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2cfd5-110">Property value</span></span>

<span data-ttu-id="2cfd5-111">Une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="2cfd5-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cfd5-112">Notes</span><span class="sxs-lookup"><span data-stu-id="2cfd5-112">Remarks</span></span>

<span data-ttu-id="2cfd5-113">Cette propriété est utilisée automatiquement en interne quand vous utilisez la `For Each In` construction dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="2cfd5-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="2cfd5-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2cfd5-114">Requirements</span></span>



| <span data-ttu-id="2cfd5-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2cfd5-115">Requirement</span></span> | <span data-ttu-id="2cfd5-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2cfd5-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cfd5-117">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="2cfd5-117">End of client support</span></span><br/> | <span data-ttu-id="2cfd5-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2cfd5-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2cfd5-119">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="2cfd5-119">End of server support</span></span><br/> | <span data-ttu-id="2cfd5-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2cfd5-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2cfd5-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="2cfd5-121">Redistributable</span></span><br/>       | <span data-ttu-id="2cfd5-122">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="2cfd5-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2cfd5-123">DLL</span><span class="sxs-lookup"><span data-stu-id="2cfd5-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="2cfd5-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cfd5-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cfd5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2cfd5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cfd5-126">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="2cfd5-126">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
