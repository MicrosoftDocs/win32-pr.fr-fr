---
description: Les langages de script complexes sont divisés en clusters par ScriptShape. La réorganisation des caractères se produit toujours dans les limites du cluster. Les clusters eux-mêmes sont assurés d’avancer dans le sens de l’ordre de lecture.
ms.assetid: 50b4b643-af96-4a6f-80f9-27a71ce16b0e
title: Gestion de l’emplacement du signe insertion et du test de positionnement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60396a668c89f7392b28adde0bb123060bf50348
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520399"
---
# <a name="managing-caret-placement-and-hit-testing"></a>Gestion de l’emplacement du signe insertion et du test de positionnement

Les langages de script complexes sont divisés en [clusters](uniscribe-glossary.md) par [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape). La réorganisation des caractères se produit toujours dans les limites du cluster. Les clusters eux-mêmes sont assurés d’avancer dans le sens de l’ordre de lecture.

Les informations de cluster dans le groupe de clusters logiques sont utilisées pour partager la largeur d’un cluster de glyphes de manière égale entre les caractères logiques qu’ils représentent. Par exemple, le glyphe Lam Lam est divisé en quatre zones :

-   La moitié principale du Lam.
-   La moitié de fin du Lam.
-   Moitié gauche de l’Alef.
-   La moitié de la fin de l’Alef.

Les conventions d’emplacement du signe insertion au sein des clusters dépendent du script. Pour le script arabe, si la position du signe insertion est définie entre un caractère de base et sa marque de combinaison, le signe insertion est affiché à mi-chemin dans le caractère de base. Pour le script thaï, le signe insertion ne peut pas être positionné au sein d’un cluster. Ainsi, lorsque l’utilisateur avance le signe insertion, l’application doit avancer tous les glyphes qui composent le cluster.

Les fonctions [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) et [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) se traduisent entre les positions du signe insertion (en pixels de décalage de point de code) et les positions x (en pixels). La fonction **ScriptXtoCP** a connaissance des conventions de position du signe insertion de chaque script :

-   Pour l’Inde et le thaï, les positions du signe insertion sont alignées sur les limites du cluster.
-   Pour l’arabe, les positions du signe insertion sont interpolées avec les clusters.
-   Pour l’hébreu, dans les versions antérieures à Usp10.dll, la version 1,420, les positions du signe insertion sont interpolées avec les clusters. À partir de Usp10.dll, version 1,420, les positions du signe insertion sont alignées sur les limites du cluster.

[**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) et [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) fonctionnent uniquement dans les exécutions. Les fonctions requièrent que certains paramètres proviennent d’appels Uniscribe antérieurs, comme indiqué dans le tableau suivant.



| Paramètre                                        | Source                                                 |
|--------------------------------------------------|--------------------------------------------------------|
| *tests*                                            | Tel qu’il est retourné par [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize). |
| *cGlyphspwLogClust*<br/> *psva*<br/> | Tel qu’il est retourné par [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape).     |
| *piAdvance*                                      | Tel qu’il est retourné par [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace).     |



 

L’application doit établir la série dans laquelle un décalage de signe insertion ou une position x donnée avant de passer les informations à [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) ou [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp). Si l’application n’enregistre pas les informations de largeur, elle peut effectuer un test de positionnement et un placement de signe insertion après l’affichage de chaque exécution. En guise d’alternative, l’application peut mettre en cache suffisamment d’informations pour effectuer des tests de positionnement et placer le curseur sur la ligne active sans nécessiter de retraitement du paragraphe.

[**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) retourne une valeur de bord de fin pour que l’application sache le côté du caractère ou du cluster sur lequel l’utilisateur a cliqué. La valeur est égale à 0 ou à la largeur du caractère ou du cluster en points de code. La position de caractère retournée correspond à la position du caractère sur lequel l’utilisateur a cliqué. Pour plus d’informations, consultez [affichage du signe insertion dans les chaînes bidirectionnelles](displaying-the-caret-in-bidirectional-strings.md).

Pour les langues telles que le thaï, pour lesquelles l’utilisateur ne souhaite pas placer le signe insertion dans un cluster, [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) définit l’indicateur côté fin sur 0 ou sur la largeur du cluster. Pour les langues telles que l’arabe, pour lesquelles l’utilisateur s’attend à pouvoir effectuer des modifications au sein d’un cluster, **ScriptXtoCP** affecte à l’indicateur de fin de fin la valeur 0 ou 1.

Pour aider l’application à établir des emplacements valides pour le signe insertion lors du traitement des touches de direction, Uniscribe fournit des informations sur les positions de signe insertion valides dans le membre **fCharStop** dans les attributs logiques retournés par [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak). La **valeur true** est retournée pour la plupart des caractères et **false** pour les caractères interclusters dans les scripts tels que le thaï. L’application doit vérifier la valeur **fNeedsCaretInfo** dans la structure des [**\_ Propriétés de script**](/windows/desktop/api/Usp10/ns-usp10-script_properties) pour un élément afin de déterminer s’il est nécessaire d’appeler **ScriptBreak** pour vérifier les positions de signe insertion valides. Si la valeur **fNeedsCaretInfo** est **false**, tous les points de code sont des positions de signe insertion valides.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 




