---
title: Élément THEMe
description: Élément THEMe
ms.assetid: fe7e793e-1774-412c-aed2-721ed2cf1bb3
keywords:
- apparences de Lecteur Windows Media, élément theme
- apparences, élément THEMe
- Élément THEMe
- référence pour les apparences, élément THEMe
- éléments, thème
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8cd0d40b4b020cf5416569417401af9e4f3a33b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013194"
---
# <a name="theme-element"></a>Élément THEMe

L’élément **Theme** est l’élément de niveau parent d’une apparence et contient un ou plusieurs éléments **View** , qui à leur tour contiennent tous les autres éléments d’une apparence. Dans le code de script, l’élément **Theme** est accessible via l’attribut global **Theme** plutôt que via un nom spécifié par un attribut **ID** , ce qui n’est pas pris en charge par l’élément **Theme** .

L’élément **Theme** prend en charge les attributs suivants.



| Attribut                                | Description                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [auteur](theme-author.md)               | Spécifie ou récupère le nom de l’auteur de l’apparence.                                                                      |
| [authorVersion](theme-authorversion.md) | Spécifie ou récupère le numéro de version de l’apparence, tel qu’il est assigné par l’auteur.                                                |
| [intellectuelle](theme-copyright.md)         | Spécifie ou récupère la chaîne de copyright pour l’apparence.                                                                       |
| [currentViewID](theme-currentviewid.md) | Spécifie ou récupère la **vue** actuellement affichée.                                                                        |
| [title](theme-title.md)                 | Spécifie ou récupère le titre de l’apparence.                                                                                   |
| [version](theme-version.md)             | spécifie ou récupère le numéro de version Lecteur Windows Media pour lequel l’apparence a été créée. Ne peut être défini qu’au moment de la conception. |



 

L’élément **Theme** prend en charge les méthodes suivantes.



| Méthode                                         | Description                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [Évènement CloseView](theme-closeview.md)               | Ferme une **vue** ouverte.                                                                                        |
| [loadPreference](theme-loadpreference.md)     | Charge une préférence à partir du Registre.                                                                           |
| [logString](theme-logstring.md)               | Consigne une chaîne définie par l’utilisateur dans le fichier d’erreur si la journalisation est activée.                                            |
| [openDialog](theme-opendialog.md)             | Ouvre une boîte de dialogue de fichier.                                                                                        |
| [openView](theme-openview.md)                 | Ouvre une **vue** dans une nouvelle fenêtre.                                                                               |
| [openViewRelative](theme-openviewrelative.md) | Ouvre une **vue** dans une nouvelle fenêtre à une position initiale spécifiée par rapport à l’angle supérieur gauche de l’apparence. |
| [playSound](theme-playsound.md)               | Lit le fichier son spécifié.                                                                                 |
| [savePreference](theme-savepreference.md)     | Enregistre une préférence dans le registre.                                                                             |
| [showErrorDialog](theme-showerrordialog.md)   | Affiche la boîte de dialogue erreur standard.                                                                         |



 

L’élément **Theme** ne prend pas en charge les gestionnaires d’événements.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence de programmation de l’apparence**](skin-programming-reference.md)
</dt> </dl>

 

 




