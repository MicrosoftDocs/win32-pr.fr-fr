---
title: Comment signer un package d’application à l’aide de SignTool
description: Découvrez comment utiliser SignTool pour signer vos packages d’application Windows pour qu’ils puissent être déployés.
ms.assetid: 93541EB4-3419-45D1-AA63-563E6C6D3055
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f1abfdf0e43fb4d87dbf892f30c2a3ba63e775
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "106511105"
---
# <a name="how-to-sign-an-app-package-using-signtool"></a><span data-ttu-id="b16b4-103">Comment signer un package d’application à l’aide de SignTool</span><span class="sxs-lookup"><span data-stu-id="b16b4-103">How to sign an app package using SignTool</span></span>

> [!Note]  
> <span data-ttu-id="b16b4-104">Pour signer un package d’application Windows, consultez [signer un package d’application à l’aide de SignTool](/windows/msix/package/sign-app-package-using-signtool).</span><span class="sxs-lookup"><span data-stu-id="b16b4-104">For signing a Windows app package, see [Sign an app package using SignTool](/windows/msix/package/sign-app-package-using-signtool).</span></span>

 

<span data-ttu-id="b16b4-105">Découvrez comment utiliser [**SignTool**](/windows-hardware/drivers/devtest/signtool) pour signer vos packages d’application Windows pour qu’ils puissent être déployés.</span><span class="sxs-lookup"><span data-stu-id="b16b4-105">Learn how to use [**SignTool**](/windows-hardware/drivers/devtest/signtool) to sign your Windows app packages so they can be deployed.</span></span> <span data-ttu-id="b16b4-106">[**SignTool**](/windows-hardware/drivers/devtest/signtool) fait partie du kit de développement logiciel (SDK) Windows.</span><span class="sxs-lookup"><span data-stu-id="b16b4-106">[**SignTool**](/windows-hardware/drivers/devtest/signtool) is part of the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="b16b4-107">Tous les packages d’application Windows doivent être signés numériquement avant de pouvoir être déployés.</span><span class="sxs-lookup"><span data-stu-id="b16b4-107">All Windows app packages must be digitally signed before they can be deployed.</span></span> <span data-ttu-id="b16b4-108">Alors que Microsoft Visual Studio 2012 et versions ultérieures peuvent signer un package d’application lors de sa création, les packages que vous créez à l’aide de l’outil [app Packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) de la SDK Windows ne sont pas signés.</span><span class="sxs-lookup"><span data-stu-id="b16b4-108">While Microsoft Visual Studio 2012 and later can sign an app package during its creation, packages that you create by using the [app packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) tool from the Windows SDK aren't signed.</span></span>

> [!Note]  
> <span data-ttu-id="b16b4-109">Vous pouvez utiliser uniquement [**SignTool**](/windows-hardware/drivers/devtest/signtool) pour signer vos packages d’application Windows sur Windows 8 et versions ultérieures, ou windows server 2012 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b16b4-109">You can only use [**SignTool**](/windows-hardware/drivers/devtest/signtool) to sign your Windows app packages on Windows 8 and later or Windows Server 2012 and later.</span></span> <span data-ttu-id="b16b4-110">Vous ne pouvez pas utiliser **SignTool** pour signer des packages d’application sur des systèmes d’exploitation de niveau supérieur tels que Windows 7 ou windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="b16b4-110">You can't use **SignTool** to sign app packages on down-level operating systems such as Windows 7 or Windows Server 2008 R2.</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="b16b4-111">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="b16b4-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="b16b4-112">Technologies</span><span class="sxs-lookup"><span data-stu-id="b16b4-112">Technologies</span></span>

