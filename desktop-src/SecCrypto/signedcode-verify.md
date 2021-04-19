---
description: Vérifie la signature Authenticode sur le code signé.
ms.assetid: eecd692d-6b20-4644-a3d9-fba07ee667d7
title: SignedCode. Verify, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ad9ad2cdbf9c8b7970f50446bba0da7a3afdcd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540064"
---
# <a name="signedcodeverify-method"></a><span data-ttu-id="c93a6-103">SignedCode. Verify, méthode</span><span class="sxs-lookup"><span data-stu-id="c93a6-103">SignedCode.Verify method</span></span>

<span data-ttu-id="c93a6-104">\[La méthode **verify** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="c93a6-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c93a6-105">Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler les fonctions [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)et [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de l’API Win32 pour signer du contenu avec une signature numérique Authenticode.</span><span class="sxs-lookup"><span data-stu-id="c93a6-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="c93a6-106">Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="c93a6-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="c93a6-107">Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]</span><span class="sxs-lookup"><span data-stu-id="c93a6-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="c93a6-108">La méthode **verify** vérifie la signature Authenticode sur le code signé.</span><span class="sxs-lookup"><span data-stu-id="c93a6-108">The **Verify** method verifies the Authenticode signature on the signed code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c93a6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c93a6-109">Syntax</span></span>


```VB
SignedCode.Verify( _
  [ ByVal bUIAllowed ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c93a6-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c93a6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c93a6-111">*bUIAllowed* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c93a6-111">*bUIAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c93a6-112">Valeur booléenne qui spécifie si une boîte de dialogue est utilisée pour vérifier la signature.</span><span class="sxs-lookup"><span data-stu-id="c93a6-112">A Boolean value that specifies whether a dialog box is used to verify the signature.</span></span> <span data-ttu-id="c93a6-113">Si la valeur est true, une boîte de dialogue est générée pour déterminer si le code est approuvé.</span><span class="sxs-lookup"><span data-stu-id="c93a6-113">If true, a dialog box is generated to determine whether the code is trusted.</span></span> <span data-ttu-id="c93a6-114">La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="c93a6-114">The default value is false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c93a6-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c93a6-115">Return value</span></span>

<span data-ttu-id="c93a6-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c93a6-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c93a6-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c93a6-117">Requirements</span></span>



| <span data-ttu-id="c93a6-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c93a6-118">Requirement</span></span> | <span data-ttu-id="c93a6-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c93a6-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c93a6-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="c93a6-120">Redistributable</span></span><br/> | <span data-ttu-id="c93a6-121">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="c93a6-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c93a6-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c93a6-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="c93a6-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c93a6-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c93a6-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c93a6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c93a6-125">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="c93a6-125">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
