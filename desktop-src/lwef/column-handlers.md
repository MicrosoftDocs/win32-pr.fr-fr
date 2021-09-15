---
title: Création de gestionnaires de colonnes
description: le mode détails dans le Windows Windows Explorer affiche normalement plusieurs colonnes standard.
ms.assetid: 805e0e13-d09e-40f8-955b-c585f388e07e
keywords:
- gestionnaires de colonnes
- inscrire, gestionnaires de colonnes
- GetColumnInfo
- GetItemData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 940796e75f29ba0fcfa025d9a56267e14bdff38f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518429"
---
# <a name="creating-column-handlers"></a>Création de gestionnaires de colonnes

\[cette fonctionnalité est prise en charge uniquement sous Windows XP ou version antérieure. \]

le mode détails dans le Windows Windows Explorer affiche normalement plusieurs colonnes standard. Chaque colonne répertorie des informations, telles que la taille ou le type de fichier, pour chaque fichier dans le dossier actif. En implémentant et en inscrivant un gestionnaire de colonnes, vous pouvez rendre les colonnes personnalisées disponibles pour l’affichage.

Les procédures générales d’implémentation et d’inscription d’un gestionnaire d’extensions de Shell sont décrites dans [création de gestionnaires d’extensions de Shell](/windows/desktop/shell/handlers). Ce document se concentre sur les aspects de l’implémentation qui sont spécifiques aux gestionnaires de colonnes.

Les rubriques suivantes sont présentées.

