---
description: Récupère la collection de certificats dans le fichier exécutable signé.
ms.assetid: ecc05117-8b98-4e49-9671-71829df24597
title: SignedCode. Certificates, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b24a07041dae1ea2387ced93d1d2ae541a806029
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529879"
---
# <a name="signedcodecertificates-property"></a><span data-ttu-id="a0422-103">SignedCode. Certificates, propriété</span><span class="sxs-lookup"><span data-stu-id="a0422-103">SignedCode.Certificates property</span></span>

<span data-ttu-id="a0422-104">\[La propriété **certificats** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="a0422-104">\[The **Certificates** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a0422-105">Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler les fonctions [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)et [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de l’API Win32 pour signer du contenu avec une signature numérique Authenticode.</span><span class="sxs-lookup"><span data-stu-id="a0422-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="a0422-106">Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="a0422-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="a0422-107">Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]</span><span class="sxs-lookup"><span data-stu-id="a0422-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="a0422-108">La propriété **certificats** récupère la collection de certificats dans le fichier exécutable signé.</span><span class="sxs-lookup"><span data-stu-id="a0422-108">The **Certificates** property retrieves the collection of certificates in the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0422-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0422-109">Syntax</span></span>


```VB
SignedCode.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="a0422-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a0422-110">Property value</span></span>

<span data-ttu-id="a0422-111">Collection de [**certificats**](certificates.md) qui contient tous les certificats dans le fichier exécutable signé.</span><span class="sxs-lookup"><span data-stu-id="a0422-111">The [**Certificates**](certificates.md) collection that contains all the certificates in the signed executable file.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0422-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0422-112">Requirements</span></span>



| <span data-ttu-id="a0422-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0422-113">Requirement</span></span> | <span data-ttu-id="a0422-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0422-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0422-115">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a0422-115">Redistributable</span></span><br/> | <span data-ttu-id="a0422-116">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="a0422-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a0422-117">DLL</span><span class="sxs-lookup"><span data-stu-id="a0422-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="a0422-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0422-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0422-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0422-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0422-120">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="a0422-120">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
