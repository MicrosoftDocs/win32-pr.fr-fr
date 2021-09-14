---
title: Création de contrôles communs
description: Cette rubrique explique comment créer une fenêtre qui appartient à une classe de fenêtre définie dans la bibliothèque de contrôles communs, Comctl32.dll.
ms.assetid: BCF25606-5B49-43A5-8107-E7220BE3253C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944e8aa70b3367f1d3a12e4f50032e6677c5d706
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857991"
---
# <a name="creating-common-controls"></a>Création de contrôles communs

Cette rubrique explique comment créer une fenêtre qui appartient à une classe de fenêtre définie dans la bibliothèque de contrôles communs, Comctl32.dll.


La plupart des contrôles communs appartiennent à une classe de fenêtre définie dans la DLL de contrôle commune. La classe de fenêtre et la procédure de fenêtre correspondante définissent les propriétés, l’apparence et le comportement du contrôle. Pour vous assurer que la DLL de contrôles communs est chargée, incluez la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) dans votre application. Vous créez un contrôle commun en spécifiant le nom de la classe de fenêtre lors de l’appel de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou en spécifiant le nom de classe approprié dans un modèle de boîte de dialogue.


Chaque type de contrôle commun possède un ensemble de styles de contrôle que vous pouvez utiliser pour faire varier l’apparence et le comportement du contrôle. La bibliothèque de contrôles communs comprend également un ensemble de styles de contrôle qui s’appliquent à deux ou plusieurs types de contrôles communs. Les styles de contrôles communs sont décrits dans la section [styles](common-control-styles.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des contrôles communs](common-controls-intro.md)
</dt> </dl>

 

 