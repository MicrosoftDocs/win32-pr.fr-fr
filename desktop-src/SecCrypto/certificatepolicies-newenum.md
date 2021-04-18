---
description: La \_ propriété NewEnum de certificatePolicies récupère une interface IEnumVARIANT sur un objet qui peut être utilisé pour énumérer la collection.
ms.assetid: 631a11c8-4442-493e-9406-bc63f79db548
title: CertificatePolicies._NewEnum, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2d5e90d4b906661119936ca1e893e3b6e17c9bf5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526762"
---
# <a name="certificatepolicies_newenum-property"></a><span data-ttu-id="32226-103">CertificatePolicies. \_ NewEnum, propriété</span><span class="sxs-lookup"><span data-stu-id="32226-103">CertificatePolicies.\_NewEnum property</span></span>

<span data-ttu-id="32226-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="32226-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="32226-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour récupérer les stratégies de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="32226-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="32226-106">La propriété **\_ NewEnum** récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="32226-106">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="32226-107">Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="32226-107">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="32226-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32226-108">Syntax</span></span>


```VB
CertificatePolicies._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="32226-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="32226-109">Property value</span></span>

<span data-ttu-id="32226-110">Une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="32226-110">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="32226-111">Notes</span><span class="sxs-lookup"><span data-stu-id="32226-111">Remarks</span></span>

<span data-ttu-id="32226-112">Cette propriété est utilisée automatiquement en interne quand vous utilisez la `For Each In` construction dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="32226-112">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="32226-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32226-113">Requirements</span></span>



| <span data-ttu-id="32226-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32226-114">Requirement</span></span> | <span data-ttu-id="32226-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="32226-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32226-116">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="32226-116">End of client support</span></span><br/> | <span data-ttu-id="32226-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32226-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="32226-118">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="32226-118">End of server support</span></span><br/> | <span data-ttu-id="32226-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32226-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="32226-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="32226-120">Redistributable</span></span><br/>       | <span data-ttu-id="32226-121">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="32226-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="32226-122">DLL</span><span class="sxs-lookup"><span data-stu-id="32226-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="32226-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32226-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
