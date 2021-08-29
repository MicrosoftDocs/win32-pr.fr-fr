---
title: Accès aux métadonnées et aux attributs dans l’application
description: Obtention et définition des métadonnées et des attributs dans l’application
ms.assetid: 308a722d-1c65-41eb-a0e2-21171eb410d5
keywords:
- Windows Gestionnaire de périphériques de média, métadonnées
- Gestionnaire de périphériques, métadonnées
- Guide de programmation, métadonnées
- applications de bureau, métadonnées
- création d’applications de Gestionnaire de périphériques Windows Media, métadonnées
- metadata
- Windows Gestionnaire de périphériques de média, attributs
- Gestionnaire de périphériques, attributs
- Guide de programmation, attributs
- applications de bureau, attributs
- création d’Windows applications multimédias Gestionnaire de périphériques d’attributs
- attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8c67300e2d4dc81adf90641e33be685baf439cb444a0c186d8a45191b5a30e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957569"
---
# <a name="accessing-metadata-and-attributes-in-the-app"></a>Accès aux métadonnées et aux attributs dans l’application

Une discussion générale sur les métadonnées et les attributs est disponible dans [obtention et définition des métadonnées et des attributs](getting-and-setting-metadata-and-attributes.md). Cette section traite des appels de méthode d’application spécifiques pour extraire ou définir des valeurs.

Les applications peuvent récupérer des attributs ou des métadonnées sur un stockage spécifique en appelant [**IWMDMStorage :: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes), [**IWMDMStorage2 :: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2), [**IWMDMStorage3 :: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) ou [**IWMDMStorage4 :: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata). **GetMetadata** récupère une collection complète de toutes les métadonnées associées à un stockage, et l’application peut ensuite énumérer toutes les valeurs ou demander des valeurs spécifiques de la collection. **GetSpecifiedMetadata** crée un objet de métadonnées pour le compte de l’appelant. l’appelant peut demander un sous-ensemble des données disponibles en remplissant le paramètre *ppwszPropNames* à l’aide d’un tableau des chaînes de propriétés du média Windows Gestionnaire de périphériques souhaité et du nombre de ce tableau. L’objet de métadonnées retourné sera rempli avec les propriétés qui peuvent être récupérées. Les propriétés qui n’ont pas pu être récupérées seront absentes. Les métadonnées sont retournées en fonction du meilleur effort.

Un appareil peut définir des attributs ou des métadonnées sur un stockage en appelant [**IWMDMStorage :: SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes), [**IWMDMStorage2 :: SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)ou [**IWMDMStorage3 :: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata). Notez qu’il n’y a aucune garantie que les valeurs définies sont conservées, car elles peuvent être stockées dans un magasin de fichiers externes non persistant, les valeurs peuvent ne pas être prises en charge ou l’appareil peut ne pas prendre en charge les propriétés comme étant accessibles en écriture.

Vous pouvez également obtenir ou définir les métadonnées relatives à un appareil en appelant [**IWMDMDevice3 :: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) ou [**IWMDMDevice3 :: SetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty). Une table distincte de constantes de métadonnées d’appareil est indiquée à la fin des [constantes de métadonnées](metadata-constants.md).

Des exemples d’utilisation de ces méthodes sont fournis dans la documentation de référence de chaque méthode.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**création d’une Application de Gestionnaire de périphériques multimédia Windows**](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[**Obtention et définition des métadonnées et des attributs**](getting-and-setting-metadata-and-attributes.md)
</dt> </dl>

 

 