-   <span data-ttu-id="b16b4-113">[Présentation de la signature de code](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b16b4-113">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
-   <span data-ttu-id="b16b4-114">[Packages d’applications et déploiement](/previous-versions/windows/apps/hh464929(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="b16b4-114">[App packages and deployment](/previous-versions/windows/apps/hh464929(v=win.10))</span></span>
-   [<span data-ttu-id="b16b4-115">Outils pour signer des fichiers et vérifier les signatures</span><span class="sxs-lookup"><span data-stu-id="b16b4-115">Tools to Sign Files and Check Signatures</span></span>](/windows/desktop/SecCrypto/tools-to-sign-files-and-check-signatures)

### <a name="prerequisites"></a><span data-ttu-id="b16b4-116">Prérequis</span><span class="sxs-lookup"><span data-stu-id="b16b4-116">Prerequisites</span></span>

-   <span data-ttu-id="b16b4-117">[**SignTool**](/windows-hardware/drivers/devtest/signtool), qui fait partie de l’SDK Windows</span><span class="sxs-lookup"><span data-stu-id="b16b4-117">[**SignTool**](/windows-hardware/drivers/devtest/signtool), which is part of the Windows SDK</span></span>
-   <span data-ttu-id="b16b4-118">Un certificat de signature de code valide, par exemple, un fichier d’échange d’informations personnelles (. pfx) créé avec les outils [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) et [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx)</span><span class="sxs-lookup"><span data-stu-id="b16b4-118">A valid code signing certificate, for example, a Personal Information Exchange (.pfx) file created with the [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) tools</span></span>

    <span data-ttu-id="b16b4-119">Pour plus d’informations sur la création d’un certificat de signature de code valide, consultez [comment créer un certificat de signature de package d’application](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="b16b4-119">For info about creating a valid code signing certificate, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>

-   <span data-ttu-id="b16b4-120">Une application Windows empaquetée, par exemple, un fichier. AppX créé à l’aide de l’outil [app Packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md)</span><span class="sxs-lookup"><span data-stu-id="b16b4-120">A packaged Windows app, for example, an .appx file created by using the [app packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) tool</span></span>

<span data-ttu-id="b16b4-121">**Considérations supplémentaires**</span><span class="sxs-lookup"><span data-stu-id="b16b4-121">**Additional considerations**</span></span>

<span data-ttu-id="b16b4-122">Le certificat que vous utilisez pour signer le package d’application doit respecter les critères suivants :</span><span class="sxs-lookup"><span data-stu-id="b16b4-122">The certificate that you use to sign the app package must meet these criteria:</span></span>

-   <span data-ttu-id="b16b4-123">Le nom du sujet du certificat doit correspondre à l’attribut du serveur de **publication** contenu dans l’élément [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) du fichier AppxManifest.xml stocké dans le package.</span><span class="sxs-lookup"><span data-stu-id="b16b4-123">The subject name of the certificate must match the **Publisher** attribute that is contained in the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element of the AppxManifest.xml file that is stored within the package.</span></span> <span data-ttu-id="b16b4-124">Le nom de l’éditeur faisant partie de l’identité d’une application Windows empaquetée, vous devez faire en sorte que le nom du sujet du certificat corresponde au nom de l’éditeur de l’application.</span><span class="sxs-lookup"><span data-stu-id="b16b4-124">The publisher name is part of the identity of a packaged Windows app, so you have to make the subject name of the certificate match the publisher name of the app.</span></span> <span data-ttu-id="b16b4-125">Cela permet de vérifier l’identité des packages signés par rapport à la signature numérique.</span><span class="sxs-lookup"><span data-stu-id="b16b4-125">This allows the identity of signed packages to be checked against the digital signature.</span></span> <span data-ttu-id="b16b4-126">Pour plus d’informations sur la signature des erreurs susceptibles de se produire lors de la signature d’un package d’application à l’aide de [**SignTool**](/windows-hardware/drivers/devtest/signtool), consultez la section Notes de la rubrique [comment créer un certificat de signature de package d’application](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="b16b4-126">For info about signing errors that can arise from signing an app package using [**SignTool**](/windows-hardware/drivers/devtest/signtool), see the Remarks section of [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>
-   <span data-ttu-id="b16b4-127">Le certificat doit être valide pour la signature de code.</span><span class="sxs-lookup"><span data-stu-id="b16b4-127">The certificate must be valid for code signing.</span></span> <span data-ttu-id="b16b4-128">Cela signifie que ces deux éléments doivent être vrais :</span><span class="sxs-lookup"><span data-stu-id="b16b4-128">This means that both of these items must be true:</span></span>

    -   <span data-ttu-id="b16b4-129">Le champ utilisation améliorée de la clé du certificat doit être désactivé ou contenir la valeur EKU pour la signature de code (1.3.6.1.5.5.7.3.3).</span><span class="sxs-lookup"><span data-stu-id="b16b4-129">The Extended Key Usage (EKU) field of the certificate must either be unset or contain the EKU value for code signing (1.3.6.1.5.5.7.3.3).</span></span>
    -   <span data-ttu-id="b16b4-130">Le champ utilisation de la clé (KU) du certificat doit être désactivé ou contenir le bit d’utilisation pour la signature numérique (0x80).</span><span class="sxs-lookup"><span data-stu-id="b16b4-130">The Key Usage (KU) field of the certificate must either be unset or contain the usage bit for digital signature (0x80).</span></span>

-   <span data-ttu-id="b16b4-131">Le certificat contient une clé privée.</span><span class="sxs-lookup"><span data-stu-id="b16b4-131">The certificate contains a private key.</span></span>
-   <span data-ttu-id="b16b4-132">Le certificat est valide.</span><span class="sxs-lookup"><span data-stu-id="b16b4-132">The certificate is valid.</span></span> <span data-ttu-id="b16b4-133">Il est actif, n’a pas expiré et n’a pas été révoqué.</span><span class="sxs-lookup"><span data-stu-id="b16b4-133">It is active, hasn't expired, and hasn't been revoked.</span></span>

## <a name="instructions"></a><span data-ttu-id="b16b4-134">Instructions</span><span class="sxs-lookup"><span data-stu-id="b16b4-134">Instructions</span></span>

### <a name="step-1-determine-the-hash-algorithm-to-use"></a><span data-ttu-id="b16b4-135">Étape 1 : déterminer l’algorithme de hachage à utiliser</span><span class="sxs-lookup"><span data-stu-id="b16b4-135">Step 1: Determine the hash algorithm to use</span></span>

<span data-ttu-id="b16b4-136">Lorsque vous signez le package d’application, vous devez utiliser le même algorithme de hachage que celui que vous avez utilisé lors de la création du package d’application.</span><span class="sxs-lookup"><span data-stu-id="b16b4-136">When you sign the app package, you must use the same hash algorithm that you used when you created the app package.</span></span> <span data-ttu-id="b16b4-137">Si vous avez utilisé les paramètres par défaut pour créer le package d’application, l’algorithme de hachage utilisé est SHA256.</span><span class="sxs-lookup"><span data-stu-id="b16b4-137">If you used default settings to create the app package, the hash algorithm used is SHA256.</span></span>

<span data-ttu-id="b16b4-138">Si vous avez utilisé App Packager avec un algorithme de hachage spécifique pour créer le package d’application, utilisez le même algorithme pour signer le package.</span><span class="sxs-lookup"><span data-stu-id="b16b4-138">If you used the app packager with a specific hash algorithm to create the app package, use the same algorithm to sign the package.</span></span> <span data-ttu-id="b16b4-139">Pour déterminer l’algorithme de hachage à utiliser pour la signature d’un package, vous pouvez extraire le contenu du package et inspecter le fichier AppxBlockMap.xml.</span><span class="sxs-lookup"><span data-stu-id="b16b4-139">To determine the hash algorithm to use for signing a package, you can extract the package contents and inspect the AppxBlockMap.xml file.</span></span> <span data-ttu-id="b16b4-140">L’attribut **HashMethod** de l’élément [**blockmap**](/uwp/schemas/blockmapschema/element-blockmap) indique l’algorithme de hachage qui a été utilisé lors de la création du package d’application.</span><span class="sxs-lookup"><span data-stu-id="b16b4-140">The **HashMethod** attribute of the [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) element indicates the hash algorithm that was used when creating the app package.</span></span> <span data-ttu-id="b16b4-141">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b16b4-141">For example:</span></span>

``` syntax
<BlockMap xmlns="http://schemas.microsoft.com/appx/2010/blockmap" 
HashMethod="https://www.w3.org/2001/04/xmlenc#sha256">
```

<span data-ttu-id="b16b4-142">L’élément [**blockmap**](/uwp/schemas/blockmapschema/element-blockmap) précédent indique que l’algorithme SHA256 a été utilisé.</span><span class="sxs-lookup"><span data-stu-id="b16b4-142">The preceding [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) element indicates that the SHA256 algorithm was used.</span></span> <span data-ttu-id="b16b4-143">Ce tableau répertorie le mappage des algorithmes actuellement disponibles :</span><span class="sxs-lookup"><span data-stu-id="b16b4-143">This table lists the mapping of the currently available algorithms:</span></span>

| <span data-ttu-id="b16b4-144">Valeur **HashMethod**</span><span class="sxs-lookup"><span data-stu-id="b16b4-144">**HashMethod** value</span></span>                            | <span data-ttu-id="b16b4-145">*HashAlgorithm* à utiliser</span><span class="sxs-lookup"><span data-stu-id="b16b4-145">*hashAlgorithm* to use</span></span> |
|-------------------------------------------------|------------------------|
| <https://www.w3.org/2001/04/xmlenc#sha256>       | <span data-ttu-id="b16b4-146">SHA256 (valeur par défaut. AppX)</span><span class="sxs-lookup"><span data-stu-id="b16b4-146">SHA256 (.appx default)</span></span> |
| <https://www.w3.org/2001/04/xmldsig-more#sha384> | <span data-ttu-id="b16b4-147">SHA384</span><span class="sxs-lookup"><span data-stu-id="b16b4-147">SHA384</span></span>                 |
| <https://www.w3.org/2001/04/xmlenc#sha512>       | <span data-ttu-id="b16b4-148">SHA512</span><span class="sxs-lookup"><span data-stu-id="b16b4-148">SHA512</span></span>                 |



 

### <a name="step-2-run-signtoolexe-to-sign-the-package"></a><span data-ttu-id="b16b4-149">Étape 2 : exécuter SignTool.exe pour signer le package</span><span class="sxs-lookup"><span data-stu-id="b16b4-149">Step 2: Run SignTool.exe to sign the package</span></span>

<span data-ttu-id="b16b4-150">**Pour signer le package avec un certificat de signature à partir d’un fichier. pfx**</span><span class="sxs-lookup"><span data-stu-id="b16b4-150">**To sign the package with a signing certificate from a .pfx file**</span></span>

-   ``` syntax
    SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password filepath.appx
    ```

<span data-ttu-id="b16b4-151">[**SignTool**](/windows-hardware/drivers/devtest/signtool) utilise par défaut le paramètre/FD *HashAlgorithm* sur SHA1 s’il n’est pas spécifié, et SHA1 n’est pas valide pour la signature des packages d’application.</span><span class="sxs-lookup"><span data-stu-id="b16b4-151">[**SignTool**](/windows-hardware/drivers/devtest/signtool) defaults the /fd *hashAlgorithm* parameter to SHA1 if it's not specified, and SHA1 isn't valid for signing app packages.</span></span> <span data-ttu-id="b16b4-152">Vous devez donc spécifier ce paramètre lorsque vous signez un package d’application.</span><span class="sxs-lookup"><span data-stu-id="b16b4-152">So, you must specify this parameter when you sign an app package.</span></span> <span data-ttu-id="b16b4-153">Pour signer un package d’application créé avec le hachage SHA256 par défaut, vous devez spécifier le paramètre/FD *HashAlgorithm* en tant que SHA256 :</span><span class="sxs-lookup"><span data-stu-id="b16b4-153">To sign an app package that was created with the default SHA256 hash, you specify the /fd *hashAlgorithm* parameter as SHA256:</span></span>

``` syntax
SignTool sign /fd SHA256 /a /f signingCert.pfx /p password filepath.appx
```

<span data-ttu-id="b16b4-154">Vous pouvez omettre le paramètre *de mot de passe* /p Si vous utilisez un fichier. pfx qui n’est pas protégé par un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="b16b4-154">You can omit the /p *password* parameter if you use a .pfx file that isn't password protected.</span></span> <span data-ttu-id="b16b4-155">Vous pouvez également utiliser d’autres options de sélection de certificat qui sont prises en charge par [**SignTool**](/windows-hardware/drivers/devtest/signtool) pour signer des packages d’application.</span><span class="sxs-lookup"><span data-stu-id="b16b4-155">You can also use other certificate selection options that are supported by [**SignTool**](/windows-hardware/drivers/devtest/signtool) to sign app packages.</span></span> <span data-ttu-id="b16b4-156">Pour plus d’informations sur ces options, consultez [SignTool](/windows/desktop/SecCrypto/signtool).</span><span class="sxs-lookup"><span data-stu-id="b16b4-156">For more info about these options, see [SignTool](/windows/desktop/SecCrypto/signtool).</span></span>

> [!Note]  
> <span data-ttu-id="b16b4-157">Vous ne pouvez pas utiliser l’opération d’horodatage [**SignTool**](/windows-hardware/drivers/devtest/signtool) sur un package d’application signé ; l’opération n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b16b4-157">You can't use the [**SignTool**](/windows-hardware/drivers/devtest/signtool) time stamp operation on a signed app package; the operation isn't supported.</span></span>

 

<span data-ttu-id="b16b4-158">Si vous souhaitez horodater le package de l’application, vous devez le faire pendant l’opération de signature.</span><span class="sxs-lookup"><span data-stu-id="b16b4-158">If you want to time stamp the app package, you must do it during the sign operation.</span></span> <span data-ttu-id="b16b4-159">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="b16b4-159">For example:</span></span>

``` syntax
SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password /tr timestampServerUrl 
filepath.appx
```

<span data-ttu-id="b16b4-160">Définissez le paramètre/TR *timestampServerUrl* sur l’URL d’un serveur de datage RFC 3161.</span><span class="sxs-lookup"><span data-stu-id="b16b4-160">Make the /tr *timestampServerUrl* parameter equal to the URL for an RFC 3161 time stamp server.</span></span>

## <a name="remarks"></a><span data-ttu-id="b16b4-161">Notes</span><span class="sxs-lookup"><span data-stu-id="b16b4-161">Remarks</span></span>

<span data-ttu-id="b16b4-162">Cette section traite de la résolution des erreurs de signature des packages d’application.</span><span class="sxs-lookup"><span data-stu-id="b16b4-162">This section discusses troubleshooting signing errors for app packages.</span></span>

### <a name="troubleshooting-app-package-signing-errors"></a><span data-ttu-id="b16b4-163">Résolution des erreurs de signature des packages d’application</span><span class="sxs-lookup"><span data-stu-id="b16b4-163">Troubleshooting app package signing errors</span></span>

<span data-ttu-id="b16b4-164">En plus des erreurs de signature que [**SignTool**](/windows-hardware/drivers/devtest/signtool) peut retourner, **SignTool** peut également retourner des erreurs spécifiques à la signature des packages d’application.</span><span class="sxs-lookup"><span data-stu-id="b16b4-164">In addition to the signing errors that [**SignTool**](/windows-hardware/drivers/devtest/signtool) can return, **SignTool** can also return errors that are specific to the signing of app packages.</span></span> <span data-ttu-id="b16b4-165">Ces erreurs apparaissent généralement sous la forme d’erreurs internes :</span><span class="sxs-lookup"><span data-stu-id="b16b4-165">These errors usually appear as internal errors:</span></span>

``` syntax
SignTool Error: An unexpected internal error has occurred.
Error information: "Error: SignerSign() failed." (-2147024885 / 0x8007000B) 
```

<span data-ttu-id="b16b4-166">Si le code d’erreur commence par 0x8008, tel que 0x80080206 \_ AppX \_ E \_ contenu endommagé), cela indique que le package en cours de signature n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="b16b4-166">If the error code starts with 0x8008, such as 0x80080206 APPX\_E\_CORRUPT\_CONTENT), it indicates that the package being signed is invalid.</span></span> <span data-ttu-id="b16b4-167">Dans ce cas, avant de pouvoir signer le package, vous devez régénérer le package.</span><span class="sxs-lookup"><span data-stu-id="b16b4-167">In this case, before you can sign the package, you must rebuild the package.</span></span> <span data-ttu-id="b16b4-168">Pour obtenir la liste complète des \* Erreurs 0x8008, consultez [**codes d’erreur com (sécurité et configuration)**](/windows/desktop/com/com-error-codes-4).</span><span class="sxs-lookup"><span data-stu-id="b16b4-168">For the full list of 0x8008\* errors, see [**COM Error Codes (Security and Setup)**](/windows/desktop/com/com-error-codes-4).</span></span>

<span data-ttu-id="b16b4-169">Plus généralement, l’erreur est 0x8007000b (format erroné de l’erreur \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="b16b4-169">More commonly, the error is 0x8007000b (ERROR\_BAD\_FORMAT).</span></span> <span data-ttu-id="b16b4-170">Dans ce cas, vous pouvez trouver des informations d’erreur plus spécifiques dans le journal des événements :</span><span class="sxs-lookup"><span data-stu-id="b16b4-170">In this case, you can find more specific error information in the event log:</span></span>

<span data-ttu-id="b16b4-171">**Pour rechercher dans le journal des événements**</span><span class="sxs-lookup"><span data-stu-id="b16b4-171">**To search the event log**</span></span>

1.  <span data-ttu-id="b16b4-172">Exécutez eventvwr. msc.</span><span class="sxs-lookup"><span data-stu-id="b16b4-172">Run Eventvwr.msc.</span></span>
2.  <span data-ttu-id="b16b4-173">Ouvrez le journal des événements : observateur d’événements (local) > les journaux des applications et des services > Microsoft > Windows > AppxPackagingOM > Microsoft-Windows-AppxPackaging/Operational</span><span class="sxs-lookup"><span data-stu-id="b16b4-173">Open the event log: Event Viewer (Local) > Applications and Services Logs > Microsoft > Windows > AppxPackagingOM > Microsoft-Windows-AppxPackaging/Operational</span></span>
3.  <span data-ttu-id="b16b4-174">Recherchez l’événement d’erreur le plus récent.</span><span class="sxs-lookup"><span data-stu-id="b16b4-174">Look for the most recent error event.</span></span>

<span data-ttu-id="b16b4-175">L’erreur interne correspond généralement à l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b16b4-175">The internal error usually corresponds to one of these:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b16b4-176">ID de l’événement</span><span class="sxs-lookup"><span data-stu-id="b16b4-176">Event ID</span></span></th>
<th><span data-ttu-id="b16b4-177">Exemple de chaîne d’événement</span><span class="sxs-lookup"><span data-stu-id="b16b4-177">Example event string</span></span></th>
<th><span data-ttu-id="b16b4-178">Suggestion</span><span class="sxs-lookup"><span data-stu-id="b16b4-178">Suggestion</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b16b4-179">150</span><span class="sxs-lookup"><span data-stu-id="b16b4-179">150</span></span></td>
<td><span data-ttu-id="b16b4-180">erreur 0x8007000B : le nom de l’éditeur du manifeste de l’application (CN = contoso) doit correspondre au nom du sujet du certificat de signature (CN = contoso, C = US).</span><span class="sxs-lookup"><span data-stu-id="b16b4-180">error 0x8007000B: The app manifest publisher name (CN=Contoso) must match the subject name of the signing certificate (CN=Contoso, C=US).</span></span></td>
<td><span data-ttu-id="b16b4-181">Le nom de l’éditeur du manifeste de l’application doit correspondre exactement au nom du sujet de la signature.</span><span class="sxs-lookup"><span data-stu-id="b16b4-181">The app manifest publisher name must exactly match the subject name of the signing.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="b16b4-182">Ces noms sont spécifiés entre guillemets et respectent tous deux la casse et l’espace blanc.</span><span class="sxs-lookup"><span data-stu-id="b16b4-182">These names are specified in quotes and are both case and whitespace sensitive.</span></span>
</blockquote>
<br/> <span data-ttu-id="b16b4-183">Vous pouvez mettre à jour la chaîne d’attribut du serveur de <strong>publication</strong> définie pour l’élément <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity</strong></a> dans le fichier AppxManifest.xml pour qu’elle corresponde au nom du sujet du certificat de signature prévu.</span><span class="sxs-lookup"><span data-stu-id="b16b4-183">You can update the <strong>Publisher</strong> attribute string that is defined for the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity</strong></a> element in the AppxManifest.xml file to match the subject name of the intended signing certificate.</span></span> <span data-ttu-id="b16b4-184">Ou sélectionnez un autre certificat de signature avec un nom d’objet qui correspond au nom de l’éditeur du manifeste de l’application.</span><span class="sxs-lookup"><span data-stu-id="b16b4-184">Or, select a different signing certificate with a subject name that matches the app manifest publisher name.</span></span> <span data-ttu-id="b16b4-185">Le nom de l’éditeur du manifeste et le nom de l’objet du certificat sont répertoriés dans le message de l’événement.</span><span class="sxs-lookup"><span data-stu-id="b16b4-185">The manifest publisher name and the certificate subject name are both listed in the event message.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b16b4-186">151</span><span class="sxs-lookup"><span data-stu-id="b16b4-186">151</span></span></td>
<td><span data-ttu-id="b16b4-187">erreur 0x8007000B : la méthode de hachage de signature spécifiée (SHA512) doit correspondre à la méthode de hachage utilisée dans le mappage de bloc de package d’application (SHA256).</span><span class="sxs-lookup"><span data-stu-id="b16b4-187">error 0x8007000B: The signature hash method specified (SHA512) must match the hash method used in the app package block map (SHA256).</span></span></td>
<td><span data-ttu-id="b16b4-188">Le hashAlgorithm spécifié dans le paramètre/fd est incorrect (voir étape 1 : déterminer l’algorithme de hachage à utiliser).</span><span class="sxs-lookup"><span data-stu-id="b16b4-188">The hashAlgorithm specified in the /fd parameter is incorrect (see Step 1: Determine the hash algorithm to use).</span></span> <span data-ttu-id="b16b4-189">Exécutez à nouveau <a href="/windows-hardware/drivers/devtest/signtool"><strong>SignTool</strong></a> avec HashAlgorithm qui correspond au mappage de bloc de package d’application.</span><span class="sxs-lookup"><span data-stu-id="b16b4-189">Rerun <a href="/windows-hardware/drivers/devtest/signtool"><strong>SignTool</strong></a> with the hashAlgorithm that matches the app package block map.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b16b4-190">152</span><span class="sxs-lookup"><span data-stu-id="b16b4-190">152</span></span></td>
<td><span data-ttu-id="b16b4-191">erreur 0x8007000B : le contenu du package d’application doit être validé par rapport à son mappage de bloc.</span><span class="sxs-lookup"><span data-stu-id="b16b4-191">error 0x8007000B: The app package contents must validate against its block map.</span></span></td>
<td><span data-ttu-id="b16b4-192">Le package d’application est endommagé et doit être régénéré pour générer un nouveau mappage de bloc.</span><span class="sxs-lookup"><span data-stu-id="b16b4-192">The app package is corrupt and needs to be rebuilt to generate a new block map.</span></span> <span data-ttu-id="b16b4-193">Pour plus d’informations sur la création d’un package d’application, consultez Création d’un package d’application avec <a href="make-appx-package--makeappx-exe-.md">app Packager</a> ou <a href="/previous-versions/hh975357(v=vs.110)">création d’un package d’application avec Visual Studio 2012</a>.</span><span class="sxs-lookup"><span data-stu-id="b16b4-193">For more info about creating an app package, see creating an app package with <a href="make-appx-package--makeappx-exe-.md">app packager</a> or <a href="/previous-versions/hh975357(v=vs.110)">Creating an app package with Visual Studio 2012</a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="security-considerations"></a><span data-ttu-id="b16b4-194">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="b16b4-194">Security Considerations</span></span>

<span data-ttu-id="b16b4-195">Une fois le package signé, le certificat que vous avez utilisé pour signer le package doit toujours être approuvé par l’ordinateur sur lequel le package doit être déployé.</span><span class="sxs-lookup"><span data-stu-id="b16b4-195">After the package is signed, the certificate that you used to sign the package must still be trusted by the computer on which the package is to be deployed.</span></span> <span data-ttu-id="b16b4-196">En ajoutant un certificat aux [magasins de certificats de l’ordinateur local](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), vous affectez le certificat de confiance de tous les utilisateurs sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b16b4-196">By adding a certificate to [local machine certificate stores](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), you affect the certificate trust of all users on the computer.</span></span> <span data-ttu-id="b16b4-197">Nous vous recommandons d’installer les certificats de signature de code que vous souhaitez pour tester des packages d’application dans le magasin de certificats personnes autorisées, et de supprimer rapidement ces certificats quand vous n’en avez plus besoin.</span><span class="sxs-lookup"><span data-stu-id="b16b4-197">We recommend that you install any code signing certificates that you want for testing app packages to the Trusted People certificate store, and promptly remove those certificates when no longer necessary.</span></span> <span data-ttu-id="b16b4-198">Si vous créez vos propres certificats de test pour la signature des packages d’application, nous vous recommandons également de limiter les privilèges associés au certificat de test.</span><span class="sxs-lookup"><span data-stu-id="b16b4-198">If you create your own test certificates for signing app packages, we also recommend that you restrict the privileges associated with the test certificate.</span></span> <span data-ttu-id="b16b4-199">Pour plus d’informations sur la création de certificats de test pour la signature de packages d’application, consultez [comment créer un certificat de signature de package d’application](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="b16b4-199">For more info about creating test certificates for signing app packages, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b16b4-200">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b16b4-200">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b16b4-201">**Exemples**</span><span class="sxs-lookup"><span data-stu-id="b16b4-201">**Samples**</span></span>
</dt> <dt>

[<span data-ttu-id="b16b4-202">Exemple de création de package d’application</span><span class="sxs-lookup"><span data-stu-id="b16b4-202">Create app package sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

<span data-ttu-id="b16b4-203">**Concepts**</span><span class="sxs-lookup"><span data-stu-id="b16b4-203">**Concepts**</span></span>
</dt> <dt>

<span data-ttu-id="b16b4-204">[Meilleures pratiques pour la signature de code](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b16b4-204">[Code-Signing Best Practices](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="b16b4-205">[Signature d’un package dans Visual Studio 2012](/previous-versions/br230260(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="b16b4-205">[Signing a package in Visual Studio 2012](/previous-versions/br230260(v=vs.110))</span></span>
</dt> <dt>

[<span data-ttu-id="b16b4-206">SignTool</span><span class="sxs-lookup"><span data-stu-id="b16b4-206">SignTool</span></span>](/windows/desktop/SecCrypto/signtool)
</dt> <dt>

[<span data-ttu-id="b16b4-207">Package d’application (MakeAppx.exe)</span><span class="sxs-lookup"><span data-stu-id="b16b4-207">App packager (MakeAppx.exe)</span></span>](make-appx-package--makeappx-exe-.md)
</dt> <dt>

[<span data-ttu-id="b16b4-208">Création d’un certificat de signature de package d’application</span><span class="sxs-lookup"><span data-stu-id="b16b4-208">How to create an app package signing certificate</span></span>](how-to-create-a-package-signing-certificate.md)
</dt> </dl>