-   [Fonctionnement des gestionnaires de colonnes](#how-column-handlers-work)
-   [Inscription des gestionnaires de colonnes](#registering-column-handlers)
-   [Implémentation de gestionnaires de colonnes](#implementing-column-handlers)
    -   [La méthode Initialize](#the-initialize-method)
    -   [La méthode GetColumnInfo](#the-getcolumninfo-method)
    -   [Méthode GetItemData](#the-getitemdata-method)

## <a name="how-column-handlers-work"></a>Fonctionnement des gestionnaires de colonnes

l’illustration suivante montre l’explorateur de Windows en mode détails.

![capture d’écran de l’Explorateur Windows en mode Détails](images/columnproviderhandler1.jpg)

avec Windows 2000, le dossier peut également prendre en charge un certain nombre de colonnes qui, par défaut, ne sont pas affichées. L’utilisateur peut afficher des colonnes supplémentaires en cliquant avec le bouton droit sur l’un des en-têtes de colonne et en sélectionnant la commande **plus...** dans le menu. Une boîte de dialogue s’affiche, qui répertorie les colonnes disponibles pour le dossier et permet à l’utilisateur de sélectionner les colonnes à afficher. L’illustration suivante montre cette boîte de dialogue pour l’exemple précédent.

![capture d’écran de l’Explorateur Windows avec la boîte de dialogue Choisir les détails affichée](images/columnproviderhandler2.jpg)

En créant un gestionnaire de colonnes, vous pouvez créer des colonnes personnalisées et les ajouter à cette liste. Par exemple, une collection de fichiers qui contiennent de la musique peut utiliser un gestionnaire de colonnes pour afficher les colonnes qui répertorient l’artiste et la pièce contenues dans chaque fichier.

un gestionnaire de colonnes est un objet global qui est appelé chaque fois que Windows Explorer affiche le mode détails. Toutefois, les gestionnaires de colonnes sont généralement utilisés pour afficher des colonnes personnalisées uniquement pour les membres d’un [type de fichier](/windows/desktop/shell/fa-file-types)particulier. avant d’afficher le mode détails, Windows Explorer interroge tous les gestionnaires de colonne inscrits pour leurs caractéristiques de colonne. si l’utilisateur a sélectionné l’une des colonnes du gestionnaire, Windows Explorer interroge le gestionnaire pour obtenir les données associées. Lorsqu’un gestionnaire de colonnes reçoit une demande de données, il le fournit si le fichier est membre de son type pris en charge. Sinon, elle ignore la demande en renvoyant S \_ false.

## <a name="registering-column-handlers"></a>Inscription des gestionnaires de colonnes

Les gestionnaires de colonnes sont inscrits sous la sous-clé suivante.

```
HKEY_CLASSES_ROOT
   Folder
      shellex
         ColumnHandlers
```

Créez une sous-clé de **ColumnHandlers** nommée avec la forme de chaîne du GUID de l’identificateur de classe (CLSID) du gestionnaire. Pour obtenir une présentation générale de l’inscription des gestionnaires d’extensions de Shell, consultez [création de gestionnaires d’extensions de Shell](/windows/desktop/shell/handlers). L’exemple suivant montre comment enregistrer un gestionnaire de colonnes.

```
HKEY_CLASSES_ROOT
   Folder
      shellex
         ColumnHandlers
            {My Column Handler CLSID GUID}
```

## <a name="implementing-column-handlers"></a>Implémentation de gestionnaires de colonnes

Comme tous les gestionnaires d’extensions de Shell, les gestionnaires de colonnes sont des objets COM (Component Object Model) in-process implémentés en tant que dll. Ils exportent l’interface [**IColumnProvider**](/windows/desktop/api/shlobj/nn-shlobj-icolumnprovider) en plus de [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown).

Windows L’Explorateur appelle les trois méthodes exportées par [**IColumnProvider**](/windows/desktop/api/shlobj/nn-shlobj-icolumnprovider) pour demander les informations dont il a besoin pour afficher la colonne. la procédure utilisée par Windows Explorer est la suivante :

1.  Appelez [**IColumnProvider :: Initialize**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize) pour spécifier le dossier qui va être affiché.
2.  Appelez [**IColumnProvider :: GetColumnInfo**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo) pour récupérer l’identificateur et les caractéristiques de la colonne.
3.  Si la colonne a été sélectionnée par l’utilisateur, appelez [**IColumnProvider :: GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) pour chaque fichier du dossier afin de récupérer les données qui appartiennent à l’entrée de colonne du fichier.

### <a name="the-initialize-method"></a>La méthode Initialize

Windows L’Explorateur appelle [**IColumnProvider :: Initialize**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize) pour initialiser le gestionnaire de colonnes. La méthode a trois paramètres, mais seul *wszFolder* est actuellement utilisé. Elle est définie sur le dossier dont l’affichage Détails va être affiché. Stockez le nom du dossier pour une utilisation ultérieure et initialisez l’objet gestionnaire en fonction des besoins.

### <a name="the-getcolumninfo-method"></a>La méthode GetColumnInfo

Windows L’Explorateur appelle ensuite [**IColumnProvider :: GetColumnInfo**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo) pour demander l’identificateur et les caractéristiques de la colonne. Elle transmet un index pour la colonne dans le paramètre *dwIndex* . Cet index est une valeur arbitraire utilisée pour énumérer les colonnes. Windows L’Explorateur passe également un pointeur vers une structure [**SHCOLUMNINFO**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) . Cette structure est utilisée pour retourner l’identificateur et les caractéristiques de la colonne. **IColumnProvider :: GetColumnInfo** doit assigner des valeurs appropriées aux membres de la structure et retourner.

Les colonnes sont identifiées par leur ID de jeu de propriétés OLE (FMTID) et par un ID de propriété associé (PID). Le premier membre de la structure [**SHCOLUMNINFO**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) , **scid**, est un pointeur vers une structure [**SHCOLUMNID**](/windows/desktop/shell/objects) qui est utilisée pour identifier la colonne. Son membre **fmtid** contient le fmtid de la colonne, et son membre **PID** contient le PID de la colonne. Par exemple, une paire FMTID/PID standard qui est couramment utilisée pour identifier les colonnes est le PID de l’auteur de la propriété des informations de résumé définie.

Si possible, votre gestionnaire doit utiliser des FMTIDs et des PID existants pour identifier la colonne qu’il prend en charge. Si vous utilisez une structure [**SHCOLUMNID**](/windows/desktop/shell/objects) personnalisée, la colonne affiche des données uniquement pour les fichiers qui sont pris en charge par le gestionnaire. Si le dossier contient d’autres fichiers, leurs entrées sont vides. Si un dossier contient des fichiers issus de plusieurs types de fichiers, l’utilisation de valeurs FMTID/PID standard peut permettre de fusionner les données de différents types dans la même colonne.

Définissez le membre **VT** sur le type [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) des données que vous souhaitez afficher dans la colonne. Le type le plus couramment utilisé est VT \_ LPSTR, car la plupart des colonnes affichent leurs données sous forme de chaînes de caractères. Les membres restants de la structure [**SHCOLUMNINFO**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) sont utilisés pour définir les caractéristiques de la colonne. Affectez les valeurs appropriées.

### <a name="the-getitemdata-method"></a>Méthode GetItemData

si la colonne du gestionnaire de colonnes a été sélectionnée, Windows Explorer appelle [**IColumnProvider :: GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) pour chaque fichier du dossier à afficher. Le paramètre *pscid* est un pointeur vers une structure [**SHCOLUMNID**](/windows/desktop/shell/objects) qui identifie la colonne. Le paramètre *PSCD* pointe vers une structure [**SHCOLUMNDATA**](/windows/desktop/api/shlobj/ns-shlobj-shcolumndata) qui identifie le fichier particulier.

Le paramètre *pvarData* retourne les données qui doivent s’afficher dans la colonne du gestionnaire pour le fichier spécifié par *PSCD*. Si ce fichier est pris en charge par votre gestionnaire de colonnes, affectez sa valeur de données à *pvarData* et renvoyez \_ OK. Si le fichier n’est pas pris en charge par votre gestionnaire de colonnes, retourne \_ la valeur false sans assigner de valeur à *pvarData*.

De nombreux dossiers contiennent un certain nombre de fichiers qui ne sont pas pris en charge par un gestionnaire de colonnes particulier. Pour améliorer l’efficacité, [**IColumnProvider :: GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) doit d’abord vérifier le membre **pwszExt** de la structure vers laquelle pointe *PSCD*. Ce membre contient l’extension de nom de fichier. Si l’extension indique que le fichier n’est pas membre d’un type de fichier pris en charge par votre gestionnaire, évitez tout traitement inutile en renvoyant immédiatement S \_ false.

 

 