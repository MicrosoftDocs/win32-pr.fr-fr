---
title: SCROLLBAR, contrôle
description: Définit un contrôle de barre de défilement.
ms.assetid: 9b0b60b1-4b4b-494e-90d0-aaa67e7ea88c
keywords:
- Menus de contrôle de barre de défilement et autres ressources
topic_type:
- apiref
api_name:
- SCROLLBAR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ef4069988603c7c89ec2ed8a363d3515a0b8bb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101636"
---
# <a name="scrollbar-control"></a>SCROLLBAR, contrôle

Définit un contrôle de barre de défilement. Le contrôle est un rectangle qui contient une case de défilement et contient des flèches de direction aux deux extrémités. Le contrôle de barre de défilement envoie un message de notification à son parent chaque fois que l’utilisateur clique sur la souris dans le contrôle. Le parent est responsable de la mise à jour de la position de la boîte de défilement. Les contrôles de barre de défilement peuvent être positionnés n’importe où dans une fenêtre et utilisés chaque fois que nécessaire pour fournir une entrée de défilement.

``` syntax
SCROLLBAR id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*style*
</dt> <dd>

Zéro ou une combinaison des styles suivants : **WS \_ TABSTOP**, **WS \_ Group** et WS est **\_ désactivé**.

En plus de ces styles, le paramètre de *style* peut contenir une combinaison (ou aucune) des styles de la classe ScrollBar.

Si vous ne spécifiez pas de style, le style par défaut est de type **SBS \_ Horiz**.

</dd> </dl>

Pour plus d’informations sur la syntaxe générale d’une instruction de contrôle, consultez [paramètres de contrôle communs](common-control-parameters.md). Notez que vous ne pouvez pas spécifier de texte pour ce contrôle.

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation de l’instruction **ScrollBar** :

``` syntax
#define IDC_SCROLLBARV                  1010

SCROLLBAR IDC_SCROLLBARV, 7, 55, 187, 44, SBS_VERT
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Barres de défilement](../controls/about-scroll-bars.md)
</dt> </dl>

 

 