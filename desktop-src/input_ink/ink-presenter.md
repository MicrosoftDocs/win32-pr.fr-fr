---
description: Les API d’affichage d’entrées manuscrites permettent aux applications Win32 de gérer les entrées, le traitement et le rendu des entrées manuscrites (standard ou personnalisées), par le biais d’un objet InkPresenter inséré dans l’arborescence virtuelle DirectComposition de l’application.
ms.assetid: 8BD52813-3741-4C1F-B62A-B3C366A86362
title: Présentateur d’encre
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9bd9f4c3c98b443110a0a7948075ab836a9493c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203876"
---
# <a name="ink-presenter"></a>Présentateur d’encre

Les API de présentateur d’encre permettent aux applications Microsoft Win32 de gérer l’entrée, le traitement et le rendu des entrées manuscrites (standard et modifiées) via un objet [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) inséré dans l’arborescence d’éléments visuels [DirectComposition](../directcomp/directcomposition-portal.md) de l’application.

> [!Note]
>
> L’entrée d’encre standard (info-bulle ou bouton de gomme) n’est pas modifiée à l’aide d’une offre secondaire, telle qu’un bouton de stylet, un bouton droit de la souris ou similaire.

Les applications plateforme Windows universelle (UWP) utilisant Extensible Application Markup Language (XAML) fournissent cette fonctionnalité via un contrôle [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) avec un objet [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) qui se connecte à l’arborescence d’éléments visuels [DirectComposition](../directcomp/directcomposition-portal.md) XAML. Pour plus d’informations, consultez [interactions du stylet et](/windows/uwp/design/input/pen-and-stylus-interactions)du stylet.

Le [convertisseur d’encre](ink-renderer.md) est conçu pour être utilisé par les développeurs d’applications Windows universelles qui souhaitent fournir des fonctionnalités d’InkPresenter [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)basés sur XAML / [](/uwp/api/windows.ui.input.inking.inkpresenter) dans les applications Win32 natives.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                               | Description                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Classes de présentateur d’encre](ink-presenter-classes.md)<br/>       | Les rubriques contenues dans cette section fournissent les spécifications de référence pour les classes de présentateur d’encre. <br/>    |
| [Interfaces de présentateur d’encre](ink-presenter-interfaces.md)<br/> | Les rubriques contenues dans cette section fournissent les spécifications de référence pour les interfaces de présentateur d’encre. <br/> |



 

## <a name="related-topics"></a>Rubriques connexes

[Présentation](ink-presenter.md)de l’encre, [interactions du stylet et](/windows/uwp/design/input/pen-and-stylus-interactions)du stylet, [exemple d’analyse](/samples/microsoft/windows-universal-samples/inkanalysis/)de l’encre, exemple d' [encrage simple](/samples/microsoft/windows-universal-samples/simpleink/), [exemple d’écriture](/samples/microsoft/windows-universal-samples/complexink/) manuscrite complexe
