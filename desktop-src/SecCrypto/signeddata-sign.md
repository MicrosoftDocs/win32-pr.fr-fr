---
description: Crée une signature numérique sur le contenu à signer. Une signature numérique se compose d’un hachage du contenu à signer qui est chiffré à l’aide de la clé privée du signataire.
ms.assetid: ee98a36c-f9a9-4247-ae48-7b1a10b92be4
title: SignedData. Sign, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9f885bb110b51264bc6108ca8c0f881cc48f7710
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532939"
---
# <a name="signeddatasign-method"></a><span data-ttu-id="a2919-104">SignedData. Sign, méthode</span><span class="sxs-lookup"><span data-stu-id="a2919-104">SignedData.Sign method</span></span>

<span data-ttu-id="a2919-105">\[La méthode **Sign** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="a2919-105">\[The **Sign** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a2919-106">Utilisez plutôt la [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="a2919-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="a2919-107">La méthode **Sign** crée une [*signature numérique*](../secgloss/d-gly.md) sur le contenu à signer.</span><span class="sxs-lookup"><span data-stu-id="a2919-107">The **Sign** method creates a [*digital signature*](../secgloss/d-gly.md) on the content to be signed.</span></span> <span data-ttu-id="a2919-108">Une signature numérique se compose d’un [*hachage*](../secgloss/h-gly.md) du contenu à signer qui est chiffré à l’aide de la clé privée du signataire.</span><span class="sxs-lookup"><span data-stu-id="a2919-108">A digital signature consists of a [*hash*](../secgloss/h-gly.md) of the content to be signed that is encrypted by using the private key of the signer.</span></span> <span data-ttu-id="a2919-109">Cette méthode ne peut être utilisée qu’une fois que la propriété [**SignedData. Content**](signeddata-content.md) a été initialisée.</span><span class="sxs-lookup"><span data-stu-id="a2919-109">This method can only be used after the [**SignedData.Content**](signeddata-content.md) property has been initialized.</span></span> <span data-ttu-id="a2919-110">Si la méthode **Sign** est appelée sur un objet qui a déjà une signature, l’ancienne signature est remplacée.</span><span class="sxs-lookup"><span data-stu-id="a2919-110">If the **Sign** method is called on an object that already has a signature, the old signature is replaced.</span></span> <span data-ttu-id="a2919-111">La signature est créée à l’aide de l’algorithme de signature SHA1.</span><span class="sxs-lookup"><span data-stu-id="a2919-111">The signature is created by using the SHA1 signing algorithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2919-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2919-112">Syntax</span></span>


```VB
SignedData.Sign( _
  [ ByVal Signer ], _
  [ ByVal bDetached ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a2919-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2919-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2919-114">*Signataire* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="a2919-114">*Signer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a2919-115">Référence à l’objet [**signataire**](signer.md) du signataire des données.</span><span class="sxs-lookup"><span data-stu-id="a2919-115">A reference to the [**Signer**](signer.md) object of the signer of the data.</span></span> <span data-ttu-id="a2919-116">L’objet **signataire** doit avoir accès à la [*clé privée*](../secgloss/p-gly.md) du [*certificat*](../secgloss/c-gly.md) utilisé pour la signature.</span><span class="sxs-lookup"><span data-stu-id="a2919-116">The **Signer** object must have access to the [*private key*](../secgloss/p-gly.md) of the [*certificate*](../secgloss/c-gly.md) used to sign.</span></span> <span data-ttu-id="a2919-117">Ce paramètre peut avoir la **valeur null**; Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="a2919-117">This parameter can be **NULL**; for more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a2919-118">*bDetached* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="a2919-118">*bDetached* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a2919-119">Si la **valeur est true**, les données à signer sont détachées ; autrement dit, le contenu signé n’est pas inclus dans l’objet signé.</span><span class="sxs-lookup"><span data-stu-id="a2919-119">If **True**, the data to be signed is detached; that is, the content that is signed is not included as part of the signed object.</span></span> <span data-ttu-id="a2919-120">Pour vérifier la signature sur du contenu détaché, une application doit avoir une copie du contenu d’origine.</span><span class="sxs-lookup"><span data-stu-id="a2919-120">To verify the signature on detached content, an application must have a copy of the original content.</span></span> <span data-ttu-id="a2919-121">Le contenu détaché est souvent utilisé pour réduire la taille d’un objet signé à envoyer sur le Web, si le destinataire du message signé contient une copie originale des données signées.</span><span class="sxs-lookup"><span data-stu-id="a2919-121">Detached content is often used to decrease the size of a signed object to be sent across the web, if the recipient of the signed message has an original copy of the signed data.</span></span> <span data-ttu-id="a2919-122">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="a2919-122">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="a2919-123">*EncodingType* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="a2919-123">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a2919-124">Valeur de l’énumération de [ \_ \_ type d’encodage](capicom-encoding-type.md) CAPICOM qui indique comment les données signées doivent être encodées.</span><span class="sxs-lookup"><span data-stu-id="a2919-124">A value of the [CAPICOM\_ENCODING\_TYPE](capicom-encoding-type.md) enumeration that indicates how the signed data is to be encoded.</span></span> <span data-ttu-id="a2919-125">La valeur par défaut est CAPICOM \_ encode \_ Base64.</span><span class="sxs-lookup"><span data-stu-id="a2919-125">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="a2919-126">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a2919-126">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="a2919-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2919-127">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="a2919-128">Signification</span><span class="sxs-lookup"><span data-stu-id="a2919-128">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="a2919-129"><dt>**\_coder \_ tout**</dt></span><span class="sxs-lookup"><span data-stu-id="a2919-129"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="a2919-130">Ce type d’encodage est utilisé uniquement lorsque les données d’entrée ont un type d’encodage inconnu.</span><span class="sxs-lookup"><span data-stu-id="a2919-130">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="a2919-131">Si cette valeur est utilisée pour spécifier le type d’encodage de la sortie, CAPICOM est utilisé à la \_ \_ place.</span><span class="sxs-lookup"><span data-stu-id="a2919-131">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="a2919-132">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="a2919-132">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="a2919-133"><dt>**\_Encode \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="a2919-133"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="a2919-134">Les données sont enregistrées sous la forme d’une chaîne encodée en base64.</span><span class="sxs-lookup"><span data-stu-id="a2919-134">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="a2919-135"><dt>**codage d’un \_ \_ fichier binaire CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="a2919-135"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="a2919-136">Les données sont enregistrées sous la forme d’une séquence binaire pure.</span><span class="sxs-lookup"><span data-stu-id="a2919-136">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2919-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a2919-137">Return value</span></span>

<span data-ttu-id="a2919-138">Cette méthode retourne une chaîne qui contient les données signées et encodées.</span><span class="sxs-lookup"><span data-stu-id="a2919-138">This method returns a string that contains the encoded, signed data.</span></span>

<span data-ttu-id="a2919-139">Si cette méthode échoue, une erreur est levée.</span><span class="sxs-lookup"><span data-stu-id="a2919-139">If this method fails, an error will be thrown.</span></span> <span data-ttu-id="a2919-140">L’objet **Err** contient des informations supplémentaires sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="a2919-140">The **Err** object will contain additional information about the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2919-141">Notes</span><span class="sxs-lookup"><span data-stu-id="a2919-141">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a2919-142">Lorsque cette méthode est appelée à partir d’un script Web, le script doit utiliser votre clé privée pour créer une signature numérique.</span><span class="sxs-lookup"><span data-stu-id="a2919-142">When this method is called from a web script, the script needs to use your private key to create a digital signature.</span></span> <span data-ttu-id="a2919-143">Autoriser les sites Web non approuvés à utiliser votre clé privée est un risque pour la sécurité.</span><span class="sxs-lookup"><span data-stu-id="a2919-143">Allowing untrusted websites to use your private key is a security risk.</span></span> <span data-ttu-id="a2919-144">Une boîte de dialogue qui vous demande si le site Web peut utiliser votre clé privée s’affiche lorsque cette méthode est appelée pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="a2919-144">A dialog box that asks whether the website can use your private key appears when this method is first called.</span></span> <span data-ttu-id="a2919-145">Si vous autorisez le script à utiliser votre clé privée pour créer une signature numérique et que vous sélectionnez ne plus afficher cette boîte de dialogue, la boîte de dialogue n’apparaît plus pour les scripts de ce domaine qui utilisent votre clé privée pour créer une signature numérique.</span><span class="sxs-lookup"><span data-stu-id="a2919-145">If you allow the script to use your private key to create a digital signature and select "Do not show this dialog box again," the dialog box will no longer appear for any script within that domain that uses your private key to create a digital signature.</span></span> <span data-ttu-id="a2919-146">Toutefois, les scripts en dehors de ce domaine qui tentent d’utiliser votre clé privée pour créer une signature numérique entraînent toujours l’affichage de cette boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="a2919-146">However, scripts outside that domain that attempt to use your private key to create a digital signature will still cause this dialog box to appear.</span></span> <span data-ttu-id="a2919-147">Si vous n’autorisez pas le script à utiliser votre clé privée et que vous sélectionnez ne plus afficher cette boîte de dialogue, les scripts de ce domaine se verront automatiquement refuser la possibilité d’utiliser votre clé privée pour créer des signatures numériques.</span><span class="sxs-lookup"><span data-stu-id="a2919-147">If you do not allow the script to use your private key and select "Do not show this dialog box again," scripts within that domain will automatically be refused the ability to use your private key to create digital signatures.</span></span>

 

<span data-ttu-id="a2919-148">Étant donné que la création d’une [*signature numérique*](../secgloss/d-gly.md) requiert l’utilisation d’une [*clé privée*](../secgloss/p-gly.md), les applications Web qui essaient d’utiliser cette méthode nécessitent des invites d’interface utilisateur qui permettent à l’utilisateur d’approuver l’utilisation de la clé privée, pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a2919-148">Because creating a [*digital signature*](../secgloss/d-gly.md) requires the use of a [*private key*](../secgloss/p-gly.md), web-based applications that attempt to use this method will require user interface prompts that allow the user to approve the use of the private key, for security reasons.</span></span>

<span data-ttu-id="a2919-149">Les résultats suivants s’appliquent à la valeur du paramètre de *signataire* :</span><span class="sxs-lookup"><span data-stu-id="a2919-149">The following results apply to the *Signer* parameter value:</span></span>

-   <span data-ttu-id="a2919-150">Si le paramètre de *signataire* n’a pas la **valeur null**, cette méthode utilise la clé privée désignée par le certificat associé pour chiffrer la signature.</span><span class="sxs-lookup"><span data-stu-id="a2919-150">If the *Signer* parameter is not **NULL**, this method uses the private key pointed to by the associated certificate to encrypt the signature.</span></span> <span data-ttu-id="a2919-151">Si la clé privée vers laquelle pointe le certificat n’est pas disponible, la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="a2919-151">If the private key pointed to by the certificate is not available, the method fails.</span></span>
-   <span data-ttu-id="a2919-152">Si le paramètre de *signataire* a la **valeur null** et qu’il y a exactement un certificat dans l' \_ utilisateur actuel mon magasin qui a accès à une clé privée, ce certificat est utilisé pour créer la signature.</span><span class="sxs-lookup"><span data-stu-id="a2919-152">If the *Signer* parameter is **NULL** and there is exactly one certificate in the CURRENT\_USER MY store that has access to a private key, that certificate is used to create the signature.</span></span>
-   <span data-ttu-id="a2919-153">Si le paramètre du *signataire* a la valeur **null**, la valeur de la propriété [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) est true et qu’il y a plusieurs certificats dans le magasin de l' \_ utilisateur actuel mon magasin avec une clé privée disponible, une boîte de dialogue s’affiche et permet à l’utilisateur de sélectionner le certificat à utiliser.</span><span class="sxs-lookup"><span data-stu-id="a2919-153">If the *Signer* parameter is **NULL**, the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property value is true, and there is more than one certificate in the CURRENT\_USER MY store with an available private key, a dialog box appears that allows the user to select which certificate is used.</span></span>
-   <span data-ttu-id="a2919-154">Si le paramètre de *signataire* a la **valeur null** et que la propriété [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) a la valeur false, la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="a2919-154">If the *Signer* parameter is **NULL** and the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property is false, the method fails.</span></span>
-   <span data-ttu-id="a2919-155">Si le paramètre de *signataire* a la **valeur null** et qu’il n’existe aucun certificat dans le magasin de l' \_ utilisateur actuel avec une clé privée disponible, la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="a2919-155">If the *Signer* parameter is **NULL** and there is no certificate in the CURRENT\_USER MY store with an available private key, the method fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2919-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2919-156">Requirements</span></span>



| <span data-ttu-id="a2919-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2919-157">Requirement</span></span> | <span data-ttu-id="a2919-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2919-158">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2919-159">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a2919-159">Redistributable</span></span><br/> | <span data-ttu-id="a2919-160">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="a2919-160">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a2919-161">DLL</span><span class="sxs-lookup"><span data-stu-id="a2919-161">DLL</span></span><br/>             | <dl> <span data-ttu-id="a2919-162"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2919-162"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2919-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2919-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2919-164">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="a2919-164">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="a2919-165">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="a2919-165">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
