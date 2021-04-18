---
description: Retourne un objet KeyUsage qui indique l’utilisation valide de la clé du certificat.
ms.assetid: e4590e95-ffa2-4953-bfc1-4d7c70271029
title: 'ICertificate2 :: KeyUsage, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.KeyUsage
- ICertificate2.KeyUsage
- ICertificate.KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85fe008880d9613586d38dba7afaca39bb29f72f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526668"
---
# <a name="icertificate2keyusage-method"></a><span data-ttu-id="6bfee-103">ICertificate2 :: KeyUsage, méthode</span><span class="sxs-lookup"><span data-stu-id="6bfee-103">ICertificate2::KeyUsage method</span></span>

<span data-ttu-id="6bfee-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6bfee-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="6bfee-105">Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="6bfee-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6bfee-106">La méthode **KeyUsage** retourne un objet [**KeyUsage**](keyusage.md) qui indique l’utilisation valide de la clé du certificat.</span><span class="sxs-lookup"><span data-stu-id="6bfee-106">The **KeyUsage** method returns a [**KeyUsage**](keyusage.md) object that indicates the valid key usage of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bfee-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6bfee-107">Syntax</span></span>


```VB
Certificate.KeyUsage()
```



## <a name="parameters"></a><span data-ttu-id="6bfee-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6bfee-108">Parameters</span></span>

<span data-ttu-id="6bfee-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6bfee-109">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bfee-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6bfee-110">Requirements</span></span>



| <span data-ttu-id="6bfee-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6bfee-111">Requirement</span></span> | <span data-ttu-id="6bfee-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="6bfee-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bfee-113">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="6bfee-113">End of client support</span></span><br/> | <span data-ttu-id="6bfee-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6bfee-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6bfee-115">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="6bfee-115">End of server support</span></span><br/> | <span data-ttu-id="6bfee-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6bfee-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6bfee-117">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="6bfee-117">Redistributable</span></span><br/>       | <span data-ttu-id="6bfee-118">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="6bfee-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6bfee-119">DLL</span><span class="sxs-lookup"><span data-stu-id="6bfee-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6bfee-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bfee-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bfee-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bfee-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bfee-122">Objets de chiffrement</span><span class="sxs-lookup"><span data-stu-id="6bfee-122">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="6bfee-123">**Certificat**</span><span class="sxs-lookup"><span data-stu-id="6bfee-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
