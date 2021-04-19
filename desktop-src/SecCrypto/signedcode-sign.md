---
description: Crée une signature numérique Authenticode et signe le fichier exécutable spécifié dans la propriété SignedCode. FileName.
ms.assetid: db17be29-35ec-4468-b5cc-5ba64c4cf3fb
title: SignedCode. Sign, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36e5c813b997ae452d44764ed88f51b273c75528
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541435"
---
# <a name="signedcodesign-method"></a><span data-ttu-id="2f297-103">SignedCode. Sign, méthode</span><span class="sxs-lookup"><span data-stu-id="2f297-103">SignedCode.Sign method</span></span>

<span data-ttu-id="2f297-104">\[La méthode **Sign** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="2f297-104">\[The **Sign** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2f297-105">Utilisez plutôt les services d’appel de plateforme (PInvoke) pour appeler les fonctions [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)et [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de l’API Win32 pour signer du contenu avec une signature numérique Authenticode.</span><span class="sxs-lookup"><span data-stu-id="2f297-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="2f297-106">Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="2f297-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="2f297-107">Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]</span><span class="sxs-lookup"><span data-stu-id="2f297-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="2f297-108">La méthode **Sign** crée une signature numérique Authenticode et signe le fichier exécutable spécifié dans la propriété [**SignedCode. FileName**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="2f297-108">The **Sign** method creates an Authenticode digital signature and signs the executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f297-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f297-109">Syntax</span></span>


```VB
SignedCode.Sign( _
  [ ByVal Signer ] _
)
```



## <a name="parameters"></a><span data-ttu-id="2f297-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f297-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f297-111">*Signataire* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="2f297-111">*Signer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2f297-112">Objet [**signataire**](signer.md) qui a accès à la clé privée du certificat utilisé pour signer le code.</span><span class="sxs-lookup"><span data-stu-id="2f297-112">A [**Signer**](signer.md) object that has access to the private key of the certificate used to sign the code.</span></span> <span data-ttu-id="2f297-113">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="2f297-113">The default value is **Null**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f297-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2f297-114">Return value</span></span>

<span data-ttu-id="2f297-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2f297-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f297-116">Notes</span><span class="sxs-lookup"><span data-stu-id="2f297-116">Remarks</span></span>

<span data-ttu-id="2f297-117">Avant l’appel de la méthode **Sign** , le fichier qui contient le code doit être spécifié dans la propriété [**filename**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="2f297-117">Before the **Sign** method is called, the file that contains the code must be specified in the [**FileName**](signedcode-filename.md) property.</span></span>

<span data-ttu-id="2f297-118">Si le fichier exécutable est déjà signé, cette méthode remplace la signature existante.</span><span class="sxs-lookup"><span data-stu-id="2f297-118">If the executable file is already signed, this method overwrites the existing signature.</span></span>

<span data-ttu-id="2f297-119">Les résultats suivants s’appliquent à la valeur du paramètre de *signataire* :</span><span class="sxs-lookup"><span data-stu-id="2f297-119">The following results apply to the *Signer* parameter value:</span></span>

-   <span data-ttu-id="2f297-120">Si le paramètre de *signataire* n’a pas la **valeur null**, cette méthode utilise la clé privée désignée par le certificat associé pour chiffrer la signature.</span><span class="sxs-lookup"><span data-stu-id="2f297-120">If the *Signer* parameter is not **NULL**, this method uses the private key pointed to by the associated certificate to encrypt the signature.</span></span> <span data-ttu-id="2f297-121">Si la clé privée vers laquelle pointe le certificat n’est pas disponible, la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="2f297-121">If the private key pointed to by the certificate is not available, the method fails.</span></span>
-   <span data-ttu-id="2f297-122">Si le paramètre de *signataire* a la **valeur null** et qu’il y a exactement un certificat dans l' \_ utilisateur actuel mon magasin qui a accès à une clé privée avec la fonctionnalité de signature de code, ce certificat est utilisé pour créer la signature.</span><span class="sxs-lookup"><span data-stu-id="2f297-122">If the *Signer* parameter is **NULL** and there is exactly one certificate in the CURRENT\_USER MY store that has access to a private key with code signing capability, that certificate is used to create the signature.</span></span>
-   <span data-ttu-id="2f297-123">Si le paramètre de *signataire* est **null**, la valeur de la propriété [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) est true et il existe plusieurs certificats dans le magasin de l' \_ utilisateur actuel mon magasin avec une clé privée disponible avec la fonctionnalité de signature de code, une boîte de dialogue s’affiche et permet à l’utilisateur de sélectionner le certificat à utiliser.</span><span class="sxs-lookup"><span data-stu-id="2f297-123">If the *Signer* parameter is **NULL**, the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property value is true, and there is more than one certificate in the CURRENT\_USER MY store with an available private key with code signing capability, a dialog box appears that allows the user to select which certificate is used.</span></span>
-   <span data-ttu-id="2f297-124">Si le paramètre de *signataire* a la **valeur null** et que la propriété [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) a la valeur false, la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="2f297-124">If the *Signer* parameter is **NULL** and the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property is false, the method fails.</span></span>
-   <span data-ttu-id="2f297-125">Si le paramètre de *signataire* a la **valeur null** et qu’il n’existe aucun certificat dans le magasin de l' \_ utilisateur actuel avec une clé privée disponible avec la fonction de signature de code, la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="2f297-125">If the *Signer* parameter is **NULL** and there are no certificates in the CURRENT\_USER MY store with an available private key with code signing capability, the method fails.</span></span>

<span data-ttu-id="2f297-126">Cette méthode utilise l’algorithme de hachage SHA-1.</span><span class="sxs-lookup"><span data-stu-id="2f297-126">This method uses the SHA-1 hashing algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f297-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f297-127">Requirements</span></span>



| <span data-ttu-id="2f297-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f297-128">Requirement</span></span> | <span data-ttu-id="2f297-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f297-129">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f297-130">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="2f297-130">Redistributable</span></span><br/> | <span data-ttu-id="2f297-131">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="2f297-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2f297-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2f297-132">DLL</span></span><br/>             | <dl> <span data-ttu-id="2f297-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f297-133"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
