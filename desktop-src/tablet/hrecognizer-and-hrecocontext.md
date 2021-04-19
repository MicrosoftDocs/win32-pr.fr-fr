---
description: Vous faites référence à un module de reconnaissance d’encre avec un handle HRECOGNIZER et un contexte de reconnaissance comme handle HRECOCONTEXT. Une bibliothèque de liens dynamiques (DLL) de module de reconnaissance peut implémenter des identificateurs pour plusieurs langages.
ms.assetid: 23002d02-cf8f-489b-a50f-4a18ac091825
title: HRECOGNIZER et HRECOCONTEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12af1bb5569a22a612f0a3ed667a55aac81da2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514839"
---
# <a name="hrecognizer-and-hrecocontext"></a>HRECOGNIZER et HRECOCONTEXT

Vous faites référence à un module de reconnaissance d’encre avec un handle [HRECOGNIZER](hrecognizer-handle.md) et un contexte de reconnaissance comme handle [HRECOCONTEXT](hrecocontext-handle.md) .

Une bibliothèque de liens dynamiques (DLL) de module de reconnaissance peut implémenter des identificateurs pour plusieurs langages. Si c’est le cas, chaque langue est sélectionnée par un CLSID qui est passé lors de la création de l’objet [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) dans l’application. En outre, une DLL de reconnaissance peut créer plusieurs descripteurs de reconnaissance lorsqu’elle est chargée, une ou plusieurs pour chaque langue reconnue.

Un contexte de module de reconnaissance est créé pour représenter l’événement qui consiste à reconnaître un élément d’encre spécifique. Lorsque le contexte est créé, le descripteur d’objets de module de reconnaissance associé est passé à la fonction [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext) . Cela associe le langage au contexte du module de reconnaissance.

Un contexte de module de reconnaissance peut représenter la reconnaissance de toute l’encre dans le corps d’un message électronique, l’encre d’un champ unique dans une application ou une ligne unique de texte écrite dans le panneau de saisie Tablet PC. Le volume d’encre dans un contexte de reconnaissance unique peut varier d’un trait unique à une page entière ou plus.

Le contexte du module de reconnaissance est défini par les paramètres suivants :

-   Guide de reconnaissance.
-   N’importe quel Factoids.
-   Indicateurs éventuels.
-   Contexte de texte.
-   Liste de mots.
-   Mode de saisie semi-automatique des caractères.

Le handle du contexte de module de reconnaissance est passé à toutes les fonctions qui utilisent ces paramètres. La modification d’un paramètre modifie le contexte du module de reconnaissance.

L’application peut utiliser plusieurs contextes pour reconnaître l’encre à partir de différentes parties de l’écran. Un contexte individuel peut reconnaître plusieurs lignes de texte. Toutefois, un contexte individuel ne peut pas traiter deux paragraphes écrits côte à côte, par exemple plusieurs colonnes dans un article de journal.

Pour reconnaître une nouvelle encre, créez un nouveau contexte. Vous pouvez également utiliser la fonction [**CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext) pour effectuer une copie d’un contexte qui n’a pas l’encre et les résultats, ou la fonction [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext) pour effacer un contexte de son encre et de ses résultats. Avec ces approches, une application Ink peut réutiliser un contexte.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**SetGuide fonction)**](/windows/desktop/api/recapis/nf-recapis-setguide)
</dt> <dt>

[**GetGuide fonction)**](/windows/desktop/api/recapis/nf-recapis-getguide)
</dt> <dt>

[**SetFactoid fonction)**](/windows/desktop/api/recapis/nf-recapis-setfactoid)
</dt> <dt>

[**SetFlags fonction)**](/windows/desktop/api/recapis/nf-recapis-setflags)
</dt> <dt>

[**SetEnabledUnicodeRanges fonction)**](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)
</dt> <dt>

[**GetEnabledUnicodeRanges fonction)**](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)
</dt> <dt>

[**SetCACMode fonction)**](/windows/desktop/api/recapis/nf-recapis-setcacmode)
</dt> <dt>

[**SetTextContext fonction)**](/windows/desktop/api/recapis/nf-recapis-settextcontext)
</dt> <dt>

[**SetWordList fonction)**](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 



