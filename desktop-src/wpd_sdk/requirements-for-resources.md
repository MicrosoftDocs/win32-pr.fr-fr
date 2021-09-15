---
description: Conditions requises pour les ressources
ms.assetid: 6b654cd6-7e9f-4e12-a687-4110e600ba7b
title: Conditions requises pour les ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5702555704137f4280e527f0fc26f176435238ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522936"
---
# <a name="requirements-for-resources"></a>Conditions requises pour les ressources

Windows Les appareils mobiles définissent les catégories de ressources suivantes comme des valeurs **PROPERTYKEY** . Ces valeurs sont utilisées pour décrire des ressources individuelles dans un objet. Le membre *PID* de la clé de propriété peut être différent pour décrire des ressources différentes du même type pour tous les types, à l’exception de la **\_ ressource wpd \_ par défaut**, qui ne peut décrire qu’une seule ressource. La page Description liée pour chaque type de ressource répertorie les attributs pris en charge par cette ressource.



| Ressource PROPERTYKEY                                                | Description                                                                                                    |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**\_ressource wpd \_ par défaut**](wpd-resource-default.md)              | Spécifie l’ensemble du fichier situé derrière l’objet. Il s’agit de la seule ressource requise pour un objet avec une ressource. |
| [**image de l' \_ album des ressources wpd \_ \_**](wpd-resource-album-art.md)         | Spécifie une image qui représente l’illustration de l’album pour l’objet.                                           |
| [**\_ \_ clip audio de la ressource wpd \_**](wpd-resource-audio-clip.md)       | Spécifie un clip audio pour l’objet.                                                                        |
| [**PHOTO du contact de la \_ ressource wpd \_ \_**](wpd-resource-contact-photo.md) | Spécifie une image qui représente une photo de la personne à laquelle il est question dans l’objet contact.                |
| [**\_ressource wpd \_ générique**](wpd-resource-generic.md)              | Ressource générique de type de données non défini. Ce doit être traité comme un tableau d’octets.                             |
| [**\_icône de ressource wpd \_**](wpd-resource-icon.md)                    | icône ;                                                                                                       |
| [**\_miniature des ressources wpd \_**](wpd-resource-thumbnail.md)          | Une image miniature.                                                                                             |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de référence de programmation**](programming-reference.md)
</dt> </dl>

 

 



