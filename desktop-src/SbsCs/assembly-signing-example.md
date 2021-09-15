---
description: L’exemple suivant montre comment générer un assembly côte à côte signé constitué du manifeste de l’assembly, du catalogue de vérification et des fichiers d’assembly.
ms.assetid: fa95f292-36e6-4e88-8a0d-aa8bd08def2b
title: Exemple de signature d’assembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e4c47482074f7decdc44af6b94bc7df31df6969
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238121"
---
# <a name="assembly-signing-example"></a>Exemple de signature d’assembly

L’exemple suivant montre comment générer un assembly côte à côte signé constitué du manifeste de l’assembly, du catalogue de vérification et des fichiers d’assembly. Les assemblys côte à côte partagés doivent être signés. Le système d’exploitation vérifie la signature de l’assembly avant d’installer un assembly partagé dans le magasin global côte à côte (WinSxS). Cela complique l’usurpation de l’éditeur de l’assembly côte à côte.

Notez que la modification des fichiers d’assembly ou du contenu du manifeste après la génération du catalogue d’assemblys invalide le catalogue et l’assembly. Si vous devez mettre à jour les fichiers d’assembly ou le manifeste après avoir créé et signé le catalogue, vous devez signer à nouveau l’assembly et générer un nouveau catalogue.

Commencez par les fichiers d’assembly, le manifeste de l’assembly et le fichier de certificat que vous allez utiliser pour signer l’assembly. Le fichier de certificat doit avoir une taille de 2048 bits ou plus. Vous n’êtes pas obligé d’utiliser un certificat approuvé. Le certificat est utilisé uniquement pour vérifier que l’assembly n’a pas été endommagé.

exécutez l’utilitaire de [Pktextract.exe](pktextract-exe.md) fourni dans le kit de développement logiciel (SDK) de Microsoft Windows pour extraire le jeton de clé publique du fichier de certificat. Pour que Pktextract fonctionne correctement, le fichier de certificat doit être présent dans le même répertoire que l’utilitaire. Utilisez la valeur de jeton de clé publique extraite pour mettre à jour l’attribut **PublicKeyToken** de l’élément **assemblyIdentity** dans le fichier manifeste.

Voici un exemple de fichier manifeste nommé MySampleAssembly. manifest. L’assembly MySampleAssembly contient un seul fichier, MYFILE.DLL. Notez que la valeur de l’attribut **PublicKeyToken** de l’élément **assemblyIdentity** a été mise à jour avec la valeur du jeton de clé publique.

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

exécutez ensuite l’utilitaire [Mt.exe](mt-exe.md) fourni dans le SDK Windows. Les fichiers d’assembly doivent se trouver dans le même répertoire que le manifeste. Dans cet exemple, il s’agit du répertoire MySampleAssembly. Appelez Mt.exe pour l’exemple comme suit :

**c : \\ MySampleAssembly>mt.exe-manifest MySampleAssembly. manifest-hashupdate-makecdfs**

Voici comment se présente l’exemple de manifeste après l’exécution de Mt.exe. Notez que l’exécution de Mt.exe avec l’option hashupdate ajoute le hachage SHA-1 du fichier. Ne modifiez pas cette valeur.

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

L’exécution de Mt.exe avec l’option-makecdfs génère un fichier nommé MySampleAssembly. manifest. CDF qui décrit le contenu du catalogue de sécurité qui sera utilisé pour valider le manifeste.

L’étape suivante consiste à exécuter Makecat.exe sur ce. CDF pour créer le catalogue de sécurité pour l’assembly. L’appel à Makecat.exe pour cet exemple se présente comme suit :

**c : \\ MySampleAssembly>MakeCat MySampleAssembly. manifest. CDF**

La dernière étape consiste à exécuter SignTool.exe pour signer le fichier catalogue avec le certificat. Il doit s’agir du même certificat que celui utilisé dans le précédent pour générer le jeton de clé publique. Pour plus d’informations sur SignTool.exe consultez la rubrique [**SignTool**](../seccrypto/signtool.md) . L’appel à **SignTool** pour l’exemple se présente comme suit :

**c : \\ MySampleAssembly>le signe SignTool/f \<fullpath> MyCompany. pfx/du https : \/ /www.mycompany.com/MySampleAssembly/t https : \/ /timestamp.DigiCert.com MySampleAssembly.cat**

Si vous disposez d’un certificat numérique authentifié et que votre autorité de certification utilise le format de fichier PVK pour stocker la clé privée, vous pouvez utiliser l’importateur de fichiers de certificat numérique (pvkimprt.exe) PVK pour importer la clé dans votre fournisseur de services de chiffrement (CSP). Cet utilitaire vous permet d’exporter au format standard de PFX/P12. Pour plus d’informations sur l’importateur de fichiers de certificats numériques PVK, consultez la section ressources de déploiement de MSDN Library ou contactez votre autorité de certification. Vous pourrez peut-être obtenir pvkimprt.exe à partir de https://office.microsoft.com/downloads/2000/pvkimprt.aspx .

Voir aussi [création de fichiers et catalogues signés](creating-signed-files-and-catalogs.md).

 

 
