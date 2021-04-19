---
description: L’exemple suivant montre comment générer un assembly côte à côte signé constitué du manifeste de l’assembly, du catalogue de vérification et des fichiers d’assembly.
ms.assetid: fa95f292-36e6-4e88-8a0d-aa8bd08def2b
title: Exemple de signature d’assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e4c47482074f7decdc44af6b94bc7df31df6969
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "106527087"
---
# <a name="assembly-signing-example"></a><span data-ttu-id="912ac-103">Exemple de signature d’assembly</span><span class="sxs-lookup"><span data-stu-id="912ac-103">Assembly Signing Example</span></span>

<span data-ttu-id="912ac-104">L’exemple suivant montre comment générer un assembly côte à côte signé constitué du manifeste de l’assembly, du catalogue de vérification et des fichiers d’assembly.</span><span class="sxs-lookup"><span data-stu-id="912ac-104">The following example discusses how to generate a signed side-by-side assembly consisting of the assembly manifest, the verification catalog, and the assembly files.</span></span> <span data-ttu-id="912ac-105">Les assemblys côte à côte partagés doivent être signés.</span><span class="sxs-lookup"><span data-stu-id="912ac-105">Shared side-by-side assemblies should be signed.</span></span> <span data-ttu-id="912ac-106">Le système d’exploitation vérifie la signature de l’assembly avant d’installer un assembly partagé dans le magasin global côte à côte (WinSxS).</span><span class="sxs-lookup"><span data-stu-id="912ac-106">The operating system verifies the assembly signature before installing a shared assembly to the global side-by-side store (WinSxS).</span></span> <span data-ttu-id="912ac-107">Cela complique l’usurpation de l’éditeur de l’assembly côte à côte.</span><span class="sxs-lookup"><span data-stu-id="912ac-107">This makes it difficult to spoof the publisher of the side-by-side assembly.</span></span>

<span data-ttu-id="912ac-108">Notez que la modification des fichiers d’assembly ou du contenu du manifeste après la génération du catalogue d’assemblys invalide le catalogue et l’assembly.</span><span class="sxs-lookup"><span data-stu-id="912ac-108">Note that changing the assembly files or the contents of the manifest after generating the assembly catalog invalidates the catalog and the assembly.</span></span> <span data-ttu-id="912ac-109">Si vous devez mettre à jour les fichiers d’assembly ou le manifeste après avoir créé et signé le catalogue, vous devez signer à nouveau l’assembly et générer un nouveau catalogue.</span><span class="sxs-lookup"><span data-stu-id="912ac-109">If you must update the assembly files or manifest after creating and signing the catalog, you must again sign the assembly and generate a new catalog.</span></span>

<span data-ttu-id="912ac-110">Commencez par les fichiers d’assembly, le manifeste de l’assembly et le fichier de certificat que vous allez utiliser pour signer l’assembly.</span><span class="sxs-lookup"><span data-stu-id="912ac-110">Start with the assembly files, assembly manifest, and the certificate file you will use to sign the assembly.</span></span> <span data-ttu-id="912ac-111">Le fichier de certificat doit avoir une taille de 2048 bits ou plus.</span><span class="sxs-lookup"><span data-stu-id="912ac-111">The certificate file must be 2048 bits or larger.</span></span> <span data-ttu-id="912ac-112">Vous n’êtes pas obligé d’utiliser un certificat approuvé.</span><span class="sxs-lookup"><span data-stu-id="912ac-112">You are not required to use a trusted certificate.</span></span> <span data-ttu-id="912ac-113">Le certificat est utilisé uniquement pour vérifier que l’assembly n’a pas été endommagé.</span><span class="sxs-lookup"><span data-stu-id="912ac-113">The certificate is used only to verify that the assembly has not been damaged.</span></span>

<span data-ttu-id="912ac-114">Exécutez l’utilitaire de [Pktextract.exe](pktextract-exe.md) fourni dans le kit de développement logiciel (SDK) Microsoft Windows pour extraire le jeton de clé publique du fichier de certificat.</span><span class="sxs-lookup"><span data-stu-id="912ac-114">Run the [Pktextract.exe](pktextract-exe.md) utility provided in the Microsoft Windows Software Development Kit (SDK) to extract the public key token from the certificate file.</span></span> <span data-ttu-id="912ac-115">Pour que Pktextract fonctionne correctement, le fichier de certificat doit être présent dans le même répertoire que l’utilitaire.</span><span class="sxs-lookup"><span data-stu-id="912ac-115">For Pktextract to work properly, the certificate file must be present in the same directory as the utility.</span></span> <span data-ttu-id="912ac-116">Utilisez la valeur de jeton de clé publique extraite pour mettre à jour l’attribut **PublicKeyToken** de l’élément **assemblyIdentity** dans le fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="912ac-116">Use the extracted public key token value to update the **publicKeyToken** attribute of the **assemblyIdentity** element in the manifest file.</span></span>

