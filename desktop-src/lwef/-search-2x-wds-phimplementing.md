---
title: Implémentation d’un gestionnaire de protocole pour WDS
description: La création d’un gestionnaire de protocole implique l’implémentation de ISearchProtocol pour gérer des objets UrlAccessor, IUrlAccessor pour générer des métadonnées sur et pour identifier les filtres appropriés pour les éléments dans le magasin de données, IProtocolHandlerSite pour instancier un objet SearchProtocol et identifier les filtres appropriés, et IFilterto filtrer les fichiers propriétaires ou pour énumérer et filtrer les fichiers stockés de manière hiérarchique.
ms.assetid: d4bcf370-4152-4cfd-a92e-eb9196d23ab4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32e33a7ebf6d5f14d0ec4d78031e25b17d59bac5fb99ee7ea6d20046fbe95c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963489"
---
# <a name="implementing-a-protocol-handler-for-wds"></a>Implémentation d’un gestionnaire de protocole pour WDS

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.

La création d’un gestionnaire de protocole implique l’implémentation de [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) pour gérer des objets UrlAccessor, [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) pour générer des métadonnées sur et pour identifier les filtres appropriés pour les éléments dans le magasin de données, IProtocolHandlerSite pour instancier un objet SearchProtocol et identifier les filtres appropriés, et [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)pour filtrer des fichiers propriétaires ou pour énumérer et filtrer des fichiers stockés de manière hiérarchique. Le gestionnaire de protocole doit être multithread.

Cette section contient les rubriques suivantes :

