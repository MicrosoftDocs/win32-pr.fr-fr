---
title: How to create an app package signing certificate (Comment créer un certificat de signature de package d’application)
description: Découvrez comment utiliser MakeCert.exe et Pvk2Pfx.exe pour créer un certificat de signature de code de test, afin de pouvoir signer vos packages d’applications Windows.
ms.assetid: DEDD3727-3F0E-403D-9A6E-55949E98FE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382771c23d57b580508017d0bbf24bd742a6eeaf
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031064"
---
# <a name="how-to-create-an-app-package-signing-certificate"></a><span data-ttu-id="4dfa0-103">How to create an app package signing certificate (Comment créer un certificat de signature de package d’application)</span><span class="sxs-lookup"><span data-stu-id="4dfa0-103">How to create an app package signing certificate</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4dfa0-104">MakeCert.exe est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-104">MakeCert.exe is deprecated.</span></span> <span data-ttu-id="4dfa0-105">Pour plus d’informations sur la création d’un certificat, consultez [créer un certificat pour la signature de package](/windows/msix/package/create-certificate-package-signing).</span><span class="sxs-lookup"><span data-stu-id="4dfa0-105">For current guidance on creating a certificate, see [Create a certificate for package signing](/windows/msix/package/create-certificate-package-signing).</span></span>

 

<span data-ttu-id="4dfa0-106">Découvrez comment utiliser [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) et [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) pour créer un certificat de signature de code de test, afin de pouvoir signer vos packages d’applications Windows.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-106">Learn how to use [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) to create a test code signing certificate, so that you can sign your Windows app packages.</span></span>

<span data-ttu-id="4dfa0-107">Vous devez signer numériquement vos applications Windows empaquetées avant de les déployer.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-107">You must digitally sign your packaged Windows apps before you deploy them.</span></span> <span data-ttu-id="4dfa0-108">Si vous n’utilisez pas Microsoft Visual Studio 2012 pour créer et signer vos packages d’application, vous devez créer et gérer vos propres certificats de signature de code.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-108">If you don't use Microsoft Visual Studio 2012 to create and sign your app packages, you need to create and manage your own code signing certificates.</span></span> <span data-ttu-id="4dfa0-109">Vous pouvez créer des certificats à l’aide de [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) et [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) à partir du kit WDK (Windows Driver Kit).</span><span class="sxs-lookup"><span data-stu-id="4dfa0-109">You can create certificates by using [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) from the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="4dfa0-110">Ensuite, vous pouvez utiliser les certificats pour signer les packages d’application, afin qu’ils puissent être déployés localement à des fins de test.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-110">Then you can use the certificates to sign the app packages, so they can be deployed locally for testing.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="4dfa0-111">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="4dfa0-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="4dfa0-112">Technologies</span><span class="sxs-lookup"><span data-stu-id="4dfa0-112">Technologies</span></span>

