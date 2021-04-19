---
description: Définit ou récupère la description du fichier exécutable signé.
ms.assetid: 39ce37bd-fe3e-4195-a132-93f3743f7370
title: Propriété SignedCode. Description
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Description
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b5783dd5e662aed33722a1c587bfcdc3cab76c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543807"
---
# <a name="signedcodedescription-property"></a><span data-ttu-id="357c2-103">Propriété SignedCode. Description</span><span class="sxs-lookup"><span data-stu-id="357c2-103">SignedCode.Description property</span></span>

<span data-ttu-id="357c2-104">\[La propriété **Description** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="357c2-104">\[The **Description** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="357c2-105">Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler les fonctions [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)et [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de l’API Win32 pour signer du contenu avec une signature numérique Authenticode.</span><span class="sxs-lookup"><span data-stu-id="357c2-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="357c2-106">Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="357c2-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="357c2-107">Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]</span><span class="sxs-lookup"><span data-stu-id="357c2-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="357c2-108">La propriété **Description** définit ou récupère la description du fichier exécutable signé.</span><span class="sxs-lookup"><span data-stu-id="357c2-108">The **Description** property sets or retrieves the description of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="357c2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="357c2-109">Syntax</span></span>


```VB
SignedCode.Description As String
```



## <a name="property-value"></a><span data-ttu-id="357c2-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="357c2-110">Property value</span></span>

<span data-ttu-id="357c2-111">Description du fichier exécutable signé.</span><span class="sxs-lookup"><span data-stu-id="357c2-111">The description of the signed executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="357c2-112">Notes</span><span class="sxs-lookup"><span data-stu-id="357c2-112">Remarks</span></span>

<span data-ttu-id="357c2-113">La description est le texte qui apparaît dans la boîte de dialogue vérification Authenticode.</span><span class="sxs-lookup"><span data-stu-id="357c2-113">The description is the text that appears in the Authenticode verification dialog box.</span></span> <span data-ttu-id="357c2-114">Le texte doit décrire le fichier exécutable signé.</span><span class="sxs-lookup"><span data-stu-id="357c2-114">The text should describe the signed executable file.</span></span> <span data-ttu-id="357c2-115">Si cette propriété a la **valeur null**, la boîte de dialogue affiche le nom du fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="357c2-115">If this property is **NULL**, the dialog box displays the name of the executable file.</span></span>

## <a name="requirements"></a><span data-ttu-id="357c2-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="357c2-116">Requirements</span></span>



| <span data-ttu-id="357c2-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="357c2-117">Requirement</span></span> | <span data-ttu-id="357c2-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="357c2-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="357c2-119">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="357c2-119">Redistributable</span></span><br/> | <span data-ttu-id="357c2-120">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="357c2-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="357c2-121">DLL</span><span class="sxs-lookup"><span data-stu-id="357c2-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="357c2-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="357c2-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="357c2-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="357c2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="357c2-124">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="357c2-124">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
