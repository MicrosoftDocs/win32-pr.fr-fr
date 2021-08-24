---
description: par défaut, à partir de Windows les éléments du panneau de configuration Vista ne sont pas affichés lorsque Windows est exécuté en mode sans échec.
title: accès au panneau de configuration en Mode Coffre
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f37bcb0f-9417-4cc4-a57d-4f67a9ccda19
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 777a44c7fe30b0481096a1c5d62c98410277a3bc76169925aff4ae5e59e549d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710789"
---
# <a name="accessing-the-control-panel-in-safe-mode"></a>accès au panneau de configuration en Mode Coffre

par défaut, à partir de Windows les éléments du panneau de configuration Vista ne sont pas affichés lorsque Windows est exécuté en mode sans échec. Pour permettre l’affichage d’un nouvel élément du panneau de configuration en mode sans échec, les valeurs de Registre appropriées au type d’élément peuvent être définies. Les valeurs sont interprétées comme suit :



| Valeur | Signification                                                            |
|-------|--------------------------------------------------------------------|
| 1     | L’élément doit apparaître en mode sans échec minimal.                  |
| 2     | L’élément doit apparaître en mode sans échec uniquement si la mise en réseau est activée. |
| 3     | L’élément doit toujours apparaître dans toute forme de mode sans échec.            |



 

Cet exemple montre les entrées requises pour un élément implémenté sous la forme d’un fichier .cpl ou .dll. Il spécifie que l’élément doit apparaître en mode sans échec avec mise en réseau.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.EnableInSafeMode
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 2
```

Cet exemple montre les entrées requises pour un élément implémenté sous la forme d’un fichier de .exe. Il spécifie que l’élément doit apparaître dans n’importe quelle forme de mode sans échec.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         System.ControlPanel.EnableInSafeMode = [REG_DWORD] 3
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Éléments du panneau de configuration](control-panel-applications.md)
</dt> <dt>

[Conseils sur l’expérience utilisateur](user-experience-guidelines.md)
</dt> <dt>

[Inscription des éléments du panneau de configuration](registering-control-panel-items.md)
</dt> <dt>

[Utilisation de CPLApplet](using-cplapplet.md)
</dt> <dt>

[Traitement des messages du panneau de configuration](message-processing.md)
</dt> <dt>

[Exécution des éléments du panneau de configuration](executing-control-panel-items.md)
</dt> <dt>

[Extension des éléments du panneau de configuration système](extending-system-control-panel-items.md)
</dt> <dt>

[Affectation des catégories du panneau de configuration](assigning-control-panel-categories.md)
</dt> <dt>

[Création de liens de tâches pouvant faire l’objet d’une recherche pour un élément du panneau de configuration](creating-searchable-task-links.md)
</dt> </dl>

 

 



