---
title: Outil de création de package de l’application (MakeAppx.exe)
description: App Packager (MakeAppx.exe) crée un package d’application à partir de fichiers sur le disque ou extrait les fichiers d’un package d’application sur le disque.
ms.assetid: 9B7BF420-8E19-4BFD-B378-D09E61F68A39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41595550f3bee7b1149959886ed649e9212224b2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101468"
---
# <a name="app-packager-makeappxexe"></a>Outil de création de package de l’application (MakeAppx.exe)

> [!Note]  
> Pour obtenir des conseils sur l’utilisation de cet outil sur UWP, consultez [créer un package d’application avec l’outil MakeAppx.exe](/windows/msix/package/create-app-package-with-makeappx-tool).

 

App Packager (MakeAppx.exe) crée un package d’application à partir de fichiers sur le disque ou extrait les fichiers d’un package d’application sur le disque. À partir de Windows 8.1, app Packager crée également un lot de packages d’application à partir de packages d’application sur le disque ou extrait les packages d’application d’un bundle de packages d’application sur le disque. Il est inclus dans Microsoft Visual Studio et le kit de développement logiciel (SDK) Windows pour Windows 8 ou le kit de développement logiciel (SDK) Windows pour Windows 8.1. Visitez [téléchargements pour les développeurs]( https://msdn.microsoft.com/windows/apps/br229516.aspx) pour les obtenir.

L’outil MakeAppx.exe se trouve généralement à ces emplacements :

-   Sur x86 : C : \\ Program Files (x86) \\ windows kits \\ 8,0 \\ bin \\ x86 \\makeappx.exe ou C : \\ program files (x86) \\ Windows kits \\ 8,1 \\ bin \\ x86 \\makeappx.exe
-   Sur x64 dans deux emplacements :
    -   C : \\ Program Files (x86) \\ windows kits \\ 8,0 \\ bin \\ x86 \\makeappx.exe ou C : \\ program files (x86) \\ Windows kits \\ 8,1 \\ bin \\ x86 \\makeappx.exe
    -   C : \\ Program Files (x86) \\ windows kits \\ 8,0 \\ bin \\ x64 \\makeappx.exe ou C : \\ program files (x86) \\ Windows kits \\ 8,1 \\ bin \\ x64 \\makeappx.exe

Il n’existe aucune version ARM de l’outil.

-   [Pour créer un package à l’aide d’une structure de répertoires](#to-create-a-package-using-a-directory-structure)
-   [Pour créer un package à l’aide d’un fichier de mappage](#to-create-a-package-using-a-mapping-file)
-   [Pour signer le package à l’aide de SignTool](#to-sign-the-package-using-signtool)
-   [Pour extraire des fichiers d’un package](#to-extract-files-from-a-package)
-   [Pour créer un regroupement de packages à l’aide d’une structure de répertoires](#to-create-a-package-bundle-using-a-directory-structure)
-   [Pour créer un lot de packages à l’aide d’un fichier de mappage](#to-create-a-package-bundle-using-a-mapping-file)
-   [Pour extraire des packages d’un bundle](#to-extract-packages-from-a-bundle)
-   [Pour chiffrer un package à l’aide d’un fichier de clé](#to-encrypt-a-package-with-a-key-file)
-   [Pour chiffrer un package à l’aide d’une clé de test globale](#to-encrypt-a-package-with-a-global-test-key)
-   [Pour déchiffrer un package à l’aide d’un fichier de clé](#to-decrypt-a-package-with-a-key-file)
-   [Pour déchiffrer un package avec une clé de test globale](#to-decrypt-a-package-with-a-global-test-key)
-   [Utilisation](#usage)

## <a name="using-app-packager"></a>Utilisation d’App packager

> [!Note]  
> Les chemins d’accès relatifs sont pris en charge dans l’ensemble de l’outil.

 

### <a name="to-create-a-package-using-a-directory-structure"></a>Pour créer un package à l’aide d’une structure de répertoires

Placez le AppxManifest.xml à la racine d’un répertoire contenant tous les fichiers de charge utile pour votre application. Une structure de répertoires identique est créée pour le package d’application et est disponible lorsque le package est extrait au moment du déploiement.

1.  Placez tous les fichiers dans une structure de répertoire unique, en créant des sous-répertoires selon vos besoins.

2.  Créez un manifeste de package valide, AppxManifest.xml, et placez-le dans le répertoire racine.

3.  Exécutez cette commande :

    **MakeAppx Pack/d** *entrée \_ DirectoryPath* **/p** _filePath_**. AppX**

### <a name="to-create-a-package-using-a-mapping-file"></a>Pour créer un package à l’aide d’un fichier de mappage

1.  Créez un manifeste de package valide, AppxManifest.xml.

2.  Créez un fichier de mappage. La première ligne contient les **\[ fichiers \]** de chaîne et les lignes qui suivent spécifient les chemins source (disque) et de destination (package) dans les chaînes entre guillemets.

    ``` syntax
    [Files]
    "C:\MyApp\StartPage.htm"     "default.html"
    "C:\MyApp\readme.txt"        "doc\readme.txt"
    "\\MyServer\path\icon.png"   "icon.png"
    "MyCustomManifest.xml"       "AppxManifest.xml"
    ```

3.  Exécutez cette commande :

    **MakeAppx Pack/f** *mappage de \_ filePath* **/p** _filePath_**. AppX**

### <a name="to-sign-the-package-using-signtool"></a>Pour signer le package à l’aide de SignTool

1.  Créez le certificat. Le serveur de publication figurant dans le manifeste doit correspondre aux informations d’objet du serveur de publication du certificat de signature. Pour plus d’informations sur la création d’un certificat de signature, consultez [comment créer un certificat de signature de package d’application](how-to-create-a-package-signing-certificate.md).

2.  Exécutez SignTool.exe pour signer le package :

    Le **signe SignTool/a/v/FD** *HashAlgorithm* **/f** *nomfichiercertificat* _filePath_**. AppX**

    *HashAlgorithm* doit correspondre à l’algorithme de hachage utilisé pour créer le blockmap lorsque l’application a été empaquetée. Avec l’utilitaire de Packaging MakeAppx, l’algorithme de hachage du blockmap de l’AppX par défaut est **SHA256**. Exécutez SignTool.exe en spécifiant **SHA256** comme algorithme de résumé de fichier (/FD) :

    Le **signe SignTool/a/v/FD SHA256/F** *nomfichiercertificat* _filePath_**. AppX**

    Pour plus d’informations sur la façon de signer des packages, consultez [Comment signer un package d’application à l’aide de SignTool](how-to-sign-a-package-using-signtool.md).

### <a name="to-extract-files-from-a-package"></a>Pour extraire des fichiers d’un package

1.  Exécutez cette commande :

    **MakeAppx décompresser** le _fichier_/p **. AppX/d** *\_ Répertoire de sortie*

2.  Le package décompressé a la même structure que le package installé.

### <a name="to-create-a-package-bundle-using-a-directory-structure"></a>Pour créer un regroupement de packages à l’aide d’une structure de répertoires

Nous utilisons la commande **Bundle** pour créer un bundle d’applications à l’adresse <output bundle name> en ajoutant tous les packages de <content directory> (y compris les sous-dossiers). Si <content directory> contient un manifeste de Bundle, AppxBundleManifest.xml, il est ignoré.

1.  Placez tous les packages dans une structure de répertoire unique, en créant des sous-répertoires comme vous le souhaitez.

2.  Exécutez cette commande :

    **Bundle MakeAppx/d** *entrée \_ DirectoryPath* **/p** _filePath_**. appxbundle**

### <a name="to-create-a-package-bundle-using-a-mapping-file"></a>Pour créer un lot de packages à l’aide d’un fichier de mappage

Nous utilisons la commande **Bundle** pour créer un bundle d’applications à l’adresse <output bundle name> en ajoutant tous les packages à partir d’une liste de packages dans <mapping file> . Si <mapping file> contient un manifeste de Bundle, AppxBundleManifest.xml, il est ignoré.

1.  Créez un <mapping file>. La première ligne contient les **\[ fichiers \]** de chaîne et les lignes qui suivent spécifient les packages à ajouter au bundle. Chaque package est décrit par une paire de chemins d’accès entre guillemets, séparés par des espaces ou des tabulations. La paire de chemins représente la source (sur disque) et la destination du package (dans le cas d’une offre groupée). Tous les noms de package de destination doivent avoir l’extension. Appx.

    ``` syntax
        [Files]
        "C:\MyApp\MyApp_x86.appx"                 "MyApp_x86.appx"
        "C:\Program Files (x86)\ResPack.appx"    "resources\resPack.appx"
        "\\MyServer\path\ResPack.appx"           "Respack.appx"
        "my app files\respack.appx"              "my app files\respack.appx"
    ```

2.  Exécutez cette commande :

    **Package MakeAppx/f** *mappage de \_ filePath* **/p** _filePath_**. appxbundle**

### <a name="to-extract-packages-from-a-bundle"></a>Pour extraire des packages d’un bundle

1.  Exécutez cette commande :

    **MakeAppx désassocier/p** _\_ nom de l’offre groupée_**. appxbundle/d** *\_ Répertoire de sortie*

2.  L’offre groupée décompressée a la même structure que l’offre groupée de packages installée.

### <a name="to-encrypt-a-package-with-a-key-file"></a>Pour chiffrer un package à l’aide d’un fichier de clé

1.  Créez un fichier de clé. Les fichiers de clés doivent commencer par une ligne contenant la chaîne « \[ Keys \] » suivie de lignes décrivant les clés avec lesquelles chiffrer le package. Chaque clé est décrite par une paire de chaînes entre guillemets, en les séparant par des espaces ou des tabulations. La première chaîne représente l’ID de clé et la deuxième chaîne représente la clé de chiffrement au format hexadécimal.

    ``` syntax
        [Keys]
        "0"                 "1AC4CDCFF1924D2885A0607269787BA6BF09B7FFEBF74ED4B9D86E423CF9186B"
    ```

2.  Exécutez cette commande :

    **MakeAppx.exe chiffrer/p** _\_ nom du package_**. AppX/EP** _\_ \_ nom du package chiffré_**. eappx/KF** _keyfile \_ Name_**. txt**

3.  Le package d’entrée sera chiffré dans le package chiffré spécifié à l’aide du fichier de clé fourni.

### <a name="to-encrypt-a-package-with-a-global-test-key"></a>Pour chiffrer un package à l’aide d’une clé de test globale

1.  Exécutez cette commande :

    **MakeAppx.exe chiffrer/p** _\_ nom du package_**. AppX/EP** _\_ \_ nom du package chiffré_**. eappx/kt**

2.  Le package d’entrée sera chiffré dans le package chiffré spécifié à l’aide de la clé de test globale.

### <a name="to-decrypt-a-package-with-a-key-file"></a>Pour déchiffrer un package à l’aide d’un fichier de clé

1.  Créez un fichier de clé. Les fichiers de clés doivent commencer par une ligne contenant la chaîne « \[ Keys \] » suivie de lignes décrivant les clés avec lesquelles chiffrer le package. Chaque clé est décrite par une paire de chaînes entre guillemets, en les séparant par des espaces ou des tabulations. La première chaîne représente l’ID de clé de 32 octets encodé en base64, tandis que la deuxième chaîne représente la clé de chiffrement de 32 octets encodée en base64.

    ``` syntax
        [Keys]
        "OWVwSzliRGY1VWt1ODk4N1Q4R2Vqc04zMzIzNnlUREU="                 "MjNFTlFhZGRGZEY2YnVxMTBocjd6THdOdk9pZkpvelc="
    ```

2.  Exécutez cette commande :

    **MakeAppx.exe déchiffrer/p** _\_ nom du package_**. AppX/EP** _\_ \_ nom du package non chiffré_**. eappx/KF** _keyfile \_ Name_**. txt**

3.  Le package d’entrée sera déchiffré dans le package non chiffré spécifié à l’aide du fichier de clé fourni.

### <a name="to-decrypt-a-package-with-a-global-test-key"></a>Pour déchiffrer un package avec une clé de test globale

1.  Exécutez cette commande :

    **MakeAppx.exe déchiffrer/p** _\_ nom du package_**. AppX/EP** _\_ \_ nom du package non chiffré_**. eappx/kt**

2.  Le package d’entrée sera déchiffré dans le package non chiffré spécifié à l’aide de la clé de test globale.

## <a name="usage"></a>Utilisation

L’argument de ligne de commande **/p** est toujours requis, avec **/d**, **/f** ou **/EP**. Notez que **/d**, **/f** et **/EP** s’excluent mutuellement.

**\[ Options \] du Pack MakeAppx** **/p** *\<output package name\>* **/d***\<content directory\>*

**\[ Options \] du Pack MakeAppx** **/p** *\<output package name\>* **/f***\<mapping file\>*

**\[ Options \] de décompression MakeAppx** **/p** *\<input package name\>* **/d***\<output directory\>*

**\[ Options \] du bundle MakeAppx** **/p** *\<output bundle name\>* **/d***\<content directory\>*

**\[ Options \] du bundle MakeAppx** **/p** *\<output bundle name\>* **/f***\<mapping file\>*

**MakeAppx dégrouper les \[ options \]** **/p** *\<input bundle name\>* **/d***\<output directory\>*

**\[ Options \] Encrypt MakeAppx** **/p** *\<input package name\>* **/EP***\<output package name\>*

**\[ Options \] de déchiffrement MakeAppx** **/p** *\<input package name\>* **/EP***\<output package name\>*

## <a name="command-line-syntax"></a>Syntaxe de ligne de commande

Voici la syntaxe d’utilisation courante de la ligne de commande pour MakeAppx.

**MakeAppx \[ Pack \| déballer \| \| dégrouper \| chiffrer/ \| déchiffrer \]** \[ **/h** **/KF** **/kt** **/l** **/o** **/non** **/NV** **/v** **/PFN** **/ ?**\]

**MakeAppx** packs ou décompresse les fichiers dans un package, regroupe ou dissocie les packages dans un bundle, ou chiffre ou déchiffre le package d’application ou le bundle dans le répertoire d’entrée ou le fichier de mappage spécifié. Voici la liste des paramètres qui s’appliquent à **MakeAppx Pack**, **MakeAppx décompresser**, **MakeAppx Bundle**, **MakeAppx dégrouper**, **MakeAppx chiffrer** ou **MakeAppx déchiffrer**.

<dl> <dt>

<span id="_l"></span><span id="_L"></span>**/l**
</dt> <dd>

Cette option est utilisée pour les packages localisés. La valeur par défaut se déclenche sur les packages localisés. Cette option désactive uniquement cette validation spécifique, sans exiger que toutes les validations soient désactivées.

</dd> <dt>

<span id="_o"></span><span id="_O"></span>**/o**
</dt> <dd>

Remplacez le fichier de sortie s’il existe. Si vous ne spécifiez pas cette option ou l’option **/non** , l’utilisateur est invité à indiquer s’il souhaite remplacer le fichier.

Vous ne pouvez pas utiliser cette option avec la commande **/non**.

</dd> <dt>

<span id="_no"></span><span id="_NO"></span>**/non**
</dt> <dd>

Empêche le remplacement du fichier de sortie s’il existe. Si vous ne spécifiez pas cette option ou l’option **/o** , l’utilisateur est invité à indiquer s’il souhaite remplacer le fichier.

Vous ne pouvez pas utiliser cette option avec **/o**.

</dd> <dt>

<span id="_nv"></span><span id="_NV"></span>**/nv**
</dt> <dd>

Ignore la validation sémantique. Si vous ne spécifiez pas cette option, l’outil effectue une validation complète du package.

</dd> <dt>

<span id="_v"></span><span id="_V"></span>**/f**
</dt> <dd>

Activez la journalisation détaillée dans la console.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Affichez le texte d’aide.

</dd> </dl>

**MakeAppx Pack** , **MakeAppx DEBALLER** , **MakeAppx Bundle**, **MakeAppx debundle**, **MakeAppx Encrypt** et **MakeAppx decrypte** sont des commandes mutuellement exclusives. Voici les paramètres de ligne de commande qui s’appliquent spécifiquement à chaque commande :

**Pack MakeAppx** \[ **h**\]

Crée un package.

<dl> <dt>

<span id="_h_algorithm"></span><span id="_H_ALGORITHM"></span> *algorithme* /h
</dt> <dd>

Spécifie l’algorithme de hachage à utiliser lors de la création du mappage de bloc. Voici les valeurs valides pour l' *algorithme*:

<dl> <dd>SHA256 (par défaut)</dd> <dd>SHA384</dd> <dd>SHA512</dd> </dl>

Vous ne pouvez pas utiliser cette option avec la commande **décompresser** .

</dd> </dl>

**Décompression MakeAppx** \[ **PFN**\]

Extrait tous les fichiers du package spécifié dans le répertoire de sortie spécifié. La sortie a la même structure de répertoire que le package.

<dl> <dt>

<span id="_pfn"></span><span id="_PFN"></span>**/pfn**
</dt> <dd>

Spécifie un répertoire nommé avec le nom complet du package. Ce répertoire est créé sous l’emplacement de sortie fourni. Vous ne pouvez pas utiliser cette option avec la commande **Pack** .

</dd> </dl>

**Désassemblage MakeAppx** \[ **PFN**\]

Décompresse tous les packages dans un sous-répertoire sous le chemin de sortie spécifié, nommé d’après le nom complet du bundle. La sortie a la même structure de répertoire que l’offre groupée de packages installée.

<dl> <dt>

<span id="_pfn"></span><span id="_PFN"></span>**/pfn**
</dt> <dd>

Spécifie un répertoire nommé avec le nom complet du groupement de packages. Ce répertoire est créé sous l’emplacement de sortie fourni. Vous ne pouvez pas utiliser cette option avec la commande **Bundle** .

</dd> </dl>

**Chiffrement MakeAppx** \[ **KF**, **kt**\]

Crée un package d’application chiffré à partir du package d’application d’entrée spécifié au package de sortie spécifié.

<dl> <dt>

<span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/KF***<key file>*
</dt> <dd>

Chiffre le package ou le bundle à l’aide de la clé du fichier de clé spécifié. Vous ne pouvez pas utiliser cette option avec **kt**.

</dd> <dt>

<span id="_kt"></span><span id="_KT"></span>**/kt**
</dt> <dd>

Chiffre le package ou le bundle à l’aide de la clé de test globale. Vous ne pouvez pas utiliser cette option avec **KF**.

</dd> </dl>

**Déchiffrement MakeAppx** \[ **KF**, **kt**\]

Crée un package d’application non chiffré à partir du package d’application d’entrée spécifié au package de sortie spécifié.

<dl> <dt>

<span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/KF***<key file>*
</dt> <dd>

Déchiffre le package ou l’offre groupée à l’aide de la clé du fichier de clé spécifié. Vous ne pouvez pas utiliser cette option avec **kt**.

</dd> <dt>

<span id="_kt"></span><span id="_KT"></span>**/kt**
</dt> <dd>

Déchiffre le package ou le bundle à l’aide de la clé de test globale. Vous ne pouvez pas utiliser cette option avec **KF**.

</dd> </dl>

## <a name="semantic-validation-performed-by-makeappx"></a>Validation sémantique effectuée par MakeAppx

MakeAppx effectue une validation sémantique limitée qui est conçue pour intercepter les erreurs de déploiement les plus courantes et pour s’assurer que le package d’application est valide.

Cette validation vérifie que :

-   tous les fichiers référencés dans le manifeste du package sont inclus dans le package d’application ;
-   une application n’a pas deux clés identiques ;
-   Une application ne s’inscrit pas pour un protocole interdit dans cette liste : SMB, fichier, MS-WWA-WEB, MS-WWA.

Cette validation sémantique n’est pas terminée, et il n’est pas garanti que les packages générés par MakeAppx soient installés.

 

 