---
title: Comment implémenter des info-bulles pour les icônes de barre d’État
description: Une méthode non intrusive pour afficher un message explicatif pour une icône de barre d’état consiste à implémenter une info-bulle. L’info-bulle disparaît lorsque vous cliquez dessus, mais vous pouvez également spécifier une valeur de délai d’attente.
ms.assetid: AA7F17F2-63A4-4954-9DAB-788B73984628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2bd100dc6edb2aac7b4c8c5df3781e76391ae2d9d0ad456533384ed8701f14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958578"
---
# <a name="how-to-implement-tooltips-for-status-bar-icons"></a>Comment implémenter des info-bulles pour les icônes de barre d’État

Une méthode non intrusive pour afficher un message explicatif pour une icône de barre d’état consiste à implémenter une info-bulle. L’info-bulle disparaît lorsque vous cliquez dessus, mais vous pouvez également spécifier une valeur de délai d’attente.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

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



## <a name="remarks"></a>Remarques

Pour obtenir une présentation détaillée de la barre d’État, consultez [la barre des tâches](/windows/desktop/shell/taskbar).

Pour afficher une info-bulle, vous devez définir l' \_ indicateur d’informations NSI dans la structure [**NOTIFYICONDATA**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) et utiliser les membres **szInfo** et **uTimeout** pour spécifier le texte d’info-bulle et la durée du délai d’attente.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

 