<span data-ttu-id="912ac-117">Voici un exemple de fichier manifeste nommé MySampleAssembly. manifest.</span><span class="sxs-lookup"><span data-stu-id="912ac-117">Here is an example of a manifest file named MySampleAssembly.manifest.</span></span> <span data-ttu-id="912ac-118">L’assembly MySampleAssembly contient un seul fichier, MYFILE.DLL.</span><span class="sxs-lookup"><span data-stu-id="912ac-118">The MySampleAssembly assembly contains only one file, MYFILE.DLL.</span></span> <span data-ttu-id="912ac-119">Notez que la valeur de l’attribut **PublicKeyToken** de l’élément **assemblyIdentity** a été mise à jour avec la valeur du jeton de clé publique.</span><span class="sxs-lookup"><span data-stu-id="912ac-119">Note that the value for the **publicKeyToken** attribute of the **assemblyIdentity** element has been updated with the value of the public key token.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity 
        type="win32" 
        name="Microsoft.Windows.MySampleAssembly" 
        version="1.0.0.0" 
        processorArchitecture="x86"         
        publicKeyToken="0000000000000000"/>
    <file name="myfile.dll"/>
</assembly>
```

<span data-ttu-id="912ac-120">Exécutez ensuite l’utilitaire [Mt.exe](mt-exe.md) fourni dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="912ac-120">Next run the [Mt.exe](mt-exe.md) utility provided in the Windows SDK.</span></span> <span data-ttu-id="912ac-121">Les fichiers d’assembly doivent se trouver dans le même répertoire que le manifeste.</span><span class="sxs-lookup"><span data-stu-id="912ac-121">The assembly files must be located in the same directory as the manifest.</span></span> <span data-ttu-id="912ac-122">Dans cet exemple, il s’agit du répertoire MySampleAssembly.</span><span class="sxs-lookup"><span data-stu-id="912ac-122">In this example this is the MySampleAssembly directory.</span></span> <span data-ttu-id="912ac-123">Appelez Mt.exe pour l’exemple comme suit :</span><span class="sxs-lookup"><span data-stu-id="912ac-123">Call Mt.exe for the example as follows:</span></span>

<span data-ttu-id="912ac-124">**c : \\ MySampleAssembly>mt.exe-manifest MySampleAssembly. manifest-hashupdate-makecdfs**</span><span class="sxs-lookup"><span data-stu-id="912ac-124">**c:\\ MySampleAssembly>mt.exe -manifest MySampleAssembly.manifest -hashupdate -makecdfs**</span></span>

<span data-ttu-id="912ac-125">Voici comment se présente l’exemple de manifeste après l’exécution de Mt.exe.</span><span class="sxs-lookup"><span data-stu-id="912ac-125">Here is how the example manifest looks after running Mt.exe.</span></span> <span data-ttu-id="912ac-126">Notez que l’exécution de Mt.exe avec l’option hashupdate ajoute le hachage SHA-1 du fichier.</span><span class="sxs-lookup"><span data-stu-id="912ac-126">Notice that running Mt.exe with the hashupdate option adds the SHA-1 hash of the file.</span></span> <span data-ttu-id="912ac-127">Ne modifiez pas cette valeur.</span><span class="sxs-lookup"><span data-stu-id="912ac-127">Do not change this value.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity 
        type="win32" 
        name=" Microsoft.Windows.MySampleAssembly" 
        version="1.0.0.0" 
        processorArchitecture="x86"         
        publicKeyToken="0000000000000000"/>
    <file name="myfile.dll"
hash="a1d362d6278557bbe965a684ac7adb4e57427a29" hashalg="SHA1"/>
</assembly>
```

<span data-ttu-id="912ac-128">L’exécution de Mt.exe avec l’option-makecdfs génère un fichier nommé MySampleAssembly. manifest. CDF qui décrit le contenu du catalogue de sécurité qui sera utilisé pour valider le manifeste.</span><span class="sxs-lookup"><span data-stu-id="912ac-128">Running Mt.exe with the -makecdfs option generates a file named MySampleAssembly.manifest.cdf that describes the contents of the security catalog that will be used to validate the manifest.</span></span>

