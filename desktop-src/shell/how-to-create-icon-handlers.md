---
description: Décrit comment créer un gestionnaire pour les affectations d’icônes personnalisées.
ms.assetid: 23ed3a21-cf62-4440-b983-fae23aa56890
title: Comment créer des gestionnaires d’icône
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c620b6f6a4c05f8996a26c8365e4f4201ee0b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973171"
---
# <a name="how-to-create-icon-handlers"></a>Comment créer des gestionnaires d’icône

Un [type de fichier](fa-file-types.md) est souvent associé à une icône personnalisée, afin de rendre ses membres facilement identifiables dans l’Explorateur Windows. La méthode la plus simple pour assigner une icône personnalisée à un type de fichier consiste à enregistrer le fichier de l’icône. Toutefois, une icône inscrite de cette façon sera la même pour tous les membres du type de fichier. Vous pouvez disposer d’une plus grande flexibilité pour assigner des icônes aux membres du type de fichier en implémentant un *Gestionnaire d’icône*.

Un gestionnaire d’icônes est un type de gestionnaire d’extensions de Shell qui vous permet d’affecter dynamiquement des icônes aux membres d’un type de fichier. Chaque fois qu’un fichier du type est affiché, l’interpréteur de commandes interroge le gestionnaire pour obtenir l’icône appropriée. Par exemple, un gestionnaire d’icône peut assigner des icônes différentes à différents membres du type de fichier, ou faire varier l’icône en fonction de l’état actuel du fichier.

Les procédures générales d’implémentation et d’inscription d’un gestionnaire d’extensions de Shell sont décrites dans [création de gestionnaires d’extensions de Shell](handlers.md). Ce document se concentre sur les aspects de l’implémentation qui sont spécifiques aux gestionnaires d’icônes.

-   [Implémentation de gestionnaires d’icône](#step-1-implementing-icon-handlers)
-   [Implémentation de l’interface IExtractIcon](#step-2-implementing-the-iextracticon-interface)
-   [Inscription des gestionnaires d’icône](#step-3-registering-icon-handlers)
-   [Rubriques connexes](#related-topics)

## <a name="instructions"></a>Instructions

### <a name="step-1-implementing-icon-handlers"></a>Étape 1 : implémentation des gestionnaires d’icône

Comme tous les gestionnaires d’extensions de Shell, les gestionnaires d’icônes sont des objets COM (Component Object Model) in-process implémentés en tant que dll. Ils doivent exporter deux interfaces en plus de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) et [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona).

L’interpréteur de commandes Initialise le gestionnaire via son interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) . Elle utilise cette interface pour demander l’identificateur de classe du gestionnaire (CLSID) et lui fournit le nom du fichier. Le reste de l’opération a lieu par le biais de l’interface [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) . Pour obtenir une description générale de l’implémentation des gestionnaires d’extensions de Shell, y compris l’interface **IPersistFile** , consultez [création de gestionnaires d’extension de Shell](handlers.md). Le reste de ce document explique comment implémenter l’interface **IExtractIcon** .

### <a name="step-2-implementing-the-iextracticon-interface"></a>Étape 2 : implémentation de l’interface IExtractIcon

Une fois l’interface initialisée, l’interpréteur de commandes utilise l’interface [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) du gestionnaire pour demander l’icône appropriée. L’interface possède deux méthodes : [**IExtractIcon :: GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation) et [**IExtractIcon :: Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract).

Les icônes sont identifiées par leur emplacement dans le système de fichiers. La méthode [**IExtractIcon :: GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation) est appelée pour demander ces informations. Définissez le paramètre *szIconFile* sur le nom de fichier. Si le fichier contient plusieurs icônes, définissez *piIndex* sur l’index de l’icône. Assignez les valeurs appropriées aux deux variables de l’indicateur. Si vous ne souhaitez pas spécifier de nom de fichier ou si vous ne souhaitez pas que le shell extraie l’icône, définissez l’indicateur **Gil \_ NOTFILENAME** dans le paramètre *pwFlags* . Vous n’avez pas besoin d’affecter une valeur à *szIconFile*, mais le gestionnaire doit fournir des handles d’icône lorsque l’interpréteur de commandes appelle [**IExtractIcon :: Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract).

Si vous retournez un nom de fichier, le shell tente normalement de charger l’icône à partir de son cache. Pour empêcher le chargement d’une icône mise en cache, définissez l’indicateur **Gil \_ DONTCACHE** dans le paramètre *pwFlags* . Si une icône mise en cache n’est pas chargée, l’interpréteur de commandes appelle [**IExtractIcon :: Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract) pour demander le handle d’icône.

Si un fichier et un index ont été spécifiés par [**IExtractIcon :: GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation), ils sont passés à [**IExtractIcon :: Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract) dans les paramètres *pszFile* et *nIconIndex* , respectivement. Si un nom de fichier est fourni, votre gestionnaire peut retourner \_ la valeur S false pour que le shell extraie l’icône. Dans le cas contraire, votre gestionnaire doit extraire ou créer des icônes de grande taille et de petite taille, et assigner leurs descripteurs HICON aux paramètres *phiconLarge* et *phiconSmall* . L’interpréteur de commandes ajoute les icônes à son cache pour accélérer les appels suivants au gestionnaire.

### <a name="step-3-registering-icon-handlers"></a>Étape 3 : enregistrement des gestionnaires d’icône

Lorsque vous [Enregistrez de manière statique une icône](icon.md) pour un [type de fichier](fa-file-types.md), vous créez une sous-clé **DefaultIcon** sous le ProgID pour le type de fichier. Sa valeur par défaut est le fichier qui contient l’icône. Pour inscrire un gestionnaire d’icône, vous devez toujours disposer de la sous-clé **DefaultIcon** , mais sa valeur par défaut doit être définie sur « %1 ». Ajoutez une sous-clé **IconHandler** à la sous-clé **shellex** de la sous-clé ProgID et définissez sa valeur par défaut sur la forme de chaîne du GUID CLSID du gestionnaire. Pour obtenir une présentation générale de l’inscription des gestionnaires d’extensions de Shell, consultez [création de gestionnaires d’extensions de Shell](handlers.md).

L’exemple suivant modifie l’entrée de Registre à partir de [Personnalisation des icônes](icon.md) afin que le type de fichier. MYP utilise désormais un gestionnaire de menu contextuel au lieu d’une icône définie statiquement.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      DefaultIcon
         (Default) = %1
      Shellex
         IconHandler
            (Default) = {The handler's CLSID GUID}
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de gestionnaires d’extensions d’environnement](handlers.md)
</dt> <dt>

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)
</dt> </dl>

 

 
