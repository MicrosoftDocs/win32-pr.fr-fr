---
title: Notification de l’index des modifications (fonctionnalités héritées de l’environnement Windows)
description: Avec Microsoft Windows Desktop Search (WDS) 2,6, les gestionnaires de protocoles pour un magasin de données donné peuvent indiquer à l’indexeur WDS quand les données de leur magasin ont changé.
ms.assetid: 700b1707-dd11-4a30-8f00-5c4aae1173ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6021cfe5cd7061a3d3255e56d08e665a6caedf03
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104200538"
---
# <a name="notifying-the-index-of-changes-legacy-windows-environment-features"></a>Notification de l’index des modifications (fonctionnalités héritées de l’environnement Windows)

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.

Avec Microsoft Windows Desktop Search (WDS) 2,6, les gestionnaires de protocoles pour un magasin de données donné peuvent indiquer à l’indexeur WDS quand les données de leur magasin ont changé. Cela améliore les performances en garantissant que l’indexeur n’analyse pas l’intégralité du magasin sur les index incrémentiels. À l’aide des API de notification, les gestionnaires de protocole peuvent notifier l’indexeur qu’un élément a été déplacé ou supprimé, et ils peuvent ajouter des étendues à la file d’attente d’analyse de l’indexeur WDS des URL nécessitant une indexation. La notification est utile pour les applications telles que la messagerie électronique, où le gestionnaire de protocole surveille le magasin et notifie l’indexeur que les éléments ont changé et nécessitent une indexation.

## <a name="isearchitemschangedsink"></a>ISearchItemsChangedSink

Les gestionnaires de protocole notifient l’indexeur des modifications par le biais de l’interface [**ISearchItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink) . Les informations sur les modifications de données doivent être collectées dans les \_ \_ types de modification d’élément de recherche et \_ \_ de type de recherche de type d' \_ énumération de modification, puis communiquées à l’indexeur via la méthode **OnItemsChanged** de l’interface **ISearchItemsChangedSink** .

Pour accéder à cette interface, un gestionnaire de protocole personnalisé doit d’abord instancier un objet [**ISearchManager**](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager) pour accéder à l’objet [**ISearchCatalogManager**](/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager) . À partir de là, il est possible d’instancier un objet [**ISearchItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink) et d’informer l’indexeur des modifications apportées aux données.

La méthode OnItemsChanged vous permet de collecter et de communiquer les modifications de données à votre magasin de données client pour initialiser l’indexation.



| Sens | Variable              | Description                                                              |
|-----------|-----------------------|--------------------------------------------------------------------------|
| Dans        | dwNumberofChanges     | Nombre total de modifications dans la notification.                             |
| Dans        | DataChangeEntries\[\] | Toutes les notifications de modification dans un tableau de structures de modification d’élément de recherche \_ \_ . |
| Sortie       | dwBatchId             | ID de lot qui sera renvoyé avec des erreurs.                       |
| Sortie       | hrCompletionCodes\[\] | Indique si chaque URL a été acceptée pour l’indexation.                    |



 

La \_ \_ structure de modification de l’élément de recherche identifie le type de modification qui s’est produit, ainsi que l’URL actuelle et l’URL précédente de l’élément, le cas échéant. La structure est définie comme suit :



| Nom de la propriété | Type de propriété                  | Description                                                                |
|---------------|--------------------------------|----------------------------------------------------------------------------|
| Modifier        | \_type \_ de recherche de \_ modification       | Type de modification notifié.                                 |
| URL           | LPWSTR                         | URL de l’objet qui a changé.                                   |
| OldURL        | LPWSTR                         | Si la notification est un déplacement, l’ancienne URL est fournie et doit être unique. |
| Priority      | \_priorité de notification de recherche \_ | Priorité de la modification.                                                |



 

Le \_ type \_ de recherche de l' \_ énumération des modifications est défini comme suit :



| Valeur Enum                           | Valeur   | Description                                                                                     |
|--------------------------------------|---------|-------------------------------------------------------------------------------------------------|
| modifier la recherche \_ \_ Ajouter                  | 0       | La notification est destinée à une URL supplémentaire.                                                      |
| recherche de modification de la recherche \_ \_               | 1       | La notification est destinée à la suppression d’une URL.                                                  |
| modification de \_ la modification de la recherche \_               | 2       | La notification est qu’une URL a été modifiée.                                               |
| RECHERCHE \_ modifier le déplacement du changement de \_ \_ nom         | 3       | La notification concerne le déplacement et le changement de nom d’un objet en une nouvelle URL.                          |
| Rechercher dans le répertoire de sémantique de \_ modification \_ \_ | 0x10000 | La notification est destinée à une URL de conteneur.                                                        |
| Rechercher \_ les \_ sémantiques de modification \_ superficielles   | 0x20000 | La notification concerne une URL de conteneur qui ne doit avoir que ses propriétés de conteneur indexées. |
| sécurité de modification de la \_ \_ sémantique de la recherche \_  | 0x40000 | La notification concerne une URL ou une URL de conteneur dont les propriétés de sécurité ont été modifiées.    |



 

L’énumération de la priorité de notification de recherche \_ \_ est définie comme suit :



| Valeur Enum               | Valeur | Description                                                                                                                                                                    |
|--------------------------|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rechercher \_ la \_ priorité normale | 0     | Seule une priorité normale doit être utilisée lors de l’indexation de l’URL. Ces notifications sont traitées avant l’indexation normale en arrière-plan normale des fichiers et des magasins d’un utilisateur. |



 

 

 
