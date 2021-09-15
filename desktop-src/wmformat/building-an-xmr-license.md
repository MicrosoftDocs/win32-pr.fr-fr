---
title: Génération d’une licence XMR
description: Génération d’une licence XMR
ms.assetid: c43e4913-82a6-4dd0-9d1f-1fb237ecbb30
keywords:
- Windows Media Format SDK, importation DRM
- Windows Media Format SDK, importer
- Windows Media Format SDK, licences XMR
- Windows Media Format SDK, licences
- Windows Media Format SDK, extensible Media Rights (XMR)
- gestion des droits numériques (DRM), importation
- DRM (gestion des droits numériques), importation
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- gestion des droits numériques (DRM), licences XMR
- DRM (gestion des droits numériques), licences XMR
- gestion des droits numériques (DRM), XMR (extensible Media Rights)
- DRM (gestion des droits numériques), XMR (extensible Media Rights)
- API étendues du client DRM, importation
- API étendues du client, importation
- API étendues du client DRM, licences XMR
- API étendues clientes, licences XMR
- API étendues du client DRM, licences
- API étendues clientes, licences
- API étendues du client DRM, XMR (extensible Media Rights)
- API étendues clientes, droits multimédias extensibles (XMR)
- licences, XMR
- Droits multimédias extensibles (XMR)
- XMR (droits multimédias extensibles)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc275419116362c08cabe4dc70aa227687705fdb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411390"
---
# <a name="building-an-xmr-license"></a>Génération d’une licence XMR

pour générer une licence de Windows media DRM à traiter, vous devez utiliser le schéma binaire XMR (Extensible media Rights). XMR est un schéma permettant de transmettre des restrictions et des droits d’utilisation de média et doit être concédé sous licence séparément.

le matériel important d’une licence est chiffré à l’aide de la clé publique dans la collection de certificats DRM Windows, et n’est donc visible que pour le sous-système de l’API étendue du Client media drm Windows. .

Il vous incombe de vous assurer que la structure de licence et les paramètres de stratégie sont valides et cohérents avec l’intention de l’émetteur de licence et qu’ils sont conformes aux règles de conformité.

vous devez lire les règles de conformité de l’importation Media DRM Windows pour connaître l’ensemble complet d’objets XMR qui doivent être présents dans la licence.

Pour transmettre la licence XMR au sous-système DRM, appelez la méthode [**IWMDRMLicenseManagement :: StoreLicense**](iwmdrmlicensemanagement-storelicense.md) . Utilisez le format suivant pour transmettre la licence dans le paramètre *bstrLicenseResponse* :


```C++
<LICENSERESPONSE>
    <LICENSE version="3.0.0.0">insert base64-encoded XMR license here</LICENSE>
</LICENSERESPONSE>
```



Cette chaîne doit être au format Unicode (UTF-16).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Importation DRM**](drm-import.md)
</dt> </dl>

 

 




