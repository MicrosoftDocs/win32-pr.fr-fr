---
description: L’objet DivisionUnit représente un élément structurel unique d’un objet DivisionResult. Un objet DivisionUnit peut représenter un dessin, un segment unique de reconnaissance de l’écriture manuscrite, une ligne d’écriture manuscrite ou un bloc d’écriture manuscrite.
ms.assetid: 13f6121c-2b83-4788-9d06-460dc03094bf
title: Utilisation de l’objet DivisionUnit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade8b617ae8e64c2641ef53a628a44e72e4fc35f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862482"
---
# <a name="working-with-the-divisionunit-object"></a>Utilisation de l’objet DivisionUnit

L’objet **DivisionUnit** représente un élément structurel unique d’un objet **DivisionResult** . Un objet **DivisionUnit** peut représenter un dessin, un segment unique de reconnaissance de l’écriture manuscrite, une ligne d’écriture manuscrite ou un bloc d’écriture manuscrite.

L’énumération [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) définit les types d’éléments structurels reconnus par l’analyse de la disposition. Dans Automation, l’objet **DivisionUnit** est appelé [**IInkDivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit).

La propriété [**DivisionType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_divisiontype) de l’objet **DivisionUnit** retourne le type d’élément structurel de l’objet **DivisionUnit** . La propriété [**RecognitionString**](/previous-versions/windows/desktop/legacy/ms703283(v=vs.85)) de l’objet **DivisionUnit** retourne le texte de reconnaissance pour les éléments d’écriture manuscrite, ou **null** pour les éléments de dessin.

La propriété [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_strokes) de l’objet **DivisionUnit** contient le sous-ensemble des traits de l’objet **DivisionResult** qui correspondent à cet élément. Étant donné que les éléments d’écriture manuscrite existent pour différents niveaux de détail, les collections de **traits** pour les différents éléments peuvent se chevaucher. Plus précisément, un segment de reconnaissance partage les traits avec la ligne et le bloc dont il fait partie, et une ligne partage les traits avec le bloc dont il fait partie.

La propriété [**RotationTransform**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionunit-get_rotationtransform) de l’objet **DivisionUnit** retourne une matrice pour faire pivoter les traits de l’élément horizontalement. Pour les éléments paragraph et Drawing, la propriété **RotationTransform** retourne la matrice d’identité. Un module de reconnaissance de texte fonctionne bien mieux sur l’écriture manuscrite alignée horizontalement que sur l’écriture manuscrite qui ne l’est pas. Dans Automation, c’est ce que l’on appelle la propriété **RotationTransform** et elle retourne un objet [**InkTransform**](inktransform-class.md) qui contient la matrice de transformation. La propriété **RotationTransform** retourne la **valeur null** pour les éléments paragraph et Drawing.

Pour plus d’informations sur l’objet **DivisionResult** , consultez [utilisation de l’objet DivisionResult](working-with-the-divisionresult-object.md).

 

 
