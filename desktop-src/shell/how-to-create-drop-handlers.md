---
description: Comment implémenter et inscrire un gestionnaire de suppression.
title: Comment créer des gestionnaires de suppression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b4349ba36a12670458a453b0622475d59d755
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412497"
---
# <a name="how-to-create-drop-handlers"></a>Comment créer des gestionnaires de suppression

Par défaut, les fichiers ne sont pas des cibles de dépôt. Vous pouvez transformer les membres d’un [type de fichier](fa-file-types.md) en cibles de dépôt en implémentant et en inscrivant un *Gestionnaire de suppression*.

Si un gestionnaire de suppression est inscrit pour un type de fichier, il est appelé chaque fois qu’un objet est glissé ou supprimé sur un membre du type de fichier. L’interpréteur de commandes gère l’opération en appelant les méthodes appropriées sur l’interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) du gestionnaire.

Les procédures générales d’implémentation et d’inscription d’un gestionnaire d’extensions de Shell sont décrites dans [création de gestionnaires d’extensions de Shell](handlers.md). Ce document se concentre sur les aspects de l’implémentation qui sont spécifiques aux gestionnaires de suppression.

## <a name="instructions"></a>Instructions

### <a name="step-1-implementing-drop-handlers"></a>Étape 1 : implémentation des gestionnaires de suppression

Comme tous les gestionnaires d’extensions de Shell, les gestionnaires de suppression sont des objets COM (Component Object Model) in-process implémentés en tant que dll. Elles exportent deux interfaces en plus de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) et [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).

L’interpréteur de commandes Initialise le gestionnaire via son interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) . Elle utilise cette interface pour demander l’identificateur de classe du gestionnaire (CLSID) et lui fournit le nom du fichier. Pour obtenir une description générale de l’implémentation des gestionnaires d’extensions de Shell, y compris l’interface **IPersistFile** , consultez [création de gestionnaires d’extension de Shell](handlers.md).

Une fois le gestionnaire Drop initialisé, l’interpréteur de commandes appelle la méthode appropriée sur l’interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) du gestionnaire.

### <a name="step-2-registering-drop-handlers"></a>Étape 2 : inscription des gestionnaires de suppression

Les gestionnaires de suppression sont inscrits sous la sous-clé de ce type de fichier.

```
HKEY_CLASSES_ROOT
   ProgID
      shellex
         DropHandler
```

Créez une sous-clé de **DropHandler** nommée pour le gestionnaire et définissez la valeur par défaut de la sous-clé sur la forme de chaîne du GUID CLSID du gestionnaire. Pour obtenir une présentation générale de l’inscription des gestionnaires d’extensions de Shell, consultez [création de gestionnaires d’extensions de Shell](handlers.md).

L’exemple suivant illustre les entrées de Registre qui activent un gestionnaire Drop pour un exemple de type de fichier. MYP.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         DropHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de gestionnaires d’extensions d’environnement](handlers.md)
</dt> <dt>

[**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)
</dt> <dt>

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> </dl>

 

 
