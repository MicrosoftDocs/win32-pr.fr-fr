---
description: Définit ou récupère la collection de certificats qui peuvent être utilisés pour créer la chaîne de certificats.
ms.assetid: cdf378f9-0d71-4dd9-93cc-85f09a51c5fc
title: CertificateStatus. Certificates, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 325b5c45fc6ae626363de286a6e131f1782cb83f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545910"
---
# <a name="certificatestatuscertificates-property"></a><span data-ttu-id="7a2e1-103">CertificateStatus. Certificates, propriété</span><span class="sxs-lookup"><span data-stu-id="7a2e1-103">CertificateStatus.Certificates property</span></span>

<span data-ttu-id="7a2e1-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7a2e1-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7a2e1-105">Utilisez plutôt la [**structure X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="7a2e1-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="7a2e1-106">La propriété **certificats** définit ou récupère la collection de certificats qui peuvent être utilisés pour créer la chaîne de certificats.</span><span class="sxs-lookup"><span data-stu-id="7a2e1-106">The **Certificates** property sets or retrieves the collection of certificates that can be used to build the certificate chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a2e1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a2e1-107">Syntax</span></span>


```VB
CertificateStatus.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="7a2e1-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7a2e1-108">Property value</span></span>

<span data-ttu-id="7a2e1-109">Objet de [**certificats**](certificates.md) qui représente la collection de certificats qui peut être utilisée pour générer la chaîne de certificats.</span><span class="sxs-lookup"><span data-stu-id="7a2e1-109">A [**Certificates**](certificates.md) object that represents the collection of certificates that can be used to build the certificate chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a2e1-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a2e1-110">Requirements</span></span>



| <span data-ttu-id="7a2e1-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a2e1-111">Requirement</span></span> | <span data-ttu-id="7a2e1-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a2e1-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a2e1-113">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7a2e1-113">End of client support</span></span><br/> | <span data-ttu-id="7a2e1-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a2e1-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7a2e1-115">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="7a2e1-115">End of server support</span></span><br/> | <span data-ttu-id="7a2e1-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a2e1-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7a2e1-117">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="7a2e1-117">Redistributable</span></span><br/>       | <span data-ttu-id="7a2e1-118">CAPICOM 2,1 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="7a2e1-118">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7a2e1-119">DLL</span><span class="sxs-lookup"><span data-stu-id="7a2e1-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7a2e1-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a2e1-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
