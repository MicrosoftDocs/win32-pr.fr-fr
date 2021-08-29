---
description: L’installation d’un gestionnaire de protocole implique la copie de la ou des DLL vers un emplacement approprié dans le répertoire Program Files, puis l’inscription du gestionnaire de protocole dans le registre.
ms.assetid: 07c40c0c-2729-462c-ba40-e05ffea2b889
title: installation et inscription de gestionnaires de protocole (recherche Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a71a47c7ea3fbc82607749239838a7f03fb784d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880125"
---
# <a name="installing-and-registering-protocol-handlers-windows-search"></a>installation et inscription de gestionnaires de protocole (recherche Windows)

L’installation d’un gestionnaire de protocole implique la copie de la ou des DLL vers un emplacement approprié dans le répertoire Program Files, puis l’inscription du gestionnaire de protocole dans le registre. L’application d’installation peut également ajouter une racine de recherche et des règles d’étendue pour définir une étendue d’analyse par défaut pour la source de données Shell.

Cette rubrique est organisée comme suit :

-   [À propos des URL](#about-urls)
-   [Implémentation d’interfaces de gestionnaires de protocole](#implementing-protocol-handler-interfaces)
    -   [ISearchProtocol et ISearchProtocol2](#isearchprotocol-and-isearchprotocol2)
    -   [IUrlAccessor, IUrlAccessor2, IUrlAccessor3 et IUrlAccessor4](#iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4)
    -   [IProtocolHandlerSite](#iprotocolhandlersite)
-   [Implémentation de gestionnaires de filtres pour les conteneurs](#implementing-filter-handlers-for-containers)
-   [Installation et inscription d’un gestionnaire de protocole](#installing-and-registering-a-protocol-handler)
    -   [Instructions pour l’inscription d’un gestionnaire de protocole](#guidelines-for-registering-a-protocol-handler)
    -   [Inscription d’un gestionnaire de protocole](#installing-and-registering-a-protocol-handler)
    -   [Inscription du gestionnaire de type de fichier du gestionnaire de protocole](#registering-the-protocol-handlers-file-type-handler)
-   [Vérification de l’indexation de vos éléments](#ensuring-that-your-items-are-indexed)
-   [Rubriques connexes](#related-topics)

## <a name="about-urls"></a>À propos des URL

Windows La recherche utilise des URL pour identifier de manière unique les éléments dans la hiérarchie de votre source de données de Shell. L’URL qui est le premier nœud de la hiérarchie est appelée [racine de recherche](-search-3x-wds-extidx-csm-searchroots.md). Windows La recherche commence l’indexation à la racine de recherche, en demandant que le gestionnaire de protocole énumère les liens enfants pour chaque URL.

La structure d’URL standard est la suivante :


```
<protocol>:// [{user SID}/] <localhost>/<path>/[<ItemID>]
```



La syntaxe de l’URL est décrite dans le tableau suivant.



| Syntaxe           | Description                                                                                                                                                                                                        |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| &lt;protocol&gt; | Identifie le gestionnaire de protocole à appeler pour l’URL.                                                                                                                                                           |
| {SID utilisateur}       | Identifie le contexte de sécurité de l’utilisateur sous lequel le gestionnaire de protocole est appelé. Si aucun identificateur de sécurité (SID) utilisateur n’est identifié, le gestionnaire de protocole est appelé dans le contexte de sécurité du service système. |
| &lt;path&gt;     | Définit la hiérarchie du magasin, où chaque barre oblique (« / ») est un séparateur entre les noms de dossiers.                                                                                                            |
| &lt;ItemID&gt;   | Représente une chaîne unique qui identifie l’élément enfant (par exemple, le nom de fichier).                                                                                                                            |



 

l’indexeur de recherche Windows supprime la barre oblique finale des url. Par conséquent, vous ne pouvez pas compter sur l’existence d’une barre oblique finale pour identifier un répertoire par rapport à un élément. Votre gestionnaire de protocole doit être en mesure de gérer cette syntaxe d’URL. Assurez-vous que le nom du protocole que vous sélectionnez pour identifier votre source de données Shell n’est pas en conflit avec les noms actuels. Nous vous recommandons d’utiliser cette Convention d’affectation de noms : `companyName.scheme` .

Pour plus d’informations sur la création d’une source de données Shell, consultez [implémentation des interfaces d’objet de dossier de base](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

## <a name="implementing-protocol-handler-interfaces"></a>Implémentation d’interfaces de gestionnaires de protocole

La création d’un gestionnaire de protocole requiert l’implémentation des trois interfaces suivantes :

-   [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) pour gérer les objets UrlAccessor.
-   [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) pour exposer des propriétés et identifier les filtres appropriés pour les éléments dans la source de données Shell.
-   [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) pour filtrer les fichiers propriétaires ou pour énumérer et filtrer les fichiers stockés hiérarchiquement.

Outre les trois interfaces obligatoires répertoriées, les autres interfaces sont facultatives, et vous pouvez implémenter les interfaces facultatives les plus appropriées pour la tâche en cours.

### <a name="isearchprotocol-and-isearchprotocol2"></a>ISearchProtocol et ISearchProtocol2

Les interfaces SearchProtocol initialisent et gèrent les objets UrlAccessor du gestionnaire de protocole. L’interface [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) est une extension facultative de [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol)et comprend une méthode supplémentaire pour spécifier des informations supplémentaires sur l’utilisateur et l’élément.

### <a name="iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4"></a>IUrlAccessor, IUrlAccessor2, IUrlAccessor3 et IUrlAccessor4

Les interfaces [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) sont décrites dans le tableau suivant.



| Interface                                                 | Description                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor)              | Pour une URL spécifiée, l’interface [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) fournit l’accès aux propriétés de l’élément qui est exposé dans l’URL. Il peut également lier ces propriétés à un filtre propre au gestionnaire de protocole (autrement dit, un filtre autre que celui associé au nom de fichier). |
| [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) (facultatif) | L’interface [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) étend [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) avec des méthodes qui obtiennent une page de codes pour les propriétés de l’élément et son URL d’affichage, et qui obtiennent le type d’élément dans l’URL (document ou répertoire).                                    |
| [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) (facultatif) | L’interface [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) étend [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) avec une méthode qui obtient un tableau de sid d’utilisateur, ce qui permet à l’hôte de protocole de recherche d’emprunter l’identité de ces utilisateurs pour indexer l’élément.                                                      |
| [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) (facultatif) | L’interface [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) étend les fonctionnalités de l’interface [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) avec une méthode qui détermine si le contenu de l’élément doit être indexé.                                                                 |



 

L’objet UrlAccessor est instancié et initialisé par un objet SearchProtocol. Les interfaces [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) fournissent un accès à des informations importantes par le biais des méthodes décrites dans le tableau suivant.



| Méthode                                                                                        | Description                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUrlAccessor::GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified)                 | Retourne l’heure de la dernière modification de l’URL. Si cette heure est plus récente que la dernière fois que l’indexeur a traité cette URL, les gestionnaires de filtres (implémentations de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) sont appelés pour extraire (éventuellement) les données modifiées pour cet élément. Les heures de modification des répertoires sont ignorées. |
| [**IUrlAccessor::IsDirectory**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-isdirectory)                         | Identifie si l’URL représente un dossier contenant des URL enfants.                                                                                                                                                                                                                                                            |
| [**IUrlAccessor::BindToStream**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtostream)                       | Établit une liaison avec une [interface IStream](/windows/win32/api/objidl/nn-objidl-istream) qui représente les données d’un fichier dans un magasin de données personnalisé.                                                                                                                                                                           |
| [**IUrlAccessor::BindToFilter**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtofilter)                       | Crée une liaison avec un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)spécifique au gestionnaire de protocole, qui peut exposer des propriétés pour l’élément.                                                                                                                                                                                                                 |
| [**IUrlAccessor4::ShouldIndexItemContent**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor4-shouldindexitemcontent) | Indique si le contenu de l’élément doit être indexé.                                                                                                                                                                                                                                                                      |



 

### <a name="iprotocolhandlersite"></a>IProtocolHandlerSite

L’interface [**IProtocolHandlerSite**](/windows/desktop/api/Searchapi/nn-searchapi-iprotocolhandlersite) est utilisée pour instancier un gestionnaire de filtre, qui est hébergé dans un processus isolé. Le gestionnaire de filtre approprié est obtenu pour un identificateur de classe persistante (CLSID), une classe de stockage de document ou une extension de nom de fichier spécifiés. L’avantage de demander au processus hôte de se lier à [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) est que le processus hôte peut gérer le processus de localisation d’un gestionnaire de filtres approprié et contrôler la sécurité impliquée dans l’appel du gestionnaire.

## <a name="implementing-filter-handlers-for-containers"></a>Implémentation de gestionnaires de filtres pour les conteneurs

Si vous implémentez un gestionnaire de protocole hiérarchique, vous devez implémenter un gestionnaire de filtres pour un conteneur qui énumère les URL enfants. Un gestionnaire de filtres est une implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . Le processus d’énumération est une boucle par le biais des méthodes [**IFilter :: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) et [**IFilter :: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) de l’interface **IFilter** ; chaque URL enfant est exposée comme valeur de la propriété.

[**IFilter :: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) retourne les propriétés du conteneur. Pour énumérer les URL enfants, **IFilter :: GetChunk** retourne l’un des éléments suivants :

-   A-la [ \_ Rechercher \_ UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)):

    URL de l’élément sans l’heure de la dernière modification. [**IFilter :: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) retourne un PROPVARIANT contenant l’URL enfant.

-   A-la [ \_ Rechercher \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md):

    L’URL et l’heure de dernière modification. [**IFilter :: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) retourne un PROPVARIANT contenant un vecteur de l’URL enfant et de l’heure de la dernière modification.

Le retour de la [ \_ recherche de \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) est plus efficace, car l’indexeur peut déterminer immédiatement si l’élément doit être indexé sans appeler les méthodes [**ISearchProtocol :: CreateAccessor**](/windows/desktop/api/Searchapi/nf-searchapi-isearchprotocol-createaccessor) et [**IUrlAccessor :: GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified) .

L’exemple de code suivant montre comment retourner la [propriété \_ \_ UrlToIndexWithModificationTime de recherche](../properties/props-system-search-urltoindexwithmodificationtime.md) de renvoi à la valeur.

> [!IMPORTANT]
>
> Copyright (c) Microsoft Corporation. Tous droits réservés.

 


```
// Parameters are assumed to be valid

HRESULT GetPropVariantForUrlAndTime
    (PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // Allocate the propvariant pointer.
    size_t const cbAlloc = sizeof(**ppPropValue);
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(cbAlloc));

    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // Zero init the value

        // Now allocate enough memory for 2 nested PropVariants.
        // PKEY_Search_UrlToIndexWithModificationTime is an array of two PROPVARIANTs.
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // Set the container PROPVARIANT to be a vector of two PROPVARIANTS.
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // Now fill the array of PROPVARIANTS.
                // Put the pointer to the URL into the vector.
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // Put the FILETIME into vector.
                (*ppPropValue)->capropvar.pElems[1].vt = VT_FILETIME; 
                (*ppPropValue)->capropvar.pElems[1].filetime = ftLastModified;
            }

            else
            {
                CoTaskMemFree(pVector);
            }
        }
 
        if (FAILED(hr))
        {
            CoTaskMemFree(*ppPropValue);
            *ppPropValue = NULL;
        }
    }
    return S_OK;
}

```



> [!Note]  
> Un composant [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) container doit toujours énumérer toutes les URL enfants, même si les URL enfants n’ont pas changé, car l’indexeur détecte les suppressions via le processus d’énumération. Si la sortie de date dans [une \_ \_ UrlToIndexWithModificationTime de recherche](../properties/props-system-search-urltoindexwithmodificationtime.md) de la valeur de la variable indique que les données n’ont pas changé, l’indexeur ne met pas à jour les données de cette URL.

 

## <a name="installing-and-registering-a-protocol-handler"></a>Installation et inscription d’un gestionnaire de protocole

L’installation de gestionnaires de protocole implique la copie de la ou des DLL vers un emplacement approprié dans le répertoire Program Files, puis l’inscription de la ou des DLL. Les gestionnaires de protocole doivent implémenter l’inscription automatique pour l’installation. L’application d’installation peut également ajouter une racine de recherche et des règles d’étendue pour définir une étendue d’analyse par défaut pour la source de données Shell, qui est décrite dans la section Vérification de l' [indexation de vos éléments](#ensuring-that-your-items-are-indexed) à la fin de cette rubrique.

### <a name="guidelines-for-registering-a-protocol-handler"></a>Instructions pour l’inscription d’un gestionnaire de protocole

Vous devez suivre ces instructions lors de l’inscription d’un gestionnaire de protocole :

-   Le programme d’installation doit utiliser le programme d’installation EXE ou MSI.
-   Des notes de publication doivent être fournies.
-   Une entrée ajout/suppression de programmes doit être créée pour chaque complément installé.
-   Le programme d’installation doit prendre en charge tous les paramètres du Registre pour le type de fichier spécifique ou le magasin que le complément actuel comprend.
-   Si un complément précédent est remplacé, le programme d’installation doit avertir l’utilisateur.
-   Si un complément plus récent a remplacé le complément précédent, il doit être possible de restaurer les fonctionnalités précédentes du complément et de faire de nouveau le complément par défaut pour ce type de fichier.
-   Le programme d’installation doit définir une étendue d’analyse par défaut pour l’indexeur en ajoutant une racine de recherche et des règles d’étendue à l’aide du gestionnaire de la portée d’analyse (CSM).

### <a name="registering-a-protocol-handler"></a>Inscription d’un gestionnaire de protocole

Vous devez faire quatorze entrées dans le registre pour inscrire le composant de gestionnaire de protocole, où :

-   *Ver \_ IND \_ ProgID* est le ProgID indépendant de la version de l’implémentation du gestionnaire de protocole.
-   *Ver \_ L' \_ identificateur* de programme DEP est le ProgID dépendant de la version de l’implémentation du gestionnaire de protocole.
-   *CLSID \_ 1* est le CLSID de l’implémentation du gestionnaire de protocole.

**Pour inscrire un gestionnaire de protocole :**

1.  Enregistrez le ProgID indépendant de la version avec les clés et valeurs suivantes :

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CurVer
             (Default) = <Ver_Dep_ProgID>
    ```

2.  Enregistrez le ProgID dépendant de la version avec les clés et valeurs suivantes :

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

3.  Enregistrez le CLSID du gestionnaire de protocole avec les clés et valeurs suivantes :

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          {InprocServer32}
             (Default) = <DLL Install Path>
             Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ProgID>
             (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ShellFolder>
             Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          TypeLib
             (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          VersionIndependentProgID
             (Default) = <Ver_Ind_ProgID>
    ```

4.  inscrire le gestionnaire de protocole avec Windows recherche. Dans l’exemple suivant, <Protocol Name> est le nom du Protocole lui-même, tel que fichier, MAPI, etc. :

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    avant Windows Vista :

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Desktop Search
                DS
                   Index
                      ProtocolHandlers
                         <Protocol Name>
                            HasRequirements = dword:00000000
                            HasStartPage = dword:00000000
    ```

### <a name="registering-the-protocol-handlers-file-type-handler"></a>Inscription du gestionnaire de type de fichier du gestionnaire de protocole

Vous devez créer deux entrées dans le registre pour inscrire le gestionnaire de type de fichier du gestionnaire de protocole (qui est également appelé extension d’interpréteur de commandes).

1.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Desktop
                         NameSpace
                            {CLSID of PH Implementation}
                               (Default) = <Shell Implementation Description>
    ```

2.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Shell Extensions
                         Approved
                            {CLSID of PH Implementation} = <Shell Implementation Description>
    ```

## <a name="ensuring-that-your-items-are-indexed"></a>Vérification de l’indexation de vos éléments

Une fois que vous avez implémenté votre gestionnaire de protocole, vous devez spécifier les éléments de Shell que votre gestionnaire de protocole doit indexer. Vous pouvez utiliser le gestionnaire de catalogue pour lancer la réindexation (pour plus d’informations, consultez [utilisation du gestionnaire de catalogues](-search-3x-wds-mngidx-catalog-manager.md)). Vous pouvez également utiliser le gestionnaire de portée d’analyse (CSM) pour configurer les règles par défaut indiquant les URL que vous souhaitez que l’indexeur analyse (pour plus d’informations, consultez [utilisation du gestionnaire de portée d’analyse](-search-3x-wds-extidx-csm.md) et [gestion des règles d’étendue](-search-3x-wds-extidx-csm-scoperules.md)). Vous pouvez également ajouter une racine de recherche (pour plus d’informations, consultez [gestion des racines de recherche](-search-3x-wds-extidx-csm-searchroots.md)). une autre option consiste à suivre la procédure décrite dans l’exemple de réindexation dans [Windows exemples du kit de développement logiciel (SDK) de recherche](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).

L’interface [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) fournit des méthodes qui informent le moteur de recherche des conteneurs à l’analyse et/ou à la surveillance, et les éléments sous ces conteneurs à inclure ou exclure lors de l’analyse ou de la surveillance. dans Windows 7 et versions ultérieures, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) étend **ISearchCrawlScopeManager** avec la méthode [**ISearchCrawlScopeManager2 :: GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) qui obtient la version, qui informe les clients si l’état de l’CSM a changé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Fonctionnement des gestionnaires de protocole](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Développement de gestionnaires de protocole](-search-3x-wds-phaddins.md)
</dt> <dt>

[Notification de l’index des modifications](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Ajout d’icônes et de menus contextuels](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Exemple de code : extensions de Shell pour les gestionnaires de protocole](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Création d’un connecteur de recherche pour un gestionnaire de protocole](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Débogage de gestionnaires de protocole](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
