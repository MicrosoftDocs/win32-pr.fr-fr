---
description: Les cartes de texture sont des images numérisées dessinées sur des formes en trois dimensions pour ajouter des détails visuels.
ms.assetid: 0ea5cb07-a21a-4e2c-93e2-54966153bb8a
title: Ressources de texture compressées (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9b7ef048c0e1780f92246a407863a4fa48a94a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201094"
---
# <a name="compressed-texture-resources-direct3d-9"></a>Ressources de texture compressées (Direct3D 9)

Les cartes de texture sont des images numérisées dessinées sur des formes en trois dimensions pour ajouter des détails visuels. Ils sont mappés à ces formes au cours de la pixellisation, et le processus peut consommer de grandes quantités du bus système et de la mémoire. Pour réduire la quantité de mémoire consommée par les textures, Direct3D prend en charge la compression des surfaces de texture. Certains périphériques Direct3D prennent en charge les surfaces de texture compressées en mode natif. Sur ces appareils, lorsque vous avez créé une surface compressée et que vous y avez chargé les données, la surface peut être utilisée dans Direct3D comme n’importe quelle autre surface de texture. Direct3D gère la décompression lorsque la texture est mappée à un objet 3D.

## <a name="storage-efficiency-and-texture-compression"></a>Efficacité de stockage et compression de texture

Tous les formats de compression de texture sont des puissances de deux. Bien que cela ne signifie pas qu’une texture est nécessairement carrée, cela signifie que x et y sont des puissances de deux. Par exemple, si une texture est 512 par 128 octets, le mappage MIP suivant serait 256 par 64, et ainsi de suite, chaque niveau diminuant d’une puissance de deux. À des niveaux inférieurs, où la texture est filtrée à 16 par 2 et 8 par 1, il y aura des bits gaspillés, car le bloc de compression est toujours un bloc de texels de 4 par 4. Les portions inutilisées du bloc sont complétées. Bien qu’il y ait gaspillage des bits aux niveaux les plus bas, le gain global est toujours significatif. Le pire cas est, en théorie, une texture 2K de 1 (2 ⁰ de puissance). Ici, une seule ligne de pixels est encodée par bloc, tandis que le reste du bloc est inutilisé.

## <a name="mixing-formats-within-a-single-texture"></a>Mélange de formats dans une seule texture

Il est important de noter qu’une seule texture doit spécifier que ses données sont stockées sous la forme de 64 ou 128 bits par groupe de 16 texels. Si les blocs 64 bits, c’est-à-dire le format DXT1, sont utilisés pour la texture, il est possible de mélanger les formats alpha opaque et 1 bits sur la base de chaque bloc au sein de la même texture. En d’autres termes, la comparaison de l’amplitude de l’entier non signé de la couleur \_ 0 et de la couleur \_ 1 est effectuée de manière unique pour chaque bloc de 16 texels.

Une fois les blocs 128 bits utilisés, le canal alpha doit être spécifié dans explicite (format DXT2 et DXT3) ou en mode interpolé (format DXT4 et DXT5) pour la texture entière. Comme pour la couleur, quand le mode interpolé (format DXT4 et DXT5) est sélectionné, huit alpha interpolés ou six modes alphabétiques interpolés peuvent être utilisés bloc par bloc. Là encore, la comparaison de magnitude des alpha \_ 0 et alpha \_ 1 est effectuée de manière unique sur une base bloc par bloc.

Direct3D fournit des services pour compresser les surfaces utilisées pour la texturation des modèles 3D. Cette section fournit des informations sur la création et la manipulation des données dans une surface de texture compressée.

Les informations sont contenues dans les rubriques suivantes.

-   [Textures opaques et alpha 1 bits (Direct3D 9)](opaque-and-1-bit-alpha-textures.md)
-   [Textures avec canaux alpha (Direct3D 9)](textures-with-alpha-channels.md)
-   [Formats de texture compressés (Direct3D 9)](compressed-texture-formats.md)
-   [Utilisation de textures compressées (Direct3D 9)](using-compressed-textures.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Textures Direct3D](direct3d-textures.md)
</dt> </dl>

 

 



