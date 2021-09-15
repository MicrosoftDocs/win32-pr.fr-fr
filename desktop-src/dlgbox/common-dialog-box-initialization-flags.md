---
title: Indicateurs d’initialisation de la boîte de dialogue commune
description: Les indicateurs sont utilisés pour modifier le comportement et l’apparence d’une boîte de dialogue commune.
ms.assetid: 072cdcab-00d1-4a09-97fb-a6de2d51392e
keywords:
- Bibliothèque de boîtes de dialogue communes, initialisation
- boîtes de dialogue communes, initialisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b0c994e743178e3b6a17129275affed099d3004
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519197"
---
# <a name="common-dialog-box-initialization-flags"></a>Indicateurs d’initialisation de la boîte de dialogue commune

Les indicateurs sont utilisés pour modifier le comportement et l’apparence d’une boîte de dialogue commune. Les indicateurs d’initialisation sont les valeurs que vous définissez dans le membre **Flags** de la structure utilisée pour créer la boîte de dialogue. Vous utilisez les indicateurs pour spécifier les contrôles d’une boîte de dialogue qui reçoivent des valeurs initiales, pour désactiver les contrôles sélectionnés et pour modifier la plage de valeurs que l’utilisateur peut définir avec les contrôles. Vous utilisez également les indicateurs pour activer les procédures de hook et les modèles personnalisés pour les boîtes de dialogue.

Par exemple, vous pouvez définir la valeur des **\_ effets CF** dans le membre **Flags** de la structure [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) pour indiquer à la boîte de dialogue **police** d’afficher les contrôles Effects. Ces contrôles permettent à l’utilisateur de choisir une couleur de police, ainsi que les effets du barré et du trait de soulignement.

Les valeurs d’indicateur d’initialisation sont uniques à chaque boîte de dialogue commune et sont décrites en détail par les membres **indicateurs** des structures suivantes qui correspondent :

-   [**LES ChooseColor.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
-   [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
-   [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
-   [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
-   [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
-   [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)
-   [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)

 

 




