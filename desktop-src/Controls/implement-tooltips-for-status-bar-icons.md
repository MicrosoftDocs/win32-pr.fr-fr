---
title: Comment implémenter des info-bulles pour les icônes de barre d’État
description: Une méthode non intrusive pour afficher un message explicatif pour une icône de barre d’état consiste à implémenter une info-bulle. L’info-bulle disparaît lorsque vous cliquez dessus, mais vous pouvez également spécifier une valeur de délai d’attente.
ms.assetid: AA7F17F2-63A4-4954-9DAB-788B73984628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277fb8d15654ae51565c1a461a9a8414d3e9213c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463786"
---
# <a name="how-to-implement-tooltips-for-status-bar-icons"></a>Comment implémenter des info-bulles pour les icônes de barre d’État

Une méthode non intrusive pour afficher un message explicatif pour une icône de barre d’état consiste à implémenter une info-bulle. L’info-bulle disparaît lorsque vous cliquez dessus, mais vous pouvez également spécifier une valeur de délai d’attente.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions

### <a name="implement-tooltips-for-status-bar-icons"></a>Implémenter des info-bulles pour les icônes de barre d’État

Le fragment de code suivant montre comment ajouter une info-bulle à une icône de barre d’État.


```C++
#define ARRAYSIZE(a) (sizeof(a)/sizeof(a[0]))

NOTIFYICONDATA IconData = {0};

IconData.cbSize = sizeof(IconData);
IconData.hWnd   = hwndNI;
IconData.uFlags = NIF_INFO;

HRESULT hr = StringCchCopy(IconData.szInfo, 
                           ARRAYSIZE(IconData.szInfo), 
                           TEXT("Your message text goes here."));

if(FAILED(hr))
{
  // TODO: Write an error handler in case the call to StringCchCopy fails.
}
IconData.uTimeout = 15000; // in milliseconds

Shell_NotifyIcon(NIM_MODIFY, &IconData);
            
```



## <a name="remarks"></a>Notes

Pour obtenir une présentation détaillée de la barre d’État, consultez [la barre des tâches](/windows/desktop/shell/taskbar).

Pour afficher une info-bulle, vous devez définir l' \_ indicateur d’informations NSI dans la structure [**NOTIFYICONDATA**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) et utiliser les membres **szInfo** et **uTimeout** pour spécifier le texte d’info-bulle et la durée du délai d’attente.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

 