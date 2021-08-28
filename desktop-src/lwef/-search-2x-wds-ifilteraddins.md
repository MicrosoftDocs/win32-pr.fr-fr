---
title: Développement de compléments IFilter
description: vous pouvez étendre Microsoft Windows Desktop Search (WDS) avec des compléments de filtre, des composants qui implémentent IFilterinterface, pour inclure de nouveaux types de fichiers.
ms.assetid: 71dd515d-a73e-4e0a-b0da-c8a6209d09fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497d4bffdb9564e0737bee3cd0b63fa8026633a2cc81aad37cb989423e460487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480893"
---
# <a name="developing-ifilter-add-ins"></a>Développement de compléments IFilter

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.

vous pouvez étendre Microsoft Windows Desktop Search (WDS) avec des compléments de filtre, des composants qui implémentent l’interface [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter), pour inclure de nouveaux types de fichiers. Les filtres sont chargés d’accéder aux données et de les analyser dans des fichiers, et de retourner des paires de propriétés et de valeurs ainsi que des blocs de texte pour l’indexation. Pendant le processus d’indexation, WDS appelle le filtre approprié avec l’URL de chaque fichier ou élément. Le filtre extrait d’abord les métadonnées qui correspondent aux propriétés marquées comme étant récupérables dans le schéma WDS, telles que le titre, la taille de fichier et la date de dernière modification. Ensuite, il divise le contenu de l’élément en segments de texte. WDS ajoute les propriétés et le texte retournés par le filtre au catalogue. WDS peut indexer n’importe quel type de fichier pour lequel il possède un filtre inscrit.

