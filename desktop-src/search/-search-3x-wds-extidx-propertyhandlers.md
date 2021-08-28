---
description: Microsoft Windows Search utilise des gestionnaires de propriétés pour extraire les valeurs des propriétés des éléments et utilise le schéma de système de propriétés pour déterminer comment une propriété spécifique doit être indexée.
ms.assetid: b475329a-1ed7-43a4-8e11-3700889a4ce9
title: développement de gestionnaires de propriétés pour la recherche de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3933353d8bf00c3a68a2259daf94a1ce4f13d295
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627324"
---
# <a name="developing-property-handlers-for-windows-search"></a>développement de gestionnaires de propriétés pour la recherche de Windows

Microsoft Windows Search utilise des gestionnaires de propriétés pour extraire les valeurs des propriétés des éléments et utilise le schéma de système de propriétés pour déterminer comment une propriété spécifique doit être indexée. pour lire et indexer des valeurs de propriété, les gestionnaires de propriétés sont appelés en mode out-of-process en Windows la recherche pour améliorer la sécurité et la robustesse. en revanche, les gestionnaires de propriétés sont appelés dans le processus par Windows Explorer pour lire et écrire des valeurs de propriété.

cette rubrique complète la rubrique du [système de propriétés](../properties/building-property-handlers.md) avec des informations spécifiques à Windows Search et contient les sections suivantes :

