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
ms.openlocfilehash: 9b4cb426c245c73b6644a95e45d7e2577b4f85f6ed7a28980894183854c1b26e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942989"
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



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Élément du panneau de configuration</th>
<th><em>name</em></th>
<th>Remarques</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Affichage</td>
<td>Bureau</td>
<td>Prend également en charge le remplacement de la page du <strong>Bureau</strong> .
<blockquote>
[!Note]<br />
cela n’est plus pris en charge sous Windows Vista.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>affichage Paramètres avancé</td>
<td>Appareil</td>
<td>Propriétés avancées spécifiques au non-hardisme.
<blockquote>
[!Note]<br />
cela n’est plus pris en charge sous Windows Vista.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>affichage Paramètres avancé</td>
<td>Affichage</td>
<td>Propriétés avancées spécifiques au matériel.
<blockquote>
[!Note]<br />
cela n’est plus pris en charge sous Windows Vista.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Options Internet</td>
<td>Internet</td>
<td>Le nombre maximal de pages d’extension est 18.</td>
</tr>
<tr class="odd">
<td>Clavier</td>
<td>Clavier</td>
<td>Le nombre maximal de pages d’extension est de 30.</td>
</tr>
<tr class="even">
<td>Souris</td>
<td>Souris</td>
<td>Prend également en charge le remplacement des pages standard. Le nombre maximal de pages d’extension est de 8.</td>
</tr>
<tr class="odd">
<td>Options d’alimentation</td>
<td>Alimentation</td>
<td>Le nombre maximal de pages, y compris les pages standard, est 18.</td>
</tr>
<tr class="even">
<td>Système</td>
<td>Système</td>
<td>Le nombre maximal de pages d’extension est de 8.
<blockquote>
[!Note]<br />
cela n’est plus pris en charge sous Windows Vista.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

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

 

 




