---
description: Ajoute un objet certificat à la collection.
ms.assetid: 0973018d-1e83-41b4-a250-7dd5be2fb664
title: 'ICertificates2 :: Add, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Add
- ICertificates2.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d56120c6f584e828c3aadca037d75263d5350f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528912"
---
# <a name="icertificates2add-method"></a><span data-ttu-id="0b4ff-103">ICertificates2 :: Add, méthode</span><span class="sxs-lookup"><span data-stu-id="0b4ff-103">ICertificates2::Add method</span></span>

<span data-ttu-id="0b4ff-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0b4ff-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="0b4ff-105">Utilisez plutôt la [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="0b4ff-105">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="0b4ff-106">La méthode **Add** ajoute un objet [**certificat**](certificate.md) à la collection.</span><span class="sxs-lookup"><span data-stu-id="0b4ff-106">The **Add** method adds a [**Certificate**](certificate.md) object to the collection.</span></span> <span data-ttu-id="0b4ff-107">Cette méthode est introduite dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="0b4ff-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b4ff-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b4ff-108">Syntax</span></span>


```VB
Certificates.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="0b4ff-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b4ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b4ff-110">*Certificat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b4ff-110">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b4ff-111">Objet de [**certificat**](certificate.md) à ajouter à la collection.</span><span class="sxs-lookup"><span data-stu-id="0b4ff-111">The [**Certificate**](certificate.md) object to be added to the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b4ff-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b4ff-112">Return value</span></span>

<span data-ttu-id="0b4ff-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0b4ff-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b4ff-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b4ff-114">Requirements</span></span>



| <span data-ttu-id="0b4ff-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b4ff-115">Requirement</span></span> | <span data-ttu-id="0b4ff-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b4ff-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b4ff-117">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="0b4ff-117">End of client support</span></span><br/> | <span data-ttu-id="0b4ff-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b4ff-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0b4ff-119">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="0b4ff-119">End of server support</span></span><br/> | <span data-ttu-id="0b4ff-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b4ff-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0b4ff-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="0b4ff-121">Redistributable</span></span><br/>       | <span data-ttu-id="0b4ff-122">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="0b4ff-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0b4ff-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0b4ff-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="0b4ff-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b4ff-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
