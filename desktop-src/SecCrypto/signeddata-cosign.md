---
description: Crée une signature numérique sur le contenu précédemment signé.
ms.assetid: c0a3de75-afba-45ba-b701-2729f4495eda
title: SignedData. cosign, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.CoSign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1ab2a24a20fd65fad9622b775bedc59cfa28301a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533465"
---
# <a name="signeddatacosign-method"></a><span data-ttu-id="f55a4-103">SignedData. cosign, méthode</span><span class="sxs-lookup"><span data-stu-id="f55a4-103">SignedData.CoSign method</span></span>

<span data-ttu-id="f55a4-104">\[La méthode de **cosignature** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="f55a4-104">\[The **CoSign** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f55a4-105">Utilisez plutôt la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="f55a4-105">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="f55a4-106">La méthode **cosign** crée une [*signature numérique*](../secgloss/d-gly.md) sur le contenu précédemment signé.</span><span class="sxs-lookup"><span data-stu-id="f55a4-106">The **CoSign** method creates a [*digital signature*](../secgloss/d-gly.md) on previously signed content.</span></span>

## <a name="syntax"></a><span data-ttu-id="f55a4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f55a4-107">Syntax</span></span>


```VB
SignedData.CoSign( _
  [ ByVal Signer ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f55a4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f55a4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f55a4-109">*Signataire* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f55a4-109">*Signer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f55a4-110">Référence à l’objet [**signataire**](signer.md) du signataire des données.</span><span class="sxs-lookup"><span data-stu-id="f55a4-110">A reference to the [**Signer**](signer.md) object of the signer of the data.</span></span> <span data-ttu-id="f55a4-111">L’objet **signataire** doit avoir accès à la clé privée du certificat utilisé pour la signature.</span><span class="sxs-lookup"><span data-stu-id="f55a4-111">The **Signer** object must have access to the private key of the certificate used to sign.</span></span> <span data-ttu-id="f55a4-112">Ce paramètre peut avoir la **valeur null**; Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="f55a4-112">This parameter can be **NULL**; for more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f55a4-113">*EncodingType* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f55a4-113">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f55a4-114">Valeur de l’énumération de [**\_ \_ type d’encodage**](capicom-encoding-type.md) CAPICOM qui indique comment les données signées doivent être encodées.</span><span class="sxs-lookup"><span data-stu-id="f55a4-114">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates how the signed data is to be encoded.</span></span> <span data-ttu-id="f55a4-115">La valeur par défaut est CAPICOM \_ encode \_ Base64.</span><span class="sxs-lookup"><span data-stu-id="f55a4-115">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="f55a4-116">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f55a4-116">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="f55a4-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f55a4-117">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="f55a4-118">Signification</span><span class="sxs-lookup"><span data-stu-id="f55a4-118">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="f55a4-119"><dt>**\_coder \_ tout**</dt></span><span class="sxs-lookup"><span data-stu-id="f55a4-119"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="f55a4-120">Ce type d’encodage est utilisé uniquement lorsque les données d’entrée ont un type d’encodage inconnu.</span><span class="sxs-lookup"><span data-stu-id="f55a4-120">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="f55a4-121">Si cette valeur est utilisée pour spécifier le type d’encodage de la sortie, CAPICOM est utilisé à la \_ \_ place.</span><span class="sxs-lookup"><span data-stu-id="f55a4-121">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="f55a4-122">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="f55a4-122">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="f55a4-123"><dt>**\_Encode \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="f55a4-123"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="f55a4-124">Les données sont enregistrées sous la forme d’une chaîne encodée en base64.</span><span class="sxs-lookup"><span data-stu-id="f55a4-124">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="f55a4-125"><dt>**codage d’un \_ \_ fichier binaire CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="f55a4-125"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="f55a4-126">Les données sont enregistrées sous la forme d’une séquence binaire pure.</span><span class="sxs-lookup"><span data-stu-id="f55a4-126">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f55a4-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f55a4-127">Return value</span></span>

<span data-ttu-id="f55a4-128">Cette méthode retourne une chaîne qui contient les données signées et encodées.</span><span class="sxs-lookup"><span data-stu-id="f55a4-128">This method returns a string that contains the encoded, signed data.</span></span>

<span data-ttu-id="f55a4-129">Si cette méthode échoue, une erreur est levée.</span><span class="sxs-lookup"><span data-stu-id="f55a4-129">If this method fails, an error will be thrown.</span></span> <span data-ttu-id="f55a4-130">L’objet **Err** contient des informations supplémentaires sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="f55a4-130">The **Err** object will contain additional information about the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="f55a4-131">Notes</span><span class="sxs-lookup"><span data-stu-id="f55a4-131">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f55a4-132">Lorsque cette méthode est appelée à partir d’un script Web, le script doit utiliser votre [*clé privée*](../secgloss/p-gly.md) pour créer une signature numérique.</span><span class="sxs-lookup"><span data-stu-id="f55a4-132">When this method is called from a web script, the script needs to use your [*private key*](../secgloss/p-gly.md) to create a digital signature.</span></span> <span data-ttu-id="f55a4-133">Autoriser les sites Web non approuvés à utiliser votre clé privée est un risque pour la sécurité.</span><span class="sxs-lookup"><span data-stu-id="f55a4-133">Allowing untrusted websites to use your private key is a security risk.</span></span> <span data-ttu-id="f55a4-134">Une boîte de dialogue qui vous demande si le site Web peut utiliser votre clé privée s’affiche lorsque cette méthode est appelée pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="f55a4-134">A dialog box that asks whether the website can use your private key appears when this method is first called.</span></span> <span data-ttu-id="f55a4-135">Si vous autorisez le script à utiliser votre clé privée pour créer une signature numérique et que vous sélectionnez ne plus afficher cette boîte de dialogue, la boîte de dialogue n’apparaît plus pour les scripts de ce domaine qui utilisent votre clé privée pour créer une signature numérique.</span><span class="sxs-lookup"><span data-stu-id="f55a4-135">If you allow the script to use your private key to create a digital signature and select "Do not show this dialog box again," the dialog box will no longer appear for any script within that domain that uses your private key to create a digital signature.</span></span> <span data-ttu-id="f55a4-136">Toutefois, les scripts en dehors de ce domaine qui tentent d’utiliser votre clé privée pour créer une signature numérique entraînent toujours l’affichage de cette boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f55a4-136">However, scripts outside that domain that attempt to use your private key to create a digital signature will still cause this dialog box to appear.</span></span> <span data-ttu-id="f55a4-137">Si vous n’autorisez pas le script à utiliser votre clé privée et que vous sélectionnez ne plus afficher cette boîte de dialogue, les scripts de ce domaine se verront automatiquement refuser la possibilité d’utiliser votre clé privée pour créer des signatures numériques.</span><span class="sxs-lookup"><span data-stu-id="f55a4-137">If you do not allow the script to use your private key and select "Do not show this dialog box again," scripts within that domain will automatically be refused the ability to use your private key to create digital signatures.</span></span>

 

<span data-ttu-id="f55a4-138">Il n’est pas garanti que les cosignataires soient dans un ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="f55a4-138">Cosigners are not guaranteed to be in any particular order.</span></span>

<span data-ttu-id="f55a4-139">Les résultats suivants s’appliquent à la valeur du paramètre de *signataire* :</span><span class="sxs-lookup"><span data-stu-id="f55a4-139">The following results apply to the *Signer* parameter value:</span></span>

-   <span data-ttu-id="f55a4-140">Si le paramètre de *signataire* n’a pas la **valeur null**, cette méthode utilise la clé privée désignée par le certificat associé pour chiffrer la cosignature.</span><span class="sxs-lookup"><span data-stu-id="f55a4-140">If the *Signer* parameter is not **NULL**, this method uses the private key pointed to by the associated certificate to encrypt the cosignature.</span></span> <span data-ttu-id="f55a4-141">Si la clé privée vers laquelle pointe le certificat n’est pas disponible, la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="f55a4-141">If the private key pointed to by the certificate is not available, the method fails.</span></span>
-   <span data-ttu-id="f55a4-142">Si le paramètre de *signataire* a la **valeur null** et qu’il y a exactement un certificat dans l' \_ utilisateur actuel mon magasin qui a accès à une clé privée, ce certificat est utilisé pour créer la cosignature.</span><span class="sxs-lookup"><span data-stu-id="f55a4-142">If the *Signer* parameter is **NULL** and there is exactly one certificate in the CURRENT\_USER MY store that has access to a private key, that certificate is used to create the cosignature.</span></span>
-   <span data-ttu-id="f55a4-143">Si le paramètre du *signataire* a la valeur **null**, la valeur de la propriété [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) est true et qu’il y a plusieurs certificats dans le magasin de l' \_ utilisateur actuel mon magasin avec une clé privée disponible, une boîte de dialogue s’affiche et permet à l’utilisateur de sélectionner le certificat à utiliser.</span><span class="sxs-lookup"><span data-stu-id="f55a4-143">If the *Signer* parameter is **NULL**, the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property value is true, and there is more than one certificate in the CURRENT\_USER MY store with an available private key, a dialog box appears that allows the user to select which certificate is used.</span></span>
-   <span data-ttu-id="f55a4-144">Si le paramètre de *signataire* a la **valeur null** et que la propriété [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) a la valeur false, la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="f55a4-144">If the *Signer* parameter is **NULL** and the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property is false, the method fails.</span></span>
-   <span data-ttu-id="f55a4-145">Si le paramètre de *signataire* a la **valeur null** et qu’il n’existe aucun certificat dans le magasin de l' \_ utilisateur actuel avec une clé privée disponible, la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="f55a4-145">If the *Signer* parameter is **NULL** and there is no certificate in the CURRENT\_USER MY store with an available private key, the method fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="f55a4-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f55a4-146">Requirements</span></span>



| <span data-ttu-id="f55a4-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f55a4-147">Requirement</span></span> | <span data-ttu-id="f55a4-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="f55a4-148">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f55a4-149">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="f55a4-149">Redistributable</span></span><br/> | <span data-ttu-id="f55a4-150">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="f55a4-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f55a4-151">DLL</span><span class="sxs-lookup"><span data-stu-id="f55a4-151">DLL</span></span><br/>             | <dl> <span data-ttu-id="f55a4-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f55a4-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f55a4-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f55a4-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f55a4-154">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="f55a4-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="f55a4-155">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="f55a4-155">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
