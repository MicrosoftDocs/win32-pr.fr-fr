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
# <a name="how-to-sign-an-app-package-using-signtool"></a>Comment signer un package d’application à l’aide de SignTool

> [!Note]  
> Pour signer un package d’application Windows, consultez [signer un package d’application à l’aide de SignTool](/windows/msix/package/sign-app-package-using-signtool).

 

Découvrez comment utiliser [**SignTool**](/windows-hardware/drivers/devtest/signtool) pour signer vos packages d’application Windows pour qu’ils puissent être déployés. [**SignTool**](/windows-hardware/drivers/devtest/signtool) fait partie du kit de développement logiciel (SDK) Windows.

Tous les packages d’application Windows doivent être signés numériquement avant de pouvoir être déployés. Alors que Microsoft Visual Studio 2012 et versions ultérieures peuvent signer un package d’application lors de sa création, les packages que vous créez à l’aide de l’outil [app Packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) de la SDK Windows ne sont pas signés.

> [!Note]  
> Vous pouvez utiliser uniquement [**SignTool**](/windows-hardware/drivers/devtest/signtool) pour signer vos packages d’application Windows sur Windows 8 et versions ultérieures, ou windows server 2012 et versions ultérieures. Vous ne pouvez pas utiliser **SignTool** pour signer des packages d’application sur des systèmes d’exploitation de niveau supérieur tels que Windows 7 ou windows Server 2008 R2.

 

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Présentation de la signature de code](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Packages d’applications et déploiement](/previous-versions/windows/apps/hh464929(v=win.10))
-   [Outils pour signer des fichiers et vérifier les signatures](/windows/desktop/SecCrypto/tools-to-sign-files-and-check-signatures)

### <a name="prerequisites"></a>Prérequis

-   [**SignTool**](/windows-hardware/drivers/devtest/signtool), qui fait partie de l’SDK Windows
-   Un certificat de signature de code valide, par exemple, un fichier d’échange d’informations personnelles (. pfx) créé avec les outils [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) et [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx)

    Pour plus d’informations sur la création d’un certificat de signature de code valide, consultez [comment créer un certificat de signature de package d’application](how-to-create-a-package-signing-certificate.md).

-   Une application Windows empaquetée, par exemple, un fichier. AppX créé à l’aide de l’outil [app Packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md)

**Considérations supplémentaires**

Le certificat que vous utilisez pour signer le package d’application doit respecter les critères suivants :

-   Le nom du sujet du certificat doit correspondre à l’attribut du serveur de **publication** contenu dans l’élément [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) du fichier AppxManifest.xml stocké dans le package. Le nom de l’éditeur faisant partie de l’identité d’une application Windows empaquetée, vous devez faire en sorte que le nom du sujet du certificat corresponde au nom de l’éditeur de l’application. Cela permet de vérifier l’identité des packages signés par rapport à la signature numérique. Pour plus d’informations sur la signature des erreurs susceptibles de se produire lors de la signature d’un package d’application à l’aide de [**SignTool**](/windows-hardware/drivers/devtest/signtool), consultez la section Notes de la rubrique [comment créer un certificat de signature de package d’application](how-to-create-a-package-signing-certificate.md).
-   Le certificat doit être valide pour la signature de code. Cela signifie que ces deux éléments doivent être vrais :

    -   Le champ utilisation améliorée de la clé du certificat doit être désactivé ou contenir la valeur EKU pour la signature de code (1.3.6.1.5.5.7.3.3).
    -   Le champ utilisation de la clé (KU) du certificat doit être désactivé ou contenir le bit d’utilisation pour la signature numérique (0x80).

-   Le certificat contient une clé privée.
-   Le certificat est valide. Il est actif, n’a pas expiré et n’a pas été révoqué.

## <a name="instructions"></a>Instructions

### <a name="step-1-determine-the-hash-algorithm-to-use"></a>Étape 1 : déterminer l’algorithme de hachage à utiliser

Lorsque vous signez le package d’application, vous devez utiliser le même algorithme de hachage que celui que vous avez utilisé lors de la création du package d’application. Si vous avez utilisé les paramètres par défaut pour créer le package d’application, l’algorithme de hachage utilisé est SHA256.

