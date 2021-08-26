---
title: Création et initialisation d’un enregistreur DRM
description: Création et initialisation d’un enregistreur DRM
ms.assetid: ce0508e1-f69f-4e09-8c32-8c9dac48b5ec
keywords:
- Windows Media Format SDK, enregistreurs DRM
- gestion des droits numériques (DRM), création d’enregistreurs DRM
- DRM (gestion des droits numériques), création d’enregistreurs DRM
- gestion des droits numériques (DRM), initialisation des enregistreurs DRM
- DRM (gestion des droits numériques), initialisation des enregistreurs DRM
- API étendues du client DRM, enregistreurs DRM
- API étendues clientes, enregistreurs DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24067e082de38bc396153be918025e2608246e39185c45eaa84bfe0e5c02407
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007049"
---
# <a name="creating-and-initializing-a-drm-writer"></a>Création et initialisation d’un enregistreur DRM

les étapes suivantes sont requises pour initialiser un objet writer ASF pour l’importation d’exemples de média chiffré dans Windows DRM media.

1.  Suivez les étapes 1 à 4 de la [licence d’importation et du matériel de clé](importing-license-and-key-material.md).
2.  créez et initialisez un objet writer ASF à l’aide du matériel de clé DRM de Media Windows approprié. Pour plus d’informations, consultez Activation de la [prise en charge de DRM](enabling-drm-support.md).
3.  Définissez chacun des attributs suivants en appelant [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute):
    -   \_HEADERSIGNPRIVKEY DRM
    -   \_V1LICENSEACQURL DRM
    -   \_KEYID DRM
    -   \_LICENSEACQURL DRM
4.  si une version sous licence de Windows Media Rights Manager n’est pas installée sur l’ordinateur exécutant votre logiciel, les quatre attributs suivants doivent également être définis :
    -   \_LASIGNATUREROOTCERT DRM
    -   \_LASIGNATURECERT DRM
    -   \_LASIGNATURELICSRVCERT DRM
    -   \_LASIGNATUREPRIVKEY DRM
    -   l’Application pour les certificats de chiffrement nécessaires peut être effectuée en complétant le [Windows le contrat de licence multimédia en ligne (WMLA)](https://www.microsoft.com/licensing/default) .
5.  Créer une clé de session et remplir une structure de [**\_ clé de \_ session \_ d’importation WMDRM**](wmdrm-import-session-key.md) . La clé de session est utilisée pour chiffrer une clé de contenu. Pour obtenir un exemple, consultez [exemple de création de clé de session](create-session-key-example.md).
6.  Créer une clé de contenu à partir d’un vecteur d’initialisation RC4 aléatoire et remplir une structure de [**\_ clé de \_ contenu \_ d’importation WMDRM**](wmdrm-import-content-key.md) . La clé de contenu est utilisée pour chiffrer les exemples de supports. Pour obtenir un exemple, consultez [créer un exemple de clé de contenu](create-content-key-example.md).
7.  Chiffrez la clé de contenu avec la clé de session, à l’aide du chiffrement RC4.
8.  Extrayez la clé de collection de certificats de l’ordinateur. Pour obtenir un exemple, consultez [obtenir un exemple de certificat d’ordinateur](get-machine-certificate-example.md).
9.  Chiffrez la clé de session avec la clé publique extraite du certificat.
10. Remplir une structure [**d' \_ \_ initialisation d' \_ importation WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .
11. appelez la méthode [**IWMDRMWriter3 :: SetProtectStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) pour indiquer au kit de développement logiciel (SDK) que les exemples qui arrivent dans le writer sont déjà protégés et doivent être envoyés directement au client Windows Media DRM pour l’importation.
12. Appelez [**IWMWriter :: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

les étapes restantes pour créer un fichier protégé par DRM sont documentées dans le Guide de programmation du kit de développement logiciel (SDK) Windows Media Format. Pour plus d’informations, consultez [création de fichiers protégés](creating-protected-files.md).

L’étape suivante consiste à itérer au sein de chaque exemple de support, à le chiffrer et à le transmettre à l’objet Writer. Pour plus d’informations, consultez les [exemples de média de chiffrement et d’importation](encrypting-and-importing-media-samples.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Attributs**](attributes.md)
</dt> <dt>

[**Importation DRM**](drm-import.md)
</dt> </dl>

 

 




