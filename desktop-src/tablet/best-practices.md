---
description: Vue d’ensemble des meilleures pratiques lors de l’utilisation de l’objet panneau de saisie Pen.
ms.assetid: 5b127743-0c88-4c4c-bcb6-5a91690cd2a1
title: Meilleures pratiques (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd492dfeda94ce9dce056b286ef1989f3389658c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522292"
---
# <a name="best-practices-tablet-pc"></a>Meilleures pratiques (Tablet PC)

Voici quelques recommandations à prendre en compte lors de l’utilisation de l’objet [**PenInputPanel**](peninputpanel-class.md) .

-   [Préférer le contrôle InkEdit](#prefer-inkedit-control)
-   [Désactiver le mode Ink sur les contrôles InkEdit](#disable-ink-mode-on-inkedit-controls)
-   [Utilisation des contrôles sans fenêtre](#using-windowless-controls)
-   [Rubriques connexes](#related-topics)

## <a name="prefer-inkedit-control"></a>Préférer le contrôle InkEdit

[InkEdit](inkedit-control-reference.md) est le contrôle par défaut auquel attacher l’objet [**PenInputPanel**](peninputpanel-class.md) . Le contrôle InkEdit fournit la prise en charge de [Text Services Framework (TSF)](text-services-framework.md).

## <a name="disable-ink-mode-on-inkedit-controls"></a>Désactiver le mode Ink sur les contrôles InkEdit

Lorsqu’il est attaché à un contrôle [InkEdit](inkedit-control-reference.md) , affectez à la propriété [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) du contrôle InkEdit la valeur [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) . Si la propriété **InkMode** n’est pas définie sur la valeur **InkMode** , le contrôle InkEdit interprète le premier TAP comme un trait, le transmet au module de reconnaissance et insère le texte dans le contrôle InkEdit. Étant donné que vous avez déjà un objet [**PenInputPanel**](peninputpanel-class.md) joint pour accepter l’entrée manuscrite, il n’est pas nécessaire que le contrôle InkEdit soit également activé pour l’entrée manuscrite.

## <a name="using-windowless-controls"></a>Utilisation des contrôles sans fenêtre

Lorsqu’un objet [**PenInputPanel**](peninputpanel-class.md) est attaché à une fenêtre parente qui contient plus d’un contrôle sans fenêtre, l’objet **PenInputPanel** ne sait pas comment suivre le signe insertion lorsque le focus se déplace entre des enfants sans fenêtre. Une entrée d’écriture manuscrite peut être envoyée à un enfant incorrect lorsque le focus passe d’un contrôle sans fenêtre à un autre alors que l’entrée est en attente.

Pour utiliser l’objet [**PenInputPanel**](peninputpanel-class.md) dans un environnement sans fenêtre, vous pouvez utiliser la technique suivante :

1.  Instanciez un contrôle [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) et positionnez-le sur le contrôle sans fenêtre.
2.  Attachez l’objet [**PenInputPanel**](peninputpanel-class.md) au nouveau contrôle zone de texte.
3.  Laissez le contrôle de zone de texte collecter le texte reconnu à partir de l’objet [**PenInputPanel**](peninputpanel-class.md) .
4.  Lorsque le focus est modifié en dehors du contrôle Text Box, appelez la méthode [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) de l’objet [**PenInputPanel**](peninputpanel-class.md) .
5.  Copiez le texte reconnu à partir du contrôle zone de texte dans l’enfant sans fenêtre.
6.  Détachez l’objet [**PenInputPanel**](peninputpanel-class.md) en affectant à sa propriété [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (code managé uniquement) ou à la propriété [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) la valeur null.
7.  Détruisez le contrôle Text Box.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**PenInputPanel, classe**](peninputpanel-class.md)
</dt> <dt>

[Microsoft. Ink. PenInputPanel](/previous-versions/ms583923(v=vs.100))
</dt> <dt>

[Text Services Framework](../tsf/text-services-framework.md)
</dt> </dl>

 

 