Si vous avez utilisé App Packager avec un algorithme de hachage spécifique pour créer le package d’application, utilisez le même algorithme pour signer le package. Pour déterminer l’algorithme de hachage à utiliser pour la signature d’un package, vous pouvez extraire le contenu du package et inspecter le fichier AppxBlockMap.xml. L’attribut **HashMethod** de l’élément [**blockmap**](/uwp/schemas/blockmapschema/element-blockmap) indique l’algorithme de hachage qui a été utilisé lors de la création du package d’application. Par exemple :

``` syntax
<BlockMap xmlns="http://schemas.microsoft.com/appx/2010/blockmap" 
HashMethod="https://www.w3.org/2001/04/xmlenc#sha256">
```

L’élément [**blockmap**](/uwp/schemas/blockmapschema/element-blockmap) précédent indique que l’algorithme SHA256 a été utilisé. Ce tableau répertorie le mappage des algorithmes actuellement disponibles :

| Valeur **HashMethod**                            | *HashAlgorithm* à utiliser |
|-------------------------------------------------|------------------------|
| <https://www.w3.org/2001/04/xmlenc#sha256>       | SHA256 (valeur par défaut. AppX) |
| <https://www.w3.org/2001/04/xmldsig-more#sha384> | SHA384                 |
| <https://www.w3.org/2001/04/xmlenc#sha512>       | SHA512                 |



 

### <a name="step-2-run-signtoolexe-to-sign-the-package"></a>Étape 2 : exécuter SignTool.exe pour signer le package

**Pour signer le package avec un certificat de signature à partir d’un fichier. pfx**

-   ``` syntax
    SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password filepath.appx
    ```

[**SignTool**](/windows-hardware/drivers/devtest/signtool) utilise par défaut le paramètre/FD *HashAlgorithm* sur SHA1 s’il n’est pas spécifié, et SHA1 n’est pas valide pour la signature des packages d’application. Vous devez donc spécifier ce paramètre lorsque vous signez un package d’application. Pour signer un package d’application créé avec le hachage SHA256 par défaut, vous devez spécifier le paramètre/FD *HashAlgorithm* en tant que SHA256 :

``` syntax
SignTool sign /fd SHA256 /a /f signingCert.pfx /p password filepath.appx
```

Vous pouvez omettre le paramètre *de mot de passe* /p Si vous utilisez un fichier. pfx qui n’est pas protégé par un mot de passe. Vous pouvez également utiliser d’autres options de sélection de certificat qui sont prises en charge par [**SignTool**](/windows-hardware/drivers/devtest/signtool) pour signer des packages d’application. Pour plus d’informations sur ces options, consultez [SignTool](/windows/desktop/SecCrypto/signtool).

> [!Note]  
> Vous ne pouvez pas utiliser l’opération d’horodatage [**SignTool**](/windows-hardware/drivers/devtest/signtool) sur un package d’application signé ; l’opération n’est pas prise en charge.

 

Si vous souhaitez horodater le package de l’application, vous devez le faire pendant l’opération de signature. Par exemple :

``` syntax
SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password /tr timestampServerUrl 
filepath.appx
```

Définissez le paramètre/TR *timestampServerUrl* sur l’URL d’un serveur de datage RFC 3161.

## <a name="remarks"></a>Notes

Cette section traite de la résolution des erreurs de signature des packages d’application.

### <a name="troubleshooting-app-package-signing-errors"></a>Résolution des erreurs de signature des packages d’application

En plus des erreurs de signature que [**SignTool**](/windows-hardware/drivers/devtest/signtool) peut retourner, **SignTool** peut également retourner des erreurs spécifiques à la signature des packages d’application. Ces erreurs apparaissent généralement sous la forme d’erreurs internes :

``` syntax
SignTool Error: An unexpected internal error has occurred.
Error information: "Error: SignerSign() failed." (-2147024885 / 0x8007000B) 
```

Si le code d’erreur commence par 0x8008, tel que 0x80080206 \_ AppX \_ E \_ contenu endommagé), cela indique que le package en cours de signature n’est pas valide. Dans ce cas, avant de pouvoir signer le package, vous devez régénérer le package. Pour obtenir la liste complète des \* Erreurs 0x8008, consultez [**codes d’erreur com (sécurité et configuration)**](/windows/desktop/com/com-error-codes-4).

Plus généralement, l’erreur est 0x8007000b (format erroné de l’erreur \_ \_ ). Dans ce cas, vous pouvez trouver des informations d’erreur plus spécifiques dans le journal des événements :

