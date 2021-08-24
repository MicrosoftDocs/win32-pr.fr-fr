---
description: Un bloc d’État peut être utilisé pour capturer tous les États des appareils (Voir l’état des blocs d’État enregistrer et restaurer (Direct3D 9)).
ms.assetid: e14077e4-1453-4aa3-b2de-4d3a829a819a
title: Enregistrement de tous les États d’appareil avec un StateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffda5b5d637a31c774e97af85ddeca78b0995ee53c015bb2dcd245b42277a4cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520080"
---
# <a name="saving-all-device-states-with-a-stateblock-direct3d-9"></a>Enregistrement de tous les États d’appareil avec un StateBlock (Direct3D 9)

Un bloc d’État peut être utilisé pour capturer tous les États des appareils (Voir l' [État des blocs d’État enregistrer et restaurer (Direct3D 9)](state-blocks-save-and-restore-state.md)). Les éléments d’état suivants sont inclus dans l’état de l’appareil :

-   État du vertex (voir [enregistrement des États des vertex avec un StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).
-   État de pixel (voir [enregistrement de l’état de Pixel avec un StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)).
-   Chaque texture assignée à un échantillonneur.
-   Chaque texture de vertex.
-   Chaque texture de mappage de déplacement.
-   Palette de texture actuelle.
-   Pour chaque flux de vertex : un pointeur vers la mémoire tampon de vertex, chaque argument de [**IDirect3DDevice9 :: SetStreamSource**](/windows/desktop/api)et le séparateur (le cas échéant) à partir de [**IDirect3DDevice9 :: SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).
-   Pointeur vers la mémoire tampon d’index.
-   La fenêtre d’affichage.
-   Rectangle de ciseaux.
-   Matrices universelles, de vue et de projection.
-   Transformations de texture.
-   Plans de découpage (le cas échéant).
-   La matière actuelle.

Pour capturer tous les États d’appareil avec un bloc d’État, spécifiez D3DSBT \_ All lors de l’appel de [**IDirect3DDevice9 :: CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[État de l’enregistrement et de la restauration des blocs d’État](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