-   [Décisions de conception pour les gestionnaires de propriétés](#design-decisions-for-property-handlers)
    -   [Décisions de propriété](#property-decisions)
    -   [Prise en charge du texte intégral](#full-text-support)
    -   [Considérations sur le Implementatation du système d’exploitation](#operating-system-implementatation-considerations)
-   [Écriture de fichiers de description de propriété](#writing-property-description-files)
-   [Implémentation de gestionnaires de propriétés](#implementing-property-handlers)
    -   [IInitializeWithStream](#iinitializewithstream)
    -   [IPropertyStore](#ipropertystore)
    -   [IPropertyStoreCapabilities](#ipropertystorecapabilities)
-   [Vérifier que vos éléments sont indexés](#ensuring-your-items-get-indexed)
-   [Installation et inscription de gestionnaires de propriétés](#installing-and-registering-property-handlers)
-   [Test et dépannage des gestionnaires de propriétés](#testing-and-troubleshooting-property-handlers)
    -   [Tests d’installation et de configuration](#installation-and-setup-tests)
    -   [Dépannage des gestionnaires de propriétés](#troubleshooting-property-handlers)
-   [Utilisation de gestionnaires de propriétés System-Supplied](#using-system-supplied-property-handlers)
-   [Rubriques connexes](#related-topics)

 

## <a name="design-decisions-for-property-handlers"></a>Décisions de conception pour les gestionnaires de propriétés

L’implémentation de gestionnaires de propriétés implique les étapes suivantes :

1.  Prendre des décisions de conception concernant les propriétés que vous souhaitez prendre en charge.
2.  Création d’un fichier de description de propriété (. propDesc) pour les propriétés qui ne sont pas déjà dans le système de propriétés.
3.  Implémentation et test du gestionnaire de propriétés.
4.  Installation et enregistrement du gestionnaire de propriétés et des fichiers de description de propriété.
5.  Test de l’installation et de l’inscription du gestionnaire de propriétés.

Avant de commencer, vous devez prendre en compte les questions de conception suivantes :

-   Quelles sont les propriétés prises en charge par le format de fichier ?
-   Ces propriétés sont-elles déjà dans le schéma système ?
-   Puis-je utiliser un gestionnaire de propriétés fourni par le système existant ?
-   Quelles propriétés peuvent être affichées aux utilisateurs finaux ?
-   Quelles sont les propriétés modifiables par les utilisateurs ?
-   La prise en charge de la recherche en texte intégral provient-elle d’un gestionnaire de propriétés ou d’un filtre ?
-   Dois-je prendre en charge les applications héritées ? Si c’est le cas, que dois-je implémenter ?

> [!Note]  
> Avant de continuer, consultez [utilisation de System-Supplied gestionnaires de propriétés](#using-system-supplied-property-handlers) pour déterminer si vous pouvez utiliser un gestionnaire de propriétés fourni par le système, ce qui vous permet de gagner du temps et des ressources de développement.

 

une fois ces décisions prises, vous pouvez écrire des descriptions formelles de vos propriétés personnalisées afin que le moteur de recherche Windows puisse commencer à indexer vos fichiers et propriétés. Ces descriptions formelles sont des fichiers XML, décrits dans schéma de la [propriété Description](/previous-versions//cc144127(v=vs.85)).

### <a name="property-decisions"></a>Décisions de propriété

Lorsque vous envisagez les propriétés à prendre en charge, vous devez identifier les besoins en matière d’indexation et de recherche des utilisateurs. Par exemple, vous pouvez identifier les propriétés potentiellement utiles 100 pour votre type de fichier, mais les utilisateurs peuvent être intéressés par la recherche sur une seule poignée. en outre, vous souhaiterez peut-être afficher un groupe différent, plus grand ou plus petit de ces propriétés pour les utilisateurs dans Windows Explorer et autoriser les utilisateurs à modifier uniquement un sous-ensemble de ces propriétés affichées.

Votre type de fichier peut prendre en charge toutes les propriétés personnalisées que vous définissez, ainsi qu’un ensemble de propriétés définies par le système. Avant de créer une propriété personnalisée, consultez les [Propriétés système](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) pour voir si la propriété que vous souhaitez prendre en charge est déjà définie par une propriété système. Veillez à toujours prendre en charge les propriétés définies par le système les plus importantes.

Nous vous recommandons d’utiliser une matrice pour vous aider à concevoir vos propriétés :



| Nom de la propriété | Est indexable ? | Est affichable ? | Est modifiable ? |
|---------------|---------------|-----------------|--------------|
| property1     | O             | O               | N            |
| propriété...   | O             | O               | N            |
| propriétéN     | N             | N               | N            |



 

Pour chacune de ces propriétés, vous devez déterminer les attributs à utiliser, puis les décrire formellement dans les fichiers XML de description de propriété (. propDesc). Les attributs incluent le type de données, l’étiquette, la chaîne d’aide de la propriété, etc. Pour les propriétés indexables, vous devez prêter une attention particulière aux attributs de propriété suivants qui se trouvent dans l’élément XML [searchInfo](../properties/propdesc-schema-searchinfo.md)   du fichier de description de propriété.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>inInvertedIndex</td>
<td>Optionnel. Indique si une valeur de propriété de chaîne doit être décomposée en mots et chaque mot stocké dans l’index inversé. L’index inversé permet une recherche efficace de mots et d’expressions sur la valeur de propriété à l’aide de CONTAINs ou FREETEXT (par exemple, SELECT... OÙ contient &quot; someText &quot; ). Si la valeur est <strong>false</strong>, les recherches sont effectuées par rapport à la chaîne entière. La plupart des propriétés de chaîne doivent avoir la valeur <strong>true</strong>; les propriétés qui ne sont pas des chaînes doivent avoir la valeur <strong>false</strong>. La valeur par défaut est <strong>false</strong>.</td>
</tr>
<tr class="even">
<td>isColumn</td>
<td>Optionnel. indique si la propriété doit être stockée dans le Windows base de données de recherche en tant que colonne. Le stockage de la propriété en tant que colonne permet la récupération, le tri, le regroupement et le filtrage (autrement dit, à l’aide d’un prédicat à l’exception de CONTAINs ou FREETEXT) sur l’ensemble de la valeur de colonne. Les propriétés affichées pour l’utilisateur doivent avoir la valeur <strong>true</strong> , sauf s’il s’agit d’une propriété textuelle très volumineuse (telle que le corps d’un document) qui serait recherchée dans l’index inversé. La valeur par défaut est <strong>false</strong>.</td>
</tr>
<tr class="odd">
<td>isColumnSparse</td>
<td>Optionnel. Indique si une propriété ne prend pas d’espace si la valeur est <strong>null</strong>. Une propriété non allouée prend de l’espace pour chaque élément, même si la valeur est <strong>null</strong>. Si la propriété est à valeurs multiples, cet attribut a toujours la <strong>valeur true</strong>. Cet attribut doit avoir la valeur <strong>false</strong> uniquement si une valeur est présente pour chaque élément. La valeur par défaut est <strong>true</strong>.</td>
</tr>
<tr class="even">
<td>columnIndexType</td>
<td>Optionnel. pour optimiser l’interrogation, le moteur de recherche Windows peut créer des index secondaires pour les propriétés qui ont isColumn =<strong>TRUE</strong>. Cela nécessite plus d’espace disque et de traitement pendant l’indexation, mais améliore les performances lors de l’interrogation. Si la propriété tend à être triée, regroupée ou filtrée (c’est-à-dire en utilisant =, ! =, <, >, comme, MATCHES) fréquemment par les utilisateurs, cet attribut doit être défini sur &quot; OnDisk &quot; . La valeur par défaut est &quot; NotIndexed &quot; . Les valeurs suivantes sont valides :
<ul>
<li>NotIndexed : aucun index secondaire n’est créé.</li>
<li>OnDisk : créez et stockez un index secondaire sur le disque.</li>
</ul></td>
</tr>
<tr class="odd">
<td>maxSize</td>
<td>Optionnel. indique la taille maximale autorisée pour la valeur de propriété stockée dans le Windows base de données de recherche. Cette limite s’applique aux éléments indvidual d’un vecteur, et non au vecteur dans son ensemble. Les valeurs au-delà de cette taille sont tronquées. La valeur par défaut est &quot; 128 &quot; (octets).<br/> actuellement, Windows Search n’utilise pas le maxSize lors du calcul de la quantité de données qu’il accepte à partir d’un fichier. au lieu de cela, la limite Windows utilisée par la recherche est le produit de la taille du fichier et le MaxGrowFactor (taille de fichier N * MaxGrowFactor) lu à partir du registre sur HKEY_LOCAL_MACHINE->Software->Microsoft->Windows Search->gathering Manager->MaxGrowFactor. La valeur par défaut de MaxGrowFactor est quatre (4). par conséquent, si la taille totale de votre type de fichier est faible, mais que les propriétés sont plus volumineuses, Windows recherche peut ne pas accepter toutes les données de propriété que vous souhaitez émettre. Toutefois, vous pouvez augmenter le MaxGrowFactor en fonction de vos besoins. <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Pour l’attribut columnIndexType, l’avantage des requêtes plus rapides doit être pesé par rapport à l’augmentation du temps d’indexation et des coûts d’espace que les indices secondaires peuvent engendrer. Toutefois, ce coût est uniquement payé pour les éléments qui ont une valeur non **null** . par conséquent, pour la plupart des propriétés, cet attribut peut avoir la valeur « OnDisk ».

 

### <a name="full-text-support"></a>Prise en charge du texte intégral

En règle générale, la recherche en texte intégral est prise en charge par les composants appelés [filtres](-search-3x-wds-extidx-filters.md). Toutefois, pour les types de fichiers texte avec des formats de fichiers non compliqués, les gestionnaires de propriétés peuvent être en mesure de fournir cette fonctionnalité avec moins d’efforts de développement. Vous devez consulter la section [contenu de texte intégral](../properties/building-property-handlers-property-handlers.md) pour obtenir une comparaison des fonctionnalités de filtre et de gestionnaire de propriétés pour vous aider à déterminer ce qui convient le mieux à votre type de fichier. Il est particulièrement important que les filtres puissent gérer plusieurs identificateurs de code de langue (LCID) par fichier alors que les gestionnaires de propriétés ne le peuvent pas.

> [!Note]  
> Étant donné que les gestionnaires de propriétés ne peuvent pas segmenter le contenu de la même façon que les filtres, les fichiers volumineux (même s’il s’agit de formats de fichiers non compliqués) doivent être complètement chargés en mémoire.

 

### <a name="operating-system-implementatation-considerations"></a>Considérations sur le Implementatation du système d’exploitation

### <a name="implementation-information-for-windows-7"></a>informations d’implémentation pour Windows 7

dans Windows 7 et versions ultérieures, il existe un nouveau comportement lors de l’inscription d’un gestionnaire de propriétés, d’un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)ou d’une nouvelle extension. Lorsqu’un nouveau gestionnaire de propriétés et/ou **IFilter** est installé, les fichiers avec les extensions correspondantes sont automatiquement réindexés.

dans Windows 7, il est recommandé d’installer un [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter) conjointement avec les gestionnaires de propriétés correspondants, et d’inscrire le **ifilter** avant le gestionnaire de propriétés. L’inscription du gestionnaire de propriétés lance la réindexation immédiate des fichiers précédemment indexés sans nécessiter un redémarrage, et tire parti des IFilter précédemment inscrits à des fins d’indexation du contenu.

Si seul un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) est installé, sans gestionnaire de propriétés correspondant, la réindexation automatique se produit soit après un redémarrage du service d’indexation, soit par un redémarrage du système.

pour plus d’informations sur les indicateurs de description de propriété spécifiques à Windows 7, consultez les rubriques de référence suivantes :

-   [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags)
-   [TYPE de PROPDESC \_ COLUMNINDEX \_](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)
-   [PROPDESC \_ SEARCHINFO, \_ indicateurs](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)

### <a name="implementation-information-for-windows-vista-and-earlier"></a>informations d’implémentation pour Windows Vista et versions antérieures

avant Windows Vista, les filtres fournissaient la prise en charge de l’analyse et de l’énumération du contenu et des propriétés du fichier. Avec l’introduction du système de propriétés, les gestionnaires de propriétés gèrent les propriétés de fichier, tandis que les filtres gèrent le contenu du fichier. pour Windows Vista, vous devez développer uniquement une implémentation partielle de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)en coordination avec un gestionnaire de propriétés, comme décrit dans [meilleures pratiques pour la création de gestionnaires de filtres dans Windows Search](-search-3x-wds-extidx-filters.md).

alors que le système de propriétés est également inclus dans le Windows l’installation de recherche pour Windows XP, des applications tierces et héritées peuvent nécessiter que les filtres gèrent le contenu et les propriétés. par conséquent, si vous développez sur la plateforme Windows XP, vous devez fournir une implémentation de filtre complète, ainsi qu’un gestionnaire de propriétés pour votre type de fichier ou propriété personnalisée.

 

## <a name="writing-property-description-files"></a>Écriture de fichiers de description de propriété

La structure des fichiers XML de description de propriété (. propDesc) est décrite dans la rubrique [PropertyDescription](../properties/propdesc-schema-propertydescription.md) . Les attributs de l’élément [searchInfo](../properties/propdesc-schema-searchinfo.md) présentent un intérêt particulier pour la recherche. Une fois que vous avez choisi les propriétés à prendre en charge, vous devez créer et inscrire des fichiers de description de propriété pour chaque propriété. Lorsque vous inscrivez vos fichiers. propDesc, ils sont inclus dans la liste de description de la propriété du schéma et deviennent des noms de colonnes dans la Banque de propriétés du moteur de recherche.

Vous pouvez enregistrer vos descriptions de propriété personnalisées à l’aide de la fonction [PSRegisterPropertySchema](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) , une API wrapper qui appelle le IPropertySystem :: RegisterPropertySchema du sous-système de schéma. Cette fonction informe le sous-système de schéma de l’ajout de fichiers de schéma de description de propriété (. propDesc), en utilisant des chemins d’accès de fichier au (x) fichier (s). propDesc sur l’ordinateur local, généralement le répertoire d’installation de l’application sous « Program Files ». En règle générale, une installation ou une application (par exemple, votre programme d’installation de gestionnaire de propriétés) appellera cette méthode après l’installation du ou des fichiers. propDesc.

 

## <a name="implementing-property-handlers"></a>Implémentation de gestionnaires de propriétés

Le développement d’un gestionnaire de propriétés implique l’implémentation des interfaces suivantes :

-   IInitialzeWithStream : fournit l’initialisation basée sur le flux de votre gestionnaire de propriétés.
-   IPropertyStore : énumère, obtient et définit les valeurs de propriété.
-   IPropertyStoreCapabilities : facultatif. Indique si les utilisateurs peuvent modifier une propriété à partir d’une interface utilisateur.

### <a name="iinitializewithstream"></a>IInitializeWithStream

Comme décrit dans la rubrique [système de propriétés](../properties/building-property-handlers.md) , nous vous recommandons vivement d’implémenter des gestionnaires de propriétés avec **IInitializeWithStream** pour effectuer une initialisation basée sur le flux. Si vous avez choisi de ne pas implémenter IInitializeWithStream, le gestionnaire de propriétés doit refuser de s’exécuter dans le processus d’isolation en définissant l’indicateur DisableProcessIsolation sur la clé de Registre du gestionnaire de propriétés. La désactivation de l’isolation de processus est généralement prévue uniquement pour les gestionnaires de propriétés hérités et doit être évitée de manière ardue par tout nouveau code.

### <a name="ipropertystore"></a>IPropertyStore

Pour créer un gestionnaire de propriétés, vous devez implémenter l’interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) avec les méthodes suivantes.



| Méthode   | Description                                                         |
|----------|---------------------------------------------------------------------|
| Commit   | Enregistre une modification de propriété dans le fichier.                                |
| GetAt    | Récupère une clé de propriété à partir du tableau de propriétés d’un élément.        |
| GetCount | Obtient le nombre de propriétés jointes au fichier.                 |
| GetValue | Récupère des données pour une propriété spécifique.                             |
| SetValue | Définit une nouvelle valeur de propriété ou remplace ou supprime une valeur existante. |



 

 

 

Les considérations importantes relatives à l’implémentation de cette interface sont incluses dans la documentation [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .

> [!Note]  
> Si votre gestionnaire de propriétés émet plusieurs valeurs pour la même propriété pour un élément donné, seule la dernière valeur émise est stockée dans le catalogue.

 

 

### <a name="ipropertystorecapabilities"></a>IPropertyStoreCapabilities

Les gestionnaires de propriétés peuvent éventuellement implémenter cette interface pour désactiver la possibilité pour un utilisateur de modifier des propriétés spécifiques. Ces propriétés sont généralement modifiables dans la page de détails et le volet, mais leur modification n’est pas autorisée sous le gestionnaire d’implémentation de propriété. L’implémentation de cette interface offre une meilleure expérience utilisateur que l’alternative, une simple erreur d’exécution à partir de l’interpréteur de commandes.

 

## <a name="ensuring-your-items-get-indexed"></a>Vérifier que vos éléments sont indexés

Maintenant que vous avez implémenté votre gestionnaire de propriétés, vous devez vous assurer que les éléments que votre gestionnaire est inscrit pour être indexés. Vous pouvez utiliser le [Gestionnaire de catalogue](-search-3x-wds-mngidx-catalog-manager.md) pour lancer la réindexation, et vous pouvez également utiliser le [Gestionnaire de portée d’analyse](-search-3x-wds-extidx-csm.md) pour configurer des règles par défaut indiquant les URL que l’indexeur doit analyser. une autre option consiste à suivre l’exemple de code de réindexation dans les [exemples du kit de développement logiciel (SDK) Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).

Pour plus d’informations, reportez-vous à [utilisation du gestionnaire de catalogues](-search-3x-wds-mngidx-catalog-manager.md) et [à l’utilisation du gestionnaire de portée d’analyse](-search-3x-wds-extidx-csm.md).

 

## <a name="installing-and-registering-property-handlers"></a>Installation et inscription de gestionnaires de propriétés

Avec le gestionnaire de propriétés implémenté, il doit être enregistré et son extension de nom de fichier associée au gestionnaire. L’exemple suivant montre les clés de Registre et les valeurs requises pour effectuer cette opération.

```
HKEY_CLASSES_ROOT
   CLSID
      {<CLSID for property handler>}
         (Default) = <Property Handler Name>
         InProcServer32
            (Default) = <full path to property handler dll>
            ThreadingModel = <your threading model>
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PropertySystem
                  PropertyHandlers
                     <.fileextention>
                        (Default) = {<CLSID for property handler>}
```

 

## <a name="testing-and-troubleshooting-property-handlers"></a>Test et dépannage des gestionnaires de propriétés

La liste suivante fournit des conseils sur les types de tests que vous devez effectuer :

-   Testez l’obtention de la sortie de chaque propriété unique prise en charge par le type de fichier.
-   Utilisez des valeurs de propriété volumineuses, par exemple, utilisez une large balise Meta dans des documents HTML.
-   Vérifiez que le gestionnaire de propriétés ne perd pas les handles de fichiers en les modifiant après avoir obtenu la sortie du gestionnaire de propriétés, ou à l’aide d’un outil comme oh.exe avant et après l’énumération des propriétés de fichier.
-   Testez tous les types de fichiers associés au gestionnaire de propriétés. Par exemple, vérifiez que le filtre HTML fonctionne avec les types de fichiers .htm et .html.
-   Testez les fichiers endommagés. Le gestionnaire de propriétés doit échouer correctement.
-   Si une application prend en charge le chiffrement, vérifiez que le gestionnaire de propriétés ne génère pas de texte chiffré.
-   Si votre gestionnaire de propriétés prend en charge la recherche en texte intégral :
    -   Utilisez plusieurs caractères Unicode spéciaux dans le contenu du fichier et testez leur sortie.
    -   Testez la gestion des documents de très grande taille pour vous assurer que le gestionnaire de propriétés fonctionne comme prévu.

### <a name="installation-and-setup-tests"></a>Tests d’installation et de configuration

Enfin, vous devez tester vos routines d’installation et de désinstallation.

-   L’installation doit récupérer après l’échec des installations (par exemple, en annulant, puis en redémarrant le programme d’installation).
-   La désinstallation doit supprimer tous les fichiers associés au gestionnaire de propriétés.
-   La désinstallation ne doit pas supprimer les fichiers autres que ceux associés à l’installation du gestionnaire de propriétés.
-   Les clés de Registre associées au gestionnaire de propriétés doivent être supprimées lors de la désinstallation de.
-   La désinstallation doit fonctionner même si les fichiers sont supprimés du répertoire d’installation.

### <a name="troubleshooting-property-handlers"></a>Dépannage des gestionnaires de propriétés

Voici quelques erreurs courantes lors du développement de gestionnaires de propriétés :

-   Installation des fichiers. propDesc ou des dll dans un répertoire utilisateur.
-   Inscription de composants à l’aide de chemins d’accès relatifs.
-   Inscription des composants sous HKEY \_ Current \_ User au lieu de HKEY \_ local \_ machine.
-   Oubli de définir DisableProcessIsolation pour les gestionnaires qui ne sont pas des flux.
-   Placement du fichier de test dans un emplacement non indexé.

Si vous avez des difficultés à faire fonctionner votre gestionnaire de propriétés avec l’indexeur, voici quelques conseils pour vous aider à résoudre les problèmes :

-   Vérifiez que vos descriptions de propriété (fichiers. propDesc) sont marquées isColumn = "**true**", isViewable = "**true**" et isQueryable = "**true**" selon le cas.
-   Vérifiez que vos fichiers. propDesc se trouvent dans un emplacement global.
-   Vérifiez que vous avez enregistré vos fichiers. propDesc à l’aide de chemins absolus.
-   Vérifiez que le journal des événements n’a pas enregistré d’erreurs lors de l’inscription de votre fichier. propDesc.
-   Vérifiez que vos dll se trouvent dans un emplacement global (et non sous votre profil utilisateur).
-   Vérifiez que vos dll sont inscrites sous HKEY \_ local \_ machine \\ Software \\ classes.
-   Vérifiez que vos dll sont inscrites à l’aide de chemins d’accès complets (ou de chaînes SZ de l’extension REG \_ \_ qui se développent en chemins absolus à l’aide de variables d’environnement connues par le compte système).
-   vérifiez que votre gestionnaire de propriétés fonctionne sous l’explorateur de Windows.
-   Bien que nous vous recommandons d’utiliser IInitializeWithStream, si vous devez utiliser IInitializeWithFile ou IInitializeWithItem, vérifiez que vous spécifiez DisableProcessIsolation.
-   Vérifiez que le panneau de configuration options d’indexation répertorie votre type de fichier en tant que type de fichier indexé.
-   Vérifiez que le fichier de test se trouve dans un emplacement indexé.
-   Vérifiez que le fichier de test a été modifié depuis que vous avez installé votre gestionnaire de propriétés.

Si votre fichier de test se trouve dans un emplacement indexé et que l’indexeur a déjà analysé cet emplacement, vous devez modifier le fichier d’une façon pour déclencher la réindexation du fichier.

 

## <a name="using-system-supplied-property-handlers"></a>Utilisation de gestionnaires de propriétés System-Supplied

Windows comprend un certain nombre de gestionnaires de propriétés fournis par le système que vous pouvez utiliser si le format de votre type de fichier est compatible. Si vous définissez une nouvelle extension de fichier qui utilise l’un de ces formats, vous pouvez utiliser les gestionnaires fournis par le système en inscrivant l’identificateur de classe du gestionnaire (CLSID) pour votre extension de fichier.

Vous pouvez utiliser le CLSID indiqué dans le tableau suivant pour inscrire les gestionnaires de propriétés fournis par le système pour votre type de format de fichier.



| Format          | CLSID                                  |
|-----------------|----------------------------------------|
| Doc OLE     | {8d80504a-0826-40c5-97e1-ebc68f953792} |
| Enregistrer le fichier XML de jeu   | {ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60} |
| Gestionnaire XPS/OPC | {45670FA8-ED97-4F44-BC93-305082590BFB} |
| XML             | {c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9} |



 

Avant de créer une propriété personnalisée, vous devez vous assurer qu’il n’existe pas de propriété définie par le système que vous pouvez utiliser à la place. Vous pouvez énumérer les propriétés définies par le système en appelant [**PSEnumeratePropertyDescriptions**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) ou à l’aide de l’outil en ligne de commande prop.exe.

Le schéma système définit la façon dont ces propriétés interagissent avec l’indexeur, et vous ne pouvez pas le modifier. En outre, l’application que vous utilisez pour créer, modifier et enregistrer votre type de fichier doit également se conformer à certains comportements. Par exemple, si l’application implémente l’enregistrement sécurisé (où un fichier temporaire est créé lors de la modification, puis ReplaceFile () est utilisé pour échanger la nouvelle version de l’ancien), elle doit transférer toutes les propriétés du fichier d’origine vers le nouveau fichier. Dans le cas contraire, le fichier perd les propriétés ajoutées par les utilisateurs ou d’autres applications.

 

**Exemple**

L’exemple suivant montre l’inscription du gestionnaire OLE DocFile fourni par le système pour un type de fichier avec un. Extension OLEDocFile.

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         shellex
            {BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}
               (Default) = {9DBD2C50-62AD-11d0-B806-00C04FD706EC}
```

L’exemple suivant montre l’inscription des informations de la liste de propriétés pour les propriétés de. Les fichiers OLEDocFile s’affichent sous l’onglet Détails et le volet.

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         ExtendedTileInfo = prop:System.ItemType;System.Size;System.DateModified;System.Author;System.OfflineAvailability
         FullDetails = prop:System.PropGroup.Description;System.Title;System.Subject;
System.Keywords;System.Category;System.Comment;System.PropGroup.Origin;
System.Author;System.Document.LastAuthor;System.Document.RevisionNumber;
System.Document.Version;System.ApplicationName;System.Company;System.Document.Manager;
System.Document.DateCreated;System.Document.DateSaved;System.Document.DatePrinted;
System.Document.TotalEditingTime;System.PropGroup.Content;System.ContentStatus;
System.ContentType;System.Document.PageCount;System.Document.WordCount;
System.Document.CharacterCount;System.Document.LineCount;
System.Document.ParagraphCount;System.Document.Template;System.Document.Scale;
System.Document.LinksDirty;System.Language;System.PropGroup.FileSystem;
System.ItemNameDisplay;System.ItemType;System.ItemFolderPathDisplay;
System.DateCreated;System.DateModified;System.Size;System.FileAttributes;
System.OfflineAvailability;System.OfflineStatus;System.SharedWith;
System.FileOwner;System.ComputerName
         InfoTip = prop:System.ItemType;System.Size;System.DateModified;System.Document.PageCoun
         PerceivedType = document
         PreviewDetails = prop:*System.DateModified;System.Author;System.Keywords;
*System.Size;System.Title;System.Comment;System.Category;
*System.Document.PageCount;System.ContentStatus;System.ContentType;
*System.OfflineAvailability;*System.OfflineStatus;System.Subject;
*System.DateCreated;*System.SharedWith
```

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Mappages de propriétés](-search-3x-wds-propertymappings.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[meilleures pratiques pour la création de gestionnaires de filtres dans Windows Search](-search-3x-wds-extidx-filters.md)
</dt> <dt>

[Processus d’indexation](-search-indexing-process-overview.md)
</dt> <dt>

[Développement de gestionnaires de protocole](-search-3x-wds-phaddins.md)
</dt> <dt>

[Propriétés définies par le système pour les formats de fichiers personnalisés](-shell-systemdefinedpropertiesforfileformats.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[Système de propriétés](../properties/building-property-handlers.md)
</dt> <dt>

[Propriétés système](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> <dt>

[Windows Rechercher des exemples de SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
</dt> </dl>

 

 
