---
title: Accès aux métadonnées et aux attributs dans l’application
description: Obtention et définition des métadonnées et des attributs dans l’application
ms.assetid: 308a722d-1c65-41eb-a0e2-21171eb410d5
keywords:
- Gestionnaire de périphériques Windows Media, métadonnées
- Gestionnaire de périphériques, métadonnées
- Guide de programmation, métadonnées
- applications de bureau, métadonnées
- création d’applications Windows Media Gestionnaire de périphériques, de métadonnées
- metadata
- Gestionnaire de périphériques Windows Media, attributs
- Gestionnaire de périphériques, attributs
- Guide de programmation, attributs
- applications de bureau, attributs
- création d’applications Windows Media Gestionnaire de périphériques, attributs
- attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a78dbb31ebcc5ec99b1db3503b386b09b5a3c05
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/27/2019
ms.locfileid: "104313852"
---
# <a name="accessing-metadata-and-attributes-in-the-app"></a>Accès aux métadonnées et aux attributs dans l’application

Une discussion générale sur les métadonnées et les attributs est disponible dans [obtention et définition des métadonnées et des attributs](getting-and-setting-metadata-and-attributes.md). Cette section traite des appels de méthode d’application spécifiques pour extraire ou définir des valeurs.

Les applications peuvent récupérer des attributs ou des métadonnées sur un stockage spécifique en appelant [**IWMDMStorage :: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes), [**IWMDMStorage2 :: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2), [**IWMDMStorage3 :: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) ou [**IWMDMStorage4 :: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata). **GetMetadata** récupère une collection complète de toutes les métadonnées associées à un stockage, et l’application peut ensuite énumérer toutes les valeurs ou demander des valeurs spécifiques de la collection. **GetSpecifiedMetadata** crée un objet de métadonnées pour le compte de l’appelant. L’appelant peut demander un sous-ensemble des données disponibles en remplissant le paramètre *ppwszPropNames* avec un tableau des chaînes de propriétés de gestionnaire de périphériques Windows Media souhaitées, ainsi que le nombre de ce tableau. L’objet de métadonnées retourné sera rempli avec les propriétés qui peuvent être récupérées. Les propriétés qui n’ont pas pu être récupérées seront absentes. Les métadonnées sont retournées en fonction du meilleur effort.

Un appareil peut définir des attributs ou des métadonnées sur un stockage en appelant [**IWMDMStorage :: SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes), [**IWMDMStorage2 :: SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)ou [**IWMDMStorage3 :: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata). Notez qu’il n’y a aucune garantie que les valeurs définies sont conservées, car elles peuvent être stockées dans un magasin de fichiers externes non persistant, les valeurs peuvent ne pas être prises en charge ou l’appareil peut ne pas prendre en charge les propriétés comme étant accessibles en écriture.

Vous pouvez également obtenir ou définir les métadonnées relatives à un appareil en appelant [**IWMDMDevice3 :: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) ou [**IWMDMDevice3 :: SetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty). Une table distincte de constantes de métadonnées d’appareil est indiquée à la fin des [constantes de métadonnées](metadata-constants.md).

Des exemples d’utilisation de ces méthodes sont fournis dans la documentation de référence de chaque méthode.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création d’une application Windows Media Gestionnaire de périphériques**](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[**Obtention et définition des métadonnées et des attributs**](getting-and-setting-metadata-and-attributes.md)
</dt> </dl>

 

 




