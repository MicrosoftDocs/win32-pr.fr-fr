---
title: Vérification et initialisation
description: Vérification et initialisation
ms.assetid: e92abaa2-0bac-4c78-bda7-d118c4f5b332
keywords:
- Windows Media Format SDK, vérification
- Windows Media Format SDK, initialisation
- gestion des droits numériques (DRM), vérification
- DRM (gestion des droits numériques), vérification
- gestion des droits numériques (DRM), initialisation
- DRM (gestion des droits numériques), initialisation
- API étendues du client DRM, vérification
- API étendues du client, vérification
- API étendues du client DRM, initialisation
- API étendues du client, initialisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59c54b56e0622fb65a1a57ae1909e0e6e64aaca6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314311"
---
# <a name="verification-and-initialization"></a>Vérification et initialisation

Vous devez effectuer les étapes suivantes pour vérifier que la transchiffrement est autorisée et initialiser un objet qui déchiffrera le contenu :

1.  Si vous avez déjà l’ID de clé du contenu, passez à l’étape 5.
2.  Appelez la fonction [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor) pour créer un objet d’éditeur de métadonnées et obtenir une instance de l’interface [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor) de cet objet.
3.  Appelez **IWMMetadataEditor :: QueryInterface** pour récupérer une instance de l’interface [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) .
4.  Appelez [**IWMDRMEditor :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) pour accéder à la propriété **DRM \_ DRMHeader \_ KeyId** .
5.  Initialisez les API étendues du client Windows Media DRM en appelant la fonction [**WMDRMStartup**](wmdrmstartup.md) .
6.  Appelez la fonction [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) pour créer un objet fournisseur sécurisé et obtenir une instance de l’interface [**IWMDRMProvider**](iwmdrmprovider.md) de cet objet.
7.  Appelez [**IWMDRMProvider :: CreateObject**](iwmdrmprovider-createobject.md) pour créer un objet de gestion de licences et obtenir une instance de son interface [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) .
8.  Appelez [**IWMDRMLicenseManagement :: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), en passant l’ID de la clé et le droit qui régit les actions à effectuer avec le contenu après qu’il a été chiffré. Cet appel permet de récupérer une instance de l’interface [**IWMDRMLicense**](iwmdrmlicense.md) qui peut être utilisée pour énumérer toutes les licences correspondantes.
9.  Appelez [**IWMDRMLicense :: GetInclusionList**](iwmdrmlicense-getinclusionlist.md) pour récupérer la liste des systèmes de protection de contenu (CPS) autorisés, comme spécifié par l’émetteur de licence.
10. Analyser la liste d’inclusion pour confirmer que le GUID de la sortie CPS est autorisé par la licence.
11. Si le GUID d’exportation souhaité ne figure pas dans la liste d’inclusion, appelez [**IWMDRMLicense :: GetNext**](iwmdrmlicense-getnext.md) pour accéder à la prochaine licence applicable (le cas échéant) et répétez les étapes 9 et 10. Si aucune licence n’a le GUID souhaité dans sa liste d’inclusion, l’exportation ne peut pas être effectuée.
12. Appelez [**IWMDRMLicense :: CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md) pour créer un objet déchiffreur. Transmettez le certificat d’application d’exportation. Cet appel fournira un pointeur vers une instance de l’interface [**IWMDRMDecrypt**](iwmdrmdecrypt.md) de l’objet déchiffreur et un objet binaire contenant la valeur initiale. Seule la constante **RC4 du \_ \_ type de \_ protection DRM** Windows Media est prise en charge en tant qu’argument du paramètre *dwFlags* pour l’instant.
13. Utilisez le schéma de chiffrement OAEP RSA pour déchiffrer le vecteur d’initialisation.
14. Utilisez la bibliothèque d’analyse ASF fournie par Microsoft lorsque vous entrez dans le contrat d’exportation DRM Windows Media, afin de localiser le décalage en octets pour chaque charge utile.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exportation du contenu compressé**](exporting-compressed-content.md)
</dt> </dl>

 

 




