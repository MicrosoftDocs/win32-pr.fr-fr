---
description: Les clusters de caractères sont des séquences de glyphes qui ne peuvent pas être fractionnées entre les lignes.
ms.assetid: ab852feb-9e26-429e-a02a-11fe0abdfafc
title: Utilisation de clusters de caractères
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11357a929cf8fec2a7b0caa2bb6ae1ac403e3b91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224084"
---
# <a name="using-character-clusters"></a>Utilisation de clusters de caractères

Les clusters de caractères sont des séquences de glyphes qui ne peuvent pas être fractionnées entre les lignes. Certains langages, par exemple thaï et Indo-aryen, limitent l’emplacement du signe insertion aux points entre les clusters. Cette restriction s’applique au déplacement du signe insertion initié avec les actions du clavier ou de la souris (test de positionnement).

Uniscribe fournit des informations de cluster dans les attributs visuels contenus dans une structure de [**\_ VISATTR de script**](/windows/win32/api/usp10/ns-usp10-script_visattr) et les attributs logiques contenus dans une structure de [**script \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) . Une fois que l’application a appelé [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), les informations de cluster sont représentées à la fois par séquences de la même valeur dans le tableau **\_ LOGATTR de script** et par le membre **FClusterStart** dans le tableau **\_ VISATTR de script** .

[**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) récupère également le membre **fCharStop** de la structure de [**script \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) pour identifier les positions de cluster.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



