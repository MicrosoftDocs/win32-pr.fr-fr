---
description: La \_ propriété NewEnum des extensions récupère une interface IEnumVARIANT sur un objet qui peut être utilisé pour énumérer la collection. Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).
ms.assetid: 0e461683-bb48-4961-91ef-36af1c3f863e
title: Extensions._NewEnum, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5b605241e8173b8a41779fa00b661a9e2f383ac7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525418"
---
# <a name="extensions_newenum-property"></a><span data-ttu-id="6a137-104">Extensions. \_ NewEnum, propriété</span><span class="sxs-lookup"><span data-stu-id="6a137-104">Extensions.\_NewEnum property</span></span>

<span data-ttu-id="6a137-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6a137-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="6a137-106">Utilisez plutôt la [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="6a137-106">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6a137-107">La propriété **\_ NewEnum** récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="6a137-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="6a137-108">Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="6a137-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a137-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a137-109">Syntax</span></span>


```VB
Extensions._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="6a137-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6a137-110">Property value</span></span>

<span data-ttu-id="6a137-111">Une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="6a137-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a137-112">Notes</span><span class="sxs-lookup"><span data-stu-id="6a137-112">Remarks</span></span>

<span data-ttu-id="6a137-113">Cette propriété est utilisée automatiquement en interne quand vous utilisez la `For Each In` construction dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="6a137-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a137-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a137-114">Requirements</span></span>



| <span data-ttu-id="6a137-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a137-115">Requirement</span></span> | <span data-ttu-id="6a137-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a137-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a137-117">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="6a137-117">End of client support</span></span><br/> | <span data-ttu-id="6a137-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a137-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6a137-119">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="6a137-119">End of server support</span></span><br/> | <span data-ttu-id="6a137-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a137-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6a137-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="6a137-121">Redistributable</span></span><br/>       | <span data-ttu-id="6a137-122">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="6a137-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6a137-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6a137-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6a137-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a137-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a137-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a137-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a137-126">**Extensions**</span><span class="sxs-lookup"><span data-stu-id="6a137-126">**Extensions**</span></span>](extensions.md)
</dt> </dl>

 

 
