---
description: Quand un utilisateur clique avec le bouton droit sur un objet Shell, le menu contextuel qui s’affiche normalement comprend un élément Propriétés.
title: Gestionnaires de feuille de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 72233ab5-212d-498c-8df1-1a96c8eda892
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 40ccb8d1cee0fffb993aef417b979816597cf707
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866150"
---
# <a name="property-sheet-handlers"></a>Gestionnaires de feuille de propriétés

Quand un utilisateur clique avec le bouton droit sur un objet Shell, le menu contextuel qui s’affiche normalement comprend un élément **Propriétés** . La sélection de cet élément lance une feuille de propriétés qui permet à l’utilisateur d’afficher et, dans certains cas, de modifier les propriétés de l’objet. Vous pouvez personnaliser cette feuille de propriétés en implémentant et en inscrivant un *Gestionnaire de feuille de propriétés*.

Les procédures générales d’implémentation et d’inscription d’un gestionnaire d’extensions de Shell sont décrites dans [création de gestionnaires d’extensions de Shell](handlers.md). Ce document se concentre sur les aspects de l’implémentation qui sont spécifiques aux gestionnaires de feuille de propriétés.

-   [Fonctionnement des gestionnaires de feuille de propriétés](#how-property-sheet-handlers-work)
-   [Inscription et implémentation d’un gestionnaire de feuille de propriétés pour un lecteur monté](#registering-and-implementing-a-property-sheet-handler-for-a-mounted-drive)
-   [Rubriques connexes](#related-topics)

## <a name="how-property-sheet-handlers-work"></a>Fonctionnement des gestionnaires de feuille de propriétés

L’illustration suivante montre la feuille de propriétés des propriétés d’un fichier texte Windows XP.

![feuille de propriétés](images/propsheethandler1.jpg)

Cette illustration montre la feuille de propriétés des propriétés par défaut qui s’affiche pour tous les fichiers. Pour de nombreuses feuilles de propriétés de ce type, vous pouvez ajouter une ou plusieurs pages à la feuille de propriétés en implémentant et en inscrivant un gestionnaire de feuille de propriétés.

Les gestionnaires de feuille de propriétés sont les plus couramment inscrits pour un [type de fichier](fa-file-types.md). Chaque gestionnaire peut ajouter une page personnalisée à la feuille de propriétés de propriétés pour la classe. Ces pages permettent généralement aux utilisateurs d’accéder aux propriétés spécifiques à un type de fichier particulier. Un type de fichier composé de documents texte peut, par exemple, afficher une page qui répertorie le titre et l’auteur, ainsi qu’un résumé du document. Un cas particulier de ce type de gestionnaire de feuille de propriétés est utilisé pour ajouter une page à la feuille de propriétés de propriétés pour un lecteur monté.

L’autre utilisation pour les gestionnaires de feuille de propriétés consiste à remplacer des pages dans les feuilles de propriétés affichées par les applications du panneau de configuration. Un fabricant de souris, par exemple, peut utiliser un gestionnaire de feuille de propriétés pour remplacer la page **boutons** sur la feuille de propriétés propriétés de la **souris** du panneau de configuration par une page personnalisée pour les caractéristiques de sa souris.

Comme tous les gestionnaires d’extensions de Shell, les gestionnaires de feuille de propriétés sont des objets COM (Component Object Model) in-process implémentés en tant que dll. Ils doivent exporter deux interfaces en plus de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) et [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext).

L’interface [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) est utilisée par le Shell pour initialiser le gestionnaire. Lorsque l’interpréteur de commandes appelle [**IShellExtInit :: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), il passe un objet de données avec le nom de l’objet et le pointeur vers une liste d’identificateurs d’éléments (PIDL) du dossier qui contient le fichier. Le paramètre *hRegKey* n’est pas utilisé avec les gestionnaires de feuille de propriétés. La méthode **IShellExtInit :: Initialize** doit extraire le nom de fichier de l’objet de données et stocker le nom et le PIDL du dossier pour une utilisation ultérieure. Pour plus d’informations, consultez la section *Implementing IShellExtInit* de [Creating shell extension Handlers](handlers.md).

Le reste de l’opération s’effectue par le biais de l’interface [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) du gestionnaire. Si la feuille de propriétés est associée à un type de fichier, l’interpréteur de commandes appelle [**IShellPropSheetExt :: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) pour permettre au gestionnaire d’ajouter une page à la feuille de propriétés. Si la feuille de propriétés est associée à une application du panneau de configuration, l’interpréteur de commandes appelle [**IShellPropSheetExt :: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) pour permettre au gestionnaire de remplacer une page.

## <a name="registering-and-implementing-a-property-sheet-handler-for-a-mounted-drive"></a>Inscription et implémentation d’un gestionnaire de feuille de propriétés pour un lecteur monté

Chaque lecteur monté a une feuille de propriétés qui peut être affichée par l’utilisateur. L’illustration suivante montre une feuille de propriétés de propriétés pour un lecteur de CD-ROM.

![Propriétés de CD-ROM, feuille de propriétés](images/propsheethandler2.jpg)

Il existe un large éventail d’appareils qui peuvent être montés en tant que lecteurs. Étant donné que la feuille de propriétés par défaut, conçue pour les lecteurs de disque, peut ne pas suffire pour certains périphériques, un gestionnaire de feuilles de propriétés peut être implémenté pour ajouter une page spécifique à l’appareil monté. L’implémentation de base de ce type de gestionnaire de feuille de propriétés est identique à celle décrite dans [comment inscrire et implémenter un gestionnaire de feuille de propriétés pour un type de fichier](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md), à deux exceptions près.

-   L’objet de données passé à la méthode [**IShellExtInit :: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) du gestionnaire peut contenir le chemin d’accès au lecteur au format [CFSTR \_ MOUNTEDVOLUME](clipboard.md) au lieu du format [CF \_ HDROP](clipboard.md) . Le \_ format CF HDROP est utilisé lorsque l’appareil est monté sur une lettre de lecteur. Le \_ format CFSTR MOUNTEDVOLUME est utilisé avec les systèmes de fichiers NTFS lorsque l’appareil distant est monté dans un dossier plutôt que dans une lettre de lecteur.
-   Le GUID du gestionnaire est inscrit sous la clé de shellex PropertySheetHandlers du lecteur **\_ \_ racine HKEY classes** \\  \\  \\  .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment inscrire et implémenter un gestionnaire de feuille de propriétés pour un type de fichier](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)
</dt> <dt>

[Comment inscrire et implémenter un gestionnaire de feuille de propriétés pour une application du panneau de configuration](how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application.md)
</dt> </dl>

 

 
