---
description: Un script complexe est un script pour lequel le membre fComplex des propriétés de SCRIPT \_ a la valeur true. Cette rubrique détaille les propriétés qu’un script complexe peut avoir.
ms.assetid: bceeb0d6-bda3-43bf-984e-87fbfb327578
title: À propos des scripts complexes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1e865b7638419178e3339169e56e8ceb111bcc65b925d9c337b5b71d0341827
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520649"
---
# <a name="about-complex-scripts"></a>À propos des scripts complexes

Un [script complexe](uniscribe-glossary.md) est un script pour lequel le membre **fcomplex** des [**\_ Propriétés de script**](/windows/desktop/api/Usp10/ns-usp10-script_properties) a la valeur **true**. Cette rubrique détaille les propriétés qu’un script complexe peut avoir.

## <a name="bidirectional-rendering"></a>Rendu bidirectionnel

Le rendu bidirectionnel est le traitement du texte qui lit de gauche à droite et de droite à gauche. Par exemple, dans le rendu bidirectionnel de l’arabe, le sens de lecture par défaut pour le texte est de droite à gauche, mais il est de gauche à droite pour certains nombres. Le traitement d’un script complexe doit tenir compte de la différence entre l’ordre logique (frappe) et l’ordre visuel des glyphes. En outre, le traitement doit correctement gérer le mouvement du signe insertion et le test de positionnement. Le mappage entre la position de l’écran et un index de caractère requiert une compréhension des algorithmes de disposition pour l’affichage particulier, par exemple, la sélection de texte ou l’affichage du signe insertion.

## <a name="contextual-shaping"></a>Mise en forme contextuelle

Dans le cadre de la mise en forme contextuelle, les caractères de script changent de forme en fonction des caractères qui les entourent. Une telle mise en forme se produit en anglais en écriture cursive quand un « l » minuscule change de forme en fonction du caractère qui le précède, par exemple un « a » (se connecte au « l ») ou un « o » (se connecte à un niveau élevé). Par exemple, l’arabe est un script qui présente une mise en forme contextuelle.

## <a name="combining-characters"></a>Combinaison de caractères

La combinaison de caractères, également appelée « ligatures », sont des caractères qui se joignent dans un caractère lorsqu’ils sont placés ensemble. L’arabe est un script qui comporte de nombreux caractères d’association. Un exemple de l’utilisation de la combinaison de caractères est le « a » suivi de « combinaison de caractères graves », pour lequel la représentation rendue est « à ». Le flux Unicode « U + 0061 U + 0300 » requiert un traitement pour s’assurer que la combinaison « combinaison grave » est correctement positionnée au-dessus du « a ».

## <a name="specialized-word-break-and-justification"></a>Césure et justification de mot spécialisées

Certains scripts, par exemple, le thaï, comportent des règles complexes pour diviser les mots entre les lignes ou pour justifier du texte sur une ligne.

## <a name="filtering-for-illegal-character-combinations"></a>Filtrage pour les combinaisons de caractères non conformes

Un script complexe, par exemple thaï, peut filtrer les combinaisons de caractères non conformes lorsqu’une langue n’autorise pas certaines combinaisons de caractères.

## <a name="font-fallback"></a>Police de secours

La police de secours est la sélection automatisée d’une police autre que la police sélectionnée par l’utilisateur. Dans Uniscribe, la police de secours est appliquée par la fonction [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) lorsque la totalité ou une partie du texte est dans un script que la police sélectionnée par l’utilisateur ne prend pas en charge. Pour plus d’informations, consultez Utilisation de la [police de secours](using-font-fallback.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 



