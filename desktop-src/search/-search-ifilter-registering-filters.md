---
description: Votre gestionnaire de filtres doit être inscrit. Vous pouvez également trouver un gestionnaire de filtres pour une extension de nom de fichier donnée par le biais du registre ou à l’aide de l’interface ILoadFilter.
ms.assetid: 3478b948-73c7-4533-974a-d9b5186a651b
title: Inscription des gestionnaires de filtres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18f39688bbea3bb0dd73ef28a0ba6e8b0dcf7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112450"
---
# <a name="registering-filter-handlers"></a>Inscription des gestionnaires de filtres

Votre gestionnaire de filtres doit être inscrit. Vous pouvez également trouver un gestionnaire de filtres pour une extension de nom de fichier donnée par le biais du registre ou à l’aide de l’interface [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) .

Cette rubrique est organisée comme suit :

- [Inscription des gestionnaires de filtres pour Windows Search](#registering-filter-handlers)
  - [Approche obsolète pour l’inscription des gestionnaires de filtres](#obsolete-approach-for-registering-filters-handlers)
- [Remplacement de gestionnaires de filtres existants](#replacing-existing-filter-handlers)
- [Recherche d’un gestionnaire de filtres pour une extension de fichier donnée](#finding-a-filter-handler-for-a-given-file-extension)
- [Ressources supplémentaires](#additional-resources)
- [Rubriques connexes](#related-topics)

> [!NOTE]  
> Un gestionnaire de filtres est une implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .

## <a name="registering-filters-handlers-for-windows-search"></a>Inscription des gestionnaires de filtres pour Windows Search

Les GUID dont vous avez besoin pour l’inscription d’un nouveau gestionnaire de protocole ou pour rechercher un gestionnaire de protocole existant sont répertoriés dans le tableau suivant.

| GUID                                     | Défini par l’utilisateur ou l’application | Description                                                                                               |
|------------------------------------------|-----------------------------|-----------------------------------------------------------------------------------------------------------|
| **89BCB740-6119-101A-BCB7-00DD010655AF** | Application                 | Le GUID de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) est une constante de clé de Registre pour tous les gestionnaires de filtres. |
| **{PersistentHandlerGUID}**              | Utilisateur                        | Il s’agit du GUID du gestionnaire persistant.                                                              |
| **{FilterHandlerCLSID}**                 | Utilisateur                        | Il s’agit de l’identificateur de classe (CLSID) pour le gestionnaire de filtres.                                              |
| **{ApplicationGUID}**                    | Utilisateur                        | Il s’agit d’un GUID intermédiaire (agrégé).                                                                |

Les gestionnaires de filtres doivent être inscrits dans HKEY \_ local \_ machine, car SearchFilterHost.exe s’exécute sous le compte système et ne peut donc pas accéder aux clés de Registre pour HKEY \_ Current \_ User pour l’utilisateur connecté. En outre, le groupe utilisateurs doit avoir un accès en lecture et en exécution au gestionnaire de filtres. dll proprement dit, car SearchFilterHost.exe supprime tous les droits d’administrateur et n’autorise que les droits non-administrateurs. Étant donné que l’emplacement de projet Visual Studio par défaut se trouve dans le répertoire de l’utilisateur actuel et n’accorde donc pas d’autorisations de lecture au groupe utilisateurs, vous devez déplacer le fichier. dll ou modifier les listes de contrôle d’accès pour autoriser l’accès SearchFilterHost.exe.

Lorsque vous inscrivez un nouveau gestionnaire de filtres, nous vous recommandons d’utiliser un nom descriptif, par exemple HTML IFilter.

**Pour inscrire votre nouveau gestionnaire de filtres :**

1. Spécifiez l’extension et le GUID du gestionnaire persistant qui utiliseront le gestionnaire de filtres :

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                PersistentHandler
                   (Default) = {PersistentHandlerGUID}
```

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                CLSID
                   {PersistentHandlerGUID}
                      PersistentAddinsRegistered
                         {89BCB740-6119-101A-BCB7-00DD010655AF}l
                            (Default) = {FilterHandlerCLSID}
```

2. Inscrivez votre gestionnaire de filtres avec les clés et valeurs suivantes :

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                CLSID
                   {FilterHandlerCLSID}
                      (Default) = {DescriptiveFilterHandlerName}
                      InprocServer32
                         (Default) = DLL Install Path
                         ThreadingModel = Both
```

### <a name="obsolete-approach-for-registering-filters-handlers"></a>Approche obsolète pour l’inscription des gestionnaires de filtres

Cette approche n’est pas recommandée pour une utilisation. Les filtres peuvent être inscrits pour un CLSID qui représente une classe COM (Component Object Model) et/ou pour une extension de nom de fichier. Vous pouvez inscrire les deux filtres si vous devez enregistrer un gestionnaire de filtres pour une classe et un autre gestionnaire de filtre pour une extension de nom de fichier dans la classe. Notez qu’un gestionnaire de filtre inscrit pour une extension de nom de fichier est prioritaire sur un gestionnaire de filtre pour un CLSID.

Ces entrées sont des entrées de Registre OLE standard jusqu’à et y compris l’entrée de la classe **CLSID \\ {ApplicationGUID}**. La DLL sample.dll implémente le comportement de l’objet en cours d’exécution pour la classe. txt. Notez l’entrée supplémentaire, PersistentHandler. Cette entrée spécifie la classe qui est responsable de la négociation des demandes vers les objets persistants de l’exemple de classe. L’entrée sous **PersistentAddinsRegistered** identifie l’implémentation responsable de l’interface nommée **89BCB740-6119-101A-BCB7-00DD010655AF**(IID \_ IFilter). La classe implémentant **IID \_ IFilter** a des entrées de Registre OLE standard. La DLL InprocServer32 est chargée par le biais du mécanisme OLE standard.

Windows Search observe le modèle de thread spécifié pour le gestionnaire de filtres. Lorsque le modèle de thread est défini sur **both**, le gestionnaire de filtres doit être thread-safe ; Sinon, si elle n’est pas thread-safe, spécifiez **Apartment**. Notez que les gestionnaires de filtres doivent toujours être thread-safe.

Les exemples d’entrées de registre suivants concernent un gestionnaire de filtres inscrit pour une classe et une extension de nom de fichier. **{PersistentHandlerGUID}** et **{FilterHandlerCLSID}** sont utilisés comme variables indiquant les valeurs qui doivent être spécifiées par le créateur du gestionnaire de filtres. Les valeurs sont de type REG \_ sz.

```
HKEY_LOCAL_MACHINE
   Software
      Classes
         .txt
            (Default) = SampleFile
         SampleFile
            (Default) = Class for Sample Files
            CLSID
               (Default) = {ApplicationGUID}
         CLSID
            {ApplicationGUID}
               (Default) = Sample Files
               InprocServer32
                  (Default) = sample.dll
               PersistentHandler
                  (Default) = {PersistentHandlerGUID}
            {PersistentHandlerGUID}
               (Default) = Sample file persistent handler
               PersistentAddinsRegistered
                  {89BCB740-6119-101A-BCB7-00DD010655AF}l
                     (Default) = {FilterHandlerCLSID}
            {FilterHandlerCLSID}
               (Default) = Sample Files
               InprocServer32
                  (Default) = sampfilt.dll
                  ThreadingModel = Both
```

## <a name="replacing-existing-filter-handlers"></a>Remplacement de gestionnaires de filtres existants

Nous vous recommandons de ne pas remplacer les gestionnaires de filtres intégrés pour les types de fichiers courants tels que. txt,. doc,. html,. URL, et ainsi de suite, car cela peut avoir des effets indésirables sur d’autres composants système. L’indexation des corps des messages électroniques dépend des gestionnaires de filtres. txt,. html et. rtf, par exemple.

Si un nouveau gestionnaire de filtres pour un type de fichier est en cours d’installation en remplacement d’une inscription de filtre existante, le programme d’installation doit enregistrer l’inscription actuelle et la restaurer si le nouveau gestionnaire de filtres est désinstallé. Il n’existe aucun mécanisme pour la chaîne de filtres. Par conséquent, le nouveau gestionnaire de filtres est chargé de répliquer toutes les fonctionnalités nécessaires de l’ancien filtre.

## <a name="finding-a-filter-handler-for-a-given-file-extension"></a>Recherche d’un gestionnaire de filtres pour une extension de fichier donnée

Vous pouvez utiliser l’interface [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) pour rechercher un gestionnaire de filtres pour une extension de nom de fichier donnée. Les exemples d’entrées de registre suivants montrent comment procéder pour les fichiers HTML. Dans cet exemple, le gestionnaire de filtres pour les documents HTML est nlhtml.dll. Les valeurs sont de type REG \_ sz.

**Pour rechercher le gestionnaire de filtres pour une extension de nom de fichier donnée :**

1. Vérifiez si l’extension pour le type de fichiers filtrés a un gestionnaire persistant inscrit sous l’entrée de Registre \\ HKEY \_ local \_ machine \\ Software \\ classes. extension. Si c’est le cas, laissez cette clé être {PersistentHandlerGUID}.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             .htm
                PersistentHandler
                   {PersistentHandlerGUID}
```

2. Si aucun gestionnaire persistant n’est inscrit pour l’extension, recherchez le CLSID associé au type de document sous l’entrée de Registre \\ HKEY \_ local \_ machine \\ Software \\ classes. Laissez cette clé être {ApplicationGUID}. Déterminez ensuite si un gestionnaire persistant est inscrit pour le CLSID : à l’aide de {ApplicationGUID}, localisez le gestionnaire persistant pour l' \\ entrée HKEY de l' \_ ordinateur local de l' \_ \\ \\ \\ identificateur CLSID \\ {ApplicationGUID}. Laissez cette clé être {PersistentHandlerGUID}.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                (Default) = Class for WWW HTML files
                CLSID
                   (Default) = {25336920-03F9-11CF-8FD0-00AA00686F13}
             CLSID
                {25336920-03F9-11CF-8FD0-00AA00686F13}
                   PersistentHandler
                      (Default) = {PersistentHandlerGUID}
```

3. Déterminez le GUID du gestionnaire persistant : à l’aide de {PersistentHandlerGUID}, recherchez le GUID du gestionnaire persistant pour le type de document. La valeur sous l’entrée de Registre HKEY \_ local \_ machine \\ Software \\ classes \\ CLSID \\ {PERSISTENTHANDLERGUID} \\ PersistentAddinsRegistered \\ 89BCB740-6119-101A-BCB7-00DD010655AF génère le GUID du gestionnaire persistant pour ce type de document. Laissez cette clé être {FilterHandlerCLSID}.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             {PersistentHandlerGUID}
                (Default) = HTML File Persistent Handler<dl>
                    REG_SZ     {89BCB740-6119-101A-BCB7-00DD010655AF}
                    REG_SZ     (Default) = {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

4. Déterminez le gestionnaire de filtres : à l’aide de {FilterHandlerCLSID} qui a été déterminé à l’étape précédente, recherchez le gestionnaire de filtre sous l’entrée \\ HKEY \_ local \_ machine \\ Software \\ classes \\ CLSID \\ {FilterHandlerCLSID} \\ InprocServer32. Dans cet exemple, le nom du gestionnaire de filtres descriptifs utilisé est HTML IFilter.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             CLSID
                {EEC97550-47A9-11CF-B952-00AA0051FE20}
                   (Default) = HTML IFilter
                    Data type  REG_SZ
                    InprocServer32
                    nlhtml.dll
```

## <a name="additional-resources"></a>Ressources supplémentaires

- L’exemple de code [IFilterSample](-search-sample-ifiltersample.md) , disponible sur [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), montre comment créer une classe de base [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) pour l’implémentation de l’interface **IFilter** .
- Pour obtenir une vue d’ensemble du processus d’indexation, consultez [processus d’indexation](-search-indexing-process-overview.md).
- Pour obtenir une vue d’ensemble des types de fichiers, consultez [types de fichiers](../shell/fa-file-types.md).
- Pour interroger des attributs d’association de fichiers pour un type de fichier, consultez [PerceivedTypes, SystemFileAssociations et inscription d’application](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Rubriques connexes

[Développement de gestionnaires de filtres](-search-ifilter-conceptual.md)

[À propos des gestionnaires de filtres dans Windows Search](-search-ifilter-about.md)

[Meilleures pratiques pour la création de gestionnaires de filtres dans Windows Search](-search-3x-wds-extidx-filters.md)

[Retour des propriétés d’un gestionnaire de filtres](-search-ifilter-property-filtering.md)

[Gestionnaires de filtres fournis avec Windows](-search-ifilter-implementations.md)

[Implémentation de gestionnaires de filtres dans Windows Search](-search-ifilter-constructing-filters.md)

[Test des gestionnaires de filtres](-search-ifilter-testing-filters.md)
