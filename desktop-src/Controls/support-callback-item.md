---
title: Comment prendre en charge les éléments de rappel
description: Cette rubrique montre comment assurer la prise en charge des éléments de rappel.
ms.assetid: BD32666F-9445-4871-AE21-5DC9F5FC9C1B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df078b8be8cd02f56592a74de4242b515974a740df01d3cd4bd36074d5f8e022
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968219"
---
# <a name="how-to-support-callback-items"></a>Comment prendre en charge les éléments de rappel

Cette rubrique montre comment assurer la prise en charge des éléments de rappel.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions


Si votre application va utiliser des éléments de rappel dans un contrôle ComboBoxEx, elle doit être préparée à gérer le code de notification [CBEN \_ GETDISPINFO](cben-getdispinfo.md) . Un contrôle ComboBoxEx envoie cette notification chaque fois qu’il a besoin du propriétaire pour fournir des informations spécifiques sur l’élément. Pour plus d’informations sur les éléments de rappel, consultez [éléments de rappel](comboboxex-controls.md).

La fonction suivante définie par l’application traite [CBEN \_ GETDISPINFO](cben-getdispinfo.md) en fournissant des attributs pour un élément donné. Notez qu’elle définit le membre **Mask** de la structure [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) entrante sur CBEIF \_ di \_ SETITEM. Si vous définissez le **masque** sur cette valeur, le contrôle conserve les informations de l’élément afin qu’il n’ait pas besoin de demander à nouveau les informations.

## <a name="complete-example"></a>Exemple complet


```C++
// DoItemCallback - Processes CBEN_GETDISPINFO by providing item
// attributes for a given callback item.

void WINAPI DoItemCallback(PNMCOMBOBOXEX pNMCBex)
{
    DWORD dwMask = pNMCBex->ceItem.mask;

    if(dwMask & CBEIF_TEXT)
    {
            // Insert code to provide item text.
    }

    if(dwMask & CBEIF_IMAGE) 
    {
        // Insert code to provide an item image index.
    }

    // Insert code to provide other callback information as desired.

    // Make the ComboBoxEx control hold onto the item information.
    pNMCBex->ceItem.mask = CBEIF_DI_SETITEM;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des contrôles ComboBoxEx](comboboxex-controls.md)
</dt> <dt>

[Référence du contrôle ComboBoxEx](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[Utilisation des contrôles ComboBoxEx](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[ComboBoxEx](comboboxex-control-reference.md)
</dt> </dl>

 

 