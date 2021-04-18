---
description: Définit ou récupère l’heure à laquelle le certificat a été vérifié.
ms.assetid: 1bd17df3-2fa1-4b99-ab00-659b4ad5fcd9
title: CertificateStatus. VerificationTime, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.VerificationTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 178402861c9830efbea78a31081ae7e8b31800b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520372"
---
# <a name="certificatestatusverificationtime-property"></a><span data-ttu-id="a5da6-103">CertificateStatus. VerificationTime, propriété</span><span class="sxs-lookup"><span data-stu-id="a5da6-103">CertificateStatus.VerificationTime property</span></span>

<span data-ttu-id="a5da6-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a5da6-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a5da6-105">Utilisez plutôt la [**structure X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a5da6-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a5da6-106">La propriété **VerificationTime** définit ou récupère l’heure à laquelle le certificat a été vérifié.</span><span class="sxs-lookup"><span data-stu-id="a5da6-106">The **VerificationTime** property sets or retrieves the time that the certificate was verified.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5da6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5da6-107">Syntax</span></span>


```VB
CertificateStatus.VerificationTime As Date
```



## <a name="property-value"></a><span data-ttu-id="a5da6-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a5da6-108">Property value</span></span>

<span data-ttu-id="a5da6-109">Heure à laquelle le certificat a été vérifié.</span><span class="sxs-lookup"><span data-stu-id="a5da6-109">The time that the certificate was verified.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5da6-110">Notes</span><span class="sxs-lookup"><span data-stu-id="a5da6-110">Remarks</span></span>

<span data-ttu-id="a5da6-111">Si cette propriété n’est pas définie, l’heure actuelle est utilisée.</span><span class="sxs-lookup"><span data-stu-id="a5da6-111">If this property is not set, the current time is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5da6-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5da6-112">Requirements</span></span>



| <span data-ttu-id="a5da6-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5da6-113">Requirement</span></span> | <span data-ttu-id="a5da6-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5da6-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5da6-115">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a5da6-115">End of client support</span></span><br/> | <span data-ttu-id="a5da6-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5da6-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a5da6-117">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="a5da6-117">End of server support</span></span><br/> | <span data-ttu-id="a5da6-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5da6-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a5da6-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a5da6-119">Redistributable</span></span><br/>       | <span data-ttu-id="a5da6-120">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="a5da6-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a5da6-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a5da6-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a5da6-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5da6-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
