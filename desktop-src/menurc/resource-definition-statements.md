---
title: Instructions Resource-Definition
description: Les instructions de définition de ressource définissent les ressources que le compilateur de ressources place dans la ressource (. Res).
ms.assetid: f96b8c1e-8188-40b7-8eda-c13b61b8fc41
keywords:
- compilateur de ressources, instructions de définition de ressource
- Ressource TEXTINCLUDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4937eb9d5fb9bba7b174aa9543be8b3f2eb41c90c6bc20a72650114f57fb4fa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869905"
---
# <a name="resource-definition-statements"></a>Instructions Resource-Definition

Les instructions de définition de ressource définissent les ressources que le compilateur de ressources place dans la ressource (. Res). Après le. Le fichier res est lié au fichier exécutable, l’application peut charger ses ressources au moment de l’exécution en fonction des besoins. Toutes les instructions de ressource associent un nom ou un numéro d’identification à une ressource donnée.

Les instructions de définition de ressource peuvent être réparties dans les catégories suivantes :

-   Ressources
-   Contrôles
-   Instructions

Les tableaux suivants décrivent les instructions de définition de ressource.

## <a name="resources"></a>Ressources



| Ressource                                      | Description                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACCÉLÉRATEURS**](accelerators-resource.md) | Définit les touches d’accès rapide du menu.                                                                                                                                                  |
| [**PIXELS**](bitmap-resource.md)             | Définit une image bitmap en la nommant et en spécifiant le nom du fichier qui la contient. (Pour utiliser une image bitmap particulière, l’application la demande par son nom.)                          |
| [**MIRE**](cursor-resource.md)             | Définit un curseur ou un curseur animé en le nommant et en spécifiant le nom du fichier qui le contient. (Pour utiliser un curseur particulier, l’application le demande par son nom.)       |
| [**DIALOGUE**](dialog-resource.md)             | Définit un modèle qu’une application peut utiliser pour créer des boîtes de dialogue.                                                                                                          |
| [**DIALOGEX**](dialogex-resource.md)         | Définit un modèle qu’une application peut utiliser pour créer des boîtes de dialogue.                                                                                                          |
| [**SON**](font-resource.md)                 | Spécifie le nom d’un fichier qui contient une police.                                                                                                                              |
| [**PAGE**](html-resource.md)                 | Spécifie un fichier HTML.                                                                                                                                                         |
| [**SITUÉE**](icon-resource.md)                 | Définit une icône ou une icône animée en la nommant et en spécifiant le nom du fichier qui la contient. (Pour utiliser une icône particulière, l’application la demande par son nom.)            |
| [**MENUS**](menu-resource.md)                 | Définit l’apparence et la fonction d’un menu.                                                                                                                                  |
| [**MENUEX**](menuex-resource.md)             | Définit l’apparence et la fonction d’un menu.                                                                                                                                  |
| [**MESSAGETABLE**](messagetable-resource.md) | Définit une table de messages en la nommant et en spécifiant le nom du fichier qui la contient. Le fichier est un fichier de ressources binaire généré par le compilateur de message.                |
| [**MESSAGES**](popup-resource.md)               | Définit un élément de menu qui peut contenir des éléments de menu et des sous-menus.                                                                                                                   |
| **PLUGPLAY**                                  | Obsolète.                                                                                                                                                                       |
| [**RCDATA**](rcdata-resource.md)             | Définit les ressources de données. Les ressources de données vous permettent d’inclure des données binaires dans le fichier exécutable.                                                                                      |
| [**STRINGTABLE**](stringtable-resource.md)   | Définit les ressources de type chaîne. Les ressources de type chaîne sont des chaînes Unicode ou ASCII qui peuvent être chargées à partir du fichier exécutable.                                                            |
| **TEXTINCLUDE**                               | Ressource spéciale qui est interprétée par Visual C++. Pour plus d’informations, consultez [TN035](/cpp/mfc/tn035-using-multiple-resource-files-and-header-files-with-visual-cpp?view=vs-2019).                                        |
| **TYPELIB**                                   | Ressource spéciale utilisée avec les options de l’éditeur de liens [/TLBID](/cpp/build/reference/tlbid-specify-resource-id-for-typelib?view=vs-2019) et [/TLBOUT](/cpp/build/reference/tlbout-name-dot-tlb-file?view=vs-2019) . |
| [**Défini par l’utilisateur**](user-defined-resource.md) | Définit une ressource qui contient des données spécifiques à l’application.                                                                                                                     |
| [**VERSIONINFO**](versioninfo-resource.md)   | Définit une ressource d’informations sur la version. Contient des informations telles que le numéro de version, le système d’exploitation prévu, etc.                                                  |
| **PILOTE**                                       | Obsolète.                                                                                                                                                                       |



 

