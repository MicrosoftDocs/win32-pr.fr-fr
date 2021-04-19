---
description: Supprime un objet de certificat unique de la collection.
ms.assetid: dff82825-1a7d-4c1a-94e2-7f9d1281ecf2
title: 'ICertificates2 :: Remove, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Remove
- ICertificates2.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6a2f9336a420f1d014e178f67cae02cf85f0fd44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533432"
---
# <a name="icertificates2remove-method"></a><span data-ttu-id="f7540-103">ICertificates2 :: Remove, méthode</span><span class="sxs-lookup"><span data-stu-id="f7540-103">ICertificates2::Remove method</span></span>

<span data-ttu-id="f7540-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f7540-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f7540-105">Utilisez plutôt la [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="f7540-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f7540-106">La méthode **Remove** supprime un objet [**certificat**](certificate.md) unique de la collection.</span><span class="sxs-lookup"><span data-stu-id="f7540-106">The **Remove** method removes a single [**Certificate**](certificate.md) object from the collection.</span></span> <span data-ttu-id="f7540-107">Cette méthode a été introduite dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="f7540-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7540-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7540-108">Syntax</span></span>


```VB
Certificates.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="f7540-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7540-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7540-110">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f7540-110">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7540-111">Valeur d’index de l’objet de [**certificat**](certificate.md) à supprimer.</span><span class="sxs-lookup"><span data-stu-id="f7540-111">Index value for the [**Certificate**](certificate.md) object to be removed.</span></span> <span data-ttu-id="f7540-112">Ce paramètre peut être l’un des types suivants.</span><span class="sxs-lookup"><span data-stu-id="f7540-112">This parameter can be one of the following possible types.</span></span>



| <span data-ttu-id="f7540-113">Type</span><span class="sxs-lookup"><span data-stu-id="f7540-113">Type</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="f7540-114">Signification</span><span class="sxs-lookup"><span data-stu-id="f7540-114">Meaning</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Long"></span><span id="long"></span><span id="LONG"></span><dl> <span data-ttu-id="f7540-115">\* \* \* \* <dt>Long \* \*</dt> \* \*<dt></dt></span><span class="sxs-lookup"><span data-stu-id="f7540-115"><dt>\*\*\*\*Long\*\*\*\*</dt> <dt></dt></span></span> </dl>                                                | <span data-ttu-id="f7540-116">L’objet de [**certificat**](certificate.md) à l’index spécifié dans la collection est supprimé.</span><span class="sxs-lookup"><span data-stu-id="f7540-116">The [**Certificate**](certificate.md) object at the specified index into the collection is removed.</span></span><br/>                                                                                                          |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <span data-ttu-id="f7540-117">\* \* \* \* <dt>Chaîne \*</dt> \* \* \* \*<dt></dt></span><span class="sxs-lookup"><span data-stu-id="f7540-117"><dt>\*\*\*\*String\*\*\*\*</dt> <dt></dt></span></span> </dl>                                        | <span data-ttu-id="f7540-118">Le premier objet de [**certificat**](certificate.md) de la collection qui correspond à l’empreinte [*SHA-1*](../secgloss/s-gly.md) contenue dans la chaîne spécifiée est supprimé.</span><span class="sxs-lookup"><span data-stu-id="f7540-118">The first [**Certificate**](certificate.md) object in the collection that matches the [*SHA-1*](../secgloss/s-gly.md) thumbprint contained in the specified string is removed.</span></span><br/> |
| <span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span><dl> <span data-ttu-id="f7540-119"><dt>**[**Certificat**](certificate.md)**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="f7540-119"><dt>**[**Certificate**](certificate.md)**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="f7540-120">Le premier objet de [**certificat**](certificate.md) de la collection qui correspond à l’objet de **certificat** spécifié est supprimé.</span><span class="sxs-lookup"><span data-stu-id="f7540-120">The first [**Certificate**](certificate.md) object in the collection that matches the specified **Certificate** object is removed.</span></span><br/>                                                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7540-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f7540-121">Return value</span></span>

<span data-ttu-id="f7540-122">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f7540-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7540-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7540-123">Requirements</span></span>



| <span data-ttu-id="f7540-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7540-124">Requirement</span></span> | <span data-ttu-id="f7540-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7540-125">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7540-126">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f7540-126">End of client support</span></span><br/> | <span data-ttu-id="f7540-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7540-127">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f7540-128">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="f7540-128">End of server support</span></span><br/> | <span data-ttu-id="f7540-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7540-129">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f7540-130">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="f7540-130">Redistributable</span></span><br/>       | <span data-ttu-id="f7540-131">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="f7540-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f7540-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f7540-132">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f7540-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7540-133"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
