---
title: Protection des fichiers avec DRM version 7 ou ultérieure
description: Protection des fichiers avec DRM version 7 ou ultérieure
ms.assetid: 906f16c1-6573-47e9-8228-58dc126f6357
keywords:
- Windows Media Format SDK, création de fichiers protégés
- Windows Media Format SDK, fichiers protégés
- ASF (Advanced Systems Format), création de fichiers protégés
- ASF (format des systèmes avancés), création de fichiers protégés
- ASF (Advanced Systems Format), fichiers protégés
- ASF (Advanced Systems Format), fichiers protégés
- ASF (Advanced Systems Format), WMStubDRM. lib
- ASF (format avancé des systèmes), WMStubDRM. lib
- WMStubDRM. lib, création de fichiers protégés
- WMStubDRM. lib, fichiers protégés
- gestion des droits numériques (DRM), WMStubDRM. lib
- DRM (gestion des droits numériques), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee809ea73401f22e4554e74c2ecb8855a0384e0
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "106513705"
---
# <a name="protecting-files-with-drm-version-7-or-later"></a>Protection des fichiers avec DRM version 7 ou ultérieure

Pour protéger des fichiers avec Windows Media DRM version 7 ou ultérieure, utilisez la méthode [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) de l’objet Writer pour définir des attributs DRM. Étant donné que la gestion des droits numériques (DRM) version 7 et les versions ultérieures autorisent des licences uniques pour chaque fichier protégé ou ensemble de fichiers, l’interface **IWMDRMWriter** a également des méthodes pour la création de clés. Ces méthodes sont fournies uniquement à des fins de commodité.

Pour protéger des fichiers ASF à l’aide de DRM version 7 ou ultérieure, procédez comme suit :

1.  Liez à WMStubDRM. lib et, si nécessaire, dissociez wmvcore. lib.
2.  Appelez la fonction [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) pour créer l’enregistreur DRM. Le premier argument est réservé et doit avoir la valeur **null**.
3.  Définissez un profil que le writer doit utiliser en appelant [**IWMWriter :: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) ou [**IWMWriter :: SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid). Vous devez définir un profil dans l’enregistreur avant de définir des attributs DRM. DRM est pris en charge uniquement pour les profils qui utilisent les codecs Windows Media Audio ou Windows Media Video
4.  Obtenez l’interface [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) de l’objet Writer.
5.  Appelez [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) et définissez [**utiliser \_ \_ DRM avancé**](use-advanced-drm.md) sur **true**.
6.  Si vous devez générer une nouvelle valeur initiale de clé, appelez [**IWMDRMWriter :: GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed). Dans la plupart des cas, vous allez réutiliser un Seed de clé qui a été généré précédemment. Cette valeur doit rester secrète ; Il n’est pas écrit dans le fichier.
7.  Appelez [**IWMDRMWriter :: GenerateKeyID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyid) pour créer un ID de clé, qui est la deuxième valeur utilisée pour créer la clé réelle. Contrairement à la valeur initiale de la clé, l’ID de clé est public et est écrit dans le fichier dans l’en-tête DRM en clair. Créez un nouvel ID de clé pour chaque nouveau fichier que vous créez.
8.  Appelez **IWMDRMWriter :: GenerateSigningKeyPair** si nécessaire pour générer une clé publique et privée qui sera utilisée pour signer l’objet d’en-tête ASF DRM avancé. Pour plus d’informations sur ces clés, consultez [**IWMDRMWriter :: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair).
9.  Si nécessaire, obtenez les valeurs pour remplir l’objet de signature numérique de l’en-tête DRM. Si vous n’avez pas de version de travail du gestionnaire de droits Windows Media installée sur votre système, vous devez configurer l’objet de signature numérique de l’en-tête de fichier ASF en spécifiant les quatre attributs suivants, qui doivent tous être obtenus auprès de Microsoft :

    -   [**\_LASIGNATUREROOTCERT DRM**](drm-lasignaturerootcert.md)
    -   [**\_LASIGNATURECERT DRM**](drm-lasignaturecert.md)
    -   [**\_LASIGNATURELICSRVCERT DRM**](drm-lasignaturelicsrvcert.md)
    -   [**\_LASIGNATUREPRIVKEY DRM**](drm-lasignatureprivkey.md)

    Si le gestionnaire de droits Windows Media est installé, il n’est pas nécessaire de définir ces attributs dans votre application. Le composant DRM récupère ces attributs et les utilise pour signer automatiquement l’en-tête. Si vous disposez d’une version activée de Windows Media Rights Manager sur un autre ordinateur et que vous souhaitez réutiliser ces valeurs d’objet de signature numérique, vous pouvez les Rechercher dans le registre. Le certificat du serveur de licences est stocké sous HKEY \_ local \_ machine \\ Software \\ Microsoft \\ WM Rights Manager \\ License Server \\ certs : cert1, et le certificat racine est stocké sous HKEY \_ local \_ machine \\ Software \\ Microsoft \\ WM Rights Manager \\ License Server \\ certs : cert2. Lorsque vous protégez des fichiers avec DRM version 7, vous devez utiliser les valeurs de ces clés de registre. Pour la **\_ propriété DRM LASignaturePrivKey**, utilisez **GenerateSigningKeysEx** (via le kit de développement logiciel (SDK) Windows Media Rights Manager) ou réutilisez la valeur installée par le gestionnaire de droits Windows Media sous HKEY \_ local \_ machine \\ Software \\ Microsoft \\ WM Rights Manager \\ License Server : info \_ Cert0. Pour la propriété **DRM \_ LASignatureCert** , utilisez **GenerateSigningKeysEx** (via le kit de développement logiciel (SDK) Windows Media Rights Manager) ou la valeur installée par le gestionnaire de droits Windows Media sous HKEY \_ local \_ machine \\ Software \\ Microsoft \\ WM Rights Manager \\ License Server \\ certs : cert0.