Pour plus d’informations sur les ressources MFC prédéfinies, consultez [TN023](/cpp/mfc/tn023-standard-mfc-resources?view=vs-2019) et [TN024](/cpp/mfc/tn024-mfc-defined-messages-and-resources?view=vs-2019).

## <a name="controls"></a>Contrôles



| Contrôler                                            | Description                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [**AUTO3STATE**](auto3state-control.md)           | Crée un contrôle de case à cocher à trois États automatique.                         |
| [**CASE d’option**](autocheckbox-control.md)       | Crée un contrôle de case à cocher automatique.                                     |
| [**RadioButton**](autoradiobutton-control.md) | Crée un contrôle de case d’option automatique.                                  |
| [**ACTIVÉ**](checkbox-control.md)               | Crée un contrôle de case à cocher.                                                |
| [**COMBOBOX**](combobox-control.md)               | Crée un contrôle de zone de liste déroulante.                                                |
| [**RÉGULATION**](control-control.md)                 | Crée un contrôle défini par l’application.                                     |
| [**CTEXT**](ctext-control.md)                     | Crée un contrôle de texte centré.                                            |
| [**DEFPUSHBUTTON**](defpushbutton-control.md)     | Crée un contrôle PUSHBUTTON par défaut.                                       |
| [**EDITTEXT**](edittext-control.md)               | Crée un contrôle d’édition.                                                    |
| [**GROUPBOX**](groupbox-control.md)               | Crée un contrôle de zone de groupe.                                                |
| [**SITUÉE**](icon-control.md)                       | Crée un contrôle Icon. Ce contrôle est une icône affichée dans une boîte de dialogue. |
| [**LISTBOX**](listbox-control.md)                 | Crée un contrôle de zone de liste.                                                 |
| [**LTEXT**](ltext-control.md)                     | Crée un contrôle de texte aligné à gauche.                                        |
| [**PUSHBOX**](pushbox-control.md)                 | Crée un contrôle de zone de push.                                                 |
| [**BOUTONS**](pushbutton-control.md)           | Crée un contrôle de bouton de commande.                                              |
| [**Button**](radiobutton-control.md)         | Crée un contrôle de case d’option.                                             |
| [**RTEXT**](rtext-control.md)                     | Crée un contrôle aligné à droite.                                            |
| [**Rail**](scrollbar-control.md)             | Crée un contrôle de barre de défilement.                                               |
| [**STATE3**](state3-control.md)                   | Crée un contrôle de case à cocher à trois États.                                    |



 

## <a name="statements"></a>Instructions



| .                                            | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**-**](caption-statement.md)                 | Définit le titre d’une boîte de dialogue.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**ATTRIBUTS**](characteristics-statement.md) | Spécifie des informations sur une ressource qui peut être utilisée par un outil capable de lire ou d’écrire des fichiers de définition de ressource.                                                                                                                                                                                                                                                                                                                                                                           |
| [**TYPE**](class-statement.md)                     | Définit la classe de la boîte de dialogue.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**EXSTYLE**](exstyle-statement.md)                 | Définit le style de fenêtre étendue de la boîte de dialogue.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**SON**](font-statement.md)                       | Définit la police avec laquelle le système dessinera du texte pour la boîte de dialogue.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**SOUS**](language-statement.md)               | Définit la langue de toutes les ressources jusqu’à l’instruction de [**langue**](language-statement.md) suivante ou jusqu’à la fin du fichier. Lorsque l’instruction **Language** apparaît avant le début du corps d’une définition de ressource [**Accelerators**](accelerators-resource.md), [**Dialog**](dialog-resource.md), [**menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)ou [**STRINGTABLE**](stringtable-resource.md) , la langue spécifiée s’applique uniquement à cette ressource. |
| [**MENUS**](menu-statement.md)                       | Définit le menu de la boîte de dialogue.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**MENUITEM**](menuitem-statement.md)               | Définit un élément de menu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**STYLE**](style-statement.md)                     | Définit le style de fenêtre pour la boîte de dialogue.                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**Version**](version-statement.md)                 | Spécifie les informations de version d’une ressource qui peuvent être utilisées par un outil capable de lire ou d’écrire des fichiers de définition de ressource.                                                                                                                                                                                                                                                                                                                                                                     |



 

 

 