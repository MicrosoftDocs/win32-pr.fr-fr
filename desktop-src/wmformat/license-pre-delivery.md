---
title: Pré-remise de licence
description: Pré-remise de licence
ms.assetid: 184d9118-5b60-4871-a1e3-75c45153460d
keywords:
- Windows Media Format SDK, pré-remise de licences
- Windows Media Format SDK, licences
- gestion des droits numériques (DRM), pré-remise de licences
- DRM (gestion des droits numériques), pré-remise de licences
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- API étendues du client DRM, pré-remise de licences
- API étendues clientes, pré-remise de licences
- pré-remise de licences
- licences, pré-remise de licences
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7691c48233ed986d85c47ae9c99df078d0ed1039
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510899"
---
# <a name="license-pre-delivery"></a>Pré-remise de licence

La pré-remise de licence est le processus utilisé pour extraire des licences sur un ordinateur client de manière préventive. Un scénario courant pour l’utilisation de la pré-remise est lorsqu’un utilisateur s’abonne à un service musical. Si vous n’avez pas besoin de licences, l’utilisateur doit attendre l’acquisition de la licence pour chaque nouvelle chanson.

Étant donné que la pré-remise n’est pas effectuée en réponse à une tentative d’accès, elle est généralement effectuée uniquement par le propriétaire du contenu. Autrement dit, vous ne pouvez pré-fournir des licences que pour le contenu que vous contrôlez. Le processus de pré-remise est une coordination entre un composant client et un serveur de licences créé à l’aide des objets du kit de développement logiciel (SDK) Windows Media Digital Rights Management.

La pré-remise de licence est similaire à l' [acquisition de licence non silencieuse](non-silent-license-acquisition.md). Suivez les mêmes étapes, sauf que vous n’avez pas d’en-tête DRM à transmettre à [**IWMDRMLicenseManagement :: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md). La méthode génère une stimulation qui n’est pas spécifique au contenu que vous pouvez envoyer à votre serveur de licences.

Vous pouvez également utiliser le [Gestionnaire de droits Windows Media](/previous-versions//bb676133(v=technet.10)) pour prédistribuer des licences.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Acquisition de licences**](acquiring-licenses.md)
</dt> <dt>

[**Utilisation du modèle d’événement Media Foundation**](using-the-media-foundation-model.md)
</dt> </dl>

 

 