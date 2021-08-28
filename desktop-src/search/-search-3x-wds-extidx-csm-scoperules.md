---
description: le gestionnaire de portée d’analyse (CSM) vous permet de définir des règles d’étendue qui incluent ou excluent des url de la portée de l’analyse de recherche Windows.
ms.assetid: 132a55f9-680d-438e-b983-f5ce4cf66a41
title: Gestion des règles d’étendue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134e4241e9dcd66e468935ae56a4029a51a96c37
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880221"
---
# <a name="managing-scope-rules"></a>Gestion des règles d’étendue

le gestionnaire de portée d’analyse (CSM) vous permet de définir des règles d’étendue qui incluent ou excluent des url de la portée de l’analyse de recherche Windows.

CSM vous permet d’effectuer les opérations suivantes :

-   Ajouter de nouvelles règles d’étendue à l’ensemble de règles de travail
-   Supprimer les règles d’étendue existantes
-   Énumérer les règles d’étendue par défaut
-   Déterminer si une URL particulière est incluse ou exclue de l’étendue de l’analyse ou si elle a une règle d’étendue parente ou enfant

 

Cette rubrique traite des sujets suivants :

-   [À propos des règles d’étendue](#about-scope-rules)
-   [Avant de commencer](#before-you-begin)
-   [Ajout de règles d’étendue](#adding-scope-rules)
    -   [Remarques sur les règles utilisateur](#notes-on-user-rules)
-   [Suppression des règles d’étendue](#removing-scope-rules)
-   [Rétablissement des règles par défaut](#reverting-to-default-rules)
-   [Énumération des règles d’étendue](#enumerating-scope-rules)
-   [Règles d’étendue de suivi](#tracing-scope-rules)
-   [Rubriques connexes](#related-topics)

## <a name="about-scope-rules"></a>À propos des règles d’étendue

Une règle d’étendue est une règle qui inclut ou exclut de l’analyse et de l’indexation des URL d’une racine de recherche. Les règles d’inclusion obligent l’indexeur à inclure cette URL dans l’étendue Scrawl, et les règles d’exclusion provoquent l’exclusion de l’indexeur de cette URL (et de ses enfants) de la portée de l’analyse.

Par exemple, supposons que vous avez installé une nouvelle application dont les fichiers de données se trouvent dans le dossier WorkteamA \\ ProjectFiles sur un ordinateur local. Supposons que vous souhaitiez que tout le contenu du dossier ProjectFiles soit indexé, à l’exception des éléments dans les prototypes de sous-dossier. Dans ce cas, vous avez besoin d’une règle d’inclusion pour myPH:///C : \\ WorkteamA \\ ProjectFiles \\ et d’une règle d’exclusion pour myph:///C : \\ WorkteamA \\ ProjectFiles \\ prototypes \\ .

Il existe trois types de règles, avec l’ordre de priorité suivant :

1.  Les règles de stratégie de groupe sont définies par les administrateurs et peuvent remplacer toutes les autres règles.
2.  les règles utilisateur sont définies par les utilisateurs qui modifient l’étendue dans l’interface utilisateur des options de recherche Windows. Les utilisateurs ou d’autres applications peuvent supprimer toutes les règles utilisateur et rétablir les règles par défaut.
3.  Les règles par défaut sont généralement définies par une application pour définir une étendue par défaut. Par exemple, les règles par défaut peuvent être définies lors de l’ajout d’un nouveau gestionnaire de protocole ou d’un conteneur au système.

Ensemble, ces types de règles comprennent l’ensemble de règles de *travail* à partir duquel le gestionnaire de portée d’analyse (CSM) génère la liste complète des URL à analyser. Alors que les règles par défaut peuvent être remplacées par les règles de stratégie de groupe et par les règles de l’utilisateur, elles sont conservées dans leur propre ensemble de règles par défaut, que vous pouvez restaurer à tout moment. L’indexeur analyse les URL de l’ensemble de règles de travail et ajoute des éléments, des propriétés et du contenu au catalogue.

> [!Note]  
> Les utilisateurs ayant accès au panneau de configuration peuvent modifier les règles via cette interface. Par conséquent, les applications qui offrent la gestion des étendues doivent toujours obtenir les règles directement à partir du CSM en utilisant les méthodes d’énumération au lieu de s’appuyer sur une copie enregistrée des règles utilisateur.

 

Les règles d’exclusion peuvent définir des URL de modèle avec le caractère générique « \* », par exemple : file:///C : \\ ProjectA \\ \* \\ . Une règle d’exclusion utilisant ce modèle empêche l’indexeur d’analyser les dossiers situés sous le répertoire ProjectA. Pour obtenir un exemple plus complexe, supposez qu’il existe une règle d’inclusion pour file:///C : \\ ProjectA \\ et une règle de modèle d’exclusion pour file:///C : \\ ProjectA \\ \* \\ Data \\ \* . Dans ce cas, l’indexeur analyse les éléments dans :

-   C : \\ ProjectA\\
-   C : \\ projeta \\ **version1** \\ testfiles\\
-   C : \\ ProjectA \\ **version1 \\**- \\ données temporaires\\

Mais l’indexeur n’analyse pas les éléments dans :

-   C : \\ ProjectA \\ **version1** \\ données\\

 

## <a name="before-you-begin"></a>Avant de commencer

Avant d’utiliser l’une des interfaces du gestionnaire d’étendues d’analyse, vous devez effectuer les étapes préalables suivantes :

1.  Créez l’objet **CSearchManager** et obtenez son interface **ISearchManager** .
2.  Appelez **ISearchManager :: getCatalog,** pour « SystemIndex » pour obtenir une instance de l’interface **ISearchCatalogManager** .
3.  Appelez **ISearchCatalogManager :: GetCrawlScopeManager** pour obtenir une instance de l’interface **ISearchCrawlScopeManager** .

Après avoir apporté des modifications au gestionnaire de l’étendue de l’analyse, vous devez appeler la méthode [**ISearchCrawlScopeManager ::**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall) saproduction. Cette méthode ne prend pas de paramètres et retourne S \_ OK en cas de réussite.

 

## <a name="adding-scope-rules"></a>Ajout de règles d’étendue

Les règles de travail définies pour le CSM incluent les règles utilisateur et par défaut, ainsi que toutes les règles imposées par la stratégie de groupe. Les règles utilisateur sont configurées par les utilisateurs dans une interface utilisateur, et les règles par défaut peuvent être définies par l’un des éléments suivants :

-   Stratégies de groupe implémentées par un administrateur système (celles-ci n’utilisent pas l’interface [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) .)
-   installation ou mise à jour d’une application telle que Windows Search ou un gestionnaire de protocole
-   Une application d’installation pour l’ajout d’une nouvelle banque de données ou d’un nouveau conteneur

Le [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) fournit deux méthodes pour ajouter de nouvelles règles d’étendue, comme décrit dans le tableau suivant. Les chemins d’accès pour les règles d’inclusion du système de fichiers doivent se terminer par une barre oblique inverse « \\ » (par exemple, file:///C : \\ Files \\ ), et les chemins d’accès des règles d’exclusion doivent se terminer par un astérisque (par exemple, file:///c : \\ Files \\ \* ). Seules les règles d’exclusion peuvent contenir des URL de modèle. En outre, nous vous recommandons d’inclure les identificateurs de sécurité (SID) des utilisateurs dans les chemins d’accès, pour une meilleure sécurité. Les chemins d’accès par utilisateur sont plus sécurisés, car les requêtes s’exécutent dans un processus par utilisateur, ce qui garantit qu’un utilisateur ne peut pas voir les éléments indexés à partir de la boîte de réception d’un autre utilisateur, par exemple.

Le tableau suivant décrit les méthodes de l’interface ISearchCrawlScopeManager utilisée pour ajouter de nouvelles règles d’étendue.



| Méthode                                                                              | Description                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddUserScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-adduserscoperule)       | Ajoute une règle pour une URL, telle que spécifiée par l’utilisateur. Ces règles remplacent les règles par défaut. Utilisez cette méthode si vous avez implémenté une interface utilisateur qui permet aux utilisateurs de gérer leurs propres règles d’étendue et URL.                         |
| [**AddDefaultScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-adddefaultscoperule) | Ajoute une règle pour une URL, telle que spécifiée par une autre application, comme un gestionnaire de protocole. Utilisez cette méthode lorsque vous avez implémenté un nouveau gestionnaire de protocole ou ajouté un nouveau magasin de données. Ces règles peuvent être remplacées par des règles utilisateur. |



 

Chaque méthode prend une URL vers un emplacement indexable et des indicateurs qui déterminent si l’URL doit être incluse ou exclue. Le paramètre *fFollowFlags* est réservé pour une utilisation ultérieure. Lorsque vous ajoutez une nouvelle règle d’étendue et que le gestionnaire de l’étendue de l’analyse détermine que la règle existe déjà (en fonction de l’URL ou du modèle fourni), l’ensemble de règles de travail est mis à jour. ainsi, (1) l’ancienne règle est remplacée par la nouvelle règle et (2) toutes les règles utilisateur qui contredisent celle-ci sont supprimées.

**Conseil :** La racine file://est incluse par défaut dans l’étendue de l’analyse, mais les fichiers programme ne sont pas indexés par défaut. Par conséquent, les applications avec des données enregistrées dans le répertoire Program Files doivent ajouter leur emplacement en tant que règle par défaut.

### <a name="notes-on-user-rules"></a>Remarques sur les règles utilisateur

Si une nouvelle règle d’utilisateur est identique à une règle par défaut existante, la nouvelle règle utilisateur remplace la règle par défaut dans l’ensemble de règles de travail. Si la nouvelle règle utilisateur est identique à une règle d’utilisateur existante, l’ancienne règle utilisateur est remplacée.

La définition de l’indicateur *fOverrideChildren* a les résultats suivants dans l’ensemble de règles de travail :

-   **True** entraîne la suppression de toutes les règles enfants de l’ensemble de règles de travail (règles d’utilisateur et règles par défaut).
-   La valeur FALSe entraîne l’ajout à nouveau des règles de travail à l’ensemble des règles par défaut qui sont des enfants de la nouvelle règle utilisateur. Si une règle enfant par défaut est une inclusion et que la nouvelle règle utilisateur est une exclusion, la règle par défaut est remplacée par une règle d’inclusion d’utilisateur.

 

## <a name="removing-scope-rules"></a>Suppression des règles d’étendue

Vous pouvez utiliser l’interface [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) pour supprimer une règle d’étendue de l’ensemble de règles de travail. Cette interface fournit les deux méthodes suivantes pour supprimer des règles d’étendue.



| Méthode                                                                                    | Description                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RemoveScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removescoperule)               | Supprime une règle utilisateur pour une URL spécifiée de l’ensemble de règles de travail. Si la règle utilisateur est un doublon de ou remplace une règle par défaut, la règle par défaut reste dans l’ensemble de règles de travail.                  |
| [**RemoveDefaultScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removedefaultscoperule) | Supprime une règle par défaut pour une URL spécifiée de l’ensemble de règles de travail et de l’ensemble de règles par défaut. Après avoir appelé cette méthode, vous ne pouvez pas revenir à cette règle par défaut à l’aide de RevertToDefaultScopes. |



 

Chaque méthode prend une URL et un indicateur qui spécifie si la règle à supprimer est une règle d’inclusion ou d’exclusion. Ces méthodes renvoient une erreur si une règle avec cette URL et l’indicateur d’inclusion/exclusion est introuvable.

**Conseil :** Si vous souhaitez supprimer entièrement une étendue de l’étendue de l’analyse, utilisez la méthode [**RemoveRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) , qui supprime la racine de recherche et toutes les règles d’étendue associées. Le fait de désinstaller, par exemple, est considéré comme une bonne pratique.

Il est également possible de supprimer tous les remplacements définis par l’utilisateur d’une racine de recherche et de rétablir la racine de recherche d’origine et les règles d’étendue par défaut. Pour plus d’informations, reportez-vous à la section suivante.

> [!Note]  
> sur Windows Vista, si les utilisateurs sont supprimés via les profils utilisateur dans le panneau de configuration, CSM supprime toutes les règles et toutes les racines qui incluent leur SID et supprime leurs éléments indexés du catalogue. sur Windows XP, vous devez supprimer manuellement les racines et les règles des utilisateurs.

 

 

## <a name="reverting-to-default-rules"></a>Rétablissement des règles par défaut

Le rétablissement des règles par défaut supprime toutes les règles utilisateur pour une URL ou la racine et restaure toutes les règles par défaut dans l’ensemble de règles de travail. Toutefois, elle ne supprime pas les règles définies par la stratégie de groupe. La méthode [**RevertToDefaultScopes**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-reverttodefaultscopes) n’accepte aucun paramètre et retourne un code d’erreur s’il ne peut pas rétablir les règles par défaut.

 

## <a name="enumerating-scope-rules"></a>Énumération des règles d’étendue

CSM énumère les règles de portée à l’aide d’une interface d’énumérateur de style COM standard, [**IEnumSearchScopeRules**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules) . Vous pouvez utiliser cette interface pour énumérer les règles d’étendue à plusieurs fins. Par exemple, vous souhaiterez peut-être afficher l’ensemble des règles de travail dans une interface utilisateur, ou déterminer si une règle ou l’enfant d’une règle figure déjà dans l’étendue de l’analyse.

 

## <a name="tracing-scope-rules"></a>Règles d’étendue de suivi

Le CSM vous permet également de déterminer si une URL spécifiée est incluse dans la portée de l’analyse et si elle a une règle d’étendue parente ou enfant. Vous pouvez également déterminer la raison pour laquelle une URL est incluse ou exclue de l’étendue de l’analyse. Ces méthodes ne sont pas destinées à être utilisées avec des URL de modèle.

Le tableau suivant décrit les méthodes de [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) utilisées pour l’ajout de nouvelles règles d’étendue.



| Méthode                                                                                      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetParentScopeVersionId**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-getparentscopeversionid) | Obtient l’ID de version de l’URL d’inclusion parente. Vous pouvez utiliser cette méthode pour voir si l’étendue du parent a changé depuis la dernière fois que vous l’avez vérifiée.<br/> Exemple : si une application de messagerie utilise des notifications gérées par le fournisseur, elle peut obtenir la version de l’étendue parente avant qu’elle ne se ferme et vérifier à nouveau la version lorsqu’elle s’ouvre. L’application peut ensuite déterminer si elle doit envoyer un nouvel ensemble de notifications à l’indexeur.<br/> |
| [**HasChildScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-haschildscoperule)             | Retourne la **valeur true** si l’URL spécifiée a une règle enfant (une règle s’appliquant à un enfant à n’importe quel niveau au sein de sa hiérarchie d’URL). <br/> Exemple : si l’URL est file:///C : \\ Folder \\ , cette méthode renvoie la **valeur true** si le CSM possède une règle d’étendue spécifique pour file:///C : \\ \\ subfolder \\ .<br/>                                                                                                                                              |
| [**HasParentScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-hasparentscoperule)           | Retourne la **valeur true** si l’URL spécifiée a une règle parente (une règle s’appliquant à un parent à n’importe quel niveau de la hiérarchie d’URL).<br/> Exemple : si l’URL est file:///C : \\ dossier sous \\ -dossier, cette méthode renvoie la **valeur true** si le CSM a une règle d’étendue spécifique pour file:///C : \\ Folder \\ .<br/>                                                                                                                                                   |
| [**IncludedInCrawlScope**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscope)       | Retourne la **valeur true** si l’URL spécifiée est incluse dans la portée de l’analyse.                                                                                                                                                                                                                                                                                                                                                                                  |
| [**IncludedInCrawlScopeEx**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex)   | Retourne une valeur de l’énumération [**\_ raison clusion**](/windows/win32/api/searchapi/ne-searchapi-clusion_reason) qui explique pourquoi l’URL est incluse dans la portée de l’analyse ou en est exclue, et récupère la valeur **true** si l’URL est incluse dans la portée de l’analyse. Cette méthode peut vous aider à identifier les conflits dans votre ensemble de règles de travail.                                                                                                                                       |



 

 

> [!Note]  
> Les méthodes [**IncludedInCrawlScope**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscope) et [**IncludedInCrawlScopeEx**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex) déterminent si l’URL sera analysée uniquement en fonction des règles du CSM. Il peut y avoir d’autres raisons pour lesquelles une URL n’est pas analysée, telle que le bit FANCI en cours de définition (autrement dit, un utilisateur n’a pas autorisé l’indexation rapide dans la boîte de dialogue des propriétés du dossier).

 

Si vous pensez qu’un chemin d’accès de fichier doit être exclu, mais qu’il est répertorié comme étant inclus, assurez-vous que les règles d’exclusion se terminent par « &lt; path &gt; \\ \* ». Si vous pensez qu’un fichier ou un chemin d’accès de fichier doit être inclus, mais que ce n’est pas le cas, veillez à vérifier le paramètre de bit FANCI du fichier ou du chemin d’accès. Pour ce faire, cliquez avec le bouton droit sur le chemin d’accès du fichier ou du fichier et sélectionnez **Propriétés**, puis vérifiez que la case à cocher **pour la recherche rapide, autoriser le service d’indexation à indexer ce dossier** est activée. Si le chemin d’accès au fichier ou au fichier n’est pas marqué pour l’indexation ici, il ne sera pas indexé même s’il se trouve dans une règle d’inclusion.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
</dt> <dt>

[**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2)
</dt> <dt>

[**ISearchScopeRule**](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)
</dt> <dt>

[**IEnumSearchScopeRules**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Gestion des racines de recherche](-search-3x-wds-extidx-csm-searchroots.md)
</dt> </dl>

 

 




