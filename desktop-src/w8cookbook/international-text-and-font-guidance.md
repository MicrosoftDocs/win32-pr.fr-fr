---
title: Aide sur le texte et les polices internationaux
description: Aide sur le texte et les polices internationaux
ms.assetid: 0540C9AD-8774-4F0F-B013-48C3EAE59BF2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f9d94c53e4db45666d28a7c23a0e883043ba27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104381974"
---
# <a name="international-text-and-font-guidance"></a>Aide sur le texte et les polices internationaux

## <a name="affected-platforms"></a>Plateformes affectées

<dl> Clients-Windows 8 \| Windows 8.1  
Serveurs-Windows Server 2012 \| Windows server 2012 R2  
</dl>

## <a name="description"></a>Description

Depuis avant Windows 2000, la prise en charge de l’affichage de texte pour les nouveaux scripts a été ajoutée dans chaque version majeure de Windows. Vous trouverez des descriptions des modifications apportées dans chaque version majeure dans l’article [prise en charge des scripts et des polices pour Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx) dans le [Centre de développement global](https://msdn.microsoft.com/goglobal/default).

Notez que la prise en charge d’un script peut nécessiter certaines modifications apportées aux composants de pile de texte, ainsi que les modifications apportées aux polices. Le système d’exploitation Windows possède de nombreux composants de pile de texte : DirectWrite, GDI, Uniscribe, GDI+, WPF, RichEdit, ComCtl32 et d’autres. Les informations fournies concernent principalement GDI et DirectWrite. Elle s’applique également aux infrastructures d’interface utilisateur telles que RichEdit ou l’agent de rendu MSHTML utilisé pour les applications du Windows Store de Windows 8 et pour le rendu du contenu Web, bien que ces composants puissent présenter certaines différences.

## <a name="best-practices"></a>Bonnes pratiques

**Conseils typographiques pour les développeurs**

La typographie est au cœur du langage de conception Microsoft. Chacun des principes de conception de Microsoft renforce l’importance de la typographie. Pour la première fois, les développeurs d’applications disposent d’un ensemble de frameworks qui prennent en charge des fonctionnalités typographiques avancées. Accédez à [affichage et modification de texte](/previous-versions/windows/apps/hh465442(v=win.10)) pour plus d’informations sur l’utilisation de JavaScript et HTML pour afficher et modifier du texte dans les applications du Windows Store.

**Métriques de police**

Les métriques de police sont une zone particulièrement importante pour les développeurs d’applications. Les fichiers de polices contiennent différentes valeurs liées aux métriques verticales et horizontales. Ces valeurs sont documentées dans la [spécification OpenType](https://www.microsoft.com/typography/otspec/) . elles sont exposées par le biais d’une série d’API disponibles dans [structure des \_ \_ métriques de police DWRITE](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) et au niveau de la [structure TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica).

## <a name="resources"></a>Ressources

-   [Prise en charge des scripts et des polices pour Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx)
-   [Accédez au centre de développement global](https://msdn.microsoft.com/goglobal/default)
-   [Affichage et modification de texte](/previous-versions/windows/apps/hh465442(v=win.10))
-   [Spécification OpenType](https://www.microsoft.com/typography/otspec/)
-   [DWRITE \_ , \_ structure des métriques de police](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)
-   [TEXTMETRIC, structure](/windows/win32/api/wingdi/ns-wingdi-textmetrica)

 

 