---
description: Importe un certificat précédemment encodé à partir d’une chaîne dans l’objet certificat.
ms.assetid: 8515e034-08aa-4575-9b96-34cdee3ccba8
title: 'ICertificate2 :: import, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Import
- ICertificate2.Import
- ICertificate.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ea639f1cd89b673ecf8da77302e3d812894a202b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526028"
---
# <a name="icertificate2import-method"></a><span data-ttu-id="f8f56-103">ICertificate2 :: import, méthode</span><span class="sxs-lookup"><span data-stu-id="f8f56-103">ICertificate2::Import method</span></span>

<span data-ttu-id="f8f56-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f8f56-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f8f56-105">Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="f8f56-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f8f56-106">La méthode **Import** importe un certificat précédemment encodé à partir d’une chaîne dans l’objet [**certificat**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="f8f56-106">The **Import** method imports a previously encoded certificate from a string into the [**Certificate**](certificate.md) object.</span></span> <span data-ttu-id="f8f56-107">L’appel de cette méthode réinitialise l' [*État*](../secgloss/s-gly.md) de cet objet.</span><span class="sxs-lookup"><span data-stu-id="f8f56-107">Calling this method resets the [*state*](../secgloss/s-gly.md) of this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8f56-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8f56-108">Syntax</span></span>


```VB
Certificate.Import( _
  ByVal EncodedCertificate _
)
```



## <a name="parameters"></a><span data-ttu-id="f8f56-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8f56-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8f56-110">*EncodedCertificate* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f8f56-110">*EncodedCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8f56-111">Chaîne qui contient les données de certificat encodées à importer.</span><span class="sxs-lookup"><span data-stu-id="f8f56-111">A string that contains the encoded certificate data to be imported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8f56-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8f56-112">Return value</span></span>

<span data-ttu-id="f8f56-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f8f56-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8f56-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8f56-114">Requirements</span></span>



| <span data-ttu-id="f8f56-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8f56-115">Requirement</span></span> | <span data-ttu-id="f8f56-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8f56-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8f56-117">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f8f56-117">End of client support</span></span><br/> | <span data-ttu-id="f8f56-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8f56-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f8f56-119">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="f8f56-119">End of server support</span></span><br/> | <span data-ttu-id="f8f56-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8f56-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f8f56-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="f8f56-121">Redistributable</span></span><br/>       | <span data-ttu-id="f8f56-122">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="f8f56-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f8f56-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f8f56-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f8f56-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8f56-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8f56-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8f56-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8f56-126">Objets de chiffrement</span><span class="sxs-lookup"><span data-stu-id="f8f56-126">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="f8f56-127">**Certificat**</span><span class="sxs-lookup"><span data-stu-id="f8f56-127">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
