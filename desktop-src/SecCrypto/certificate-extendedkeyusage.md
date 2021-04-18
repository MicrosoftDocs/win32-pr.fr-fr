---
description: Retourne un objet ExtendedKeyUsage qui indique les utilisations valides du certificat.
ms.assetid: e974e9e2-1011-48b7-9ebc-e754e4990286
title: 'ICertificate2 :: ExtendedKeyUsage, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.ExtendedKeyUsage
- ICertificate2.ExtendedKeyUsage
- ICertificate.ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6f349b7267d58a9376b9295e3ffd5013954a0872
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540461"
---
# <a name="icertificate2extendedkeyusage-method"></a><span data-ttu-id="7958f-103">ICertificate2 :: ExtendedKeyUsage, méthode</span><span class="sxs-lookup"><span data-stu-id="7958f-103">ICertificate2::ExtendedKeyUsage method</span></span>

<span data-ttu-id="7958f-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7958f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7958f-105">Utilisez plutôt la [**classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="7958f-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="7958f-106">La méthode **ExtendedKeyUsage** retourne un objet [**ExtendedKeyUsage**](extendedkeyusage.md) qui indique les utilisations valides du certificat.</span><span class="sxs-lookup"><span data-stu-id="7958f-106">The **ExtendedKeyUsage** method returns an [**ExtendedKeyUsage**](extendedkeyusage.md) object that indicates the valid uses of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="7958f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7958f-107">Syntax</span></span>


```VB
Certificate.ExtendedKeyUsage()
```



## <a name="parameters"></a><span data-ttu-id="7958f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7958f-108">Parameters</span></span>

<span data-ttu-id="7958f-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7958f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7958f-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7958f-110">Return value</span></span>

<span data-ttu-id="7958f-111">Objet [**ExtendedKeyUsage**](extendedkeyusage.md) associé au certificat.</span><span class="sxs-lookup"><span data-stu-id="7958f-111">The [**ExtendedKeyUsage**](extendedkeyusage.md) object that is associated with the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="7958f-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7958f-112">Requirements</span></span>



| <span data-ttu-id="7958f-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7958f-113">Requirement</span></span> | <span data-ttu-id="7958f-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="7958f-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7958f-115">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7958f-115">End of client support</span></span><br/> | <span data-ttu-id="7958f-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7958f-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7958f-117">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="7958f-117">End of server support</span></span><br/> | <span data-ttu-id="7958f-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7958f-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7958f-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="7958f-119">Redistributable</span></span><br/>       | <span data-ttu-id="7958f-120">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="7958f-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7958f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="7958f-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7958f-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7958f-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7958f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7958f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7958f-124">Objets de chiffrement</span><span class="sxs-lookup"><span data-stu-id="7958f-124">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="7958f-125">**Certificat**</span><span class="sxs-lookup"><span data-stu-id="7958f-125">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
