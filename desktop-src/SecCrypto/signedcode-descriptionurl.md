---
description: Définit ou récupère l’URL d’une description du fichier exécutable signé.
ms.assetid: 854c76fb-5cb3-4200-bab0-fa3fa5bd3abe
title: SignedCode. DescriptionURL, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.DescriptionURL
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 628d176595031f2b87b9fcb5f58ff81838d49be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528027"
---
# <a name="signedcodedescriptionurl-property"></a><span data-ttu-id="6debf-103">SignedCode. DescriptionURL, propriété</span><span class="sxs-lookup"><span data-stu-id="6debf-103">SignedCode.DescriptionURL property</span></span>

<span data-ttu-id="6debf-104">\[La propriété **DescriptionURL** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="6debf-104">\[The **DescriptionURL** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6debf-105">Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler les fonctions [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)et [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de l’API Win32 pour signer du contenu avec une signature numérique Authenticode.</span><span class="sxs-lookup"><span data-stu-id="6debf-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="6debf-106">Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="6debf-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="6debf-107">Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]</span><span class="sxs-lookup"><span data-stu-id="6debf-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="6debf-108">La propriété **DescriptionURL** définit ou récupère l’URL d’une description du fichier exécutable signé.</span><span class="sxs-lookup"><span data-stu-id="6debf-108">The **DescriptionURL** property sets or retrieves the URL of a description of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6debf-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6debf-109">Syntax</span></span>


```VB
SignedCode.DescriptionURL As String
```



## <a name="property-value"></a><span data-ttu-id="6debf-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6debf-110">Property value</span></span>

<span data-ttu-id="6debf-111">URL d’une description du fichier exécutable signé.</span><span class="sxs-lookup"><span data-stu-id="6debf-111">The URL of a description of the signed executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="6debf-112">Notes</span><span class="sxs-lookup"><span data-stu-id="6debf-112">Remarks</span></span>

<span data-ttu-id="6debf-113">**DescriptionURL** est l’URL vers laquelle la [**Description**](signedcode-description.md) qui apparaît dans la boîte de dialogue vérification Authenticode est liée.</span><span class="sxs-lookup"><span data-stu-id="6debf-113">The **DescriptionURL** is the URL to which the [**Description**](signedcode-description.md) that appears in the Authenticode verification dialog box links.</span></span> <span data-ttu-id="6debf-114">Si cette propriété a la **valeur null**, la **Description** ne fonctionne pas comme un lien.</span><span class="sxs-lookup"><span data-stu-id="6debf-114">If this property is **NULL**, the **Description** does not function as a link.</span></span>

## <a name="requirements"></a><span data-ttu-id="6debf-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6debf-115">Requirements</span></span>



| <span data-ttu-id="6debf-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6debf-116">Requirement</span></span> | <span data-ttu-id="6debf-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6debf-117">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6debf-118">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="6debf-118">Redistributable</span></span><br/> | <span data-ttu-id="6debf-119">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="6debf-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6debf-120">DLL</span><span class="sxs-lookup"><span data-stu-id="6debf-120">DLL</span></span><br/>             | <dl> <span data-ttu-id="6debf-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6debf-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6debf-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6debf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6debf-123">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="6debf-123">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
