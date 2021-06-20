---
title: Rubriques de procédures (DirectWrite)
description: Consultez les rubriques de procédures dans le Guide de programmation de l’API DirectWrite. DirectWrite permet aux applications Windows d’améliorer l’expérience de texte pour l’interface utilisateur et les documents.
ms.assetid: da4817ee-0bff-433f-b595-4250199bcc14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc35d9b92001bc8c4807f8b77434559994aaac4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406392"
---
# <a name="how-to-topics-directwrite"></a>Rubriques de procédures (DirectWrite)

Les rubriques suivantes fournissent une vue d’ensemble de l’API [DirectWrite](direct-write-portal.md) .

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                                                                                   | Description                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Comment aligner du texte](how-to-align-text.md)<br/>                                                                                                                   | Vous pouvez aligner du texte [DirectWrite](direct-write-portal.md) à l’aide de la méthode [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) de l’interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)<br/>                                                                                                                                                                                                               |
| [Comment ajouter la prise en charge de plusieurs moniteurs](how-to-add-support-for-multiple-monitors.md)<br/>                                                                     | [DirectWrite](direct-write-portal.md) prend en charge les systèmes avec plusieurs moniteurs. Différentes analyses peuvent avoir une géométrie de pixels différente (RVB, BGR ou plat) ou d’autres attributs. Pour plus d’informations sur la géométrie des pixels, consultez la rubrique de référence sur la [**\_ \_ géométrie des pixels DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) . Cette rubrique vous montre comment ajouter la prise en charge de plusieurs moniteurs à votre application DirectWrite. <br/> |
| [Comment garantir que votre application s’affiche correctement sur les affichages haute résolution](how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays.md)<br/> | Décrit comment créer une fenêtre qui s’affiche correctement sur les affichages haute résolution.<br/>                                                                                                                                                                                                                                                                                                                                               |
| [Comment s’assurer que le texte est affiché avec le sens de lecture correct](how-to-ensure-text-is-displayed-with-the-correct-reading-direction.md)<br/>                 | Certains langages, tels que l’arabe et l’hébreu, requièrent un sens de lecture de droite à gauche. Pour un objet de format de texte [DirectWrite](direct-write-portal.md) , le sens de lecture par défaut est de gauche à droite. DirectWrite ne déduit pas automatiquement le sens de lecture des paramètres régionaux. vous devez donc le faire vous-même.<br/>                                                                                                   |
| [Comment énumérer les polices](font-enumeration.md)<br/>                                                                                                               | Cette vue d’ensemble indique comment énumérer les polices de la collection de polices système, par nom de famille.<br/>                                                                                                                                                                                                                                                                                                                          |
| [Comment effectuer un test de positionnement sur une disposition de texte](how-to-perform-hit-testing-on-a-text-layout.md)<br/>                                                               | Fournit un bref didacticiel sur l’ajout d’un test de positionnement à une application [DirectWrite](direct-write-portal.md) qui affiche du texte à l’aide de l’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . <br/>                                                                                                                                                                                                                  |
| [Comment ajouter des objets intralignes à une disposition de texte](how-to-add-inline-objects-to-a-text-layout.md)<br/>                                                                 | Fournit un bref didacticiel sur l’ajout d’objets en ligne à une application [DirectWrite](direct-write-portal.md) qui affiche du texte à l’aide de l’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . <br/>                                                                                                                                                                                                                         |
| [Comment ajouter des effets de dessin client à une disposition de texte](how-to-add-custom-drawing-efffects-to-a-text-layout.md)<br/>                                                | Fournit un bref didacticiel sur l’ajout d’effets de dessin client à une application [DirectWrite](direct-write-portal.md) qui affiche du texte à l’aide de l’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) et d’un convertisseur de texte personnalisé. <br/>                                                                                                                                                                                      |



 

 

