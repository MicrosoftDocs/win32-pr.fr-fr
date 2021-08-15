---
description: Les méthodes de curseur de la souris permettent à l’application de spécifier un curseur de couleur en fournissant une surface qui contient une image.
ms.assetid: 300a8a6f-abcd-49c9-889b-14b12ff5c821
title: Utilisation des curseurs de souris (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 999bd324c8c3a1a2c743b5417f5d316a9d0f9493ccb4b749545e53e23e58917f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518917"
---
# <a name="working-with-mouse-cursors-direct3d-9"></a>Utilisation des curseurs de souris (Direct3D 9)

Les méthodes de curseur de la souris permettent à l’application de spécifier un curseur de couleur en fournissant une surface qui contient une image. Le système s’assure que ce curseur sera mis à jour à la moitié du taux d’affichage ou plus si la fréquence d’images de l’application est lente. Toutefois, le curseur n’est jamais mis à jour plus fréquemment que la fréquence d’actualisation de l’affichage.

La position du curseur de la souris est liée au curseur système, mise à l’échelle de manière appropriée pour la résolution spatiale en mode d’affichage actuelle, mais elle peut être déplacée explicitement par l’application. Cela est analogue au comportement du curseur de souris système pris en charge par l’API Win32. Pour plus d’informations sur l’utilisation d’un curseur de souris dans votre application Direct3D, consultez les rubriques de référence suivantes.

-   [**IDirect3DDevice9::ShowCursor**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)
-   [**IDirect3DDevice9::SetCursorPosition**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition)
-   [**IDirect3DDevice9::SetCursorProperties**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties)

Direct3D garantit que la souris est prise en charge par les implémentations matérielles ou par le runtime Direct3D qui effectue des opérations blitting accélérées par le matériel lors de l’appel de [**IDirect3DDevice9 ::P renvoyé**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Astuces de programmation](programming-tips.md)
</dt> </dl>

 

 
