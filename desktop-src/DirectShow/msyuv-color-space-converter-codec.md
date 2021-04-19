---
description: MSYUV est un codec de convertisseur d’espace colorimétrique YUV-à-RVB.
ms.assetid: 77b00937-ac63-4b23-b546-c0896b3c57ba
title: Codec de convertisseur d’espace de couleurs MSYUV
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838e7cd749042b2fb97adaf0b2b4cd0378a81c07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540056"
---
# <a name="msyuv-color-space-converter-codec"></a>Codec de convertisseur d’espace de couleurs MSYUV

MSYUV est un codec de convertisseur d’espace colorimétrique YUV-à-RVB. Il permet la lecture de données sources vidéo dans des formats YUV sur les clients dont la carte vidéo ne peut pas être utilisée pour les conversions YUV-à-RGB dans le matériel. Le codec participe aux graphiques de filtres via le filtre de wrapper de [décompresseur AVI](avi-decompressor-filter.md) .

Les caméras de conférence numérique avec des interfaces 1394 ou USB peuvent produire des données d’image dans différents formats YUV. Si le matériel d’affichage ne prend pas en charge la conversion YUV-à-RGB intégrée, ou si la fonctionnalité de conversion matérielle ne peut pas être utilisée pour une autre raison, les données de l’image YUV doivent être converties au format RVB avant d’être envoyées au convertisseur vidéo.

En raison de la nécessité du [convertisseur vidéo](video-renderer-filter.md)pour un type d’entrée RVB au moment de la connexion, ce filtre peut être inséré dans un graphique en amont du convertisseur vidéo pendant la génération automatique de graphiques. Plus précisément, si le générateur de graphiques détecte un format YUV dans le type de média de la broche de sortie du filtre en amont, le générateur de graphiques insère le décompresseur AVI, qui charge ensuite le codec MSYUV et le configure initialement pour effectuer la conversion en RVB. Une fois que le graphique a d’abord effectué une transition vers un État exécution ou suspendu, le filtre de convertisseur vidéo peut détecter si la carte vidéo peut effectuer la conversion dans le matériel. Si tel est le cas, le décompresseur AVI est notifié et RECONFIGURE MSYUV pour qu’il fonctionne en « mode pass-through », ce qui amène le codec à ignorer la conversion et à copier les données de l’image YUV directement sur une surface de superposition DirectDraw dans la mémoire vidéo.

Étant donné que les convertisseurs de mixage vidéo (VMR-7 et VMR-9) n’utilisent jamais GDI, ils n’ont pas besoin d’un type RVB au moment de la connexion, et le convertisseur d’espace de couleurs MSYUV n’est jamais inséré avant le VMR dans un graphique.

MSYUV convertit les formats YUV compressés en RGB, comme illustré dans la liste suivante :

-   Formats d’entrée : UYVY, YUY2, YVYU
-   Formats de sortie : RVB 8, RVB 16, RVB 24, RVB 32

Le codec de convertisseur d’espace de couleurs MSYUV est un codec VCM (Video Compression Manager). Il est utilisé dans DirectShow via le filtre de [décompresseur AVI](avi-decompressor-filter.md) . Pour obtenir un convertisseur de couleurs plus général, utilisez le [**convertisseur de couleurs DSP**](../medfound/colorconverter.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msyuv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 
