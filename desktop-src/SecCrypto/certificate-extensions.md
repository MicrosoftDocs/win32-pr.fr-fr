---
description: Retourne une collection des extensions associées au certificat.
ms.assetid: 07793061-6f94-4467-bb01-aa65db657658
title: 'ICertificate2 :: extensions, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Extensions
- ICertificate2.Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cc96dee9c33bb3f76e1fb17acb2000f9740d1b5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530974"
---
# <a name="icertificate2extensions-method"></a><span data-ttu-id="074f0-103">ICertificate2 :: extensions, méthode</span><span class="sxs-lookup"><span data-stu-id="074f0-103">ICertificate2::Extensions method</span></span>

<span data-ttu-id="074f0-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="074f0-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="074f0-105">Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="074f0-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="074f0-106">La méthode **Extensions** retourne une collection des extensions associées au certificat.</span><span class="sxs-lookup"><span data-stu-id="074f0-106">The **Extensions** method returns a collection of the extensions associated with the certificate.</span></span> <span data-ttu-id="074f0-107">Cette méthode est introduite dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="074f0-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="074f0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="074f0-108">Syntax</span></span>


```VB
Certificate.Extensions()
```



## <a name="parameters"></a><span data-ttu-id="074f0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="074f0-109">Parameters</span></span>

<span data-ttu-id="074f0-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="074f0-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="074f0-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="074f0-111">Return value</span></span>

<span data-ttu-id="074f0-112">Objet d' [**Extensions**](extensions.md) qui représente toutes les extensions associées au certificat.</span><span class="sxs-lookup"><span data-stu-id="074f0-112">An [**Extensions**](extensions.md) object that represents all of the extensions associated with the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="074f0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="074f0-113">Requirements</span></span>



| <span data-ttu-id="074f0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="074f0-114">Requirement</span></span> | <span data-ttu-id="074f0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="074f0-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="074f0-116">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="074f0-116">End of client support</span></span><br/> | <span data-ttu-id="074f0-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="074f0-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="074f0-118">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="074f0-118">End of server support</span></span><br/> | <span data-ttu-id="074f0-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="074f0-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="074f0-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="074f0-120">Redistributable</span></span><br/>       | <span data-ttu-id="074f0-121">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="074f0-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="074f0-122">DLL</span><span class="sxs-lookup"><span data-stu-id="074f0-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="074f0-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="074f0-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