**Pour rechercher dans le journal des événements**

1.  Exécutez eventvwr. msc.
2.  Ouvrez le journal des événements : observateur d’événements (local) > les journaux des applications et des services > Microsoft > Windows > AppxPackagingOM > Microsoft-Windows-AppxPackaging/Operational
3.  Recherchez l’événement d’erreur le plus récent.

L’erreur interne correspond généralement à l’un des éléments suivants :

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>ID de l’événement</th>
<th>Exemple de chaîne d’événement</th>
<th>Suggestion</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>150</td>
<td>erreur 0x8007000B : le nom de l’éditeur du manifeste de l’application (CN = contoso) doit correspondre au nom du sujet du certificat de signature (CN = contoso, C = US).</td>
<td>Le nom de l’éditeur du manifeste de l’application doit correspondre exactement au nom du sujet de la signature.
<blockquote>
[!Note]<br />
Ces noms sont spécifiés entre guillemets et respectent tous deux la casse et l’espace blanc.
</blockquote>
<br/> Vous pouvez mettre à jour la chaîne d’attribut du serveur de <strong>publication</strong> définie pour l’élément <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity</strong></a> dans le fichier AppxManifest.xml pour qu’elle corresponde au nom du sujet du certificat de signature prévu. Ou sélectionnez un autre certificat de signature avec un nom d’objet qui correspond au nom de l’éditeur du manifeste de l’application. Le nom de l’éditeur du manifeste et le nom de l’objet du certificat sont répertoriés dans le message de l’événement.</td>
</tr>
<tr class="even">
<td>151</td>
<td>erreur 0x8007000B : la méthode de hachage de signature spécifiée (SHA512) doit correspondre à la méthode de hachage utilisée dans le mappage de bloc de package d’application (SHA256).</td>
<td>Le hashAlgorithm spécifié dans le paramètre/fd est incorrect (voir étape 1 : déterminer l’algorithme de hachage à utiliser). Exécutez à nouveau <a href="/windows-hardware/drivers/devtest/signtool"><strong>SignTool</strong></a> avec HashAlgorithm qui correspond au mappage de bloc de package d’application.</td>
</tr>
<tr class="odd">
<td>152</td>
<td>erreur 0x8007000B : le contenu du package d’application doit être validé par rapport à son mappage de bloc.</td>
<td>Le package d’application est endommagé et doit être régénéré pour générer un nouveau mappage de bloc. Pour plus d’informations sur la création d’un package d’application, consultez Création d’un package d’application avec <a href="make-appx-package--makeappx-exe-.md">app Packager</a> ou <a href="/previous-versions/hh975357(v=vs.110)">création d’un package d’application avec Visual Studio 2012</a>.</td>
</tr>
</tbody>
</table>



 

## <a name="security-considerations"></a>Considérations relatives à la sécurité

Une fois le package signé, le certificat que vous avez utilisé pour signer le package doit toujours être approuvé par l’ordinateur sur lequel le package doit être déployé. En ajoutant un certificat aux [magasins de certificats de l’ordinateur local](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), vous affectez le certificat de confiance de tous les utilisateurs sur l’ordinateur. Nous vous recommandons d’installer les certificats de signature de code que vous souhaitez pour tester des packages d’application dans le magasin de certificats personnes autorisées, et de supprimer rapidement ces certificats quand vous n’en avez plus besoin. Si vous créez vos propres certificats de test pour la signature des packages d’application, nous vous recommandons également de limiter les privilèges associés au certificat de test. Pour plus d’informations sur la création de certificats de test pour la signature de packages d’application, consultez [comment créer un certificat de signature de package d’application](how-to-create-a-package-signing-certificate.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Exemples**
</dt> <dt>

[Exemple de création de package d’application](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**Concepts**
</dt> <dt>

[Meilleures pratiques pour la signature de code](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
</dt> <dt>

[Signature d’un package dans Visual Studio 2012](/previous-versions/br230260(v=vs.110))
</dt> <dt>

[SignTool](/windows/desktop/SecCrypto/signtool)
</dt> <dt>

[Package d’application (MakeAppx.exe)](make-appx-package--makeappx-exe-.md)
</dt> <dt>

[Création d’un certificat de signature de package d’application](how-to-create-a-package-signing-certificate.md)
</dt> </dl>