<span data-ttu-id="912ac-129">L’étape suivante consiste à exécuter Makecat.exe sur ce. CDF pour créer le catalogue de sécurité pour l’assembly.</span><span class="sxs-lookup"><span data-stu-id="912ac-129">The next step is to run Makecat.exe over this .cdf to create the security catalog for the assembly.</span></span> <span data-ttu-id="912ac-130">L’appel à Makecat.exe pour cet exemple se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="912ac-130">The call to Makecat.exe for this example would appear as follows:</span></span>

<span data-ttu-id="912ac-131">**c : \\ MySampleAssembly>MakeCat MySampleAssembly. manifest. CDF**</span><span class="sxs-lookup"><span data-stu-id="912ac-131">**c:\\MySampleAssembly>makecat MySampleAssembly.manifest.cdf**</span></span>

<span data-ttu-id="912ac-132">La dernière étape consiste à exécuter SignTool.exe pour signer le fichier catalogue avec le certificat.</span><span class="sxs-lookup"><span data-stu-id="912ac-132">The final step is to run SignTool.exe to sign the catalog file with the certificate.</span></span> <span data-ttu-id="912ac-133">Il doit s’agir du même certificat que celui utilisé dans le précédent pour générer le jeton de clé publique.</span><span class="sxs-lookup"><span data-stu-id="912ac-133">This should be the same certificate that was used in the preceding to generate the public key token.</span></span> <span data-ttu-id="912ac-134">Pour plus d’informations sur SignTool.exe consultez la rubrique [**SignTool**](../seccrypto/signtool.md) .</span><span class="sxs-lookup"><span data-stu-id="912ac-134">For more information about SignTool.exe see the [**SignTool**](../seccrypto/signtool.md) topic.</span></span> <span data-ttu-id="912ac-135">L’appel à **SignTool** pour l’exemple se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="912ac-135">The call to **SignTool** for the example would appear as follows:</span></span>

<span data-ttu-id="912ac-136">**c : \\ MySampleAssembly>le signe SignTool/f \<fullpath> MyCompany. pfx/du https : \/ /www.mycompany.com/MySampleAssembly/t https : \/ /timestamp.DigiCert.com MySampleAssembly.cat**</span><span class="sxs-lookup"><span data-stu-id="912ac-136">**c:\\MySampleAssembly>signtool sign /f \<fullpath>mycompany.pfx /du https:\//www.mycompany.com/MySampleAssembly /t https:\//timestamp.digicert.com MySampleAssembly.cat**</span></span>

<span data-ttu-id="912ac-137">Si vous disposez d’un certificat numérique authentifié et que votre autorité de certification utilise le format de fichier PVK pour stocker la clé privée, vous pouvez utiliser l’importateur de fichiers de certificat numérique (pvkimprt.exe) PVK pour importer la clé dans votre fournisseur de services de chiffrement (CSP).</span><span class="sxs-lookup"><span data-stu-id="912ac-137">If you have an authenticated digital certificate, and your certification authority uses the PVK file format to store the private key, you can use the PVK Digital Certificate Files Importer (pvkimprt.exe) to import the key into your cryptographic service provider (CSP).</span></span> <span data-ttu-id="912ac-138">Cet utilitaire vous permet d’exporter au format standard de PFX/P12.</span><span class="sxs-lookup"><span data-stu-id="912ac-138">This utility enables you to export to the industry standard format of PFX/P12.</span></span> <span data-ttu-id="912ac-139">Pour plus d’informations sur l’importateur de fichiers de certificats numériques PVK, consultez la section ressources de déploiement de MSDN Library ou contactez votre autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="912ac-139">For more information about the PVK Digital Certificate Files Importer, see the Deployment Resources section of the MSDN library or contact your certification authority.</span></span> <span data-ttu-id="912ac-140">Vous pourrez peut-être obtenir pvkimprt.exe à partir de https://office.microsoft.com/downloads/2000/pvkimprt.aspx .</span><span class="sxs-lookup"><span data-stu-id="912ac-140">You may be able to obtain pvkimprt.exe from https://office.microsoft.com/downloads/2000/pvkimprt.aspx.</span></span>

<span data-ttu-id="912ac-141">Voir aussi [création de fichiers et catalogues signés](creating-signed-files-and-catalogs.md).</span><span class="sxs-lookup"><span data-stu-id="912ac-141">See also, [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span>

 

 
