---
description: La \_ propriété NewEnum de ExtendedProperties récupère une interface IEnumVARIANT sur un objet qui peut être utilisé pour énumérer la collection. Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).
ms.assetid: 2692f607-3bec-4674-9d8d-3c872d523ace
title: ExtendedProperties._NewEnum, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 62f07fe7a1a193f93fc0d3bf4c04fbfc5d76ecf9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542392"
---
# <a name="extendedproperties_newenum-property"></a><span data-ttu-id="9d193-104">ExtendedProperties. \_ NewEnum, propriété</span><span class="sxs-lookup"><span data-stu-id="9d193-104">ExtendedProperties.\_NewEnum property</span></span>

<span data-ttu-id="9d193-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9d193-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="9d193-106">Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler la fonction API Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) et obtenir les propriétés.</span><span class="sxs-lookup"><span data-stu-id="9d193-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="9d193-107">Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="9d193-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="9d193-108">Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]</span><span class="sxs-lookup"><span data-stu-id="9d193-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="9d193-109">La propriété **\_ NewEnum** récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="9d193-109">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="9d193-110">Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="9d193-110">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="9d193-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d193-111">Syntax</span></span>


```VB
ExtendedProperties._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="9d193-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9d193-112">Property value</span></span>

<span data-ttu-id="9d193-113">Une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="9d193-113">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d193-114">Notes</span><span class="sxs-lookup"><span data-stu-id="9d193-114">Remarks</span></span>

<span data-ttu-id="9d193-115">Cette propriété est utilisée automatiquement en interne quand vous utilisez la `For Each In` construction dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="9d193-115">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d193-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d193-116">Requirements</span></span>



| <span data-ttu-id="9d193-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d193-117">Requirement</span></span> | <span data-ttu-id="9d193-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d193-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d193-119">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="9d193-119">End of client support</span></span><br/> | <span data-ttu-id="9d193-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d193-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9d193-121">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="9d193-121">End of server support</span></span><br/> | <span data-ttu-id="9d193-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d193-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9d193-123">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="9d193-123">Redistributable</span></span><br/>       | <span data-ttu-id="9d193-124">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="9d193-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9d193-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9d193-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9d193-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d193-126"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
