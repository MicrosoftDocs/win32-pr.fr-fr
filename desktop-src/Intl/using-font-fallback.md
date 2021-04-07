---
description: Utilisation de la police de secours
ms.assetid: 952f33b6-ca52-40a2-b914-52c1c62ae0e0
title: Utilisation de la police de secours
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9afb073a01cc1c5b90d4a4861a973846d3ae9ae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760485"
---
# <a name="using-font-fallback"></a>Utilisation de la police de secours

> [!Note]  
> Dans cette rubrique, toutes les remarques sur [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) s’appliquent également à [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype).

 

Votre application doit utiliser la police de secours pendant l’affichage du texte si certains caractères d’une chaîne ne sont pas pris en charge dans la police, ou si l’application utilise un [script complexe](uniscribe-glossary.md) non pris en charge par la police. La spécification de la police de secours est détectée pendant le processus de disposition du texte, lorsque l’application appelle la fonction [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) . Pour plus d’informations sur l’affichage de texte, consultez [affichage de texte avec Uniscribe](displaying-text-with-uniscribe.md).

## <a name="determine-the-need-for-font-fallback-for-unsupported-characters"></a>Déterminer la nécessité d’une police de secours pour les caractères non pris en charge

Si certains caractères d’une chaîne ne sont pas pris en charge dans une police demandée, l’appel d’une application à [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) s’effectue correctement. Toutefois, l’application doit analyser la mémoire tampon de sortie de glyphe pour déterminer la présence de glyphes manquants. L’index de glyphe du glyphe manquant peut être déterminé pour une police spécifique en appelant [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties). Si un glyphe particulier n’est pas disponible, l’application doit soit revenir à une police différente pour un glyphe, soit restituer un symbole graphique qui indique qu’aucun glyphe n’est disponible.

## <a name="determine-the-need-for-font-fallback-for-unsupported-complex-scripts"></a>Déterminer le besoin de police de secours pour les scripts complexes non pris en charge

La police qu’une application préfère pour l’affichage peut ne pas prendre en charge un script complexe qui est requis par le texte. Dans ce cas, l’appel de l’application à [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) échoue avec le code d’erreur E le \_ script \_ n’est pas dans la \_ \_ police.

## <a name="assign-a-fallback-font"></a>Assigner une police de secours

Une fois qu’il a déterminé que la police de secours est requise, l’application doit assigner une police de secours. L’application peut essayer les techniques suivantes :

-   Appelez [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) pour chaque police d’une liste de polices jusqu’à ce qu’un appel ait un retour acceptable.
-   Appelez [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) avec chaque police d’une liste jusqu’à ce qu’il soit possible de déterminer qu’aucune police ne fonctionnera correctement. Si le code d’erreur est toujours \_ E \_ \_ , le script n’est pas dans \_ la police, un script complexe n’est pas pris en charge par les polices. Effectuez le rendu d’un symbole graphique qui indique qu’aucun glyphe n’est disponible, ou spécifiez à nouveau le script comme non défini (aucun traitement de script) et recommencez. Pour définir le script comme non défini, définissez le membre **escript** de la structure [**d' \_ analyse des scripts**](/windows/win32/api/usp10/ns-usp10-script_analysis) sur le script \_ non défini.
-   Appelez [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) avec chaque police d’une liste jusqu’à ce qu’il soit possible de déterminer qu’aucune police ne fonctionnera correctement. Si le code d’erreur indique que certains caractères sont mappés à des glyphes manquants, divisez la chaîne en plages plus petites. Des polices différentes peuvent être assignées à des sous-plages afin que d’autres caractères puissent être rendus.

## <a name="generate-glyph-information"></a>Générer des informations de glyphe

Une fois que l’application a affecté une police qui parvient aux appels à [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), elle peut effectuer des appels à [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) pour générer des informations de largeur avancée de glyphe et de décalage à deux dimensions à partir de la sortie de **ScriptShape**. La police doit être correctement exécutée dans ces appels. Une erreur de police dans un appel à **ScriptPlace** après un succès dans un appel **ScriptShape** indique une police rompue.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



