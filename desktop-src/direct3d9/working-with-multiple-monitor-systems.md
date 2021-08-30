---
description: 'Le concept de mode plein écran exclusif est conservé dans Direct3D 9, mais il est conservé entièrement implicite dans les appels de la méthode IDirect3D9 :: CreateDevice et IDirect3DDevice9 :: Reset.'
ms.assetid: c3503d62-d9f9-4eec-8af3-ebcbfe7064d4
title: Utilisation de systèmes à plusieurs moniteurs (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cea4625038f701288676b95fc86c5ed7d56b292795c14b43031affa817bd8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025729"
---
# <a name="working-with-multiple-monitor-systems-direct3d-9"></a>Utilisation de systèmes à plusieurs moniteurs (Direct3D 9)

Le concept de mode plein écran exclusif est conservé dans Direct3D 9, mais il est conservé entièrement implicite dans les appels de la méthode [**IDirect3D9 :: CreateDevice**](/windows/desktop/api) et [**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) . Chaque fois qu’un appareil est réinitialisé ou créé avec succès en mode plein écran, l’objet Direct3D qui a créé l’appareil est marqué comme propriétaire de tous les adaptateurs sur ce système. Cet État est appelé mode exclusif et à ce stade, l’objet Direct3D est propriétaire du mode exclusif. Le mode exclusif signifie que les appareils créés par tout autre objet Direct3D9 ne peuvent ni supposer l’opération en plein écran, ni allouer de la mémoire vidéo. En outre, lorsqu’un objet Direct3D9 utilise le mode exclusif, tous les périphériques autres que l’appareil qui s’est déroulé en plein écran sont placés dans l’état perdu. Pour plus d’informations sur la gestion des appareils perdus, consultez [appareils perdus (Direct3D 9)](lost-devices.md).

En plus du mode exclusif, l’objet Direct3D9 est informé de la fenêtre de focus que l’appareil doit utiliser. Le mode exclusif est relâché lorsque le dernier appareil plein écran détenu par cet objet Direct3D9 est réinitialisé en mode fenêtre ou détruit.

Les appareils peuvent être divisés en deux catégories lorsqu’un objet Direct3D9 est propriétaire du mode exclusif. La première catégorie d’appareils est celle qui a été créée par le même objet Direct3D9 que celui qui est déjà plein écran, qui ont la même fenêtre de focus que l’appareil qui est déjà plein écran et qui représentent un adaptateur différent à partir de n’importe quel périphérique plein écran. Les appareils de cette catégorie n’ont aucune restriction quant à leur capacité de réinitialisation ou de création et ne sont pas placées dans l’état perdu. Les appareils de cette catégorie peuvent même être placés en mode plein écran.

Les appareils qui ne sont pas dans cette catégorie, qui sont créés par un autre objet Direct3D9, ou avec une fenêtre de focus différente, ou pour une carte avec un appareil déjà plein écran ne peuvent pas être réinitialisés et restent dans l’état perdu tant que le mode exclusif n’est pas perdu.

L’implication pratique est qu’une application à plusieurs analyses peut placer plusieurs appareils en mode plein écran, mais uniquement si tous ces appareils sont destinés à des adaptateurs différents, ont été créés par le même objet Direct3D9 et partagent tous la même fenêtre de focus.

Lorsque vous créez un nouveau périphérique à l’aide du même objet [**IDirect3D9**](/windows/desktop/api) et de la fenêtre de focus, votre appareil d’origine perd ses surfaces. Vous devrez appeler [**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) sur le premier appareil pour que votre application puisse l’utiliser. Par exemple, pour créer deux appareils, procédez comme suit :

1.  Créer l’appareil 1
2.  Créer l’appareil 2
3.  Réinitialiser l’appareil 1

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Astuces de programmation](programming-tips.md)
</dt> </dl>

 

 
