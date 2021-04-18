---
description: Retourne un objet BasicConstraints qui représente l’extension de contraintes de base du certificat.
ms.assetid: cc4e566a-5f68-4e28-9397-39f22a71e45b
title: 'ICertificate2 :: BasicConstraints, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.BasicConstraints
- ICertificate2.BasicConstraints
- ICertificate.BasicConstraints
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b511781c29d313715e7714f185dbff7e4b38f86c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540103"
---
# <a name="icertificate2basicconstraints-method"></a><span data-ttu-id="bd545-103">ICertificate2 :: BasicConstraints, méthode</span><span class="sxs-lookup"><span data-stu-id="bd545-103">ICertificate2::BasicConstraints method</span></span>

<span data-ttu-id="bd545-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bd545-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="bd545-105">Utilisez plutôt la [**classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="bd545-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="bd545-106">La méthode **basicConstraints** retourne un objet [**basicConstraints**](basicconstraints.md) qui représente l’extension de contraintes de base du certificat.</span><span class="sxs-lookup"><span data-stu-id="bd545-106">The **BasicConstraints** method returns a [**BasicConstraints**](basicconstraints.md) object that represents the basic constraints extension of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd545-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd545-107">Syntax</span></span>


```VB
Certificate.BasicConstraints()
```



## <a name="parameters"></a><span data-ttu-id="bd545-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd545-108">Parameters</span></span>

<span data-ttu-id="bd545-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="bd545-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bd545-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bd545-110">Return value</span></span>

<span data-ttu-id="bd545-111">Objet [**basicConstraints**](basicconstraints.md) qui représente l’extension de contraintes de base du certificat.</span><span class="sxs-lookup"><span data-stu-id="bd545-111">The [**BasicConstraints**](basicconstraints.md) object that represents the basic constraints extension of the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd545-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd545-112">Requirements</span></span>



| <span data-ttu-id="bd545-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd545-113">Requirement</span></span> | <span data-ttu-id="bd545-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd545-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd545-115">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="bd545-115">End of client support</span></span><br/> | <span data-ttu-id="bd545-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd545-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bd545-117">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="bd545-117">End of server support</span></span><br/> | <span data-ttu-id="bd545-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd545-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bd545-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="bd545-119">Redistributable</span></span><br/>       | <span data-ttu-id="bd545-120">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="bd545-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bd545-121">DLL</span><span class="sxs-lookup"><span data-stu-id="bd545-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="bd545-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd545-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
