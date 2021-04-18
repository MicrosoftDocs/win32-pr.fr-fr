---
description: 'Quand un appareil est réinitialisé avec succès (IDirect3DDevice9 :: Reset) ou créé (IDirect3D9 :: CreateDevice) dans les opérations en plein écran, l’objet Direct3D qui a créé l’appareil est marqué comme étant propriétaire de tous les adaptateurs sur ce système.'
ms.assetid: df3b6ed7-830b-4635-9295-fff05cc35891
title: Opérations de Multiple-Monitor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04427db6c91ff85706040589a89f6fdcfb3761e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513285"
---
# <a name="multiple-monitor-operations-direct3d-9"></a>Opérations de Multiple-Monitor (Direct3D 9)

Quand un appareil est réinitialisé avec succès ([**IDirect3DDevice9 :: Reset**](/windows/desktop/api)) ou créé ([**IDirect3D9 :: CreateDevice**](/windows/desktop/api)) dans les opérations en plein écran, l’objet Direct3D qui a créé l’appareil est marqué comme étant propriétaire de tous les adaptateurs sur ce système. Cet État est appelé mode exclusif et l’objet Direct3D est propriétaire du mode exclusif. Le mode exclusif signifie que les appareils créés par tout autre objet Direct3D ne peuvent ni assumer les opérations en plein écran, ni allouer de la mémoire vidéo. En outre, lorsqu’un objet Direct3D suppose le mode exclusif, tous les appareils autres que celui qui s’est déroulé en plein écran sont placés dans un état perdu. Pour plus d’informations, consultez [appareils perdus (Direct3D 9)](lost-devices.md).

En même temps que le mode exclusif, l’objet Direct3D est informé de la fenêtre de focus que l’appareil utilisera. Le mode exclusif est relâché quand l’appareil plein écran final détenu par cet objet Direct3D est réinitialisé en mode fenêtre ou détruit.

Les appareils peuvent être divisés en deux catégories lorsqu’un objet Direct3D est propriétaire du mode exclusif. La première catégorie d’appareils a les caractéristiques suivantes.

-   Ils sont créés par le même objet Direct3D qui a créé l’appareil en mode plein écran.
-   Ils ont la même fenêtre de focus que l’appareil plein écran.
-   Ils représentent un adaptateur différent à partir de n’importe quel appareil plein écran.

Les appareils de cette catégorie n’ont aucune restriction quant à leur capacité de réinitialisation ou de création, et ils ne sont pas placés dans un état perdu. Les appareils de cette catégorie peuvent même être mis en mode plein écran.

Les appareils qui ne se trouvent pas dans la première catégorie-les appareils créés par un autre objet Direct3D, créés avec une fenêtre de focus différente, et créés pour un adaptateur avec un appareil qui est déjà plein écran, ne peuvent pas être réinitialisés et restent en état de perte tant que le mode exclusif n’est pas perdu. Par conséquent, une application à plusieurs moniteurs peut placer plusieurs appareils en mode plein écran, mais uniquement si tous ces appareils sont destinés à des adaptateurs différents, ont été créés par le même objet Direct3D et partagent la même fenêtre de focus.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Présentation d’une scène](presenting-a-scene.md)
</dt> </dl>

 

 



