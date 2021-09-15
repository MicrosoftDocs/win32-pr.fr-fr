---
title: Interrogation pour obtenir des informations détaillées sur les droits
description: Interrogation pour obtenir des informations détaillées sur les droits
ms.assetid: d9d5c299-1f61-41df-ab2c-7f4d196e9290
keywords:
- Windows Media Format SDK, interrogation des droits détaillés
- Windows Media Format SDK, requêtes de droits détaillés
- gestion des droits numériques (DRM), interrogation des droits détaillés
- DRM (Digital Rights Management), interrogation des droits détaillés
- gestion des droits numériques (DRM), requêtes de droits détaillés
- DRM (gestion des droits numériques), requêtes de droits détaillés
- API étendues du client DRM, interrogation des droits détaillés
- API étendues du client, interrogation des droits détaillés
- API étendues du client DRM, requêtes de droits détaillées
- API étendues clientes, requêtes de droits détaillées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3a21fa974f0289c4e4e8983ee6d4fd1757de824
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404669"
---
# <a name="querying-for-detailed-rights-information"></a>Interrogation pour obtenir des informations détaillées sur les droits

À l’aide de la méthode [**IWMDRMLicenseQuery :: QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) , vous pouvez obtenir des informations détaillées sur les droits accordés par les licences pour un ID de clé. Les informations que vous recevez de cette méthode sont agrégées à partir de toutes les licences dans le magasin de licences local qui s’appliquent à l’ID de clé spécifié.

**QueryLicenseState** utilise la structure de [**\_ données d' \_ état \_ de licence DRM**](drmdrm-license-state-data.md) pour afficher des informations agrégées sur toutes les licences pour l’ID de clé spécifié. cette utilisation est différente de celle des autres objets du kit de développement logiciel (SDK) de Format multimédia Windows.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Obtention d’informations à partir de licences dans le magasin de licences local**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




