---
description: Certains des éléments système trouvés dans le panneau de configuration sont extensibles. Pour installer une extension du panneau de configuration, inscrivez votre extension de Shell comme suit, où nom est le nom prédéfini de l’élément système (voir le tableau ci-dessous).
title: Extension des éléments du panneau de configuration système
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b8b18b71-c95f-4c71-8df4-fe9342ce0165
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8c5948ad99111dc87578dfa15c5278cf03d5918e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469746"
---
# <a name="extending-system-control-panel-items"></a>Extension des éléments du panneau de configuration système

Certains des éléments système trouvés dans le panneau de configuration sont extensibles. Pour installer une extension du panneau de configuration, inscrivez votre extension de Shell comme suit, où *nom* est le nom prédéfini de l’élément système (voir le tableau ci-dessous).

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Controls Folder
                  name
                     shellex
                        PropertySheetHandlers
```

Cela est similaire à la façon dont vous inscrivez une extension pour un objet Shell prédéfini. Étant donné que les seules extensions d’environnement prises en charge par les éléments du panneau de configuration sont des feuilles de propriétés, l’inscription doit se trouver sous la \\ sous-clé shellex **PropertySheetHandlers** .




| Élément du panneau de configuration | <em>name</em> | Remarques | 
|--------------------|---------------|---------|
| Affichage | Bureau | Prend également en charge le remplacement de la page du <strong>Bureau</strong> .<blockquote>[!Note]<br />cela n’est plus pris en charge sous Windows Vista.</blockquote><br /> | 
| affichage Paramètres avancé | Appareil | Propriétés avancées spécifiques au non-hardisme.<blockquote>[!Note]<br />cela n’est plus pris en charge sous Windows Vista.</blockquote><br /> | 
| affichage Paramètres avancé | Affichage | Propriétés avancées spécifiques au matériel.<blockquote>[!Note]<br />cela n’est plus pris en charge sous Windows Vista.</blockquote><br /> | 
| Options Internet | Internet | Le nombre maximal de pages d’extension est 18. | 
| Clavier | Clavier | Le nombre maximal de pages d’extension est de 30. | 
| Souris | Souris | Prend également en charge le remplacement des pages standard. Le nombre maximal de pages d’extension est de 8. | 
| Options d’alimentation | Alimentation électrique | Le nombre maximal de pages, y compris les pages standard, est 18. | 
| Système | Système | Le nombre maximal de pages d’extension est de 8.<blockquote>[!Note]<br />cela n’est plus pris en charge sous Windows Vista.</blockquote><br /> | 




 

l’élément **ajout/suppression de programmes** du panneau de configuration Windows XP n’est pas une feuille de propriétés et ne peut donc pas être étendu par les méthodes présentées ici. Au lieu de cela, son contenu est obtenu à partir des éditeurs d’applications. Pour plus d’informations sur l’ajout de contenu à l' **Ajout ou** à la suppression de programmes, consultez [**IAppPublisher**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher), [**IEnumPublishedApps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps)et [**IPublishedApp**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp).

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

[Affectation des catégories du panneau de configuration](assigning-control-panel-categories.md)
</dt> <dt>

[Création de liens de tâches pouvant faire l’objet d’une recherche pour un élément du panneau de configuration](creating-searchable-task-links.md)
</dt> <dt>

[accès au panneau de configuration en Mode Coffre sous Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




