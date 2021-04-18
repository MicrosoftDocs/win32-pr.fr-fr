---
description: Récupère l’algorithme pour les données chiffrées.
ms.assetid: 37bebe69-3c62-44c4-a5e5-c8cdbf087fa4
title: EncryptedData. Algorithm, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cd73fbda4a5f77706ac2253782768e8487b8cbff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533371"
---
# <a name="encrypteddataalgorithm-property"></a><span data-ttu-id="f5b6b-103">EncryptedData. Algorithm, propriété</span><span class="sxs-lookup"><span data-stu-id="f5b6b-103">EncryptedData.Algorithm property</span></span>

<span data-ttu-id="f5b6b-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f5b6b-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f5b6b-105">Utilisez plutôt les services d’appel de code non managé (PInvoke) pour appeler les fonctions de l’API Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) et [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) pour chiffrer et déchiffrer les messages.</span><span class="sxs-lookup"><span data-stu-id="f5b6b-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="f5b6b-106">Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5b6b-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="f5b6b-107">Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]</span><span class="sxs-lookup"><span data-stu-id="f5b6b-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="f5b6b-108">La propriété **algorithme** récupère l’algorithme pour les données chiffrées.</span><span class="sxs-lookup"><span data-stu-id="f5b6b-108">The **Algorithm** property retrieves the algorithm for the encrypted data.</span></span>

<span data-ttu-id="f5b6b-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f5b6b-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5b6b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5b6b-110">Syntax</span></span>


```VB
EncryptedData.Algorithm As Algorithm
```



## <a name="property-value"></a><span data-ttu-id="f5b6b-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f5b6b-111">Property value</span></span>

<span data-ttu-id="f5b6b-112">Objet [**algorithme**](algorithm.md) qui représente l’algorithme de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="f5b6b-112">An [**Algorithm**](algorithm.md) object that represents the encryption algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5b6b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5b6b-113">Requirements</span></span>



| <span data-ttu-id="f5b6b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5b6b-114">Requirement</span></span> | <span data-ttu-id="f5b6b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5b6b-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b6b-116">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f5b6b-116">End of client support</span></span><br/> | <span data-ttu-id="f5b6b-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5b6b-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f5b6b-118">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="f5b6b-118">End of server support</span></span><br/> | <span data-ttu-id="f5b6b-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5b6b-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f5b6b-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="f5b6b-120">Redistributable</span></span><br/>       | <span data-ttu-id="f5b6b-121">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5b6b-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f5b6b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f5b6b-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f5b6b-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5b6b-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5b6b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5b6b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5b6b-125">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="f5b6b-125">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
