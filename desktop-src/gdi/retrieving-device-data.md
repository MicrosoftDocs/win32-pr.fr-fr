---
description: 'Les applications peuvent utiliser les fonctions suivantes pour récupérer des données d’appareil à l’aide d’un contexte de périphérique : GetDeviceCaps et DeviceCapabilities.'
ms.assetid: eed6a323-b7eb-41a2-adb9-592f3f912884
title: Récupération des données de l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf956a04c733883cb5fb374e4e75dc4e93e8029f9968deb90cc113cef460864
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717989"
---
# <a name="retrieving-device-data"></a>Récupération des données de l’appareil

Les applications peuvent utiliser les fonctions suivantes pour récupérer des données d’appareil à l’aide d’un contexte de périphérique : [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) et [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa).

[**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) récupère les données générales des appareils suivants :

-   Affichages raster
-   Imprimantes matricielles
-   Imprimantes jet d’encre
-   Imprimantes laser
-   Traceurs vectoriels
-   Caméras raster

Les données incluent les fonctionnalités prises en charge de l’appareil, y compris la résolution de l’appareil (pour les affichages vidéo), le format de couleur (pour les affichages vidéo et les imprimantes couleur), le nombre d’objets graphiques, les fonctionnalités raster, le dessin courbé, le dessin en courbes, le dessin polygonal et le dessin de texte. Une application récupère ces données en fournissant un handle identifiant le contexte de périphérique approprié, ainsi qu’un index spécifiant le type de données que la fonction doit récupérer.

La fonction [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa) récupère les données spécifiques aux imprimantes, y compris le nombre d’emplacements de papier disponibles, les fonctionnalités duplex de l’imprimante, les résolutions prises en charge par l’imprimante, le format de papier maximal et minimal pris en charge, etc. Une application récupère ces données en fournissant des chaînes qui spécifient un périphérique et un port d’imprimante, ainsi qu’un index spécifiant le type de données que la fonction doit récupérer.

 

 
