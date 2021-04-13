---
title: Énumération des licences dans le magasin de licences local
description: Énumération des licences dans le magasin de licences local
ms.assetid: 1f380b9e-85e4-4190-a809-65dfd4658b7c
keywords:
- Windows Media Format SDK, énumération des licences
- Windows Media Format SDK, licences
- Windows Media Format SDK, magasin de licences local
- gestion des droits numériques (DRM), énumération des licences
- DRM (gestion des droits numériques), énumération des licences
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- gestion des droits numériques (DRM), magasin de licences local
- DRM (gestion des droits numériques), magasin de licences local
- API étendues du client DRM, énumération des licences
- API étendues du client, énumération des licences
- API étendues du client DRM, licences
- API étendues clientes, licences
- API étendues du client DRM, magasin de licences local
- API étendues du client, magasin de licences local
- licences, énumération
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b1384e08a6789fedca9704f36ad8da1e31b4ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379760"
---
# <a name="enumerating-licenses-in-the-local-license-store"></a>Énumération des licences dans le magasin de licences local

L’énumération est un processus qui consiste à obtenir des informations sur les licences dans le magasin de licences local, en les exécutant pas à pas une par une. Vous pouvez créer une énumération de licences en appelant [**IWMDRMLicenseManagement :: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md).

La raison la plus courante de l’énumération par le biais de licences dans le magasin est de trouver une licence particulière pour le déchiffrement de tout le contenu.

L’interface [**IWMDRMLicense**](iwmdrmlicense.md) sert à la fois de portail aux résultats individuels de la licence et de l’énumérateur. Lorsque l’énumération de licences est créée, la première licence de la liste est chargée dans l’interface **IWMDRMLicense** . La plupart des méthodes de **IWMDRMLicense** vous permettent d’obtenir des informations sur la licence ou de créer des objets pour chiffrer ou déchiffrer le contenu en fonction de la licence. Toutefois, il existe deux méthodes qui contrôlent l’énumération : [**GetNext**](iwmdrmlicense-getnext.md) et [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md). **GetNext** charge la licence suivante dans la liste dans l’interface. **ResetEnumeration** retourne l’énumération à l’État dans lequel elle se trouvait lors de sa création. Lorsque l’énumération est réinitialisée, la première licence dans la liste est chargée à nouveau dans l’interface **IWMDRMLicense** .

Lorsque vous avez atteint la dernière licence dans la liste, l’appel suivant à **GetNext** retourne l' \_ erreur \_ plus \_ aucun élément.

Si votre application effectue une action avec le contenu couvert par DRM, vous devez vérifier les licences dans le magasin de licences local pour les droits et pour d’autres facteurs de limitation, tels que les niveaux de protection de sortie (OPLs).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Obtention d’informations à partir de licences dans le magasin de licences local**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




