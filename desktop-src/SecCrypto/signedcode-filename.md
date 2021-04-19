---
description: La propriété FileName définit ou récupère le chemin d’accès au fichier exécutable. Il s’agit de la propriété par défaut.
ms.assetid: 2d2ea87b-86db-40b4-b052-8503beafa08c
title: SignedCode. FileName, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.FileName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e6e31e57376f987b2b5cb47e5e6bd8a0d5e85fba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535411"
---
# <a name="signedcodefilename-property"></a><span data-ttu-id="ab7bc-104">SignedCode. FileName, propriété</span><span class="sxs-lookup"><span data-stu-id="ab7bc-104">SignedCode.FileName property</span></span>

<span data-ttu-id="ab7bc-105">\[La propriété **nom de fichier** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="ab7bc-105">\[The **FileName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ab7bc-106">Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler les fonctions [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)et [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de l’API Win32 pour signer du contenu avec une signature numérique Authenticode.</span><span class="sxs-lookup"><span data-stu-id="ab7bc-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="ab7bc-107">Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="ab7bc-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="ab7bc-108">Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]</span><span class="sxs-lookup"><span data-stu-id="ab7bc-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="ab7bc-109">La propriété **filename** définit ou récupère le chemin d’accès au fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="ab7bc-109">The **FileName** property sets or retrieves the path to the executable file.</span></span> <span data-ttu-id="ab7bc-110">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="ab7bc-110">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab7bc-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab7bc-111">Syntax</span></span>


```VB
SignedCode.FileName As String
```



## <a name="property-value"></a><span data-ttu-id="ab7bc-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ab7bc-112">Property value</span></span>

<span data-ttu-id="ab7bc-113">Chemin du fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="ab7bc-113">The path to the executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab7bc-114">Notes</span><span class="sxs-lookup"><span data-stu-id="ab7bc-114">Remarks</span></span>

<span data-ttu-id="ab7bc-115">Si la valeur de la propriété **filename** est modifiée, l’état de la totalité de l’objet [**SignedCode**](signedcode.md) est réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="ab7bc-115">If the value of the **FileName** property is modified, the state of the entire [**SignedCode**](signedcode.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab7bc-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab7bc-116">Requirements</span></span>



| <span data-ttu-id="ab7bc-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab7bc-117">Requirement</span></span> | <span data-ttu-id="ab7bc-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab7bc-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab7bc-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="ab7bc-119">Redistributable</span></span><br/> | <span data-ttu-id="ab7bc-120">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="ab7bc-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ab7bc-121">DLL</span><span class="sxs-lookup"><span data-stu-id="ab7bc-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="ab7bc-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab7bc-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab7bc-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab7bc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab7bc-124">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="ab7bc-124">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
