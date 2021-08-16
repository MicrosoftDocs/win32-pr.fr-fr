---
description: La fonction RegOpenUserClassesRoot fournit une vue fusionnée pour les processus, tels que les services, qui concernent des clients autres que l’utilisateur interactif.
ms.assetid: 3815d487-2d58-4ba8-85d2-cae6a642a791
title: Vue fusionnée de HKEY_CLASSES_ROOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52b48be32ec524cdac42808d7f4efddfc78854b56133e647d6f5a9b06ae88bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885417"
---
# <a name="merged-view-of-hkey_classes_root"></a>Vue fusionnée de la \_ racine de la classe HKEY \_

La fonction [**RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot) fournit une vue fusionnée pour les processus, tels que les services, qui concernent des clients autres que l’utilisateur interactif. Dans ce cas, la **clé \_ \_ racine de classes HKEY** fournit une vue du Registre qui fusionne les informations de **la \_ \_ classe de \\ logiciels \\ HKEY local machine** avec les informations des **classes de logiciel de HKEY \_ Current \_ User \\ \\**.

Le système utilise les règles suivantes pour fusionner les informations des deux sources :

-   La vue fusionnée comprend toutes les sous-clés de la clé **HKEY \_ Current \_ User \\ Software \\ classes** .
-   La vue fusionnée comprend toutes les sous-clés immédiates de la clé **HKEY \_ local \_ machine \\ Software \\ classes** qui ne dupliquent pas les sous-clés des classes de logiciels de l' **\_ \_ utilisateur \\ \\ actuel HKEY**.
-   À la fin de cette rubrique se trouve une liste des sous-clés qui se trouvent dans les classes de logiciel **HKEY \_ local \_ machine \\ \\** et **HKEY \_ Current \_ User \\ \\**. Les sous-clés immédiates de ces clés de l’arborescence de l' **\_ \_ ordinateur local HKEY** sont incluses dans l’affichage fusionné uniquement si elles ne sont pas des doublons de sous-clés immédiates de l’arborescence de l' **\_ \_ utilisateur HKEY CURRENT** . La vue fusionnée n’inclut pas le contenu de la **\_ \_ machine locale HKEY** des sous-clés dupliquées.

Si une application est exécutée avec des droits d’administrateur et que le contrôle de compte d’utilisateur est désactivé, le runtime COM ignore la configuration COM par utilisateur et accède uniquement à la configuration COM par ordinateur. Les applications qui requièrent des droits d’administrateur doivent inscrire les objets COM dépendants lors de l’installation dans le magasin de configurations COM par ordinateur (**HKEY \_ local \_ machine \\ Software \\ classes**). Pour plus d’informations, consultez [AC : UAC : COM Per-User configuration](/previous-versions/bb756926(v=msdn.10)).

**Windows Server 2003 et Windows XP/2000 :** Les applications peuvent enregistrer des objets COM dépendants dans le magasin de configuration COM par ordinateur ou par utilisateur (**HKEY \_ local \_ machine \\ Software \\ classes** ou **HKEY \_ Current \_ User \\ Software \\ classes**).

L’exemple suivant montre un ensemble de sous-clés sous les clés **HKEY \_ local \_ machine** et **HKEY \_ Current \_ User** et la vue fusionnée résultante de la racine de la **\_ \_ classe HKEY**.

**HKEY \_ \_Classes de \\ logiciels \\ de l’ordinateur local**    **CLSID**       *2*       *4*          **InprocServer32**          **LocalServer32**       *7*

**HKEY \_ \_ \\ \\ Classes logicielles utilisateur actuelles**    **CLSID**       *1*       *4*          **LocalServer**       *6*       *10*          **LocalServer**

**HKEY \_ CLASSES \_ racine**    **CLSID**       *1*       *2*       *4*          **InprocServer32**          **LocalServer**          **LocalServer32**       *6*       *7*       *10*          **LocalServer**

Les sous-clés suivantes se trouvent à la fois dans les classes de logiciels de l' **\_ \_ ordinateur \\ \\ local HKEY** et les **classes de logiciels de HKEY \_ Current \_ User \\ \\**. À partir de l’arborescence de l' **\_ \_ ordinateur local HKEY** , les sous-clés immédiates de ces clés sont incluses dans l’affichage fusionné uniquement si elles ne sont pas des doublons de sous-clés immédiates de l’arborescence de l' **\_ \_ utilisateur HKEY actuelle** . La vue fusionnée n’inclut pas le contenu de la **\_ \_ machine locale HKEY** des sous-clés dupliquées.

**\***  
**\*\\shellex**  
**\*\\shellex \\ ContextMenuHandlers**  
**\*\\shellex \\ PropertySheetHandlers**  
**AppID**  
**Identificateur**  
**Catégories de composant**  
**Lecteur**  
**Lecteur \\ shellex**  
**Lecteur \\ shellex \\ ContextMenuHandlers**  
**Lecteur \\ shellex \\ PropertySheetHandlers**  
**FileType**  
**Folder**  
**Dossier \\ shellex**  
**Dossier \\ shellex \\ ColumnHandler**  
**Dossier \\ shellex \\ ContextMenuHandlers**  
**Dossier \\ shellex \\ ExtShellFolderViews**  
**Dossier \\ shellex \\ PropertySheetHandlers**  
**Composants du programme d’installation \\**  
**Fonctionnalités du programme d’installation \\**  
**Produits du programme d’installation \\**  
**Interface**  
**MIME**  
**\\Base de données MIME**  
**\\Jeu de caractères de base de données MIME \\**  
**\\Page de codes de la base de données MIME \\**  
**\\Type de contenu de base de données MIME \\**  
**Exportation**  


 

 
