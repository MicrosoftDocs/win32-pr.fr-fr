---
description: Représente la zone utilisée par le module de reconnaissance dans laquelle l’encre peut être dessinée. La zone est appelée Guide de reconnaissance.
ms.assetid: c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7
title: InkRecognizerGuide, classe (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRecognizerGuide
- InkRecognizerGuide.IInkRecognizerGuide
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 758c2ac58803b0086a4a4083545a66d250799b414bd44e3814c90de37ca9d082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675662"
---
# <a name="inkrecognizerguide-class"></a>InkRecognizerGuide, classe

Représente la zone utilisée par le module de reconnaissance dans laquelle l’encre peut être dessinée. La zone est appelée Guide de reconnaissance.

**InkRecognizerGuide** possède les types de membres suivants :

-   [Interfaces](#interfaces)
-   [Propriétés](#properties)

### <a name="interfaces"></a>Interfaces

La classe **InkRecognizerGuide** définit ces interfaces.



| Interface               | Description                                                                  |
|:------------------------|:-----------------------------------------------------------------------------|
| **IInkRecognizerGuide** | Cet objet implémente l’interface com **IInkRecognizerGuide** .<br/> |



 

### <a name="properties"></a>Propriétés

La classe **InkRecognizerGuide** possède les propriétés suivantes.



| Propriété                                                       | Type d’accès           | Description                                                                                                                    |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**Colonnes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns)<br/>       | Lecture/écriture<br/> | Obtient ou définit le nombre de colonnes dans la zone du repère.<br/>                                                                |
| [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox)<br/>     | Lecture/écriture<br/> | Obtient ou définit la zone qui est physiquement dessinée sur l’écran de la tablette et dans laquelle l’écriture a lieu.<br/>              |
| [**GuideData**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_guidedata)<br/>   | Lecture/écriture<br/> | Obtient ou définit les données de guide pour les développeurs C++.<br/>                                                                         |
| [**Médian**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_midline)<br/>       | Lecture/écriture<br/> | Obtient ou définit la hauteur de la médiane. La hauteur de la ligne médiane est la distance entre la ligne de base et la ligne médiane de la zone dessinée.<br/> |
| [**Lignes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_rows)<br/>             | Lecture/écriture<br/> | Obtient ou définit le nombre de lignes dans la zone du repère.<br/>                                                                   |
| [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox)<br/> | Lecture/écriture<br/> | Obtient ou définit la zone d’écriture invisible de la zone de repère dans laquelle l’écriture peut avoir lieu.<br/>                  |



 

## <a name="remarks"></a>Remarques

Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .

Par défaut, il n’existe aucun guide de reconnaissance. Toutes les valeurs de propriété d’un repère par défaut sont définies sur 0. Vous devez utiliser les propriétés de cet objet pour définir le repère.

Si l’application a dessiné des instructions à l’écran sur lequel l’utilisateur est censé écrire, l’application doit définir les valeurs des propriétés du Guide de reconnaissance pour informer le module de reconnaissance. Ces propriétés sont réservées à l’utilisation du module de reconnaissance. Leur définition ne fait pas, en soi, des indices visuels à l’écran. L’application ou le contrôle dessine les indices visuels.

Le Guide de reconnaissance peut se composer de lignes et de colonnes, et ceux-ci donnent au module de reconnaissance un meilleur contexte dans lequel effectuer la reconnaissance. Les lettres telles que « t » et « I » sont plus facilement reconnues lorsqu’un guide est utilisé pour fournir le contexte à l’encre. Par exemple, vous pouvez dessiner des lignes horizontales sur un écran, qui indiquent où l’écriture doit se produire (ce type de repère se compose uniquement de lignes et pas de colonnes). En écrivant sur les lignes, au lieu d’un espace arbitraire, la précision de la reconnaissance est améliorée.

Le repère spécifie les limites de l’encre dans les coordonnées de l’espace d’encre.

La propriété [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox) peut définir une zone de taille inférieure ou égale à la zone définie par la propriété [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox) .

L’illustration suivante montre les éléments d’un guide de reconnaissance avec deux lignes et aucune colonne.

![Illustration montrant des éléments du Guide de reconnaissance](images/927cc2f3-549f-4279-aab9-bd5ade070eaf.jpg)

En plus de dessiner des lignes sur l’écran qui indiquent aux utilisateurs où écrire, vous pouvez dessiner des cellules à l’écran dans lesquelles des caractères ou des mots sont écrits. C’est ce que l’on appelle une entrée boxed et est utile avec certaines langues asiatiques. Pour déterminer si le module de reconnaissance est apte à l’entrée boxed, appelez la propriété [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) de l’objet [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) .

L’illustration suivante montre un guide de reconnaissance avec quatre colonnes.

![illustration illustrant le Guide de reconnaissance avec quatre colonnes](images/de44c07e-4b55-42d0-8e8b-997e2da79e52.jpg)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[**InkRecognizerContext, classe**](inkrecognizercontext-class.md)
</dt> </dl>

 

