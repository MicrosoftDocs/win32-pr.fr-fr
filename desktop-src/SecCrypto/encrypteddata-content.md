---
description: Définit ou récupère le contenu à chiffrer ou à déchiffrer.
ms.assetid: fdab0f19-c69e-443b-b4b3-079d23028921
title: EncryptedData. Content, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4b873d40ed04270defe04fd59f0ce00a0f84040a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525964"
---
# <a name="encrypteddatacontent-property"></a><span data-ttu-id="92e07-103">EncryptedData. Content, propriété</span><span class="sxs-lookup"><span data-stu-id="92e07-103">EncryptedData.Content property</span></span>

<span data-ttu-id="92e07-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="92e07-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="92e07-105">Utilisez plutôt les services d’appel de code non managé (PInvoke) pour appeler les fonctions de l’API Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) et [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) pour chiffrer et déchiffrer les messages.</span><span class="sxs-lookup"><span data-stu-id="92e07-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="92e07-106">Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="92e07-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="92e07-107">Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]</span><span class="sxs-lookup"><span data-stu-id="92e07-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="92e07-108">La propriété de **contenu** définit ou récupère le contenu à chiffrer ou à déchiffrer.</span><span class="sxs-lookup"><span data-stu-id="92e07-108">The **Content** property sets or retrieves the content to be encrypted or decrypted.</span></span> <span data-ttu-id="92e07-109">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="92e07-109">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="92e07-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92e07-110">Syntax</span></span>


```VB
EncryptedData.Content As String
```



## <a name="property-value"></a><span data-ttu-id="92e07-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="92e07-111">Property value</span></span>

<span data-ttu-id="92e07-112">Contenu à chiffrer ou à déchiffrer.</span><span class="sxs-lookup"><span data-stu-id="92e07-112">The content to be encrypted or decrypted.</span></span>

## <a name="requirements"></a><span data-ttu-id="92e07-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92e07-113">Requirements</span></span>



| <span data-ttu-id="92e07-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92e07-114">Requirement</span></span> | <span data-ttu-id="92e07-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="92e07-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="92e07-116">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="92e07-116">End of client support</span></span><br/> | <span data-ttu-id="92e07-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92e07-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="92e07-118">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="92e07-118">End of server support</span></span><br/> | <span data-ttu-id="92e07-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92e07-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="92e07-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="92e07-120">Redistributable</span></span><br/>       | <span data-ttu-id="92e07-121">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="92e07-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="92e07-122">DLL</span><span class="sxs-lookup"><span data-stu-id="92e07-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="92e07-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92e07-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92e07-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92e07-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92e07-125">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="92e07-125">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
