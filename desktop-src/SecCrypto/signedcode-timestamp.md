---
description: Crée une signature d’horodatage Authenticode sur le fichier exécutable signé spécifié dans la propriété SignedCode. FileName.
ms.assetid: 8f4c9901-b509-4e4c-82f9-a802b0896a11
title: SignedCode. Timestamp, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Timestamp
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1b0f4478e4ece5188a96257a8a1dcc9722caa140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541331"
---
# <a name="signedcodetimestamp-method"></a><span data-ttu-id="927ca-103">SignedCode. Timestamp, méthode</span><span class="sxs-lookup"><span data-stu-id="927ca-103">SignedCode.Timestamp method</span></span>

<span data-ttu-id="927ca-104">\[La méthode d' **horodatage** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="927ca-104">\[The **Timestamp** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="927ca-105">Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler les fonctions [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)et [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de l’API Win32 pour signer du contenu avec une signature numérique Authenticode.</span><span class="sxs-lookup"><span data-stu-id="927ca-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="927ca-106">Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="927ca-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="927ca-107">Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]</span><span class="sxs-lookup"><span data-stu-id="927ca-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="927ca-108">La méthode **timestamp** crée une signature d’horodatage Authenticode sur le fichier exécutable signé spécifié dans la propriété **SignedCode. FileName** .</span><span class="sxs-lookup"><span data-stu-id="927ca-108">The **Timestamp** method creates an Authenticode time stamp signature on the signed executable file specified in the **SignedCode.FileName** property.</span></span> <span data-ttu-id="927ca-109">Cet horodatage est une signature de compteur sur le fichier exécutable signé qui est exécuté par une autorité d’horodatage.</span><span class="sxs-lookup"><span data-stu-id="927ca-109">This time stamp is a counter signature on the signed executable file that is performed by a time stamp authority.</span></span>

## <a name="syntax"></a><span data-ttu-id="927ca-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="927ca-110">Syntax</span></span>


```VB
SignedCode.Timestamp( _
  ByVal URL _
)
```



## <a name="parameters"></a><span data-ttu-id="927ca-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="927ca-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="927ca-112">*URL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="927ca-112">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="927ca-113">Chaîne qui contient l’URL du serveur d’horodatage.</span><span class="sxs-lookup"><span data-stu-id="927ca-113">A string that contains the URL of the time stamp server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="927ca-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="927ca-114">Return value</span></span>

<span data-ttu-id="927ca-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="927ca-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="927ca-116">Notes</span><span class="sxs-lookup"><span data-stu-id="927ca-116">Remarks</span></span>

<span data-ttu-id="927ca-117">Un horodatage étend la validité d’un certificat en vérifiant que le fichier exécutable a été signé au moment où il a été horodaté.</span><span class="sxs-lookup"><span data-stu-id="927ca-117">A time stamp extends the validity of a certificate by verifying that the executable file was signed at the time that it was time stamped.</span></span>

<span data-ttu-id="927ca-118">Avant que cette méthode puisse être appelée, le fichier exécutable signé doit être spécifié dans la propriété **SignedCode. FileName** , et la méthode [**SignedCode. Sign**](signedcode-sign.md) doit être appelée pour signer le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="927ca-118">Before this method can be called, the signed executable file to be time stamped must be specified in the **SignedCode.FileName** property, and the [**SignedCode.Sign**](signedcode-sign.md) method must be called to sign the executable file.</span></span>

<span data-ttu-id="927ca-119">Si le fichier exécutable signé est déjà horodaté, cette méthode remplace l’heure d’horodatage existante.</span><span class="sxs-lookup"><span data-stu-id="927ca-119">If the signed executable file is already time stamped, this method overwrites the existing time stamp.</span></span>

## <a name="requirements"></a><span data-ttu-id="927ca-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="927ca-120">Requirements</span></span>



| <span data-ttu-id="927ca-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="927ca-121">Requirement</span></span> | <span data-ttu-id="927ca-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="927ca-122">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="927ca-123">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="927ca-123">Redistributable</span></span><br/> | <span data-ttu-id="927ca-124">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="927ca-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="927ca-125">DLL</span><span class="sxs-lookup"><span data-stu-id="927ca-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="927ca-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="927ca-126"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="927ca-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="927ca-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="927ca-128">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="927ca-128">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