-   [Remarque sur les URL](#note-on-urls)
-   [Interfaces du gestionnaire de protocole](#protocol-handler-interfaces)
-   [IFilters pour conteneurs](#ifilters-for-containers)
-   [Ajout de la fonctionnalité options du gestionnaire de protocole](#adding-protocol-handler-options-functionality)
    -   [ISearchProtocolOptions](#isearchprotocoloptions)
-   [Rubriques connexes](#related-topics)

## <a name="note-on-urls"></a>Remarque sur les URL

Microsoft Windows Desktop Search (WDS) utilise des url pour identifier de manière unique les éléments dans un système de fichiers, à l’intérieur d’un magasin de base de données ou sur le Web. Une URL qui définit un nœud d’entrée est appelée page de démarrage ; WDS commence à cette page de démarrage et analyse de manière récursive le magasin de données. La structure d’URL standard est la suivante :

`protocol://host/path/name.extension`

> [!Note]
>
> Lorsque vous souhaitez ajouter un nouveau magasin de données, vous devez sélectionner un nom pour l’identifier, qui n’est pas en conflit avec les nouveaux. Nous recommandons cette Convention d’affectation de noms : companyName. Scheme.

 

## <a name="protocol-handler-interfaces"></a>Interfaces du gestionnaire de protocole

**ISearchProtocol**

L’interface [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) appelle, initialise et gère les objets UrlAccessor. Pour plus d’informations sur l’implémentation de l’interface ISearchProtocol, consultez Référence de l' **interface ISearchProtocol**.

**IUrlAccessor**

Pour une URL spécifiée, l’interface [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) génère des métadonnées sur la structure d’emplacement ainsi que des éléments contenus, et lie ces éléments à un filtre. L’objet **IUrlAccessor** est instancié et initialisé par un objet SearchProtocol ; Toutefois, vous pouvez également implémenter une méthode d’initialisation interne afin que votre objet **IUrlAccessor** puisse effectuer des tâches d’initialisation spécifiques à votre gestionnaire de protocole, telles que la validation de l’URL pour un élément faisant l’objet d’un accès ou la vérification de l’heure de dernière modification pour déterminer si un fichier doit être traité dans l’analyse en cours.

> [!Note]
>
> Les heures de modification des répertoires sont ignorées. L’objet [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) doit énumérer les objets enfants pour déterminer s’il y a eu des modifications ou des suppressions.

 

Une grande partie de la conception de l’objet **UrlAccessor** dépend de l’ordre hiérarchique ou basé sur les liens de la structure. Pour les magasins de données hiérarchiques, l’objet **UrlAccessor** doit trouver un filtre qui peut énumérer son contenu. Une autre différence entre les gestionnaires de protocoles hiérarchiques et basés sur les liaisons est l’utilisation de la méthode IsDirectory. Dans les gestionnaires de protocole basés sur des liens, cette méthode doit retourner S \_ false. Les gestionnaires de protocole hiérarchiques doivent retourner S \_ OK pour les conteneurs.

Pour obtenir des instructions supplémentaires sur l’implémentation d’une interface [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) , consultez la référence de l' [**interface IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) .

**IProtocolHandlerSite**

Cette interface est utilisée pour instancier un objet **SearchProtocol** et fournit également l’objet **UrlAccessor** avec un filtre approprié pour un ID de classe (CLSID) spécifié.

## <a name="ifilters-for-containers"></a>IFilters pour conteneurs

Si vous implémentez un gestionnaire de protocole hiérarchique, vous devez implémenter un composant conteneur [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)qui énumère les URL représentant des conteneurs ou des dossiers. Le processus d’énumération est une boucle par le biais des méthodes **GetChunk** et **GetValue** de l’interface IFilter qui retournent une liste d’URL représentant chaque élément dans le conteneur.

En premier lieu, **GetChunk** retourne un FULLPROSPEC avec le jeu de propriétés Gather \_ PROPSET et l’un ou l’autre des éléments suivants :

-   PID \_ GTHR \_ DIRLINK, URL de l’élément sans l’heure de la dernière modification, ou
-   PID \_ GTHR \_ DIRLINK \_ avec \_ Time, URL avec l’heure de la dernière modification

Le GUID du jeu de propriétés pour la collecte \_ PROPSET est 0B63E343-9CCC-11D0-BCDB-00805FCCCE04. La propriété PROPSPEC est un PID \_ GTHR \_ DIRLINK = 2 ou un PID \_ GTHR \_ DIRLINK \_ avec \_ Time = 12 Decimal.

Le retour \_ d’un PID GTHR \_ DIRLINK \_ avec \_ Time est plus efficace, car l’indexeur peut déterminer immédiatement si l’élément doit être indexé sans appeler les méthodes ISearchProtocol->CreateUrlAccessor () et IUrlAccessor->GetLastModified ().

La méthode **GetValue** retourne alors un PROPVARIANT pour l’URL (et l’heure de dernière modification, si elle est utilisée), comme suit :

-   VT \_ LPWStr, URL de l’élément enfant, ou
-   Vecteur de l’URL suivi d’un FILETIME

L’exemple de code suivant montre comment créer le PID \_ GTHR \_ DIRLINK approprié \_ avec \_ Time.

> [!Note]
>
> **CE CODE ET CES INFORMATIONS SONT FOURNIS « EN L’ÉTAT », SANS GARANTIE D’AUCUNE SORTE, EXPRESSE OU IMPLICITE, Y COMPRIS, MAIS SANS S’Y LIMITER, LES GARANTIES IMPLICITES DE QUALITÉ MARCHANDE ET/OU D’ADÉQUATION À UN USAGE PARTICULIER.**
>
> Copyright (C) Microsoft. All rights reserved.

 


```
// params are assumed to be valid

HRESULT GetPropVariantForUrlAndTime(PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // allocate the propvariant pointer
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*ppPropValue));
    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // zero init the value

        // now allocate enough memory for 2 nested PropVariants.
        // PID_GTHR_DIRLINK_WITH_TIME is an array of 2 PROPVARIANTs
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // set the container PROPVARIANT that it is a vector of 2 PROPVARIANTS
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // now fill the array of PROPVARIANTS
                // put the pointer to the URL into the vector
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // put the FILETIME into vector
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
>
> Un composant [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)container doit toujours énumérer toutes les URL enfants, même si les URL enfants n’ont pas changé, car l’indexeur détecte les suppressions via le processus d’énumération. Si la sortie de date dans un répertoire de \_ liens \_ avec \_ l’heure indique que les données n’ont pas changé, l’indexeur ne met pas à jour les données de cette URL.

 

L’URL physique est l’URL que l’objet **UrlAccessor** traite. Si le filtre n’émet pas de DisplayUrl convivial, WDS affiche l’URL physique à l’utilisateur dans le cadre des résultats de la recherche. Le schéma WDS contient deux propriétés pour contrôler ce qui est affiché à l’utilisateur final, comme indiqué dans le tableau ci-dessous.



| GUID                                 | PROPSPEC      | Description                                         |
|--------------------------------------|---------------|-----------------------------------------------------|
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | DisplayFolder | Chemin de dossier affiché à l’utilisateur dans les résultats de la recherche |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | FolderName    | Nom complet du dossier parent                   |



 

Si votre code n’émet pas de DisplayFolder ou NomDossier, ces valeurs sont calculées à partir du DisplayUrl. Les barres obliques dans l’URL désignent des conteneurs dans le magasin ou le système de fichiers.

## <a name="adding-protocol-handler-options-functionality"></a>Ajout de la fonctionnalité options du gestionnaire de protocole

Pour que votre gestionnaire de protocole ait une page de démarrage par défaut (et une URL de nœud d’entrée), vous devez implémenter l’interface **ISearchProtocolOptions** . Dans les versions ultérieures de WDS, cette interface fournit des raccordements à la boîte de dialogue Options pour une expérience utilisateur améliorée. Cette interface fournit les fonctionnalités suivantes :

-   Détermine si les exigences de votre gestionnaire de protocole sont satisfaites. Par exemple, le magasin de votre gestionnaire de protocole peut nécessiter l’accès à une application donnée pour indexer correctement les données de l’application, mais cette application n’est pas disponible.
-   Identifie la configuration minimale requise pour que votre gestionnaire de protocole doive traiter un élément. les spécifications peuvent être exprimées dans une description conviviale et localisée, telle que « Microsoft Outlook 2000 ou plus ».
-   Définit les URL que votre gestionnaire de protocole doit traiter par défaut.

### <a name="isearchprotocoloptions"></a>ISearchProtocolOptions

Le tableau suivant décrit les méthodes que vous devez implémenter pour l’interface **ISearchProtocolOptions** .



| Méthode               | Description                                                                                             |
|----------------------|---------------------------------------------------------------------------------------------------------|
| CheckRequirements    | Détermine si la configuration minimale requise pour un gestionnaire de protocole personnalisé est remplie                             |
| GetDefaultCrawlScope | Retourne une liste d’URL par défaut dans un magasin spécifié pour un gestionnaire de protocole personnalisé                   |
| GetRequirements      | Identifie une description conviviale et localisée de la configuration minimale requise pour un gestionnaire de protocole personnalisé |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Notification de l’index des modifications](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[Ajout d’icônes, d’aperçus et de menus contextuels avec des extensions de Shell](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[Installation et inscription de gestionnaires de protocole](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 