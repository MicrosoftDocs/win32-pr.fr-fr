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
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379612"
---
# <a name="building-an-xmr-license"></a>Génération d’une licence XMR

Pour générer une licence pour le traitement DRM Windows Media, vous devez utiliser le schéma binaire XMR (extensible Media Rights). XMR est un schéma permettant de transmettre des restrictions et des droits d’utilisation de média et doit être concédé sous licence séparément.

Le matériel important d’une licence est chiffré à l’aide de la clé publique dans la collection de certificats DRM Windows Media. il est donc visible uniquement pour le sous-système de l’API étendue du client Windows Media DRM. .

Il vous incombe de vous assurer que la structure de licence et les paramètres de stratégie sont valides et cohérents avec l’intention de l’émetteur de licence et qu’ils sont conformes aux règles de conformité.

Vous devez lire les règles de conformité de l’importation Windows Media DRM pour connaître l’ensemble complet d’objets XMR qui doivent être présents dans la licence.

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

 

 




