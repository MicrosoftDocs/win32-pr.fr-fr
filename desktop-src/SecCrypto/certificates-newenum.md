---
description: La \_ propriété NewEnum des certificats récupère une interface IEnumVARIANT sur un objet qui peut être utilisé pour énumérer la collection. Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).
ms.assetid: bbe6c82c-1949-4d81-bb87-3f05613efa6d
title: Certificates._NewEnum, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 71760f23bbb19d32c3caf8011eb87b8d03941eac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543938"
---
# <a name="certificates_newenum-property"></a><span data-ttu-id="7523e-104">Certificats. \_ NewEnum, propriété</span><span class="sxs-lookup"><span data-stu-id="7523e-104">Certificates.\_NewEnum property</span></span>

<span data-ttu-id="7523e-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7523e-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7523e-106">Utilisez plutôt la [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="7523e-106">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="7523e-107">La propriété **\_ NewEnum** récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="7523e-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="7523e-108">Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="7523e-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="7523e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7523e-109">Syntax</span></span>


```VB
Certificates._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="7523e-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7523e-110">Property value</span></span>

<span data-ttu-id="7523e-111">Une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="7523e-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="7523e-112">Notes</span><span class="sxs-lookup"><span data-stu-id="7523e-112">Remarks</span></span>

<span data-ttu-id="7523e-113">Cette propriété est utilisée automatiquement en interne quand vous utilisez la `For Each In` construction dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="7523e-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="7523e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7523e-114">Requirements</span></span>



| <span data-ttu-id="7523e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7523e-115">Requirement</span></span> | <span data-ttu-id="7523e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7523e-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7523e-117">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7523e-117">End of client support</span></span><br/> | <span data-ttu-id="7523e-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7523e-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7523e-119">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="7523e-119">End of server support</span></span><br/> | <span data-ttu-id="7523e-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7523e-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7523e-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="7523e-121">Redistributable</span></span><br/>       | <span data-ttu-id="7523e-122">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="7523e-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7523e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7523e-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7523e-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7523e-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7523e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7523e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7523e-126">**Certificates**</span><span class="sxs-lookup"><span data-stu-id="7523e-126">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
