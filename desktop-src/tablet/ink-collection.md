---
description: La collection d’encres commence par le digitaliseur.
ms.assetid: 95e49f5b-d6f0-4a5a-868b-aa0caf87c39c
title: Collection d’encres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e45988ea93aac5016391e22c352b9d0123a5e122f4a79c55e41e06834ed040e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452065"
---
# <a name="ink-collection"></a>Collection d’encres

La collection d’encres commence par le digitaliseur. Un utilisateur place un stylet sur le digitaliseur et commence à écrire. Vous pouvez utiliser les fonctionnalités de la collecte d’encres de l’API pour gérer la collection de données d’encre qui « enchaîne » à partir du stylet. Vous avez accès aux informations sur le matériel disponible sur Tablet PC par le biais de la collection de [**tablettes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablets-item) et de l’objet [**tablette**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) . Vous utilisez ensuite l’objet [**InkCollector**](inkcollector-class.md) pour récupérer les données provenant du digitaliseur.

## <a name="tablets-and-the-tablet-object"></a>Tablettes et objet tablette

Une [**tablette**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) représente un appareil de numérisation de Tablet PC. Un Tablet PC peut avoir plusieurs numériseurs. À l’aide de l’objet **Tablet** , vous pouvez interroger les appareils digitaliseurs disponibles attachés au Tablet PC et leurs capacités matérielles respectives. Par exemple, vous pouvez déterminer si la **tablette** avec laquelle vous travaillez est intégrée à l’affichage ou s’il s’agit d’un appareil externe distinct.

## <a name="inkcollector-object"></a>Objet InkCollector

L’objet [**InkCollector**](inkcollector-class.md) capture l’entrée manuscrite à partir de périphériques [**tablettes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) disponibles. L’objet **InkCollector** collecte uniquement les entrées manuscrites et les gestes qui sont entrés dans une fenêtre spécifique. Un récepteur d’événements très efficace rend cette entrée en temps réel. L’objet **InkCollector** capture l’entrée et la dirige vers un objet [**Ink**](inkdisp-class.md) .

> [!Note]  
> La disposition simultanée d’encre avec plusieurs stylets peut ou non fonctionner, selon les capacités matérielles du périphérique numériseur.

 

### <a name="how-the-ink-collector-works"></a>Fonctionnement du collecteur d’encre

L’objet [**InkCollector**](inkcollector-class.md) s’attache à une fenêtre d’application connue. Il permet ensuite aux utilisateurs d’utiliser n’importe quel appareil Tablet PC disponible (y compris la souris) pour présenter l’encre en temps réel dans cette fenêtre. Les traits d’encre collectés sont stockés dans un objet [**Ink**](inkdisp-class.md) associé. Ces traits peuvent ensuite être manipulés ou envoyés à un module de reconnaissance pour la reconnaissance. L’objet **InkCollector** notifie également l’application lorsqu’un curseur est placé dans la plage des appareils Tablet PC utilisés.

Pour que l’objet [**InkCollector**](inkcollector-class.md) définisse avec précision le curseur de la souris dans une fenêtre activée pour l’écriture manuscrite, cette fenêtre doit pouvoir recevoir le message **WM \_ SETCURSOR** . Cette opération est réussie pour toutes les fenêtres normales, mais pour un contrôle dans une boîte de dialogue, la boîte de dialogue parent du contrôle filtre ce message. Pour que le contrôle reçoive le message, définissez le style de **\_ notification SS** .

## <a name="inkoverlay-object"></a>Objet InkOverlay

L’objet [**InkCollector**](inkcollector-class.md) , abordé précédemment, est utile pour les applications qui fournissent leur propre modèle de sélection, de suppression et d’autres interactions avec l’utilisateur. L’objet [**InkOverlay**](inkoverlay-class.md) est un sur-ensemble de l’objet **InkCollector** qui prend en charge la modification. Cela est utile pour les applications qui intègrent le dessin et la modification manuscrits dans leur propre canevas de document à l’aide d’un ensemble de modèles de sélection d’encre standard fournis par l’objet.

L’objet [**InkCollector**](inkcollector-class.md) et l’objet [**InkOverlay**](inkoverlay-class.md) (ainsi que le contrôle [InkPicture](inkpicture-control.md) ) utilisent tous deux des constructions courantes, telles que l’objet [**Ink**](inkdisp-class.md) et la collection [**DrawingAttributes**](inkdrawingattributes-class.md) , afin que la méthode de base pour modifier la couleur de l’encre soit la même partout. Cela vous permet de réutiliser du code et d’avoir un accès par programme courant, ce qui peut être particulièrement important si vous offrez une prise en charge des scripts dans votre application.

[**InkOverlay**](inkoverlay-class.md) est un objet com qui est utile pour les scénarios d’annotation dans lesquels les utilisateurs ne sont pas soucieux d’effectuer la reconnaissance de l’encre, mais qui sont intéressés par la taille, la forme, la couleur et la position de l’encre. Il est bien adapté à la création de notes et au griffonnage de base. L’interface utilisateur par défaut est un rectangle transparent avec une encre opaque.

[**InkOverlay**](inkoverlay-class.md) étend la classe [**InkCollector**](inkcollector-class.md) de trois manières :

-   Il déclenche des événements pour les modifications des attributs Begin-Stroke, end-Stroke et Ink.
-   Il permet aux utilisateurs de sélectionner, d’effacer et de redimensionner de l’encre.
-   Il prend en charge les commandes Couper, copier et coller.

Un scénario classique dans lequel [**InkOverlay**](inkoverlay-class.md) est utile est le marquage d’une diapositive ou d’une image de présentation. L’objet **InkOverlay** facilite l’implémentation des fonctionnalités d’encre et de mise en page requises par ce scénario.

