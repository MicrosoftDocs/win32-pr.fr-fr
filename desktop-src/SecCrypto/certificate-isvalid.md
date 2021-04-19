---
description: Crée une chaîne de vérification de certificat pour un certificat et retourne un objet CertificateStatus qui contient l’état de validité du certificat.
ms.assetid: 4463e4ac-60a5-4845-93b3-35d2f83bd86e
title: 'ICertificate2 :: IsValid, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.IsValid
- ICertificate2.IsValid
- ICertificate.IsValid
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 39fec7c1bd2b369ee512834ed1b58b59871d8ae5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530403"
---
# <a name="icertificate2isvalid-method"></a><span data-ttu-id="63ced-103">ICertificate2 :: IsValid, méthode</span><span class="sxs-lookup"><span data-stu-id="63ced-103">ICertificate2::IsValid method</span></span>

<span data-ttu-id="63ced-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="63ced-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="63ced-105">Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="63ced-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="63ced-106">La méthode **IsValid** crée une chaîne de vérification de certificat pour un certificat et retourne un objet [**CertificateStatus**](certificatestatus.md) qui contient l’état de validité du certificat.</span><span class="sxs-lookup"><span data-stu-id="63ced-106">The **IsValid** method builds a certificate verification chain for a certificate and returns a [**CertificateStatus**](certificatestatus.md) object that contains the validity status of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="63ced-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63ced-107">Syntax</span></span>


```VB
Certificate.IsValid()
```



## <a name="parameters"></a><span data-ttu-id="63ced-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63ced-108">Parameters</span></span>

<span data-ttu-id="63ced-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="63ced-109">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="63ced-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63ced-110">Requirements</span></span>



| <span data-ttu-id="63ced-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63ced-111">Requirement</span></span> | <span data-ttu-id="63ced-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="63ced-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63ced-113">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="63ced-113">End of client support</span></span><br/> | <span data-ttu-id="63ced-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63ced-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="63ced-115">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="63ced-115">End of server support</span></span><br/> | <span data-ttu-id="63ced-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63ced-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="63ced-117">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="63ced-117">Redistributable</span></span><br/>       | <span data-ttu-id="63ced-118">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="63ced-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="63ced-119">DLL</span><span class="sxs-lookup"><span data-stu-id="63ced-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="63ced-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63ced-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63ced-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63ced-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63ced-122">Objets de chiffrement</span><span class="sxs-lookup"><span data-stu-id="63ced-122">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="63ced-123">**Certificat**</span><span class="sxs-lookup"><span data-stu-id="63ced-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