-   <span data-ttu-id="4dfa0-113">[Présentation de la signature de code](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4dfa0-113">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
-   <span data-ttu-id="4dfa0-114">[Packages d’applications et déploiement](/previous-versions/windows/apps/hh464929(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="4dfa0-114">[App packages and deployment](/previous-versions/windows/apps/hh464929(v=win.10))</span></span>
-   [<span data-ttu-id="4dfa0-115">Outils pour la signature des pilotes</span><span class="sxs-lookup"><span data-stu-id="4dfa0-115">Tools for Signing Drivers</span></span>](/windows-hardware/drivers/devtest/tools-for-signing-drivers)

### <a name="prerequisites"></a><span data-ttu-id="4dfa0-116">Prérequis</span><span class="sxs-lookup"><span data-stu-id="4dfa0-116">Prerequisites</span></span>

-   <span data-ttu-id="4dfa0-117">Outils de [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) et de [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) à partir du kit WDK</span><span class="sxs-lookup"><span data-stu-id="4dfa0-117">[**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) tools from the WDK</span></span>

## <a name="instructions"></a><span data-ttu-id="4dfa0-118">Instructions</span><span class="sxs-lookup"><span data-stu-id="4dfa0-118">Instructions</span></span>

### <a name="step-1-determine-the-publisher-name-of-the-package"></a><span data-ttu-id="4dfa0-119">Étape 1 : déterminer le nom de l’éditeur du package</span><span class="sxs-lookup"><span data-stu-id="4dfa0-119">Step 1: Determine the publisher name of the package</span></span>

<span data-ttu-id="4dfa0-120">Pour que le certificat de signature que vous créez puisse être utilisé avec le package d’application que vous souhaitez signer, le nom d’objet du certificat de signature doit correspondre à l’attribut **Publisher** de l’élément [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) dans le AppxManifest.xml pour cette application.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-120">To make the signing certificate that you create usable with the app package that you want to sign, the subject name of the signing certificate must match the **Publisher** attribute of the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element in the AppxManifest.xml for that app.</span></span> <span data-ttu-id="4dfa0-121">Par exemple, supposons que le AppxManifest.xml contient :</span><span class="sxs-lookup"><span data-stu-id="4dfa0-121">For example, suppose the AppxManifest.xml contains:</span></span>

``` syntax
  <Identity Name="Contoso.AssetTracker" 
    Version="1.0.0.0" 
    Publisher="CN=Contoso Software, O=Contoso Corporation, C=US"/>
```

<span data-ttu-id="4dfa0-122">Pour le paramètre *PublisherName* que vous spécifiez avec l’utilitaire [**Makecert**](/windows-hardware/drivers/devtest/makecert) à l’étape suivante, utilisez « CN = contoso Software, O = Contoso Corporation, C = US ».</span><span class="sxs-lookup"><span data-stu-id="4dfa0-122">For the *publisherName* parameter that you specify with the [**MakeCert**](/windows-hardware/drivers/devtest/makecert) utility in the next step, use "CN=Contoso Software, O=Contoso Corporation, C=US".</span></span>

> [!Note]  
> <span data-ttu-id="4dfa0-123">Cette chaîne de paramètres est spécifiée entre guillemets et respecte à la fois la casse et l’espace blanc.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-123">This parameter string is specified in quotes and is both case and whitespace sensitive.</span></span>

 

<span data-ttu-id="4dfa0-124">La chaîne d’attribut du serveur de **publication** qui est définie pour l’élément [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) dans le AppxManifest.xml doit être identique à la chaîne que vous spécifiez avec le paramètre [**Makecert**](/windows-hardware/drivers/devtest/makecert) /n pour le nom d’objet du certificat.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-124">The **Publisher** attribute string that is defined for the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element in the AppxManifest.xml must be identical to the string that you specify with the [**MakeCert**](/windows-hardware/drivers/devtest/makecert) /n parameter for the certificate subject name.</span></span> <span data-ttu-id="4dfa0-125">Copiez et collez la chaîne dans la mesure du possible.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-125">Copy and paste the string where possible.</span></span>

### <a name="step-2-create-a-private-key-using-makecertexe"></a><span data-ttu-id="4dfa0-126">Étape 2 : créer une clé privée à l’aide de MakeCert.exe</span><span class="sxs-lookup"><span data-stu-id="4dfa0-126">Step 2: Create a private key using MakeCert.exe</span></span>

<span data-ttu-id="4dfa0-127">Utilisez l’utilitaire [**Makecert**](/windows-hardware/drivers/devtest/makecert) pour créer un certificat de test auto-signé et une clé privée :</span><span class="sxs-lookup"><span data-stu-id="4dfa0-127">Use the [**MakeCert**](/windows-hardware/drivers/devtest/makecert) utility to create a self-signed test certificate and private key:</span></span>

``` syntax
MakeCert /n publisherName /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 
expirationDate /sv MyKey.pvk MyKey.cer
```

<span data-ttu-id="4dfa0-128">Cette commande vous invite à fournir un mot de passe pour le fichier. pvk.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-128">This command prompts you to provide a password for the .pvk file.</span></span> <span data-ttu-id="4dfa0-129">Nous vous recommandons de choisir un [mot de passe fort](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) et de conserver votre clé privée dans un emplacement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-129">We recommend that you choose a [strong password](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) and keep your private key in a secure location.</span></span>

<span data-ttu-id="4dfa0-130">Nous vous recommandons d’utiliser les paramètres suggérés dans l’exemple précédent pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="4dfa0-130">We recommend that you use the suggested parameters in the preceding example for these reasons:</span></span>

<dl> <dt>

<span data-ttu-id="4dfa0-131"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="4dfa0-131"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="4dfa0-132">Crée un certificat racine auto-signé.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-132">Creates a self-signed root certificate.</span></span> <span data-ttu-id="4dfa0-133">Cela simplifie la gestion de votre certificat de test.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-133">This simplifies management for your test certificate.</span></span>

</dd> <dt>

<span data-ttu-id="4dfa0-134"><span id="_h_0"></span><span id="_H_0"></span>**/h 0**</span><span class="sxs-lookup"><span data-stu-id="4dfa0-134"><span id="_h_0"></span><span id="_H_0"></span>**/h 0**</span></span>
</dt> <dd>

<span data-ttu-id="4dfa0-135">Marque la contrainte de base pour le certificat comme une entité finale.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-135">Marks the basic constraint for the certificate as an end-entity.</span></span> <span data-ttu-id="4dfa0-136">Cela empêche l’utilisation du certificat en tant qu’autorité de certification (CA) susceptible d’émettre d’autres certificats.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-136">This prevents the certificate from being used as a Certification Authority (CA) that can issue other certificates.</span></span>

</dd> <dt>

<span data-ttu-id="4dfa0-137"><span id="_eku"></span><span id="_EKU"></span>**/eku**</span><span class="sxs-lookup"><span data-stu-id="4dfa0-137"><span id="_eku"></span><span id="_EKU"></span>**/eku**</span></span>
</dt> <dd>

<span data-ttu-id="4dfa0-138">Définit les valeurs de l’utilisation améliorée de la clé pour le certificat.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-138">Sets the Enhanced Key Usage (EKU) values for the certificate.</span></span>

> [!Note]  
> <span data-ttu-id="4dfa0-139">Ne placez pas d’espace entre les deux valeurs délimitées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-139">Don't put a space between the two comma-delimited values.</span></span>

 

-   <span data-ttu-id="4dfa0-140">1.3.6.1.5.5.7.3.3 indique que le certificat est valide pour la signature de code.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-140">1.3.6.1.5.5.7.3.3 indicates that the certificate is valid for code signing.</span></span> <span data-ttu-id="4dfa0-141">Spécifiez toujours cette valeur pour limiter l’utilisation prévue du certificat.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-141">Always specify this value to limit the intended use for the certificate.</span></span>
-   <span data-ttu-id="4dfa0-142">1.3.6.1.4.1.311.10.3.13 indique que le certificat respecte la signature de la durée de vie.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-142">1.3.6.1.4.1.311.10.3.13 indicates that the certificate respects lifetime signing.</span></span> <span data-ttu-id="4dfa0-143">En règle générale, si une signature est horodatée, tant que le certificat était valide au moment où il a été horodaté, la signature reste valide même si le certificat expire.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-143">Typically, if a signature is time stamped, as long as the certificate was valid at the point when it was time stamped, the signature remains valid even if the certificate expires.</span></span> <span data-ttu-id="4dfa0-144">Cette utilisation améliorée de la valeur force la signature à expirer, que la signature soit ou non horodatée.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-144">This EKU forces the signature to expire regardless of whether the signature is time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="4dfa0-145"><span id="_e"></span><span id="_E"></span>**/e**</span><span class="sxs-lookup"><span data-stu-id="4dfa0-145"><span id="_e"></span><span id="_E"></span>**/e**</span></span>
</dt> <dd>

<span data-ttu-id="4dfa0-146">Définit la date d’expiration du certificat.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-146">Sets the expiration date of the certificate.</span></span> <span data-ttu-id="4dfa0-147">Fournissez une valeur pour le paramètre *expirationDate* au format mm/jj/aaaa.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-147">Provide a value for the *expirationDate* parameter in the mm/dd/yyyy format.</span></span> <span data-ttu-id="4dfa0-148">Nous vous recommandons de choisir une date d’expiration uniquement si nécessaire à des fins de test, en général moins d’un an.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-148">We recommend that you choose an expiration date only as long as necessary for your testing purposes, typically less than a year.</span></span> <span data-ttu-id="4dfa0-149">Cette date d’expiration, conjointement avec l’utilisation améliorée de la signature de durée de vie, permet de limiter la fenêtre dans laquelle le certificat peut être compromis et utilisé de façon inutilisée.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-149">This expiration date in conjunction with the lifetime signing EKU can help to limit the window in which the certificate can be compromised and misused.</span></span>

</dd> </dl>

<span data-ttu-id="4dfa0-150">Pour plus d’informations sur les autres options, consultez [**Makecert**](/windows-hardware/drivers/devtest/makecert).</span><span class="sxs-lookup"><span data-stu-id="4dfa0-150">For more info about other options, see [**MakeCert**](/windows-hardware/drivers/devtest/makecert).</span></span>

### <a name="step-3-create-a-personal-information-exchange-pfx-file-using-pvk2pfxexe"></a><span data-ttu-id="4dfa0-151">Étape 3 : créer un fichier d’échange d’informations personnelles (. pfx) à l’aide de Pvk2Pfx.exe</span><span class="sxs-lookup"><span data-stu-id="4dfa0-151">Step 3: Create a Personal Information Exchange (.pfx) file using Pvk2Pfx.exe</span></span>

<span data-ttu-id="4dfa0-152">Utilisez l’utilitaire [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) pour convertir les fichiers. pvk et. [**CER créés dans**](/windows-hardware/drivers/devtest/makecert) un fichier. pfx que vous pouvez utiliser avec [SignTool](/windows/desktop/SecCrypto/signtool) pour signer un package d’application :</span><span class="sxs-lookup"><span data-stu-id="4dfa0-152">Use the [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) utility to convert the .pvk and .cer files that [**MakeCert**](/windows-hardware/drivers/devtest/makecert) created to a .pfx file that you can use with [SignTool](/windows/desktop/SecCrypto/signtool) to sign an app package:</span></span>

``` syntax
Pvk2Pfx /pvk MyKey.pvk /pi pvkPassword /spc MyKey.cer /pfx MyKey.pfx [/po pfxPassword]
```

<span data-ttu-id="4dfa0-153">Les fichiers *myKey. pvk* et *myKey. cer* sont les mêmes que ceux [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) créés à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-153">The *MyKey.pvk* and *MyKey.cer* files are the same files that [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) created in the previous step.</span></span> <span data-ttu-id="4dfa0-154">En utilisant le paramètre facultatif/po, vous pouvez spécifier un autre mot de passe pour le fichier. pfx qui en résulte. dans le cas contraire, le fichier. pfx a le même mot de passe que *myKey. pvk*.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-154">By using the optional /po parameter, you can specify a different password for the resulting .pfx; otherwise, the .pfx has the same password as *MyKey.pvk*.</span></span>

<span data-ttu-id="4dfa0-155">Pour plus d’informations sur les autres options, consultez [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx).</span><span class="sxs-lookup"><span data-stu-id="4dfa0-155">For more info about other options, see [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx).</span></span>

## <a name="remarks"></a><span data-ttu-id="4dfa0-156">Notes</span><span class="sxs-lookup"><span data-stu-id="4dfa0-156">Remarks</span></span>

<span data-ttu-id="4dfa0-157">Une fois que vous avez créé le fichier. pfx, vous pouvez utiliser le fichier avec [SignTool](/windows/desktop/SecCrypto/signtool) pour signer un package d’application.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-157">After you create the .pfx file, you can use the file with [SignTool](/windows/desktop/SecCrypto/signtool) to sign an app package.</span></span> <span data-ttu-id="4dfa0-158">Pour plus d’informations, consultez [Comment signer un package d’application à l’aide de SignTool](how-to-sign-a-package-using-signtool.md).</span><span class="sxs-lookup"><span data-stu-id="4dfa0-158">For more info, see [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md).</span></span> <span data-ttu-id="4dfa0-159">Toutefois, le certificat n’est toujours pas approuvé par l’ordinateur local pour le déploiement de packages d’application tant que vous ne l’avez pas installé dans le magasin de certificats de confiance de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-159">But the certificate is still not trusted by the local computer for deployment of app packages until you install it into the trusted certificates store of the local computer.</span></span> <span data-ttu-id="4dfa0-160">Vous pouvez utiliser [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)), qui est fourni avec Windows.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-160">You can use [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)), which comes with Windows.</span></span>

<span data-ttu-id="4dfa0-161">**Pour installer des certificats avec WindowsCertutil.exe**</span><span class="sxs-lookup"><span data-stu-id="4dfa0-161">**To install certificates with WindowsCertutil.exe**</span></span>

1.  <span data-ttu-id="4dfa0-162">Exécutez **Cmd.exe** en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-162">Run **Cmd.exe** as administrator.</span></span>
2.  <span data-ttu-id="4dfa0-163">Exécutez cette commande :</span><span class="sxs-lookup"><span data-stu-id="4dfa0-163">Run this command:</span></span>

    ``` syntax
    Certutil -addStore TrustedPeople MyKey.cer
    ```

<span data-ttu-id="4dfa0-164">Nous vous recommandons de supprimer les certificats s’ils ne sont plus utilisés.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-164">We recommend that you remove the certificates if they are no longer in use.</span></span> <span data-ttu-id="4dfa0-165">À partir de la même invite de commandes administrateur, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="4dfa0-165">From the same administrator command prompt, run this command:</span></span>

``` syntax
Certutil -delStore TrustedPeople certID
```

<span data-ttu-id="4dfa0-166">La valeur **certID** est le numéro de série du certificat.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-166">The **certID** is the serial number of the certificate.</span></span> <span data-ttu-id="4dfa0-167">Exécutez cette commande pour déterminer le numéro de série du certificat :</span><span class="sxs-lookup"><span data-stu-id="4dfa0-167">Run this command to determine the certificate serial number:</span></span>

``` syntax
Certutil -store TrustedPeople
```

## <a name="security-considerations"></a><span data-ttu-id="4dfa0-168">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="4dfa0-168">Security Considerations</span></span>

<span data-ttu-id="4dfa0-169">En ajoutant un certificat aux [magasins de certificats de l’ordinateur local](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), vous affectez le certificat de confiance de tous les utilisateurs sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-169">By adding a certificate to [local machine certificate stores](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), you affect the certificate trust of all users on the computer.</span></span> <span data-ttu-id="4dfa0-170">Nous vous recommandons d’installer les certificats de signature de code que vous souhaitez pour tester des packages d’application dans le magasin de certificats personnes autorisées.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-170">We recommend that you install any code signing certificates that you want for testing app packages to the Trusted People certificate store.</span></span> <span data-ttu-id="4dfa0-171">Supprimez rapidement ces certificats lorsqu’ils ne sont plus nécessaires pour les empêcher d’être utilisés pour compromettre la confiance du système.</span><span class="sxs-lookup"><span data-stu-id="4dfa0-171">Promptly remove those certificates when they are no longer necessary, to prevent them from being used to compromise system trust.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4dfa0-172">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4dfa0-172">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4dfa0-173">**Exemples**</span><span class="sxs-lookup"><span data-stu-id="4dfa0-173">**Samples**</span></span>
</dt> <dt>

[<span data-ttu-id="4dfa0-174">Exemple de création de package d’application</span><span class="sxs-lookup"><span data-stu-id="4dfa0-174">Create app package sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

<span data-ttu-id="4dfa0-175">**Concepts**</span><span class="sxs-lookup"><span data-stu-id="4dfa0-175">**Concepts**</span></span>
</dt> <dt>

<span data-ttu-id="4dfa0-176">[Meilleures pratiques pour la signature de code](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4dfa0-176">[Code-Signing Best Practices](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4dfa0-177">Comment signer un package d’application à l’aide de SignTool</span><span class="sxs-lookup"><span data-stu-id="4dfa0-177">How to sign an app package using SignTool</span></span>](how-to-sign-a-package-using-signtool.md)
</dt> <dt>

<span data-ttu-id="4dfa0-178">[Signature d’un package d’application](/previous-versions/br230260(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="4dfa0-178">[Signing an app package](/previous-versions/br230260(v=vs.110))</span></span>
</dt> </dl>

 

 