Pour travailler avec [**InkOverlay**](inkoverlay-class.md), vous pouvez :

1.  Instanciez un objet [**InkOverlay**](inkoverlay-class.md) .
2.  Attachez le hWnd (handle, en code managé) d’une fenêtre à la propriété [**HWND**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_hwnd) de l’objet [**InkOverlay**](inkoverlay-class.md) (propriété [handle](/previous-versions/ms582171(v=vs.100)) , en code managé).
3.  Affectez la valeur **true** à la propriété [**Enabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_enabled) de l’objet [**InkOverlay**](inkoverlay-class.md) .

L’objet [**InkOverlay**](inkoverlay-class.md) comprend la prise en charge de l’impression de base, mais vous devez implémenter l’aperçu avant impression ou d’autres fonctionnalités d’impression avancées.

[**InkOverlay**](inkoverlay-class.md) conserve l’encre au format ISF (Ink Serialized Format).

> [!Note]  
> Si le [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) de l’objet [**InkOverlay**](inkoverlay-class.md) est défini sur **Delete** ou **Select**, d’autres événements (tels que [**InkAdded**](inkdisp-inkadded.md), [**InkDeleted**](inkdisp-inkdeleted.md)et [**Stroke**](inkoverlay-stroke.md)) sont déclenchés. Ces événements sont utiles si vous souhaitez implémenter vos propres modes de suppression ou de sélection.

 

### <a name="selecting-ink"></a>Sélection de l’encre

L’objet [**InkOverlay**](inkoverlay-class.md) permet aux utilisateurs d’utiliser un outil lasso pour sélectionner des objets Ink contenus dans une région tracée. Les utilisateurs peuvent également sélectionner une entrée manuscrite en appuyant sur n’importe quel objet [**manuscrit**](inkdisp-class.md) .

Utilisez la propriété [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) pour retourner une collection de [**traits**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que vous pouvez utiliser pour manipuler la sélection d’un utilisateur.

Lorsqu’un objet [**Ink**](inkdisp-class.md) ou un ensemble d’objets **Ink** est sélectionné, les poignées de redimensionnement apparaissent aux quatre coins du cadre englobant de l’encre et à tous les milieux situés entre les angles adjacents. Si l’utilisateur fait glisser n’importe où dans la région sélectionnée, l’encre devient déplaçable à l’intérieur du contrôle.

### <a name="default-behavior"></a>Comportement par défaut

L’objet [**InkOverlay**](inkoverlay-class.md) est défini pour collecter l’encre par défaut. L’encre est 53 unités d’espace d’encre larges (1 unité d’espace d’encre = 1 HIMETRIC). L’encre est noire si l’utilisateur ne s’exécute pas en mode de contraste élevé. Sinon, Ink est défini sur la valeur **Color \_ WINDOWTEXT** (**WINDOWTEXT** en code managé). [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) a la **valeur false**.

### <a name="cursor-and-button-objects"></a>Objets curseur et bouton

Un curseur correspond à l’info-bulle du stylet utilisé sur Tablet PC. Par exemple, un crayon a deux extrémités. En règle générale, une extrémité est utilisée pour l’écriture et l’autre est utilisée pour l’effacement. Ces deux extrémités correspondent à deux curseurs. La classe [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) ne peut pas être confondue avec [**System. Windows. Forms. Cursor**](/dotnet/api/system.windows.forms.cursor?view=netcore-3.1).

Sur Tablet PC, un curseur est généralement défini pour être utilisé pour l’écriture ou l’effacement. Un curseur peut éventuellement modifier des rôles si l’application active cette fonctionnalité. Certains périphériques Tablet PC autorisent plusieurs stylets. Chaque curseur est associé à un ID de curseur unique sur le système. Un curseur peut avoir zéro ou plusieurs boutons associés. Ces boutons sont fournis à l’application en tant qu’objets CursorButton. L’application peut fournir un objet [**DrawingAttributes**](inkdrawingattributes-class.md) spécifique pour un curseur donné.

### <a name="drawing-attributes-object"></a>Objet de dessin des attributs

Un objet [**DrawingAttributes**](inkdrawingattributes-class.md) décrit comment un ensemble connu d’encres doit être dessiné. Un objet **DrawingAttributes** comprend des propriétés de base telles que [**Color**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color), [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)et [**PenTip**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip). Il peut également englober des paramètres avancés, tels que la transparence variable et le lissage de Bézier, qui peuvent fournir des effets intéressants ou améliorer la lisibilité de l’encre.

### <a name="peninputpanel-object"></a>Objet PenInputPanel

> [!Note]  
> La classe [**PenInputPanel**](peninputpanel-class.md) a été dépréciée. La classe **PenInputPanel** a été remplacée par la classe [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) .

 

L’objet [**PenInputPanel**](peninputpanel-class.md) vous permet d’ajouter facilement une entrée de stylet sur place à vos applications. Le **PenInputPanel** est disponible sous la forme d’un objet pouvant être attaché qui vous permet d’ajouter des fonctionnalités du panneau de saisie Tablet PC à des contrôles existants. L’interface utilisateur est en grande partie mandatée par la langue d’entrée actuelle. Vous avez la possibilité de choisir la méthode d’entrée par défaut pour **PenInputPanel**, à savoir l’écriture manuscrite ou le clavier. L’utilisateur final peut basculer entre les méthodes d’entrée à l’aide des boutons de l’interface utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**InkCollector, classe (C++)**](inkcollector-class.md)
</dt> <dt>

[**InkOverlay, classe (C++)**](inkoverlay-class.md)
</dt> <dt>

[**Espace de noms Microsoft. Ink**](/previous-versions/dotnet/netframework-3.5/ms581553(v=vs.90))
</dt> </dl>

 

 
