---
description: La suite de tests IFilter valide vos gestionnaires de filtres.
ms.assetid: 5ee02af1-1dc9-4d21-868f-4c439970b1ba
title: Test des gestionnaires de filtres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf58f14f0f8de4458dd887bf52b32fb68f869d64
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122621945"
---
# <a name="testing-filter-handlers"></a>Test des gestionnaires de filtres

La suite de tests [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) valide vos gestionnaires de filtres. La suite de tests effectue cette vérification en appelant des méthodes [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) et en vérifiant les valeurs retournées pour la conformité avec la spécification de l’interface **IFilter** . et le fait de vérifier que les identificateurs de bloc sont uniques et s’améliorent, que l’interface **IFilter** se comporte de manière cohérente après la réinitialisation, et que toute méthode **IFilter** qui appelle avec des paramètres non valides retourne les codes d’erreur attendus. Les programmes de suite de tests enregistrent également la sortie d’un fichier filtré par un gestionnaire de filtres et vérifient les informations d’inscription **IFilter** dans le registre.

Cette rubrique est organisée comme suit :

- [Appel de ligne de commande](#command-line-invocation)
  - [ifilttst.exe](#ifilttstexe)
  - [filtdump.exe](#filtdumpexe)
  - [filtreg.exe](#filtregexe)
  - [ifilttst.ini](#ifilttstini)
- [Procédure de test IFilter](#ifilter-test-procedure)
  - [Test de validation](#validation-test)
  - [Test de cohérence](#consistency-test)
  - [Test d’entrée non valide](#invalid-input-test)
  - [Test de différentes configurations IFilter](#testing-different-ifilter-configurations)
- [Vérification de l’indexation des éléments inscrits](#ensuring-registered-items-get-indexed)
  - [Exemple de fichier journal](#sample-log-file)
  - [Exemple de fichier dump](#sample-dump-file)
- [Ressources supplémentaires](#additional-resources)
- [Rubriques connexes](#related-topics)

> [!NOTE]  
> Si un nouveau gestionnaire de filtres pour un type de fichier est en cours d’installation en remplacement d’une inscription de filtre existante, le programme d’installation doit enregistrer l’inscription actuelle et la restaurer si le nouveau gestionnaire de filtres est désinstallé. Il n’existe aucun mécanisme pour la chaîne de filtres. Par conséquent, le nouveau gestionnaire de filtres est chargé de répliquer toutes les fonctionnalités nécessaires de l’ancien filtre.

## <a name="command-line-invocation"></a>Appel de Command-Line

La suite de tests [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) se compose de trois applications en ligne de commande : [ifilttst.exe](#ifilttstexe), [filtdump.exe](#filtdumpexe)et [filtreg.exe](#filtregexe) et un fichier d’initialisation, [ifilttst.ini](#ifilttstini).

> [!IMPORTANT]
> dans Windows 7 et versions ultérieures, les filtres écrits en code managé sont bloqués explicitement. Les filtres doivent être écrits en code natif en raison de problèmes potentiels de contrôle de version du common language runtime (CLR) avec le processus dans lequel plusieurs compléments s’exécutent.

### <a name="ifilttstexe"></a>ifilttst.exe

Le programme ifilttst.exe exécute plusieurs tests pour valider un gestionnaire de filtres. L’exemple suivant illustre l’appel du programme ifilttst.exe à partir de la ligne de commande :


```
ifilttst /i test.htm /l /d /v 1
```

L’exemple effectue les tâches suivantes :

- Indique au programme de filtrer le fichier test.htm
- Redirige les messages du journal vers test.htm. log
- Redirige les messages de vidage vers test.htm. dmp
- Définit le niveau de détail sur 1

Pour que la commande précédente fonctionne, trois fichiers doivent se trouver dans le répertoire de travail actuel : `test.htm` , [ifilttst.exe](#ifilttstexe)et [ifilttst.ini](#ifilttstini). Les commutateurs de ligne de commande sont répertoriés dans le tableau suivant.

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Commutateur et variables possibles</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>/i nom du fichier</strong></td>
<td>Fichier d’entrée ou répertoire à filtrer. Le nom de fichier peut contenir les caractères génériques <code>*</code> et <code>?</code> .</td>
</tr>
<tr class="even">
<td><strong>/l</strong></td>
<td>Les messages de journal sont dirigés vers un fichier au lieu de l’écran. Les messages de journal décrivent les tests individuels effectués et les résultats de réussite/échec des tests. Le nom du fichier journal est le même que le nom du fichier d’entrée, mais avec une extension. log.</td>
</tr>
<tr class="odd">
<td><strong>/d</strong></td>
<td>Les messages de vidage sont dirigés vers un fichier au lieu de l’écran. Les messages de vidage décrivent le contenu des segments. La structure du bloc est vidée lorsque le niveau de détail est 3. Le nom du fichier dump est le même que le nom du fichier d’entrée, mais avec une extension. dmp.</td>
</tr>
<tr class="even">
<td><strong>/-l</strong></td>
<td>Désactivez la journalisation. Cet indicateur remplace le <code>/l</code> commutateur.</td>
</tr>
<tr class="odd">
<td><strong>/-d</strong></td>
<td>Désactiver le vidage. Cet indicateur remplace le <code>/d</code> commutateur.</td>
</tr>
<tr class="even">
<td><strong>entier/v</strong></td>
<td>Niveau de commentaires. La valeur par défaut est 3.
<ul>
<li>0-le test enregistre uniquement les messages relatifs à des échecs spécifiques de l’interface <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> . Le test vide le contenu du bloc.</li>
<li>1-le test journalise les messages d’avertissement, ainsi que ceux pour le niveau 0.</li>
<li>2-le test journalise les messages relatifs aux tests qui ont réussi, ainsi qu’à ceux du niveau 1.</li>
<li>3-le test journalise les messages d’information, ainsi que ceux pour le niveau 2. En outre, le test vide la structure du bloc.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>/t entier</strong></td>
<td>Nombre de threads à lancer. La valeur par défaut est 1.</td>
</tr>
<tr class="even">
<td><strong>/r entier</strong>]</td>
<td>Filtre de manière récursive les sous-répertoires. Le paramètre Integer facultatif spécifie la profondeur d’exercice de la récursivité. Si aucun entier n’est spécifié, ou si l’entier est égal à 0, la récursivité complète est supposée. Par défaut, la profondeur de récurrence est 1.</td>
</tr>
<tr class="odd">
<td><strong>entier/c</strong></td>
<td>Nombre de boucles. Si l’entier est 0, le test effectue une boucle infinie. Par défaut, le test ne boucle qu’une seule fois.</td>
</tr>
</tbody>
</table>

> [!NOTE]  
> Vous devez inclure un espace entre le commutateur de ligne de commande et la valeur.

### <a name="filtdumpexe"></a>filtdump.exe

Le programme filtdump.exe charge un gestionnaire de filtres pour un document spécifié et imprime la sortie produite par la dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . L’exemple suivant illustre l’appel du programme filtdump.exe.

```
filtdump filename.ext
```
Filtdump.exe utilise la méthode [ILoadFilter :: LoadIFilter](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) pour charger la dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) appropriée pour l’extension de nom de fichier spécifiée et imprime les résultats. Par exemple, la commande suivante indique à filtdump.exe de charger le gestionnaire de filtre smpfilt.dll pour l’extension. SMP, d’extraire l’ensemble du texte et des propriétés du fichier MyFile. SMP et d’imprimer les résultats.

```
filtdump myfile.smp
```

### <a name="filtregexe"></a>filtreg.exe

Le programme filtreg.exe inspecte les informations d’installation [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) dans le registre. Vous appelez le programme filtreg.exe à partir de la ligne de commande en tapant son nom, comme dans l’exemple suivant.

```
filtreg
```

Filtreg.exe énumère toutes les extensions de nom de fichier associées à des gestionnaires de filtre en imprimant l’extension de nom de fichier et le nom de la dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) pour l’extension. Il s’agit d’un moyen simple de vérifier l’installation correcte d’un **IFilter**.

### <a name="ifilttstini"></a>ifilttst.ini

Une interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) est initialisée par l’appel de la méthode [**IFilter :: init**](/windows/win32/api/filter/nf-filter-ifilter-init) . La méthode **IFilter :: init** prend les quatre paramètres suivants :

1. *grfFlags*
2. *cAttributes*
3. *aAttributes*
4. *pdwFlags*

L’utilisateur du programme ifilttst.exe de la suite de tests [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) peut spécifier les valeurs de ces paramètres dans un fichier appelé ifilttst.ini. Le tableau suivant décrit les entrées dans le fichier ifilttst.ini qui spécifient les trois premiers paramètres (les paramètres d’entrée). Pour obtenir un exemple de fichier, consultez [exemple de fichier de ifilttst.ini](#sample-ifilttstini-file).

> [!NOTE]  
> Il n’existe aucune entrée de table pour le paramètre *pdwFlags* , car il s’agit d’un paramètre de sortie ; Il n’est pas nécessaire d’avoir une valeur spéciale avant l’appel à la méthode [**IFilter :: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .

 | Entrée         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Indicateurs         | Noms des indicateurs d' [**\_ initialisation IFilter**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) qui doivent être joints par l’opérateur or pour former le paramètre *GrfFlags* de la méthode [**IFilter :: init**](/windows/win32/api/filter/nf-filter-ifilter-init) . Les noms des indicateurs doivent tous être en majuscules et sur la même ligne.                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *cAttributes* | Entier décimal représentant la valeur du paramètre *cAttributes* .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| *aAttributes* | Cette entrée doit commencer par *aAttributes* et doit être différente des autres entrées *aAttributes* dans la section. Les noms légaux de l’entrée *aAttributes* sont : *aAttributes*, *aAttributes1*, *aAttributes2*, et ainsi de suite. Le premier jeton doit être un GUID. Le GUID doit être mis en forme exactement comme illustré dans la `[Test3]` section de l' [exemple de fichier ifilttst.ini](#sample-ifilttstini-file). Le deuxième jeton peut être soit un identificateur de propriété (PID) composé d’un nombre en notation hexadécimale, soit un pointeur vers une chaîne de caractères larges (LPWSTR). Vous pouvez spécifier un LPWStr en plaçant la chaîne entre guillemets doubles, comme illustré dans la `[Test6]` section de l’exemple de fichier de ifilttst.ini. |

Si les entrées Flags et *cAttributes* ne sont pas spécifiées, la valeur par défaut est 0. Si vous affectez à *cAttributes* la valeur 2, vous devez spécifier deux noms *aAttributes* . Dans la `[Test5]` section de l’exemple, *cAttributes* est 1, mais aucun *aAttributes* n’a été spécifié. Le test appelle ensuite la méthode [**IFilter :: init**](/windows/win32/api/filter/nf-filter-ifilter-init) avec *cAttributes* égal à 1 et *aAttributes* égal à **null**. Il s’agit d’un cas de test utile, car il est susceptible de provoquer une violation d’accès dans la méthode **IFilter :: init** .

Si ifilttst.exe ne parvient pas à trouver un fichier nommé ifilttst.ini dans le répertoire de travail, une configuration par défaut est utilisée pour initialiser l’objet [**IFilter :: init**](/windows/win32/api/filter/nf-filter-ifilter-init) . L’exemple suivant illustre la configuration par défaut.

```
[default]
            grfFlags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

```

### <a name="sample-ifilttstini-file"></a>Exemple de fichier de ifilttst.ini

Le fichier ifilttst.ini est organisé en sections, avec le nom de la section entre crochets. Dans l’exemple, les sections sont nommées `[Test1]` , `[Test2]` , et ainsi de suite. Tous les noms de section doivent être uniques. Le test lit les valeurs de la première section et initialise le [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) avec ces valeurs. Ensuite, tous les tests sont exécutés à l’aide de cette configuration **IFilter** . Le **IFilter** est ensuite libéré et réinitialisé à l’aide des paramètres répertoriés ci-dessus. Le processus se répète jusqu’à ce que toutes les configurations soient testées.

```
; Only extract text from the object
            [Test1]
            Flags =
            cAttributes = 0

            // Get all attributes (text-type and internal value-type properties.
            [Test2]
            Flags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

            // This also extracts just text from the object (the GUID is PSGUID_STORAGE, and the propid is
            // PID_STG_CONTENTS).
            [Test3]
            Flags = IFILTER_INIT_CANON_PARAGRAPHS IFILTER_INIT_HARD_LINE_BREAKS
            cAttributes = 1
            aAttributes1 = b725f130-47ef-101a-a5f1-02608c9eebac 13

            // Only extract requested attribute from the html object (the GUID corresponds to the HTML IFilter.
            [Test4]
            Flags = IFILTER_INIT_CANON_HYPHENS IFILTER_INIT_CANON_SPACES
            cAttributes = 1
            aAttributes1 = 70eb7a10-55d9-11cf-b75b-00aa0051fe20 2

            // Question: what happens if cAttributes is nonzero, but aAttributes is empty?
            [Test5]
            Flags = IFILTER_INIT_CANON_SPACES IFILTER_INIT_APPLY_INDEX_ATTRIBUTES IFILTER_INIT_APPLY_OTHER_ATTRIBUTES
            cAttributes = 1

            // Here is an attribute with a lpwstr instead of a propid (the lpwstr is enclosed in quotes).
            // The GUID corresponds to the meta tag clsid for the HTML IFilter.
            [Test6]
            Flags =
            cAttributes = 1
            aAttributes1 = D1B5D3F0-C0B3-11CF-9A92-00A0C908DBF1 "GENERATOR"
```

## <a name="ifilter-test-procedure"></a>Procédure de test IFilter

Une fois que le [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) a été initialisé, le programme ifilttst.exe effectue une série de tests sur le **IFilter**. En plus de suivre les procédures de test **IFilter** , assurez-vous que votre implémentation **IFilter** utilise des pratiques de code sécurisé. consultez « pratiques de Code sécurisé pour la recherche de Windows » dans [implémentation de gestionnaires de filtres dans Windows search](-search-ifilter-constructing-filters.md).

### <a name="validation-test"></a>Test de validation

Les étapes de test de validation passent par un segment à la fois dans l’objet, en vérifiant chaque bloc individuel et tous les codes de retour. Le test de validation enregistre toutes les structures de [**\_ blocs stats**](/windows/win32/api/filter/ns-filter-stat_chunk) retournées dans une liste.

Le test de validation vérifie les conditions suivantes :

- [**\_ Bloc stat**](/windows/win32/api/filter/ns-filter-stat_chunk).** les ID de bloc idChunk doivent être uniques et en constante évolution.
- [**\_ Bloc stat**](/windows/win32/api/filter/ns-filter-stat_chunk).*le paramètre flags* est un état de bloc reconnu, tel que [**CHUNKSTATE**](/windows/win32/api/filter/ne-filter-chunkstate), le texte de bloc \_ ou les \_ constantes de valeur CenabledHUNK.
- [**\_ Bloc stat**](/windows/win32/api/filter/ns-filter-stat_chunk).** le paramètre breakType est un type d’arrêt reconnu (0, 1, 2, 3, 4).
- Si les attributs d’initialisation [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) spécifient que le **IFilter** doit retourner uniquement des blocs contenant des propriétés de type valeur interne, *idChunkSource* doit être égal à 0.
- Si le segment n’est pas dérivé, s’il ne s’agit pas d’une propriété de type valeur interne, le [**\_ bloc stat**](/windows/win32/api/filter/ns-filter-stat_chunk).*idChunkSource* doit être égal au **\_ bloc stat**.*idChunk*.
- [**IFilter :: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) retourne le \_ ou les autres valeurs de retour acceptables, comme le filtre \_ e \_ End \_ des \_ segments, le filtre \_ e \_ Link \_ non disponible, etc.
- Si le segment contient du texte, [**IFilter :: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) retourne s \_ OK, filtre \_ S \_ dernier \_ texte ou filtre \_ E \_ plus de \_ \_ texte.
- Si [**IFilter :: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) retourne \_ \_ \_ le dernier texte du filtre, l’appel suivant à **IFilter :: gettext** retourne le filtre \_ E (plus de texte) \_ \_ \_ .
- Si le segment contient une valeur, [**IFilter :: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) retourne S \_ OK ou filtre \_ E \_ n’a \_ plus aucune \_ valeur.

### <a name="consistency-test"></a>Test de cohérence

Le programme de ifilttxt.exe réinitialise l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) avec les mêmes paramètres que dans le test de validation et effectue un test de cohérence. Si l’implémentation **IFilter** a été initialisée avec l’indicateur [**IFilter \_ init**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) IFilter \_ init \_ Indexing \_ uniquement, le test libère l’interface **IFilter** et la lie de nouveau avant d’effectuer un autre appel à la méthode [**IFilter :: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .

Le test de cohérence vérifie les conditions suivantes :

- Chaque structure de [**\_ bloc stat**](/windows/win32/api/filter/ns-filter-stat_chunk) retournée par la méthode [**IFilter :: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) est identique au **\_ segment stat** correspondant retourné dans le test de validation.
- [**IFilter :: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) retourne le \_ ou les autres valeurs de retour acceptables, comme le filtre \_ e \_ End \_ des \_ segments, le filtre \_ e \_ Link \_ non disponible, etc.

### <a name="invalid-input-test"></a>Test d’entrée non valide

Le programme de ifilttst.exe réinitialise l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) avec les mêmes paramètres et effectue un test d’entrée non valide. Ce test parcourt le document un segment à la fois, ce qui rend les appels de fonction incorrects, tels que l’appel de la méthode [**IFilter :: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) lorsque le mandrin actuel contient du texte. Le test vérifie que tous les codes de retour sont conformes à la spécification **IFilter** .

Le test d’entrée non valide vérifie les conditions suivantes :

- Si le bloc actuel contient du texte, [**IFilter :: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) retourne \_ le filtre E \_ no \_ values et un appel à [**IFilter :: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) se déroule correctement.
- Si le bloc actuel contient une valeur, [**IFilter :: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) retourne le filtre \_ E \_ no \_ Text et un appel à [**IFilter :: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) se déroule correctement.
- Si l’appel précédent à [**IFilter :: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) a retourné le filtre \_ e \_ plus de \_ \_ texte, les appels successifs à **IFilter :: gettext** retournent le filtre e plus de \_ \_ \_ \_ texte.
- Si l’appel précédent à [**IFilter :: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) a retourné le filtre \_ e \_ plus de \_ \_ valeurs, les appels successifs à **IFilter :: GetValue** retournent le filtre e, plus \_ \_ aucune \_ \_ valeur.
- Si l’appel précédent à [**IFilter :: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) a retourné le filtre \_ e \_ End \_ de \_ segments, les appels successifs à **IFilter :: GetChunk** retournent le filtre \_ e \_ End \_ des \_ segments.

> [!NOTE]  
> Le test d’entrée non valide compare les structures de blocs actuelles à celles retournées dans le test de validation pour s’assurer qu’elles sont identiques.

### <a name="testing-different-ifilter-configurations"></a>Test de différentes configurations IFilter

Le programme ifilttst.exe libère l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) et se reconnecte, ce qui l’initialise avec le jeu de paramètres suivant. Le test répète le cycle : test de validation, test de cohérence et test d’entrée non valide, jusqu’à ce que toutes les configurations **IFilter** souhaitées spécifiées dans [ifilttst.ini](#ifilttstini) fichier aient été testées.

## <a name="ensuring-registered-items-get-indexed"></a>Vérification de l’indexation des éléments inscrits

Le test final de votre [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) garantit que votre **IFilter** est correctement inscrit et qu’il est appelé pour indexer les éléments que vous avez enregistrés pour l’utiliser. Vous pouvez utiliser le gestionnaire de catalogues pour initier la réindexation, ou utiliser le gestionnaire de portée d’analyse (CSM) pour configurer des règles par défaut indiquant les URL que vous souhaitez que l’indexeur analyse. une fois l’indexation terminée, utilisez l’interface utilisateur de recherche Windows pour rechercher une chaîne dans le contenu ou les propriétés des éléments. Si les éléments ont été indexés, ils s’affichent dans les résultats de la recherche.

Pour plus d’informations sur la réindexation, consultez [utilisation du gestionnaire de catalogues](-search-3x-wds-mngidx-catalog-manager.md) et [utilisation du gestionnaire de portée d’analyse](-search-3x-wds-extidx-csm.md). L’exemple de code ReindexMatchingUrls montre comment spécifier les fichiers à réindexer et comment. L’exemple de code CrawlScopeCommandLine montre comment définir des options de ligne de commande pour les opérations d’indexation du gestionnaire de portée d’analyse (CSM). Les deux exemples de code sont disponibles sur [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).

### <a name="sample-log-file"></a>Exemple de fichier journal

À la demande, le programme Ifilttst.exe peut générer un journal contenant une description des étapes qu’il effectue pendant l’exécution. Les exemples suivants sont des extraits d’un fichier journal, avec le niveau de détail défini sur la valeur la plus élevée possible 3.

```
            1. INFO----**** New configuration ****
            2.
            3. Section name : Test2
            4. grfFlags     : 63
            5. cAttributes  : 0
            6. aAttributes  : NONE
            7. pdwFlags     : 0
            8.
            9. INFO----Successfully bound filter.
            10.
            11. PASS----Init() returned a valid value for pdwFlags.
            12.
            13. INFO----Successfully initialized filter.
            14.
            15. INFO----Performing validation test. In this part of the test, the chunks structures
            16.         returned by the IFilter are checked for correctness, and the return values
            17.         of the IFilter calls are checked.
            18.
            19. PASS----GetChunk() succeeded.
            20.
            21. PASS----The current chunk has a legal value for the flags field.

```

La première ligne est un message d’information indiquant qu’une nouvelle configuration a été chargée à partir du fichier ifilttst.ini. Line (3) indique le nom de la section dans le fichier ifilttst.ini à partir duquel la configuration actuelle a été lue. Les lignes (4) à (7) répertorient les paramètres de [**IFilter :: init**](/windows/win32/api/filter/nf-filter-ifilter-init). Les lignes commençant par `INFO` sont des messages d’information sur la liaison du [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) et le début du test de validation. Les lignes commençant par `PASS` sont des messages relatifs à des tests spécifiques qui ont réussi.

La ligne de l’exemple de journal suivant est un avertissement. Les avertissements attirent l’attention sur le comportement [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) qui pose problème, bien que légal. Cet avertissement indique que la méthode [**IFilter :: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) a retourné un segment de texte qui ne contient pas de texte.

```
WARNING-First call to GetText() returned FILTER_E_NO_MORE_TEXT.
```

L’exemple de message d’erreur suivant indique que le [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) a émis un segment qui n’a pas été demandé.

```
            ERROR---The IFilter has emitted a chunk which it was not requested to emit.
            Check the initialization parameters in section Test1 of the initialization file.
            INFO----Current chunk propid : 0x5
```

Dans le cas de cet exemple de message d’erreur, le [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) a émis un segment avec un PID de `0x5` . L’inspection de `[Test1]` la section dans ifilttst.ini indique que le **IFilter** a été configuré pour ne pas émettre de segments avec ce PID. Par exemple, si vous n' \_ appliquez pas d’attributs d’initialisation IFilter ou d' \_ \_ \_ initialisation IFilter, \_ \_ \_ \_ les autres attributs n’ont pas été spécifiés dans l’entrée Flags et si les *cAttributes* étaient 0, **IFilter** émettra uniquement des segments avec un PID de `0x13` et correspondant au \_ contenu PID STG \_ .

### <a name="sample-dump-file"></a>Exemple de fichier dump

À la demande, le programme Ifilttst.exe peut produire un vidage contenant les segments qu’il trouve et leur contenu. L’exemple suivant est un extrait de ce type de fichier de vidage.

```
                1. Chunk ID: ........... 2
                2. Chunk Break Type: ... END OF SENTENCE
                3. Chunk State: ........ TEXT
                4. Chunk Locale: ....... 0x411
                5. Chunk Source ID: .... 2
                6. Chunk Start Source .. 0x0
                7. Chunk Length Source . 0x0
                8. GUID ................ b725f130-47ef-101a-a5f1-02608c9eebac
                9. Property ID ......... 0x13

                10. This is a HTML IFilter test page

                11. Chunk ID: ........... 3
                12. Chunk Break Type: ... END OF SENTENCE
                13. Chunk State: ........ TEXT
                14. Chunk Locale: ....... 0x411
                15. Chunk Source ID: .... 2
                16. Chunk Start Source .. 0x0
                17. Chunk Length Source . 0x0
                18. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                19. Property ID ......... 0x2

                20. This is a HTML IFilter test page

                21. Chunk ID: ........... 4
                22. Chunk Break Type: ... END OF SENTENCE
                23. Chunk State: ........ VALUE
                24. Chunk Locale: ....... 0x411
                25. Chunk Source ID: .... 2
                26. Chunk Start Source .. 0x0
                27. Chunk Length Source . 0x0
                28. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                29. Property ID ......... 0x2

                30. This is an HTML IFilter test page
```

Les neuf premières lignes décrivent la structure de blocs actuelle. Le GUID et le PID correspondent au \_ contenu de stockage/PID PSGUID \_ STG \_ . Il s’agit d’un bloc contenant du texte brut. Le texte se trouve dans la structure de blocs suivante :

```
10. This is an HTML IFilter test page
```

Le bloc suivant, à partir de la ligne 11, a un GUID différent, correspondant à `HTML IFilter` et un PID différent, correspondant à une href html. Il s’agit d’une propriété de type valeur interne, exportée par `HTML IFilter` .

Le bloc suivant, à partir de la ligne 21, a le même GUID et PID, mais son état `VALUE` de bloc est au lieu de `TEXT` . Notez que le texte de ces deux derniers segments est le même que pour le premier segment. Toutefois, étant donné que le [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) est conçu pour appliquer trois attributs (texte brut, texte de description html et href html comme valeur) à appliquer à cette expression, les résultats sont émis dans trois segments distincts.

## <a name="additional-resources"></a>Ressources supplémentaires

- l’exemple de code [IFilterSample](-search-sample-ifiltersample.md) , disponible sur [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), illustre la création d’une classe de base ifilter pour l’implémentation de l’interface [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Pour obtenir une vue d’ensemble du processus d’indexation, consultez [processus d’indexation](-search-indexing-process-overview.md).
- Pour obtenir une vue d’ensemble des types de fichiers, consultez [types de fichiers](../shell/fa-file-types.md).
- Pour interroger des attributs d’association de fichiers pour un type de fichier, consultez [PerceivedTypes, SystemFileAssociations et inscription d’application](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Rubriques connexes

[Développement de gestionnaires de filtres](-search-ifilter-conceptual.md)

[à propos des gestionnaires de filtres dans Windows Search](-search-ifilter-about.md)

[meilleures pratiques pour la création de gestionnaires de filtres dans Windows Search](-search-3x-wds-extidx-filters.md)

[Retour des propriétés d’un gestionnaire de filtres](-search-ifilter-property-filtering.md)

[Gestionnaires de filtres fournis avec Windows](-search-ifilter-implementations.md)

[implémentation de gestionnaires de filtres dans Windows Search](-search-ifilter-constructing-filters.md)

[Inscription des gestionnaires de filtres](-search-ifilter-registering-filters.md)
