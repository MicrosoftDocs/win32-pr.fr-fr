---
description: Supprime tous les objets de certificat d’une collection de destinataires.
ms.assetid: 456fcfbc-4388-40f4-ab58-04508ee2141b
title: Recipients. Clear, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7d9bd711bbc97997045989f2eb4ffdbc51ae3559
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541055"
---
# <a name="recipientsclear-method"></a><span data-ttu-id="4a07e-103">Recipients. Clear, méthode</span><span class="sxs-lookup"><span data-stu-id="4a07e-103">Recipients.Clear method</span></span>

<span data-ttu-id="4a07e-104">\[La méthode **Clear** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="4a07e-104">\[The **Clear** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4a07e-105">Utilisez plutôt la [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="4a07e-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="4a07e-106">La méthode **Clear** supprime tous les objets de [**certificat**](certificate.md) d’une collection [**Recipients**](recipients.md) .</span><span class="sxs-lookup"><span data-stu-id="4a07e-106">The **Clear** method removes all [**Certificate**](certificate.md) objects from a [**Recipients**](recipients.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a07e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a07e-107">Syntax</span></span>


```VB
Recipients.Clear()
```



## <a name="parameters"></a><span data-ttu-id="4a07e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a07e-108">Parameters</span></span>

<span data-ttu-id="4a07e-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="4a07e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4a07e-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4a07e-110">Return value</span></span>

<span data-ttu-id="4a07e-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4a07e-111">This method does not return a value.</span></span> <span data-ttu-id="4a07e-112">Une application qui utilise cette méthode doit contenir du code pour gérer une exception levée par cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4a07e-112">An application that uses this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a07e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a07e-113">Requirements</span></span>



| <span data-ttu-id="4a07e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a07e-114">Requirement</span></span> | <span data-ttu-id="4a07e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a07e-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a07e-116">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="4a07e-116">Redistributable</span></span><br/> | <span data-ttu-id="4a07e-117">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="4a07e-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4a07e-118">DLL</span><span class="sxs-lookup"><span data-stu-id="4a07e-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="4a07e-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a07e-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a07e-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a07e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a07e-121">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="4a07e-121">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="4a07e-122">**Destinataires**</span><span class="sxs-lookup"><span data-stu-id="4a07e-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
