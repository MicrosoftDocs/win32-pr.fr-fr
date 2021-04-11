---
title: Imprimer la feuille de propriétés
description: La feuille de propriétés d’impression est une interface utilisateur standard qui permet à l’utilisateur de spécifier les propriétés d’un travail d’impression particulier.
ms.assetid: b52b71cc-a583-4a21-8a53-501ab442e6f8
keywords:
- Interface utilisateur Windows, entrée utilisateur
- Interface utilisateur Windows, bibliothèque de boîtes de dialogue communes
- entrée utilisateur, bibliothèque de boîtes de dialogue communes
- capture de l’entrée utilisateur, bibliothèque de boîtes de dialogue communes
- Bibliothèque de boîtes de dialogue communes
- boîtes de dialogue communes
- Boîte de dialogue Imprimer la feuille de propriétés
- personnalisation de la boîte de dialogue feuille de propriétés d’impression
- boîtes de dialogue prédéfinies
- boîtes de dialogue, feuille de propriétés d’impression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20905f76af290b3978bec828a382604147297998
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031826"
---
# <a name="print-property-sheet"></a>Imprimer la feuille de propriétés

La feuille de propriétés d' **impression** est une interface utilisateur standard qui permet à l’utilisateur de spécifier les propriétés d’un travail d’impression particulier. La feuille de propriétés est composée d’un ensemble de pages de propriétés qui varie selon l’imprimante ou l’application. Pour un sous-ensemble de pages de propriétés Windows standard, certaines imprimantes peuvent ajouter des pages de propriétés spécifiques au pilote et certaines applications peuvent ajouter des pages de propriétés spécifiques à l’application.

Pour créer et afficher une feuille de propriétés d' **impression** , initialisez une structure [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) et transmettez la structure à la fonction [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) .

L’illustration suivante montre une feuille de propriétés d' **impression** typique.

![feuille de propriétés de l’imprimante](images/printerpropertypagexp.png)

La plupart des membres de la structure [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) sont identiques à ceux de la structure [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) . Pour obtenir des descriptions de l’utilisation des membres de la structure commune pour interagir avec les contrôles de boîte de dialogue, consultez [boîte de dialogue Imprimer](print-dialog-box.md). Le reste de cette rubrique décrit les fonctionnalités de feuille de propriétés d' **impression** qui diffèrent de la boîte de dialogue **Imprimer** .

Vous pouvez personnaliser une feuille de propriétés d' **impression** en spécifiant un modèle de boîte de dialogue personnalisé pour la partie inférieure de la page **général** et en spécifiant des pages de propriétés supplémentaires pour suivre la page **général** . Pour plus d’informations, consultez [Personnalisation de la feuille de propriétés d’impression](#customizing-the-print-property-sheet).

