---
description: Extension du presse-papiers avec des gestionnaires de format de données personnalisés.
title: Comment créer des gestionnaires de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a3761b4dc8ce3e7d50d967d2267971537d3609e7a7cf76785623734558adac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715049"
---
# <a name="how-to-create-data-handlers"></a>Comment créer des gestionnaires de données

Lorsqu’un fichier est copié dans le presse-papiers ou glissé et déposé, le shell crée un objet de données qui prend en charge un large éventail de [formats de presse-papiers](dragdrop.md)standard. Pour les fichiers qui sont d’un type de fichier spécifique, vous pouvez étendre les formats de presse-papiers disponibles en implémentant et en inscrivant un *Gestionnaire de données*. Lorsqu’un fichier du type de fichier est transféré, l’interpréteur de commandes délègue les appels à l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) de l’objet de données au gestionnaire de données si l’un des formats personnalisés est utilisé.

Les procédures générales d’implémentation et d’inscription d’un gestionnaire d’extensions de Shell sont décrites dans [création de gestionnaires d’extensions de Shell](handlers.md). Ce document se concentre sur les aspects de l’implémentation qui sont spécifiques aux gestionnaires de données.

-   [Implémentation de gestionnaires de données](#step-1-implementing-data-handlers)
-   [Inscription des gestionnaires de données](#step-2-registering-data-handlers)
-   [Rubriques connexes](#related-topics)

## <a name="instructions"></a>Instructions

### <a name="step-1-implementing-data-handlers"></a>Étape 1 : implémentation des gestionnaires de données

Comme tous les gestionnaires d’extensions de Shell, les gestionnaires de données sont des objets COM (Component Object Model) in-process implémentés en tant que dll. Elles exportent deux interfaces en plus de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) et [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject).

L’interpréteur de commandes Initialise le gestionnaire via son interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) . Elle utilise cette interface pour demander l’identificateur de classe du gestionnaire (CLSID) et lui fournit le nom du fichier. Pour obtenir une description générale de l’implémentation des gestionnaires d’extensions de Shell, y compris l’interface **IPersistFile** , consultez [création de gestionnaires d’extension de Shell](handlers.md).

Une fois le gestionnaire de données initialisé, l’interpréteur de commandes délègue les appels de l’objet de données à l’interface [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) du gestionnaire si l’un des formats personnalisés est utilisé.

### <a name="step-2-registering-data-handlers"></a>Étape 2 : inscription des gestionnaires de données

Les gestionnaires de données sont enregistrés sous la sous-clé *ProgID* du type de fichier comme indiqué ici : **HKEY \_ classes \_ root** \\ *ProgID* \\ **shellex** \\ **DataHandler**

Créez une sous-clé nommée pour le gestionnaire sous **DataHandler** et définissez la valeur par défaut de la sous-clé de ce gestionnaire sur la forme de chaîne du GUID CLSID du gestionnaire. Pour obtenir une présentation générale de l’inscription des gestionnaires d’extensions de Shell, consultez [création de gestionnaires d’extensions de Shell](handlers.md).

L’exemple suivant illustre les entrées de Registre qui activent un gestionnaire de données pour un exemple de type de fichier. MYP.

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
      Shellex
         DataHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de gestionnaires d’extensions d’environnement](handlers.md)
</dt> <dt>

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> </dl>

 

 
