---
description: La propriété Result récupère une valeur qui indique si le certificat est valide. Il s’agit de la propriété par défaut.
ms.assetid: b1edfbde-9d54-4e9c-ba9b-33e4c354c23f
title: CertificateStatus. Result, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Result
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df13e9a9fb0454d30ce855b3d272fa521e96e0f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529655"
---
# <a name="certificatestatusresult-property"></a><span data-ttu-id="85a47-104">CertificateStatus. Result, propriété</span><span class="sxs-lookup"><span data-stu-id="85a47-104">CertificateStatus.Result property</span></span>

<span data-ttu-id="85a47-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="85a47-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="85a47-106">Utilisez plutôt la [**structure X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="85a47-106">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="85a47-107">La propriété **result** récupère une valeur qui indique si le certificat est valide.</span><span class="sxs-lookup"><span data-stu-id="85a47-107">The **Result** property retrieves a value that indicates whether the certificate is valid.</span></span> <span data-ttu-id="85a47-108">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="85a47-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="85a47-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85a47-109">Syntax</span></span>


```VB
CertificateStatus.Result As Boolean
```



## <a name="property-value"></a><span data-ttu-id="85a47-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="85a47-110">Property value</span></span>

<span data-ttu-id="85a47-111">Si la **valeur est true**, le certificat est valide.</span><span class="sxs-lookup"><span data-stu-id="85a47-111">If **true**, the certificate is valid.</span></span> <span data-ttu-id="85a47-112">La validité du certificat est vérifiée à l’aide de la valeur actuelle de la propriété [**CheckFlag**](certificatestatus-checkflag.md) et des différents paramètres de stratégie.</span><span class="sxs-lookup"><span data-stu-id="85a47-112">The certificate's validity is checked using the current setting of the [**CheckFlag**](certificatestatus-checkflag.md) property and the various policy settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="85a47-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85a47-113">Requirements</span></span>



| <span data-ttu-id="85a47-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85a47-114">Requirement</span></span> | <span data-ttu-id="85a47-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="85a47-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85a47-116">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="85a47-116">End of client support</span></span><br/> | <span data-ttu-id="85a47-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85a47-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="85a47-118">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="85a47-118">End of server support</span></span><br/> | <span data-ttu-id="85a47-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85a47-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="85a47-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="85a47-120">Redistributable</span></span><br/>       | <span data-ttu-id="85a47-121">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="85a47-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="85a47-122">DLL</span><span class="sxs-lookup"><span data-stu-id="85a47-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="85a47-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85a47-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