10. Appelez [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) autant de fois que nécessaire pour configurer l’objet enregistreur, qui définira les attributs d’en-tête DRM requis en fonction des besoins. Ces propriétés sont conservées pendant la durée de vie de l’objet enregistreur ou jusqu’à ce qu’elles soient réinitialisées avec une nouvelle valeur. Ils n’ont pas besoin d’être réinitialisés pour chaque nouveau fichier que vous créez.

    Les propriétés suivantes sont requises par l’objet writer :

    -   [**\_HEADERSIGNPRIVKEY DRM**](drm-headersignprivkey.md)
    -   [**Keyseed DRM \_**](drm-keyseed.md)
    -   [**\_V1LICENSEACQURL DRM**](drm-v1licenseacqurl.md)
    -   [**\_KEYID DRM**](drm-keyid.md)
    -   [**\_LICENSEACQURL DRM**](drm-licenseacqurl.md)

    Les propriétés suivantes sont facultatives :

    -   [**\_CONTENTID DRM**](drm-contentid.md)
    -   [**\_INDIVIDUALIZEDVERSION DRM**](drm-individualizedversion.md)

    En outre, vous pouvez spécifier des attributs de fichier DRM définis par l’utilisateur directement à l’aide de l’attribut de base [**DRM \_ DRMHeader**](drm-drmheader.md) . Vous pouvez ajouter tout attribut supplémentaire que vous souhaitez, tel que « DRMHeader. RequireSAP », par exemple, pour communiquer des informations supplémentaires qui seront utilisées par le serveur de licences lors de la création de la licence. Le serveur de licences doit être conscient de l’avancement des propriétés supplémentaires que vous ajoutez. Il n’existe aucun moyen de découvrir des propriétés inconnues par programmation.

11. Écrivez le fichier à l’aide des méthodes de l’interface [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) , comme décrit ailleurs dans cette documentation. Pour créer un flux DRM actif, il vous suffit d’écrire dans un récepteur réseau. Vous pouvez également écrire dans un récepteur de notifications push.
12. Si nécessaire, créez une licence pour le fichier à l’aide du gestionnaire des droits Windows Media. Cette tâche peut également être effectuée par un serveur de licences tiers. Pour les scénarios de DRM en direct, les utilisateurs finaux doivent obtenir une licence avant le début du flux, ou au moment où ils tentent pour la première fois de s’y connecter.

**Remarque** DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Attributs**](attributes.md)
</dt> <dt>

[**Liste des attributs DRM**](drm-attribute-list.md)
</dt> <dt>

[**Propriétés DRM**](drm-properties.md)
</dt> <dt>

[**Interface IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> <dt>

[**IWMHeaderInfo :: SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[**Interface IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Lecture des fichiers protégés**](reading-protected-files.md)
</dt> <dt>

[**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)
</dt> </dl>

 

 