Dans certains cas, vous n’avez pas besoin d’écrire un nouveau filtre. WDS 2. x contient des filtres pour plus de 200 types d’éléments (y compris des éléments en texte brut tels que HTML, XML et des fichiers de code source) et utilise la même technologie [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)que SharePoint Services. Si vous avez déjà installé des filtres pour vos types de fichiers, WDS peut utiliser ces filtres existants pour indexer ces données. En outre, WDS comprend un filtre général pour les types de fichiers qui sont en texte clair. si vous avez un type de fichier qui peut être traité par un filtre de SharePoint Services existant ou le filtre de texte en clair, vous pouvez ajouter l’extension de nom de fichier et le GUID de filtre au registre pour que WDS puisse les localiser et les utiliser (pour plus d’informations, consultez [pour inscrire un complément de filtre](#to-register-a-filter-add-in) ).

Toutefois, si vous disposez d’un format de fichier ou de données propriétaire non en texte brut, l’écriture d’une implémentation de filtre personnalisée est la seule façon de s’assurer que WDS peut indexer le format de fichier dans le catalogue. Vous ne pouvez avoir qu’un seul complément de filtre pour un type de fichier. il est donc possible de remplacer un filtre existant ou de faire en sorte qu’un autre filtre remplace le vôtre pour un type de fichier spécifique.

Cette section contient les rubriques suivantes :

-   [Interfaces de filtre requises](#required-filter-interfaces)
    -   [Interface IFilter](#ifilter-interface)
    -   [IPersistStream](#ipersiststream)
    -   [IPersistFile](#ipersistfile)
    -   [IPersistStorage](#ipersiststorage)
-   [Sortir des propriétés avec des filtres](#outputting-properties-with-filters)
    -   [Valeurs de propriété](#property-values)
-   [Filtrer l’installation du complément](#filter-add-in-installation)
    -   [CLSID requis pour l’inscription](#clsids-required-for-registration)
    -   [Modèle d’inscription](#registration-model)
    -   [Pour inscrire un complément de filtre](#to-register-a-filter-add-in)
-   [Rubriques connexes](#related-topics)

## <a name="required-filter-interfaces"></a>Interfaces de filtre requises

Un complément de filtre doit implémenter l’interface [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)et l’une des interfaces suivantes :

-   [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) -pour charger des données à partir d’un flux. Cette opération est plus sécurisée que l’utilisation de fichiers, car rien n’est écrit sur le disque. l’interface IPersistStream est la méthode préférée pour la compatibilité ascendante avec Windows Vista.
-   [IPersistFile, interface](/windows/win32/api/objidl/nn-objidl-ipersistfile) -pour charger des données à partir d’un fichier. cette interface n’est pas prise en charge dans Windows Vista.
-   [IPersistStorage, Interface](/windows/win32/api/objidl/nn-objidl-ipersiststorage) -pour charger des données à partir d’un Stockage structuré OLE COM.

Un complément de filtre utilise ces interfaces pour obtenir le contenu de l’élément et les retourner de manière itérative à l’index jusqu’à ce que la fin du fichier soit atteinte. Un complément de filtre doit être aussi robuste que possible pour gérer les fichiers endommagés et ceux qui ne satisfont pas aux formats d’entrée attendus.

### <a name="ifilter-interface"></a>Interface IFilter

Il s’agit d’une interface requise pour l’implémentation d’un filtre. Pour plus d’informations, consultez les informations de référence sur l’interface [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter).



| Méthode       | Description                                                                            |
|--------------|----------------------------------------------------------------------------------------|
| Init ()       | Initialise une session de filtrage.                                                       |
| GetChunk ()   | Positionne le filtre au début du bloc First ou Next et retourne un descripteur. |
| GetText ()    | Récupère le texte du bloc actuel.                                                 |
| GetValue()   | Récupère les valeurs de propriété du bloc actuel.                                      |
| BindRegion() | Actuellement réservé à un usage interne ; n’implémentez pas. Cette méthode retourne E \_ NOTIMPL. |



 

### <a name="ipersiststream"></a>IPersistStream

Cette interface charge un fichier à partir d’un flux pour un traitement plus sécurisé que l' [interface IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) , car le contexte dans lequel un filtre [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) s’exécute n’a pas besoin des droits pour ouvrir des fichiers sur le disque ou sur le réseau. Parmi les deux méthodes d’accès à un seul fichier, il s’agit de la méthode recommandée pour la compatibilité ascendante avec Windows.



| Méthode       | Description                                                                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| IsDirty ()    | Vérifie si une modification a été apportée. Cette méthode retourne E \_ NOTIMPL dans les filtres.                                                                      |
| InitNew ()    | Crée un nouveau stockage. Cette méthode retourne E \_ NOTIMPL dans les filtres.                                                                                  |
| Load ()       | Initialise un objet à partir du flux ayant été précédemment enregistré.                                                                               |
| Save ()       | Enregistre un objet dans le flux spécifié et indique si l’objet doit réinitialiser son indicateur de modification. Cette méthode retourne E \_ NOTIMPL dans les filtres. |
| GetSizeMax() | Retourne la taille en octets du flux requis pour enregistrer l'objet. Cette méthode retourne E \_ NOTIMPL dans les filtres.                                      |



 

### <a name="ipersistfile"></a>IPersistFile

cette interface charge un fichier par chemin d’accès absolu et n’est pas pris en charge dans Windows Vista.



| Méthode          | Description                                                                                                                  |
|-----------------|------------------------------------------------------------------------------------------------------------------------------|
| GetCurFile()    | Obtient le nom actuel du fichier associé à l’objet. Retourne le chemin d’accès spécifié dans Load ().                          |
| Load ()          | Ouvre le fichier spécifié et initialise un objet à partir du contenu du fichier. Vous pouvez différer l’ouverture du fichier jusqu’à ce que vous en ayez besoin. |
| GetClassID ()    | Retourne l’identificateur de classe (CLSID) pour le nouveau type de fichier. Vous devez utiliser uuidgen.exe pour générer un CLSID unique.           |
| IsDirty ()       | N’a besoin que \_ de retourner E NOTIMPL dans les filtres                                                                                       |
| Save ()          | N’a besoin que \_ de retourner E NOTIMPL dans les filtres                                                                                       |
| SaveCompleted() | N’a besoin que \_ de retourner E NOTIMPL dans les filtres                                                                                       |



 

### <a name="ipersiststorage"></a>IPersistStorage

Cette interface prend en charge le modèle de stockage structuré, dans lequel chaque objet contenu a son propre stockage qui est imbriqué dans le stockage du conteneur. à l’instar de l' [interface IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile), cette interface est chargée par le chemin d’accès absolu et n’est pas prise en charge dans Windows Vista.



| Méthode            | Description                                                                                                   |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| IsDirty ()         | Vérifie si une modification a été apportée. Cette méthode retourne E \_ NOTIMPL dans les filtres.                                 |
| InitNew ()         | Crée un nouveau stockage. Cette méthode retourne E \_ NOTIMPL dans les filtres.                                             |
| Load ()            | Enregistre le stockage. Cette méthode retourne E \_ NOTIMPL dans les filtres.                                                 |
| Save ()            | Retourne la taille en octets du flux requis pour enregistrer l'objet. Cette méthode retourne E \_ NOTIMPL dans les filtres. |
| SaveCompleted()   | Réservé à un usage interne. Cette méthode retourne E \_ NOTIMPL dans les filtres.                                         |
| HandsOffStorage() | Réservé à un usage interne. Cette méthode retourne E \_ NOTIMPL dans les filtres.                                         |



 

## <a name="outputting-properties-with-filters"></a>Sortir des propriétés avec des filtres

L’objectif d’un filtre est d’extraire le contenu et les propriétés des fichiers à inclure dans l’index de recherche en texte intégral. WDS appelle d’abord la méthode Load sur les implémentations IPersistFile, IPersistStream ou IPersistStorage, puis appelle la méthode Init de l’implémentation IFilter. **GetChunk** est appelé pour extraire des blocs de données de texte ou de valeur de propriété, puis **gettext** ou **GetValue** est appelé autant de fois que nécessaire pour récupérer toutes les valeurs de texte ou de propriété associées au bloc. Ce processus se répète jusqu’à ce que **GetChunk** signale qu’il n’y a plus de segments dans le document.

La méthode **GetChunk** récupère des informations sur le premier ou le prochain bloc d’informations logiques à partir du fichier filtré et retourne ces informations dans une \_ structure de blocs STAT, y compris un ID de segment à croissance monotone, des informations d’État sur la façon dont le segment actuel est associé au bloc précédent, un indicateur qui spécifie si le segment contient du texte ou une valeur, les paramètres régionaux du La spécification de propriété est un [**FULLPROPSPEC**](/windows/desktop/api/filter/ns-filter-fullpropspec) qui se compose d’un CLSID et d’un identificateur de propriété de type entier ou chaîne (par exemple, D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType). Elle identifie le type de propriété plutôt que la valeur de propriété elle-même.

L’identificateur de paramètres régionaux du bloc est utilisé pour choisir un analyseur lexical approprié et il est très important que vous l’identifiiez correctement. Si le filtre ne peut pas déterminer les paramètres régionaux du texte, il doit supposer les paramètres régionaux système par défaut, disponibles à l’aide de **GetSystemDefaultLCID**. Si vous contrôlez le format de fichier et qu’il ne contient pas d’informations de paramètres régionaux, vous devez ajouter une fonctionnalité utilisateur pour permettre l’identification des paramètres régionaux appropriés. L’utilisation d’un analyseur lexical incompatible peut entraîner une mauvaise expérience de requête pour l’utilisateur.

**GetChunk** gère uniquement l’accès aux segments et ne retourne pas le texte ou la valeur de propriété elle-même. Au lieu de cela, les appels suivants à **gettext** et **GetValue** récupèrent le corps du bloc. **Gettext** retourne des segments de texte, qui sont des chaînes Unicode, à partir du segment de texte de bloc actuel \_ . Si le segment actuel est trop volumineux, plusieurs appels à la méthode **gettext** peuvent être nécessaires. Chaque appel à la méthode **gettext** récupère le texte qui suit immédiatement le texte du dernier appel à la méthode **gettext** . Par exemple, le dernier caractère d’un appel peut être au milieu d’un mot, et le premier caractère de l’appel suivant continue ce mot. Les moteurs de recherche doivent gérer cette situation.

**GetValue** retourne des valeurs de propriété pour le segment de valeur de segment actuel \_ dans les structures PROPVARIANT, qui peuvent contenir un large éventail de types de données. **GetValue** doit allouer la structure PROPVARIANT elle-même à l’aide de CoTaskMemAlloc. L’appelant de **GetValue** est chargé de libérer la mémoire vers laquelle pointe le PROPVARIANT à l’aide de PropVariantClear, et de libérer la structure elle-même avec CoTaskMemFree. Pour plus d’informations sur PROPVARIANTs, consultez la référence [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

### <a name="property-values"></a>Valeurs de la propriété

Les filtres doivent sortir au minimum des propriétés suivantes, qui sont les colonnes par défaut dans l’affichage des résultats de WDS.



| GUID                                 | PROPSPEC      | Nom convivial  | Description                                                                                                                                     |
|--------------------------------------|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| F29F85E0-4FF9-1068-AB91-08002B27B3D9 | 2             | PrimaryTitle   | Titre qui s’affiche pour cet élément.                                                                                                              |
| F29F85E0-4FF9-1068-AB91-08002B27B3D9 | 4             | PrimaryAuthors | Personne la plus associée à cet élément.                                                                                                          |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | PrimaryDate   | PrimaryDate    | Date la plus importante pour l’élément, par exemple la date de réception de l’e-mail ou la modification des fichiers.                                                               |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | PerceivedType | PerceivedType  | Type de fichier en cours d’analyse. doit correspondre à l’un des types de recherche Windows Desktop listés dans le Type de WDS [perçu](-search-2x-wds-perceivedtype.md). |



 

Pour les éléments en texte clair, WDS extrait toutes les propriétés définies par le système, telles que la taille ou l’extension du fichier, en incluant de nouveaux types de fichiers en texte brut à l’index. Les autres types de propriétés qui peuvent être retournées à l’index sont les suivants :

-   Pour les fichiers : auteur, titre, État, Mots clés
-   Pour le média : album, genre, marque de caméra, date de prise
-   Pour les communications : de, à, CC, importance
-   Pour les contacts : poste, téléphone professionnel, entreprise

La liste ci-dessus regroupe les propriétés communes à un type perçu spécifié ; Toutefois, toute propriété peut être utilisée quel que soit le type. Par exemple, la société peut être utilisée pour le nom de l’employeur d’un contact et peut également être utilisée pour faire référence au nom d’un client auquel le fichier est associé. Un grand nombre de ces propriétés sont utilisées pour afficher les résultats de la recherche dans l’affichage des résultats WDS. Par exemple, la propriété titre d’un fichier est affichée en tant que colonne principale dans la vue des résultats par défaut. Les objets IFilter doivent générer toutes les propriétés associées au type d’élément qu’ils analysent. Impossible d’ajouter des propriétés personnalisées dans WDS 2. x. Pour obtenir la liste complète des propriétés disponibles, consultez le [schéma WDS](-search-2x-wds-schematable.md).

## <a name="filter-add-in-installation"></a>Filtrer l’installation du complément

L’installation du filtre implique la copie de la DLL à un emplacement approprié dans le répertoire Program Files et son inscription. Les filtres doivent implémenter l’inscription automatique pour l’installation et doivent suivre les instructions suivantes :

-   Le programme d’installation doit utiliser le programme d’installation EXE ou MSI.
-   Des notes de publication doivent être fournies.
-   Une entrée **Ajout/suppression de programmes** doit être créée pour chaque complément installé.
-   Le programme d’installation doit prendre en charge tous les paramètres du Registre pour le type de fichier spécifique ou le magasin que le complément actuel comprend.
-   Si un complément précédent est remplacé, le programme d’installation doit avertir l’utilisateur.
-   Si un complément plus récent a remplacé le complément précédent, il devrait y avoir la possibilité de restaurer les fonctionnalités du complément précédent et de le faire en tant que complément par défaut pour ce type de fichier ou en magasin.

### <a name="clsids-required-for-registration"></a>CLSID requis pour l’inscription

Il existe trois identificateurs de classe, ou CLSID, associés à chaque filtre. Vous devez générer un ou plusieurs de ces (utilisez uuidgen.exe) pour inscrire votre complément de filtre.

-   La première identifie tous les filtres « gestionnaire persistant », IID \_ IFilter, qui est {89BCB740-6119-101A-BCB7-00DD010655AF}. Ce CLSID est constant pour tous les filtres qui implémentent IFilter.
-   La seconde (la valeur de la clé IID d’IID \_ ) identifie l’implémentation IFilter pour votre type de fichier. Cette clé contient une valeur InprocServer32 qui spécifie le nom de la DLL par chemin d’accès et le modèle de thread. Si le filtre se trouve dans le chemin système, comme le répertoire system32, un nom de fichier suffit. Dans le cas contraire, cette valeur doit avoir une spécification de chemin d’accès complet.
-   La troisième identifie le type de fichier traité par le filtre et est retourné par la méthode GetClassID sur votre interface IPersist.

> [!Note]
>
> Dans les versions ultérieures des systèmes d’exploitation Microsoft, l’installation de fichiers dans le répertoire system32 peut devenir plus difficile. nous vous recommandons donc de les installer sous Program Files et d’inclure un chemin d’accès complet au filtre dans le registre. Pour des raisons de sécurité, il est également prudent de spécifier un chemin d’accès complet à votre DLL dans le registre. Dans le cas contraire, une version « cheval de Troie » de votre DLL pourrait être chargée si elle se trouve dans le chemin d’accès du processus avant votre version.

 

### <a name="registration-model"></a>Modèle d’inscription

Lorsque WDS est prêt à filtrer un fichier, il consulte le Registre sous l’extension du fichier pour déterminer le filtre à charger. Il suit ensuite une série de liens de Registre pour rechercher le nom de la DLL de filtre, dans cet ordre :

1.  À partir de CLSID situés à l’emplacement suivant :

    **HKEY \_ Current \_ User \\ Software \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ Filters \\ override \\ RSApp**

    **HKEY \_ Current \_ User \\ Software \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ Filters**

2.  À partir du type de contenu de fichier à :

    **HKEY \_ local \_ machine \\ classes logicielles \\ \\ \\ type de contenu de base de données MIME \\**

3.  À partir de l’extension de nom de fichier (identique à l’API LoadIFilter Win32) à l’adresse :

    **HKEY \_ Current \_ User \\ Software \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ Filters \\ override \\ RSApp**

    **HKEY \_ Current \_ User \\ Software \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ Filters**

    **HKEY \_ classes \_ racine \\ EXTPERSISTENTHANDLER->CLSID->IID IID \_ ->CLSID**

4.  À partir de la valeur par défaut :

    **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ RSSearch \\ ContentIndexCommon \\ filtres**

### <a name="to-register-a-filter-add-in"></a>Pour inscrire un complément de filtre

Vous devez faire un total de huit entrées dans le registre pour inscrire votre complément de filtre, où :

-   **. ext** est la nouvelle extension de nom de fichier
-   Le **GUID \_ 1** peut être n’importe quel nouveau GUID généré pour cette extension
-   **89BCB740-6119-101A-BCB7-00DD010655AF** est le GUID d’interface IFilter, qui est une constante pour toutes les implémentations IFilter.

1.  Enregistrez le gestionnaire persistant pour l’extension de nom de fichier avec les clés et valeurs suivantes :

    ```
    HKEY_CLASSES_ROOT\<.ext>\PersistentHandler
       (Default) = {GUID_1}
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}
       (Default) = <Persistent Handler Description>
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}\PersistentAddinsRegistered
       (Default) = (Value Not Set)
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}\PersistentAddinsRegistered\{89BCB740-6119-101A-BCB7-00DD010655AF}
       (Default) = {CLSID of IFilter implementation}
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{GUID_1}\PersistentHandler
       (Default) = {GUID_1}
    ```

2.  Inscrivez l’implémentation IFilter avec les clés et valeurs suivantes :

    ```
    HKEY_CLASSES_ROOT\CLSID\{CLSID of IFilter implementation}
       (Default) = Extension IFilter Description">
    ```

    ```
    HKEY_CLASSES_ROOT\CLSID\{CLSID of IFilter implementation}\InprocServer32
       (Default) = <DLL Install Path>
       ThreadingModel = Both
    ```

3.  inscrivez l’implémentation IFilter avec Windows Desktop Search avec la clé et la valeur suivantes :

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\RSSearch\ContentIndexCommon\Filters\Extension\<.ext>
       (Default) = {CLSID of IFilter implementation}"
    ```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[SchemaTable](-search-2x-wds-schematable.md)
</dt> <dt>

[Types perçus](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[Développement de gestionnaires de protocole](-search-2x-wds-phaddins.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**Filtres**](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 