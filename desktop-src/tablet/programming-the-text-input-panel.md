---
description: À compter de Windows Vista, le TextInputPanel remplace le PenInputPanel pour contrôler l’apparence et le comportement à l’écran du panneau de saisie de tablette. les sections suivantes décrivent la programmation du panneau de saisie à l’aide des interfaces de programmation d’application du panneau de saisie de texte. TextInputPanel pour les utilisateurs du panneau de saisie PenInputPanelUsing correction de texte AutoCompleteEnabling pour l’encre personnalisée CollectorsNote le panneau de saisie de texte est implémenté dans un fichier exécutable appelé TabTip.exe. L’exécution de TabTip.exe avec le paramètre/SeekDesktop tente d’exécuter une version de fonctionnalité réduite du panneau de saisie sur un bureau interactif non standard, tel qu’il est créé avec CreateDesktop. Pour la plupart des bureaux créés, le panneau de saisie s’exécutera automatiquement dans ce mode. Ce paramètre permet de le lancer dans des scénarios d’application inhabituels qui, sinon, empêchent le lancement automatique. Si le panneau de saisie est déjà en cours d’exécution sur le bureau, ce paramètre n’a aucun effet et l’instance de TabTip.exe s’arrête immédiatement.
ms.assetid: af0a2946-88d0-4f2e-98ca-446398aeb6b8
title: Programmation du panneau de saisie de texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5e6b379a26199e602fc68402d77fa89fb4f8fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536655"
---
# <a name="programming-the-text-input-panel"></a>Programmation du panneau de saisie de texte

À compter de Windows Vista, le [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) remplace le [**PenInputPanel**](peninputpanel-class.md) pour contrôler l’apparence et le comportement à l’écran du panneau de saisie Tablet PC.

Les sections suivantes décrivent la programmation du panneau de saisie à l’aide des interfaces de programmation d’application du panneau de saisie de texte.

-   [TextInputPanel pour les utilisateurs de PenInputPanel](textinputpanel-for-users-of-peninputpanel.md)
-   [Utilisation de la saisie semi-automatique du panneau de saisie](using-input-panel-autocomplete.md)
-   [Activation de la correction de texte pour les collecteurs d’encre personnalisés](enabling-text-correction-for-custom-ink-collectors.md)

> [!Note]  
> Le panneau de saisie de texte est implémenté dans un fichier exécutable appelé TabTip.exe. L’exécution de TabTip.exe avec le paramètre */SeekDesktop* tente d’exécuter une version de fonctionnalité réduite du panneau de saisie sur un bureau interactif non standard, tel qu’il est créé avec [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa). Pour la plupart des bureaux créés, le panneau de saisie s’exécutera automatiquement dans ce mode. Ce paramètre permet de le lancer dans des scénarios d’application inhabituels qui, sinon, empêchent le lancement automatique. Si le panneau de saisie est déjà en cours d’exécution sur le bureau, ce paramètre n’a aucun effet et l’instance de TabTip.exe s’arrête immédiatement.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Programmation du panneau de saisie à l’aide de la classe PenInputPanel](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
