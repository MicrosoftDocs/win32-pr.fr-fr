---
description: Les rubriques contenues dans cette section fournissent les spécifications de référence pour les interfaces de présentateur d’encre.
ms.assetid: 68172566-586C-41AC-82B8-5DBE8B50EC8F
title: Interfaces de présentateur d’encre
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 1839c8ebc0a7597ab7c5becaf7c7492128b4d6af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520516"
---
# <a name="ink-presenter-interfaces"></a>Interfaces de présentateur d’encre

Les rubriques contenues dans cette section fournissent les spécifications de référence pour les interfaces de [présentateur d’encre](ink-presenter.md) .

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|---|---|
| [**IInkCommitRequestHandler**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkcommitrequesthandler)<br/> | Active votre application (au lieu d’un objet [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) ) pour valider toutes les commandes DirectComposition Microsoft en attente dans l’arborescence d’éléments visuels [DirectComposition](../directcomp/directcomposition-portal.md) de l’application.<br/>   |
| [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost)<br/>                   | Active l’entrée d’encre, le traitement et le rendu via la création d’un thread d’application pour héberger un objet [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) et l’insérer dans l’arborescence d’éléments visuels [DirectComposition](../directcomp/directcomposition-portal.md) de l’application. <br/> |
| [**IInkHostWorkItem**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkhostworkitem)<br/>                 | Représente une opération d’entrée manuscrite à exécuter sur un thread d’objet [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) .<br/>                                                                                                                                                  |
| [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop)<br/>         | Représente un [**InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) qui peut être configuré et inséré dans l’arborescence d’éléments visuels [DirectComposition](../directcomp/directcomposition-portal.md) de l’application Windows classique. <br/>                                        |

## <a name="related-topics"></a>Rubriques connexes

[Présentation](ink-presenter.md)de l’encre, [interactions du stylet et](/windows/uwp/design/input/pen-and-stylus-interactions)du stylet, [exemple d’analyse](/samples/microsoft/windows-universal-samples/inkanalysis/)de l’encre, exemple d' [encrage simple](/samples/microsoft/windows-universal-samples/simpleink/), [exemple d’écriture](/samples/microsoft/windows-universal-samples/complexink/) manuscrite complexe
