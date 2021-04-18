---
description: La \_ propriété NewEnum des qualificateurs récupère une interface IEnumVARIANT sur un objet qui peut être utilisé pour énumérer la collection. Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).
ms.assetid: e51f8ca1-ef1f-475b-8368-e8296fae0f04
title: Qualifiers._NewEnum, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 01a4d62604dabacd2d78d5d2f6cbee0db7189196
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540246"
---
# <a name="qualifiers_newenum-property"></a><span data-ttu-id="1134d-104">Qualificateurs. \_ NewEnum, propriété</span><span class="sxs-lookup"><span data-stu-id="1134d-104">Qualifiers.\_NewEnum property</span></span>

<span data-ttu-id="1134d-105">\[La propriété **\_ NewEnum** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="1134d-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1134d-106">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour traiter les qualificateurs qui font partie des informations de stratégie dans l’extension des stratégies de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="1134d-106">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="1134d-107">La propriété **\_ NewEnum** récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="1134d-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="1134d-108">Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="1134d-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="1134d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1134d-109">Syntax</span></span>


```VB
Qualifiers._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="1134d-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1134d-110">Property value</span></span>

<span data-ttu-id="1134d-111">Une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="1134d-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="1134d-112">Notes</span><span class="sxs-lookup"><span data-stu-id="1134d-112">Remarks</span></span>

<span data-ttu-id="1134d-113">Cette propriété est utilisée automatiquement en interne quand vous utilisez la `For Each In` construction dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="1134d-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="1134d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1134d-114">Requirements</span></span>



| <span data-ttu-id="1134d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1134d-115">Requirement</span></span> | <span data-ttu-id="1134d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1134d-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1134d-117">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="1134d-117">Redistributable</span></span><br/> | <span data-ttu-id="1134d-118">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="1134d-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1134d-119">DLL</span><span class="sxs-lookup"><span data-stu-id="1134d-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="1134d-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1134d-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1134d-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1134d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1134d-122">**Qualificateurs**</span><span class="sxs-lookup"><span data-stu-id="1134d-122">**Qualifiers**</span></span>](qualifiers.md)
</dt> </dl>

 

 
