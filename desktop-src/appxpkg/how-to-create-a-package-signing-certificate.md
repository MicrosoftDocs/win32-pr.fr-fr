---
title: How to create an app package signing certificate (Comment créer un certificat de signature de package d’application)
description: découvrez comment utiliser MakeCert.exe et Pvk2Pfx.exe pour créer un certificat de signature de code de test afin de pouvoir signer vos packages d’application Windows.
ms.assetid: DEDD3727-3F0E-403D-9A6E-55949E98FE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc495c27e63dc4ee3a42db1b2763f4f59f7647a3a98d20193d8049dcfad965c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049067"
---
# <a name="how-to-create-an-app-package-signing-certificate"></a>How to create an app package signing certificate (Comment créer un certificat de signature de package d’application)

> [!IMPORTANT]
> MakeCert.exe est déconseillé. Pour plus d’informations sur la création d’un certificat, consultez [créer un certificat pour la signature de package](/windows/msix/package/create-certificate-package-signing).

 

découvrez comment utiliser [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) et [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) pour créer un certificat de signature de code de test afin de pouvoir signer vos packages d’application Windows.

vous devez signer numériquement vos applications Windows empaquetées avant de les déployer. si vous n’utilisez pas Microsoft Visual Studio 2012 pour créer et signer vos packages d’application, vous devez créer et gérer vos propres certificats de signature de code. vous pouvez créer des certificats à l’aide de [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) et [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) à partir du Kit de pilotes Windows (WDK). Ensuite, vous pouvez utiliser les certificats pour signer les packages d’application, afin qu’ils puissent être déployés localement à des fins de test.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Présentation de la signature de code](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Packages d’applications et déploiement](/previous-versions/windows/apps/hh464929(v=win.10))
-   [Outils pour la signature des pilotes](/windows-hardware/drivers/devtest/tools-for-signing-drivers)

### <a name="prerequisites"></a>Prérequis

-   Outils de [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) et de [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) à partir du kit WDK

## <a name="instructions"></a>Instructions

### <a name="step-1-determine-the-publisher-name-of-the-package"></a>Étape 1 : déterminer le nom de l’éditeur du package

pour que le certificat de signature que vous créez soit utilisable avec le package d’application que vous souhaitez signer, le nom du sujet du certificat de signature doit correspondre à l’attribut **Publisher** de l’élément [**identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) dans le AppxManifest.xml de cette application. Par exemple, supposons que le AppxManifest.xml contient :

``` syntax
  <Identity Name="Contoso.AssetTracker" 
    Version="1.0.0.0" 
    Publisher="CN=Contoso Software, O=Contoso Corporation, C=US"/>
```

Pour le paramètre *PublisherName* que vous spécifiez avec l’utilitaire [**Makecert**](/windows-hardware/drivers/devtest/makecert) à l’étape suivante, utilisez « CN = contoso Software, O = Contoso Corporation, C = US ».

> [!Note]  
> Cette chaîne de paramètres est spécifiée entre guillemets et respecte à la fois la casse et l’espace blanc.

 

la chaîne d’attribut **Publisher** définie pour l’élément [**identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) dans le AppxManifest.xml doit être identique à la chaîne que vous spécifiez avec le paramètre [**MakeCert**](/windows-hardware/drivers/devtest/makecert) /n pour le nom d’objet du certificat. Copiez et collez la chaîne dans la mesure du possible.

### <a name="step-2-create-a-private-key-using-makecertexe"></a>Étape 2 : créer une clé privée à l’aide de MakeCert.exe

Utilisez l’utilitaire [**Makecert**](/windows-hardware/drivers/devtest/makecert) pour créer un certificat de test auto-signé et une clé privée :

``` syntax
MakeCert /n publisherName /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 
expirationDate /sv MyKey.pvk MyKey.cer
```

Cette commande vous invite à fournir un mot de passe pour le fichier. pvk. Nous vous recommandons de choisir un [mot de passe fort](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) et de conserver votre clé privée dans un emplacement sécurisé.

Nous vous recommandons d’utiliser les paramètres suggérés dans l’exemple précédent pour les raisons suivantes :

<dl> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Crée un certificat racine auto-signé. Cela simplifie la gestion de votre certificat de test.

</dd> <dt>

<span id="_h_0"></span><span id="_H_0"></span>**/h 0**
</dt> <dd>

Marque la contrainte de base pour le certificat comme une entité finale. Cela empêche l’utilisation du certificat en tant qu’autorité de certification (CA) susceptible d’émettre d’autres certificats.

</dd> <dt>

<span id="_eku"></span><span id="_EKU"></span>**/eku**
</dt> <dd>

