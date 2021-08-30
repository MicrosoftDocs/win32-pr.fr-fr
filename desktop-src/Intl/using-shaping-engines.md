---
description: Uniscribe utilise plusieurs moteurs de mise en forme qui contiennent les connaissances en matière de mise en page pour des scripts particuliers.
ms.assetid: 3cdd18f3-51d3-4d1c-be31-f5709074cbe7
title: Utilisation de moteurs de mise en forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceb0fd75e0612340bc5051f844dda5e9d66c22eb56a88b0c497891a15faaa75d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897849"
---
# <a name="using-shaping-engines"></a>Utilisation de moteurs de mise en forme

Uniscribe utilise plusieurs moteurs de mise en forme qui contiennent les connaissances en matière de mise en page pour des scripts particuliers. Il tire également parti du moteur de mise en forme de mise en page OpenType pour gérer les fonctionnalités de script spécifiques aux polices, telles que la génération de glyphes, la mesure des étendues et la prise en charge de la césure des mots. Uniscribe gère la réorganisation des caractères bidirectionnels à l’aide de l’algorithme bidirectionnel Unicode, et comprend les formats de police de disposition non OpenType pour l’arabe, l’hébreu et la mise en forme thaï.

Étant donné que les plages de points de code exactes affectées à chaque moteur de mise en forme peuvent varier, les numéros de script ne sont pas publiés, à l’exception du SCRIPT non \_ défini. Toutefois, votre application peut tester les attributs des scripts en appelant la fonction [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) , qui accède au tableau des propriétés de script global. L’application peut utiliser les propriétés de script globales pour aider à combiner ses propres règles de disposition avec les cloisonnements du moteur de mise en forme requis.

L’application accède à un moteur de mise en forme avec un appel à la fonction [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) . Tous les moteurs de mise en forme de script complexes, les moteurs de mise en forme de chiffres et les moteurs de mise en forme ASCII valident la police indiquée dans le handle de contexte de périphérique avant la mise en forme. Les scripts complexes doivent être mis en forme à l’aide du script retourné par la fonction [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) pour être lisibles. Les autres séries restent lisibles si elles sont mises en forme avec un SCRIPT non \_ défini spécifié dans le membre **escript** de la structure d' [**\_ analyse de script**](/windows/win32/api/usp10/ns-usp10-script_analysis) , bien qu’ils puissent perdre la qualité typographique.

[**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) retourne 0 en cas de réussite ou \_ \_ le script USP E \_ n' \_ est pas dans \_ la police si la police fournie par l’application ne contient pas suffisamment de glyphes ou de tables de mise en forme. Si l’application spécifie \_ un script non défini et que certains caractères ne sont pas pris en charge par la police, la fonction fonctionne toujours. Dans ce cas, l’application doit analyser la mémoire tampon de sortie de glyphe pour rechercher la présence de glyphes manquants. Pour connaître les stratégies de traitement des glyphes manquants, consultez Utilisation de la [police de substitution](using-font-fallback.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



