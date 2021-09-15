---
description: En plus de récupérer des données de largeur de caractères pour des caractères individuels, les applications doivent également calculer la largeur et la hauteur de chaînes entières.
ms.assetid: 0c1d9142-258a-447f-8950-8d684645383b
title: Largeurs et hauteurs de chaîne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f57846d0588c518f445523361ae186e4b966bf93
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517257"
---
# <a name="string-widths-and-heights"></a>Largeurs et hauteurs de chaîne

En plus de récupérer des données de largeur de caractères pour des caractères individuels, les applications doivent également calculer la largeur et la hauteur de chaînes entières. Deux fonctions récupèrent les mesures de largeur et de hauteur de chaîne : [**GetTextExtentPoint32**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a)et [**GetTabbedTextExtent**](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta). Si la chaîne ne contient pas de caractères de tabulation, une application peut utiliser la fonction **GetTextExtentPoint32** pour récupérer la largeur et la hauteur d’une chaîne spécifiée. Si la chaîne contient des caractères de tabulation, une application doit appeler la fonction GetTabbedTextExtent.

Les applications peuvent utiliser la fonction [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) pour les opérations de retour automatique à la vue. Cette fonction retourne le nombre de caractères d’une chaîne spécifiée qui tiennent dans un espace spécifié.

## <a name="font-ascenders-and-descenders"></a>Hampes et hampes inférieures de la police

Certaines applications déterminent l’interligne entre les lignes de texte de différentes tailles à l’aide de l’ascendeur maximal et du descendant de la police. Une application peut récupérer ces valeurs en appelant la fonction [**GetTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) , puis en vérifiant les membres **tmAscent** et **tmDescent** de [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica).

La hauteur et la descente maximales sont différentes de la hauteur et de la profondeur typographiques. Dans les polices TrueType et OpenType, les jambages typographiques et descendants sont généralement le haut du glyphe f et le bas du glyphe g. Une application peut récupérer l’ascendeur typographique et le descendant pour une police TrueType ou OpenType en appelant la fonction [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) et en vérifiant les valeurs dans les membres **otmMacAscent** et **otmMacDescent** de la structure [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) .

L’illustration suivante montre la différence entre les valeurs de métriques de texte verticale retournées dans les structures [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) et [**OUTLINETEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-outlinetextmetrica) . (Les noms commençant par OTM sont membres de la structure **OUTLINETEXTMETRIC** .)

![illustration qui montre comment les valeurs de métriques de texte contrastent avec les valeurs de métriques de texte en mode plan](images/csftx-03.png)

## <a name="font-dimensions"></a>Dimensions de police

Une application peut récupérer les dimensions physiques d’une police TrueType ou OpenType en appelant la fonction [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) . Une application peut récupérer les dimensions physiques de toute autre police en appelant la fonction [**GetTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) . Pour déterminer les dimensions d’un périphérique de sortie, une application peut appeler la fonction [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) . **GetDeviceCaps** retourne à la fois les dimensions physiques et logiques.

Un pouce logique est une mesure que le système utilise pour présenter des polices lisibles à l’écran et est d’environ 30 à 40% plus grand qu’un pouce physique. L’utilisation de pouces logiques exclut une correspondance exacte entre la sortie de l’écran et l’imprimante. Les développeurs doivent savoir que le texte d’un écran n’est pas simplement une version mise à l’échelle du texte qui s’affichera sur la page, en particulier si les graphiques sont incorporés dans le texte.

 

 
