---
description: Définit ou récupère la durée pendant laquelle une URL est déterminée pour être inaccessible.
ms.assetid: f39dafc4-6017-463c-aeee-948b6173862a
title: CertificateStatus. UrlRetrievalTimeout, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.UrlRetrievalTimeout
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fcaaafa1f2e870195b612eb225696f2c23a80ee1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532490"
---
# <a name="certificatestatusurlretrievaltimeout-property"></a><span data-ttu-id="395be-103">CertificateStatus. UrlRetrievalTimeout, propriété</span><span class="sxs-lookup"><span data-stu-id="395be-103">CertificateStatus.UrlRetrievalTimeout property</span></span>

<span data-ttu-id="395be-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="395be-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="395be-105">Utilisez plutôt la [**structure X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="395be-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="395be-106">La propriété **UrlRetrievalTimeout** définit ou récupère la durée pendant laquelle une URL est déterminée comme inaccessible.</span><span class="sxs-lookup"><span data-stu-id="395be-106">The **UrlRetrievalTimeout** property sets or retrieves the length of time before a URL is determined to be unreachable.</span></span>

## <a name="syntax"></a><span data-ttu-id="395be-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="395be-107">Syntax</span></span>


```VB
CertificateStatus.UrlRetrievalTimeout As Long
```



## <a name="property-value"></a><span data-ttu-id="395be-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="395be-108">Property value</span></span>

<span data-ttu-id="395be-109">Nombre de secondes avant qu’une URL soit jugée inaccessible.</span><span class="sxs-lookup"><span data-stu-id="395be-109">The number of seconds before a URL is determined to be unreachable.</span></span>

## <a name="remarks"></a><span data-ttu-id="395be-110">Notes</span><span class="sxs-lookup"><span data-stu-id="395be-110">Remarks</span></span>

<span data-ttu-id="395be-111">Si cette propriété n’est pas définie, le délai d’attente par défaut est de 15 secondes.</span><span class="sxs-lookup"><span data-stu-id="395be-111">If this property is not set, the default time-out is 15 seconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="395be-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="395be-112">Requirements</span></span>



| <span data-ttu-id="395be-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="395be-113">Requirement</span></span> | <span data-ttu-id="395be-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="395be-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="395be-115">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="395be-115">End of client support</span></span><br/> | <span data-ttu-id="395be-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="395be-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="395be-117">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="395be-117">End of server support</span></span><br/> | <span data-ttu-id="395be-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="395be-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="395be-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="395be-119">Redistributable</span></span><br/>       | <span data-ttu-id="395be-120">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="395be-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="395be-121">DLL</span><span class="sxs-lookup"><span data-stu-id="395be-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="395be-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="395be-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
