---
description: La propriété TimeStamp récupère la matrice temporelle du fichier exécutable signé.
ms.assetid: f630b94f-015a-4387-938f-1b8c6b7895e9
title: Propriété SignedCode. TimeStamp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.TimeStamper
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5594cf46e82e47103d456fc7fe147e0470333953
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541740"
---
# <a name="signedcodetimestamper-property"></a><span data-ttu-id="2bce6-103">Propriété SignedCode. TimeStamp</span><span class="sxs-lookup"><span data-stu-id="2bce6-103">SignedCode.TimeStamper property</span></span>

<span data-ttu-id="2bce6-104">\[La propriété **horodateur** est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="2bce6-104">\[The **TimeStamper** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2bce6-105">Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler les fonctions [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)et [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de l’API Win32 pour signer du contenu avec une signature numérique Authenticode.</span><span class="sxs-lookup"><span data-stu-id="2bce6-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="2bce6-106">Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="2bce6-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="2bce6-107">Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]</span><span class="sxs-lookup"><span data-stu-id="2bce6-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="2bce6-108">La propriété **timestamp** récupère la matrice temporelle du fichier exécutable signé.</span><span class="sxs-lookup"><span data-stu-id="2bce6-108">The **TimeStamper** property retrieves the time stamper of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bce6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2bce6-109">Syntax</span></span>


```VB
SignedCode.TimeStamper As Signer
```



## <a name="property-value"></a><span data-ttu-id="2bce6-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2bce6-110">Property value</span></span>

<span data-ttu-id="2bce6-111">Objet [**signataire**](signer.md) qui fournit l’accès à l’horodatage du fichier exécutable signé.</span><span class="sxs-lookup"><span data-stu-id="2bce6-111">A [**Signer**](signer.md) object that provides access to the time stamper of the signed executable file.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bce6-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2bce6-112">Requirements</span></span>



| <span data-ttu-id="2bce6-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2bce6-113">Requirement</span></span> | <span data-ttu-id="2bce6-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="2bce6-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2bce6-115">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="2bce6-115">Redistributable</span></span><br/> | <span data-ttu-id="2bce6-116">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="2bce6-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2bce6-117">DLL</span><span class="sxs-lookup"><span data-stu-id="2bce6-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="2bce6-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bce6-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bce6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2bce6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bce6-120">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="2bce6-120">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