Définit les valeurs de l’utilisation améliorée de la clé pour le certificat.

> [!Note]  
> Ne placez pas d’espace entre les deux valeurs délimitées par des virgules.

 

-   1.3.6.1.5.5.7.3.3 indique que le certificat est valide pour la signature de code. Spécifiez toujours cette valeur pour limiter l’utilisation prévue du certificat.
-   1.3.6.1.4.1.311.10.3.13 indique que le certificat respecte la signature de la durée de vie. En règle générale, si une signature est horodatée, tant que le certificat était valide au moment où il a été horodaté, la signature reste valide même si le certificat expire. Cette utilisation améliorée de la valeur force la signature à expirer, que la signature soit ou non horodatée.

</dd> <dt>

<span id="_e"></span><span id="_E"></span>**/e**
</dt> <dd>

Définit la date d’expiration du certificat. Fournissez une valeur pour le paramètre *expirationDate* au format mm/jj/aaaa. Nous vous recommandons de choisir une date d’expiration uniquement si nécessaire à des fins de test, en général moins d’un an. Cette date d’expiration, conjointement avec l’utilisation améliorée de la signature de durée de vie, permet de limiter la fenêtre dans laquelle le certificat peut être compromis et utilisé de façon inutilisée.

</dd> </dl>

Pour plus d’informations sur les autres options, consultez [**Makecert**](/windows-hardware/drivers/devtest/makecert).

### <a name="step-3-create-a-personal-information-exchange-pfx-file-using-pvk2pfxexe"></a>étape 3 : créer un fichier de Exchange d’informations personnelles (. pfx) à l’aide de Pvk2Pfx.exe

Utilisez l’utilitaire [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) pour convertir les fichiers. pvk et. [**CER créés dans**](/windows-hardware/drivers/devtest/makecert) un fichier. pfx que vous pouvez utiliser avec [SignTool](/windows/desktop/SecCrypto/signtool) pour signer un package d’application :

``` syntax
Pvk2Pfx /pvk MyKey.pvk /pi pvkPassword /spc MyKey.cer /pfx MyKey.pfx [/po pfxPassword]
```

Les fichiers *myKey. pvk* et *myKey. cer* sont les mêmes que ceux [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) créés à l’étape précédente. En utilisant le paramètre facultatif/po, vous pouvez spécifier un autre mot de passe pour le fichier. pfx qui en résulte. dans le cas contraire, le fichier. pfx a le même mot de passe que *myKey. pvk*.

Pour plus d’informations sur les autres options, consultez [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx).

## <a name="remarks"></a>Remarques

Une fois que vous avez créé le fichier. pfx, vous pouvez utiliser le fichier avec [SignTool](/windows/desktop/SecCrypto/signtool) pour signer un package d’application. Pour plus d’informations, consultez [Comment signer un package d’application à l’aide de SignTool](how-to-sign-a-package-using-signtool.md). Toutefois, le certificat n’est toujours pas approuvé par l’ordinateur local pour le déploiement de packages d’application tant que vous ne l’avez pas installé dans le magasin de certificats de confiance de l’ordinateur local. Vous pouvez utiliser [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)), qui est fourni avec Windows.

**Pour installer des certificats avec WindowsCertutil.exe**

1.  Exécutez **Cmd.exe** en tant qu’administrateur.
2.  Exécutez cette commande :

    ``` syntax
    Certutil -addStore TrustedPeople MyKey.cer
    ```

Nous vous recommandons de supprimer les certificats s’ils ne sont plus utilisés. À partir de la même invite de commandes administrateur, exécutez la commande suivante :

``` syntax
Certutil -delStore TrustedPeople certID
```

La valeur **certID** est le numéro de série du certificat. Exécutez cette commande pour déterminer le numéro de série du certificat :

``` syntax
Certutil -store TrustedPeople
```

## <a name="security-considerations"></a>Considérations relatives à la sécurité

En ajoutant un certificat aux [magasins de certificats de l’ordinateur local](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), vous affectez le certificat de confiance de tous les utilisateurs sur l’ordinateur. Nous vous recommandons d’installer les certificats de signature de code que vous souhaitez pour tester des packages d’application dans le magasin de certificats personnes autorisées. Supprimez rapidement ces certificats lorsqu’ils ne sont plus nécessaires pour les empêcher d’être utilisés pour compromettre la confiance du système.

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

[Comment signer un package d’application à l’aide de SignTool](how-to-sign-a-package-using-signtool.md)
</dt> <dt>

[Signature d’un package d’application](/previous-versions/br230260(v=vs.110))
</dt> </dl>

 

 