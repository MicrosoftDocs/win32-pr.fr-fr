---
description: Définit ou récupère une chaîne qui contient une valeur de chaîne d’OID EKU telle que définie dans wincrypt. h.
ms.assetid: 2fdaeddc-5ed6-46a6-a4f7-827a605e890a
title: 'IEKU :: OID, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.OID
- IEKU.get_OID
- IEKU.put_OID
- EKU.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 77a519051d2bd1cb3c948bf0e2271cced7d80a20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526568"
---
# <a name="iekuoid-property"></a><span data-ttu-id="a2db6-103">IEKU :: OID, propriété</span><span class="sxs-lookup"><span data-stu-id="a2db6-103">IEKU::OID property</span></span>

<span data-ttu-id="a2db6-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a2db6-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a2db6-105">Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a2db6-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a2db6-106">La propriété **OID** définit ou récupère une chaîne qui contient une valeur de chaîne d’OID EKU telle que définie dans wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="a2db6-106">The **OID** property sets or retrieves a string that contains an EKU OID string value as defined in Wincrypt.h.</span></span>

<span data-ttu-id="a2db6-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a2db6-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2db6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2db6-108">Syntax</span></span>


```VB
EKU.OID As String
```



## <a name="property-value"></a><span data-ttu-id="a2db6-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a2db6-109">Property value</span></span>

<span data-ttu-id="a2db6-110">Chaîne qui contient la valeur de chaîne OID de l’EKU telle que définie dans wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="a2db6-110">String that contains the EKU OID string value as defined in Wincrypt.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2db6-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a2db6-111">Remarks</span></span>

<span data-ttu-id="a2db6-112">Cette propriété n’utilise pas l’objet [**OID**](oid.md) introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="a2db6-112">This property does not use the [**OID**](oid.md) object introduced in CAPICOM 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2db6-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2db6-113">Requirements</span></span>



| <span data-ttu-id="a2db6-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2db6-114">Requirement</span></span> | <span data-ttu-id="a2db6-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2db6-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2db6-116">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a2db6-116">End of client support</span></span><br/> | <span data-ttu-id="a2db6-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2db6-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a2db6-118">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="a2db6-118">End of server support</span></span><br/> | <span data-ttu-id="a2db6-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2db6-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a2db6-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a2db6-120">Redistributable</span></span><br/>       | <span data-ttu-id="a2db6-121">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="a2db6-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a2db6-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a2db6-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a2db6-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2db6-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
