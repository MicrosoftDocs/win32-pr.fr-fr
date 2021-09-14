---
title: Acquisition de licences
description: Acquisition de licences
ms.assetid: dde33d57-6c63-4e1a-8398-5db466fb22fa
keywords:
- Windows Kit de développement logiciel (SDK) Media format, API étendues clientes DRM
- Windows Media Format SDK, API étendues du client
- Windows Media Format SDK, API étendues
- Windows Media Format SDK, API
- Windows Media Format SDK, gestion des droits numériques (DRM)
- Windows Media Format SDK, acquisition de licences
- Windows Media Format SDK, licences
- gestion des droits numériques (DRM), API étendues du client
- DRM (gestion des droits numériques), API étendues du client
- gestion des droits numériques (DRM), API étendues
- DRM (gestion des droits numériques), API étendues
- gestion des droits numériques (DRM), API
- DRM (gestion des droits numériques), API
- gestion des droits numériques (DRM), acquisition de licences
- DRM (Digital Rights Management), acquisition de licences
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- API étendues du client DRM, acquisition de licences
- API étendues clientes, acquisition de licences
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c024789823ca0cd1b38959d78535ce71e2514897
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196036"
---
# <a name="acquiring-licenses"></a>Acquisition de licences

un scénario courant pour acquérir des licences est lorsqu’un utilisateur a un fichier multimédia Windows protégé et tente d’accéder au contenu pour la première fois. étant donné que les api étendues du Client de Media DRM Windows sont séparées des routines de gestion de fichiers ASF, le scénario d’acquisition de licence de base, bien qu’pris en charge, nécessite plus d’appels d’API que l’utilisation du sdk Windows Media Format et du kit de développement logiciel (sdk) Media Foundation.

cette section décrit comment utiliser les api étendues du Client Windows Media DRM pour acquérir des licences stockées dans le magasin de licences local sur un ordinateur Client. Elle contient les rubriques suivantes.



| Rubrique                                                                | Description                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Acquisition de licence en mode silencieux](silent-license-acquisition.md)         | Décrit comment acquérir des licences sans intervention de l’utilisateur.                                                                               |
| [Acquisition de licence non silencieuse](non-silent-license-acquisition.md) | Décrit comment acquérir des licences lorsque l’intervention de l’utilisateur (par exemple, le paiement du contenu) est requise.                                     |
| [Pré-remise de licence](license-pre-delivery.md)                     | Décrit comment extraire des licences d’un serveur de licences vers un ordinateur client.                                                                 |
| [Création de licences localement](creating-licenses-locally.md)           | Décrit comment créer vos propres licences sans les télécharger à partir d’un serveur de licences et comment les stocker dans le magasin de licences local. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation**](drm-programming-guide.md)
</dt> </dl>

 

 




