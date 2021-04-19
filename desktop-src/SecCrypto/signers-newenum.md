---
description: La \_ propriété NewEnum des signataires récupère une interface IEnumVARIANT sur un objet qui peut être utilisé pour énumérer la collection. Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).
ms.assetid: 99d7ddd3-a552-4125-b220-d1b28f20d1ed
title: Signers._NewEnum, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 91007e7ce282cb44267927f54ab26f8f930028f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529966"
---
# <a name="signers_newenum-property"></a><span data-ttu-id="77463-104">Des signataires. \_ NewEnum, propriété</span><span class="sxs-lookup"><span data-stu-id="77463-104">Signers.\_NewEnum property</span></span>

<span data-ttu-id="77463-105">\[La propriété **\_ NewEnum** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="77463-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="77463-106">Utilisez plutôt une collection d’objets CmsSigner.</span><span class="sxs-lookup"><span data-stu-id="77463-106">Instead, use a collection of CmsSigner objects.</span></span> <span data-ttu-id="77463-107">Pour plus d’informations, consultez la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="77463-107">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="77463-108">La propriété **\_ NewEnum** récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="77463-108">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="77463-109">Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="77463-109">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="77463-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77463-110">Syntax</span></span>


```VB
Signers._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="77463-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="77463-111">Property value</span></span>

<span data-ttu-id="77463-112">Une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="77463-112">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="77463-113">Notes</span><span class="sxs-lookup"><span data-stu-id="77463-113">Remarks</span></span>

<span data-ttu-id="77463-114">Cette propriété est utilisée automatiquement en interne quand vous utilisez la `For Each In` construction dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="77463-114">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="77463-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77463-115">Requirements</span></span>



| <span data-ttu-id="77463-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77463-116">Requirement</span></span> | <span data-ttu-id="77463-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="77463-117">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="77463-118">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="77463-118">Redistributable</span></span><br/> | <span data-ttu-id="77463-119">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="77463-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="77463-120">DLL</span><span class="sxs-lookup"><span data-stu-id="77463-120">DLL</span></span><br/>             | <dl> <span data-ttu-id="77463-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77463-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77463-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77463-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77463-123">**Signataires**</span><span class="sxs-lookup"><span data-stu-id="77463-123">**Signers**</span></span>](signers.md)
</dt> </dl>

 

 