Vous pouvez implémenter un objet de rappel pour recevoir des notifications et des messages de la fonction [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) lors de l’affichage de la feuille de propriétés. Les applications qui fournissent des modèles personnalisés ou des pages supplémentaires utilisent l’objet de rappel pour communiquer avec la feuille de propriétés. Pour plus d’informations, consultez [objet de rappel pour la feuille de propriétés imprimer](#callback-object-for-the-print-property-sheet).

La feuille de propriétés d' **impression** prend en charge la spécification de plusieurs plages de pages non contiguës à imprimer. Le membre **lpPageRanges** de la structure [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) spécifie un tableau de structures [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) dans lequel chaque structure spécifie une plage de pages.

La feuille de propriétés **Imprimer** affiche une case d’option **page active** dans le groupe de **plages de pages** des cases d’option. Pour contrôler la case d’option **page active** , utilisez les indicateurs **PD \_ CURRENTPAGE** et **PD \_ NOCURRENTPAGE** dans le membre **Flags** de la structure [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) .

Cette section décrit les rubriques suivantes.

-   [Personnalisation de la feuille de propriétés d’impression](#customizing-the-print-property-sheet)
-   [Objet de rappel pour la feuille de propriétés d’impression](#callback-object-for-the-print-property-sheet)

## <a name="customizing-the-print-property-sheet"></a>Personnalisation de la feuille de propriétés d’impression

Vous pouvez personnaliser la feuille de propriétés d' **impression** des manières suivantes :

-   Fournissez un modèle personnalisé pour la partie inférieure de la page **général** . Cela vous permet d’inclure des contrôles supplémentaires qui sont propres à votre application. La fonction [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) utilise votre modèle personnalisé à la place du modèle par défaut.
-   Fournissez des pages de propriétés supplémentaires pour suivre la page **général** .
-   Fournissez un objet de rappel. Pour plus d’informations, consultez [objet de rappel pour la feuille de propriétés imprimer](#callback-object-for-the-print-property-sheet).

Vous ne pouvez pas modifier la partie supérieure de la page **général** . Vous ne pouvez pas modifier les pages de propriétés fournies par le pilote d’imprimante.

Pour fournir un modèle personnalisé pour la page général :

1.  Créez un modèle personnalisé pour la partie inférieure de la page **général** en modifiant le modèle PRINTDLGEXORD spécifié dans le fichier Prnsetup. dlg. En règle générale, le modèle personnalisé doit avoir la même taille que le modèle par défaut. Toutefois, vous pouvez agrandir le modèle personnalisé si vous spécifiez l’indicateur **PD \_ USELARGETEMPLATE** pour créer une page **générale** plus grande. Les identificateurs de contrôle utilisés dans le modèle de boîte de dialogue d' **impression** par défaut sont définis dans le fichier Dlgs. h.
2.  Utilisez la structure [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) pour activer le modèle comme suit :
    -   Si votre modèle personnalisé est une ressource d’une application ou d’une bibliothèque de liens dynamiques, définissez l’indicateur **PD \_ ENABLEPRINTTEMPLATE** dans le membre **Flags** . Utilisez les membres **HINSTANCE** et **lpPrintTemplateName** de la structure pour identifier le nom du module et de la ressource.

        Ou

    -   Si votre modèle personnalisé est déjà en mémoire, définissez l’indicateur **PD \_ ENABLEPRINTTEMPLATEHANDLE** . Utilisez le membre **HINSTANCE** pour identifier l’objet mémoire qui contient le modèle.

3.  Si vous utilisez un modèle personnalisé pour définir des contrôles supplémentaires, vous devez fournir un objet de rappel pour traiter l’entrée de vos contrôles. L’objet de rappel implémente une méthode [**IPrintDialogCallback :: HandleMessage**](/windows/win32/api/commdlg/nf-commdlg-iprintdialogcallback-handlemessage) qui reçoit les messages envoyés à la boîte de dialogue personnalisée.

Pour fournir des pages de propriétés supplémentaires

1.  Utilisez la fonction pour créer les pages supplémentaires.
2.  Utilisez le membre **lphPropertyPages** de la structure [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) pour spécifier un tableau de handles vers les pages supplémentaires.

    Les procédures de boîte de dialogue spécifiées lorsque vous avez créé chaque page traitent les messages envoyés aux pages.

3.  Vous pouvez fournir un objet de rappel qui implémente l’interface. La fonction [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) utilise cette interface pour passer à l’application un pointeur vers une interface [**IPrintDialogServices**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogservices) . Les procédures de la boîte de dialogue pour les pages de propriétés supplémentaires peuvent utiliser cette interface pour récupérer des informations sur l’imprimante actuellement sélectionnée.

## <a name="callback-object-for-the-print-property-sheet"></a>Objet de rappel pour la feuille de propriétés d’impression

Une application qui affiche une feuille de propriétés d' **impression** peut implémenter un objet de rappel pour recevoir des notifications et des messages de la fonction [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) lors de l’affichage de la feuille de propriétés. Pour fournir un objet de rappel, spécifiez un pointeur vers l’objet dans le membre **lpCallback** de la structure [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) .

L’objet de rappel doit implémenter l’interface [**IPrintDialogCallback**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogcallback) . La fonction [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) appelle les méthodes **IPrintDialogCallback** dans les cas suivants :

-   Quand la boîte de dialogue a été initialisée
-   Quand l’utilisateur sélectionne une autre imprimante dans la liste des imprimantes installées affichée par la feuille de propriétés
-   Lorsqu’il reçoit des messages pour la boîte de dialogue enfant dans la partie inférieure de la page **général** de la feuille de propriétés

L’objet de rappel doit également implémenter l’interface [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) . La fonction [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) appelle la méthode pour passer un pointeur vers une interface [**IPrintDialogServices**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogservices) à une application. Les méthodes [**IPrintDialogCallback**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogcallback) peuvent utiliser l’interface **IPrintDialogServices** pour récupérer des informations sur l’imprimante actuellement sélectionnée. L’interface **IPrintDialogServices** est également utile pour les applications qui créent des pages supplémentaires pour suivre la page **général** de la feuille de propriétés **Imprimer** . Les procédures de la boîte de dialogue pour les pages supplémentaires peuvent appeler des méthodes **IPrintDialogServices** .

 

 