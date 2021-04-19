---
description: Récupère l’algorithme de chiffrement et la longueur de clé.
ms.assetid: 13b2a3db-f04b-4436-b64f-f194fc9ddac2
title: EnvelopedData. algorithme, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9d6550be7ac32c08568baa8ef811478de50b27c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525470"
---
# <a name="envelopeddataalgorithm-property"></a><span data-ttu-id="6fbf7-103">EnvelopedData. algorithme, propriété</span><span class="sxs-lookup"><span data-stu-id="6fbf7-103">EnvelopedData.Algorithm property</span></span>

<span data-ttu-id="6fbf7-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6fbf7-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="6fbf7-105">Utilisez plutôt la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="6fbf7-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="6fbf7-106">La propriété **algorithme** récupère l’algorithme de chiffrement et la [*longueur de clé*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="6fbf7-106">The **Algorithm** property retrieves the encryption algorithm and [*key length*](../secgloss/k-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6fbf7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fbf7-107">Syntax</span></span>


```VB
EnvelopedData.Algorithm As Algorithm
```



## <a name="property-value"></a><span data-ttu-id="6fbf7-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6fbf7-108">Property value</span></span>

<span data-ttu-id="6fbf7-109">Objet [**algorithme**](algorithm.md) qui contient l’algorithme de chiffrement et la longueur de clé.</span><span class="sxs-lookup"><span data-stu-id="6fbf7-109">An [**Algorithm**](algorithm.md) object that contains the encryption algorithm and key length.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fbf7-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fbf7-110">Requirements</span></span>



| <span data-ttu-id="6fbf7-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fbf7-111">Requirement</span></span> | <span data-ttu-id="6fbf7-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fbf7-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fbf7-113">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="6fbf7-113">End of client support</span></span><br/> | <span data-ttu-id="6fbf7-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6fbf7-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6fbf7-115">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="6fbf7-115">End of server support</span></span><br/> | <span data-ttu-id="6fbf7-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6fbf7-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6fbf7-117">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="6fbf7-117">Redistributable</span></span><br/>       | <span data-ttu-id="6fbf7-118">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="6fbf7-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6fbf7-119">DLL</span><span class="sxs-lookup"><span data-stu-id="6fbf7-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6fbf7-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fbf7-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fbf7-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fbf7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fbf7-122">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="6fbf7-122">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
